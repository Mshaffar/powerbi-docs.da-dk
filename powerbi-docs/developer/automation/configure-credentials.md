---
title: Konfigurer legitimationsoplysninger programmatisk for Power BI
description: Sådan konfigurerer du legitimationsoplysninger programmatisk, når Power BI automatiseres
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 02/23/2020
ms.openlocfilehash: bd7758be32d18fd3be06a7847edc7795c2b5f9e1
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "80114767"
---
# <a name="configure-credentials-programmatically-for-power-bi"></a>Konfigurer legitimationsoplysninger programmatisk for Power BI

Følg disse trin for at konfigurere legitimationsoplysninger programmatisk for Power BI.

## <a name="update-credentials-flow-for-data-sources"></a>Opdater et flow for legitimationsoplysninger for datakilder

1. Foretag et kald til [Hent datakilder](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasourcesingroup) for at finde datakilderne for datasættet. I svarteksten for hver enkelt datakilde kan du se typen, forbindelsesoplysningerne, gatewayen og id'et for datakilden.

    ```csharp
    // Select a datasource
    var datasources = pbiClient.Datasets.GetDatasources(datasetId).Value;
    var datasource = datasources.First();
    ```

2. Opret en streng for legitimationsoplysningerne i henhold til [Opdater eksempler på datakilder](https://docs.microsoft.com/rest/api/power-bi/gateways/updatedatasource) afhængigt af typen af legitimationsoplysninger.

    # <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

    ```csharp
    var credentials =  new BasicCredentials(username: "username", password :"*****");
    ```

    # <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

     ```csharp
    var credentials = "{\"credentialData\":[{\"name\":\"username\", \"value\":\"john\"},{\"name\":\"password\", \"value\":\"*****\"}]}";
    ```

    ---

2. Foretag et kald til [Hent gateway](https://docs.microsoft.com/rest/api/power-bi/gateways/getgateways) for at hente den offentlige nøgle til gatewayen.

    ```csharp
    var gateway = pbiClient.Gateways.GetGatewayById(datasource.GatewayId);
    ```

3. Kryptér legitimationsoplysningerne.

    # <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

    ```csharp
    var credentialsEncryptor = new AsymmetricKeyEncryptor(gateway.publicKey);
    ```

    # <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

    Kryptér strengen for legitimationsoplysningerne med den offentlige nøgle for gatewayen fra Trin 2. Forskellige gatewayversioner kan have forskellige størrelser af offentlige nøgler. Se følgende eksempler i SDK-koden, der er tilgængelig fra [GitHub-lageret PowerBI-CSharp](https://github.com/microsoft/PowerBI-CSharp/tree/master/sdk/PowerBI.Api/Extensions):
    * [AsymmetricKeyEncryptor.cs](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AsymmetricKeyEncryptor.cs)
    * [Asymmetric1024KeyEncryptionHelper.cs](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/Asymmetric1024KeyEncryptionHelper.cs)
    * [AsymmetricHigherKeyEncryptionHelper.cs](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AsymmetricHigherKeyEncryptionHelper.cs)
    * [AuthenticatedEncryption.cs](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AuthenticatedEncryption.cs) 

    ---  

4. Opret detaljer for legitimationsoplysningerne med krypterede legitimationsoplysninger.

    # <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

    Brug AssymetricKeyEncriptor-klassen med den offentlige nøgle, som blev hentet i **Trin 3**.

    ```csharp
    var credentialDetails = new CredentialDetails(
            credentials,
            PrivacyLevel.Private,
            EncryptedConnection.Encrypted,
            credentialsEncryptor);
    ```


    # <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

    ```csharp
    var credentialDetails = new CredentialDetails(
            credentials,
            CredentialTypeEnum.Basic,
            EncryptedConnectionEnum.Encrypted,
            EncryptionAlgorithmEnum.None,
            PrivacyLevelEnum.Private);
    ```

    ---

5. Foretag et kald til [Opdater datakilde](https://docs.microsoft.com/rest/api/power-bi/gateways/updatedatasource) for at angive legitimationsoplysningerne.

    ```csharp
    pbiClient.Gateways.UpdateDatasource(gatewayId, datasourceId, credentialDetails);
    ```

## <a name="configure-a-new-data-source-for-a-data-gateway"></a>Konfigurer en ny datakilde for en datagateway

1. Installér [Datagatewayen i det lokale miljø](https://powerbi.microsoft.com/gateway/) på din computer.

2. Foretag et kald til [Hent gateway](https://docs.microsoft.com/rest/api/power-bi/gateways/getgateways) for at hente id'et og den offentlige nøgle for gatewayen.

    ```csharp
    // Select a gateway
    var gateways = pbiClient.Gateways.GetGateways().Value;
    var gateway = gateways.First();
    ```

3. Opret detaljerne for legitimationsoplysningerne på samme måde som beskrevet under [Opdater et flow for legitimationsoplysninger for datakilder](#update-credentials-flow-for-data-sources) ved hjælp af den offentlige nøgle for gatewayen, som blev hentet under **Trin 2**.

4. Opret anmodningsteksten.

    ```csharp
    var request = new PublishDatasourceToGatewayRequest(
            dataSourceType: "SQL",
            connectionDetails: "{\"server\":\"myServer\",\"database\":\"myDatabase\"}",
            credentialDetails: credentialDetails,
            dataSourceName: "my sql datasource");
    ```

5. Foretag et kald til API'en for [Opret datakilde](https://docs.microsoft.com/rest/api/power-bi/gateways/createdatasource).

    ```csharp
    pbiClient.Gateways.CreateDatasource(gateway.Id, request);
    ```

## <a name="credential-types"></a>Typer af legitimationsoplysninger

Når du kalder [Opret datakilde](https://docs.microsoft.com/rest/api/power-bi/gateways/createdatasource) eller [Opdater datakilde](https://docs.microsoft.com/rest/api/power-bi/gateways/updatedatasource) under en **virksomhedsgateway i det lokale miljø** ved hjælp af [REST-API'er til Power BI](https://docs.microsoft.com/rest/api/power-bi/), skal legitimationsoplysningerne krypteres ved hjælp af gatewayens offentlige nøgle.

>[!NOTE]
>.NET SDK v3 kan også køre eksemplerne på .NET SDK v2, som er angivet nedenfor.

### <a name="windows-and-basic-credentials"></a>Windows og grundlæggende legitimationsoplysninger

# <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

```csharp
// Windows credentials
var credentials = new WindowsCredentials(username: "john", password: "*****");

// Or

// Basic credentials
var credentials = new BasicCredentials(username: "john", password: "*****");

var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"username\", \"value\":\"john\"},{\"name\":\"password\", \"value\":\"*****\"}]}";
```

---

### <a name="key-credentials"></a>Nøglelegitimationsoplysninger

# <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

```csharp
var credentials = new KeyCredentials("TestKey");
var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"key\", \"value\":\"ec....LA=\"}]}";
```

---

**OAuth2-legitimationsoplysninger**

# <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

```csharp
var credentials = new OAuth2Credentials("TestToken");
var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"accessToken\", \"value\":\"eyJ0....fwtQ\"}]}";
```

---

**Anonyme legitimationsoplysninger**

# <a name="net-sdk-v3"></a>[.NET SDK v3](#tab/sdk3)

```csharp
var credentials = new AnonymousCredentials();
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.NotEncrypted);
```

# <a name="net-sdk-v2"></a>[.NET SDK v2](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":\"\"}";
```

---

## <a name="troubleshooting"></a>Fejlfinding

### <a name="no-gateway-and-data-source-id-found-when-calling-get-data-sources"></a>Der blev ikke fundet noget id eller nogen datakilde for gatewayen ved kald til Hent datakilder

Dette problem betyder, at datasættet ikke er forbundet til en gateway. Når du opretter et nyt datasæt, oprettes der automatisk en datakilde uden legitimationsoplysninger for hver cloudforbindelse på brugerens cloudgateway. Denne gateway bruges til at gemme legitimationsoplysninger for cloudforbindelser.

Når du har oprettet datasættet, oprettes der en automatisk binding mellem datasættet og en passende gateway, som indeholder matchende datakilder for alle forbindelser. Hvis sådan en gateway ikke findes, eller der findes flere passende gateways, mislykkes den automatiske binding.

Hvis du bruger datasæt i det lokale miljø, skal du oprette de manglende datakilder i det lokale miljø og binde datasættet til en gateway manuelt ved hjælp af [Bind til gateway](https://docs.microsoft.com/rest/api/power-bi/datasets/bindtogateway).

Hvis du vil finde gateways, der kan bindes, skal du bruge [Find gateways](https://docs.microsoft.com/rest/api/power-bi/datasets/discovergateways).