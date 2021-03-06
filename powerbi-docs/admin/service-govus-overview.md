---
title: Power BI til US Government-kunder – oversigt
description: US Government-kunder kan føje et Power BI Pro-abonnement til deres Microsoft 365 Government-abonnement. Få mere at vide om, hvordan du tilmelder dig og gennemser tilgængelige funktioner i denne tjenestebeskrivelse.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 04/07/2020
ms.author: kfollis
LocalizationGroup: Get started
ms.openlocfilehash: aeaaf0e1e8baa70b5159d908ce1e27bb937de372
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83344704"
---
# <a name="power-bi-for-us-government-customers"></a>Power BI til US Government-kunder
Denne artikel er for kunder inden for de amerikanske offentlige myndigheder, der udruller Power BI som en del af en Office 365-plan til offentlige myndigheder. Planer til offentlige myndigheder er designet til at opfylde de særlige behov hos organisationer, der overholder amerikanske standarder og sikkerhedsstandarder. Power BI-tjenesten, der er udviklet til US Government-kunder, adskiller sig fra den kommercielle version af Power BI-tjenesten. Disse funktionsforskelle og egenskaber er beskrevet i følgende afsnit.

## <a name="add-power-bi-to-your-office-365-government-plan"></a>Føj Power BI til din Office 365-plan til offentlige myndigheder

Før du kan få et Power BI US Government-abonnement og tildele licenser til brugere, skal du tilmelde dig et Office 365 Government-abonnement. Hvis din organisation allerede har en Office 365-plan for offentlige myndigheder, skal du gå videre til [Køb et Power BI Pro-abonnement til offentlige myndigheder](#buy-a-power-bi-pro-subscription-for-government-customers).

### <a name="enroll-in-an-office-365-government-plan"></a>Tilmeld dig en Office 365-plan til offentlige myndigheder

Hvis du er ny kunde, skal du validere din organisations berettigelse, før du kan tilmelde dig en Office 365-plan til offentlige myndigheder.  Kom i gang ved at udfylde [formularen til bekræftelse af berettigelsen til Office 365 til offentlige myndigheder](https://www.microsoft.com/microsoft-365/government/eligibility-validation). Du kan sikre dig, at du vælger den rette plan til din organisation ved at gennemse [tjenestebeskrivelserne for Office 365 til de amerikanske offentlige myndigheder](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government).

> [!NOTE]
> Hvis du allerede har udrullet Power BI i et kommercielt miljø og gerne vil migrere til US Government-cloudmiljøet, skal du føje et nyt Power BI Pro-abonnement til dit Office 365 Government-abonnement. Derefter skal du replikere de kommercielle data til Power BI-tjenesten til US Government, fjerne kommercielle licenstildelinger fra brugerkonti og derefter tildele en Power BI Pro Government-licens til brugerkontiene.
>
>
## <a name="government-cloud-instances"></a>Instanser i det offentlige cloud
Office 365 indeholder forskellige miljøer, så de offentlige myndigheder kan opfylde de forskellige overensstemmelseskrav. Du kan finde flere oplysninger om hvert miljø under:

* [Office 365 GCC (Government Community Cloud)](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc) er udviklet til forbundsmyndigheder samt statslige og lokale myndigheder.

* [Office 365 GCC High (Government Community Cloud High)](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc-high-and-dod) er udviklet til forbundsmyndigheder, forsvarsindustrien, rumfartsindustrien og andre organisationer, der opbevarer kontrollerede ikke-klassificerede oplysninger. Dette miljø egner sig til nationale sikkerhedsorganisationer og virksomheder med ITAR-data (International Traffic in Arms Regulations) eller DFARS-krav (Defense Federal Acquisition Regulations Supplement).

* [Office 365 DoD-miljøet](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc-high-and-dod) er designet udelukkende til Det amerikanske forsvarsministerium. 

## <a name="connect-to-power-bi-for-us-government"></a>Oversigt over Power BI til US Government

URL-adressen til oprettelse af forbindelse til Power BI er forskellig for offentlige brugere og kommercielle brugere. Hvis du vil logge på Power BI, skal du bruge følgende URL-adresser:

| Kommerciel version  | GCC  | GCC High | DoD |
| --- | --- | --- | --- |
| [https://app.powerbi.com/](https://app.powerbi.com) |[https://app.powerbigov.us](https://app.powerbigov.us) | [https://app.high.powerbigov.us](https://app.high.powerbigov.us) | [https://app.mil.powerbigov.us](https://app.mil.powerbigov.us) |

Din konto kan være konfigureret i mere end ét cloudmiljø. Hvis din konto er konfigureret på denne måde, kan du vælge, hvilken cloud der skal oprettes forbindelse til, når du logger på Power BI Desktop.

## <a name="buy-a-power-bi-pro-subscription-for-government-customers"></a>Køb et Power BI Pro-abonnement til offentlige kunder

Når du har udrullet Office 365, kan du tilføje et Power BI Pro-abonnement. Følg den trinvise vejledning i, hvordan du [tilmelder din US Government-organisation](service-govus-signup.md), for at købe Power BI Pro Government-tjenesten. Køb tilstrækkeligt mange licenser til alle de brugere, der skal bruge Power BI, og tildel derefter disse licenser til individuelle brugerkonti.

> [!IMPORTANT]
> Power BI US Government er ikke tilgængelig som en *gratis* licens. Hver enkelt bruger skal tildeles en *Pro-licens* for at få adgang til Government Community Cloud. Hvis en brugerkonto har fået tildelt en gratis licens, er brugeren kun autoriseret til at få adgang til den kommercielle cloud og vil opleve problemer med godkendelse og adgang. Hvis du har købt Power BI Premium, behøver du ikke at tildele Pro-licenser for at aktivere brugeradgang.  Alle brugere i organisationen har adgang til rapporter, der er delt med dem, så længe rapporterne er udgivet til en Premium-kapacitet. Hvis du vil gennemgå forskellene mellem licenstyper, skal du se [Funktioner i Power BI-tjenesten efter licenstype](../fundamentals/service-features-license-type.md).
>

## <a name="connect-government-and-global-azure-cloud-services"></a>Opret forbindelse mellem Government-tjenester og globale Azure Cloud-tjenester

Azure er fordelt på flere cloudmiljøer. Du kan som standard aktivere firewallregler for at åbne en forbindelse til en cloudspecifik forekomst, men netværket på tværs af skyen er anderledes.  Hvis du vil kommunikere mellem tjenester i den offentlige cloud og tjenesterne i Government Community Cloud, skal du konfigurere særlige firewallregler. Hvis du f.eks. vil have adgang til offentlige cloudforekomster af en SQL-database fra din offentlige cloududrulning af Power BI, skal du have en firewallregel i SQL-databasen. Konfigurer særlige firewallregler for SQL-databaser, så der tillades forbindelser til Azure Government Cloud for følgende datacentre:

* USGov Iowa
* USGov Virginia
* USGov Texas
* USGov Arizona

Pladserne for IP-adresse er tilgængelige i det offentlige cloudmiljø. Hvis du vil have adgang til cloud-IP-intervallerne for US Government, skal du downloade filen [Azure IP Ranges and Service Tags – US Government Cloud](https://www.microsoft.com/download/details.aspx?id=57063). 

Hvis du vil konfigurere firewalls for SQL-databaser, skal du følge fremgangsmåden for at [oprette og administrere IP-firewallregler](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure#create-and-manage-ip-firewall-rules).

## <a name="power-bi-feature-availability"></a>Tilgængelighed af funktioner i Power BI

Der er visse forskelle mellem offentlige planer og kommercielle planer for at imødekomme kravene til offentlige cloudkunder. Se følgende tabel for at få oplysninger om, hvilke funktioner der er tilgængelige i hvert offentlige miljø:

|Funktion |   |GCC |GCC High |DoD|
|------|------|------|------|------|
|Administration|Gratis licenser|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Angiv grænser for datalagring|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Brug Active Directory-grupper til deling af adgangskontrol|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Overvågning via Office 365 Security and Compliance Administration Center|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Deling med eksterne brugere|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Forbrugsmålepunkter for dashboards og rapporter|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Azure B2B mellem GCC og den kommercielle cloud|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|Rapportoprettelse|Opret og få vist dashboards og rapporter|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Planlagt dataopdatering|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Teamdashboards, der kan opdateres|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Sideinddelte rapporter|Tilgængelig|Er på vej|Er på vej|
|  |Skabelonapps|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|Opret forbindelse til data|Importér data og rapporter fra Excel|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Importér data fra CSV-filer|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Importér data fra Power BI Desktop-filer|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Forbindelse til CDS|Tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Azure Data Lake Storage Gen2-connector|Tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|Dataadministration|Dataadministrationsgateway|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Datakryptering i Azure SQL Database|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Datakryptering i Blob Storage for Power BI|Tilgængelig|Tilgængelig|Tilgængelig|
|Integration på tværs af produkter|Integrer i SharePoint Online ved hjælp af Power BI-webdelen|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Integrer i SharePoint Online ved hjælp af Embed-webdelen|Tilgængelig|Tilgængelig|Tilgængelig|
|  |Dataflows og AI-funktioner|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Power Automate-forbindelse til datadrevne underretninger|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Power BI-fanen i Teams|Tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Automatiseret maskinel indlæring|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Azure Cognitive Services|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|
|  |Azure Machine Learning|Ikke tilgængelig|Ikke tilgængelig|Ikke tilgængelig|

## <a name="next-steps"></a>Næste trin

* [Tilmeld dig Power BI til US Government](service-govus-signup.md)
* [Microsoft Power Apps US Government](https://docs.microsoft.com/power-platform/admin/powerapps-us-government)
* [Power Automate US Government](https://docs.microsoft.com/power-automate/us-govt)
* <a href="https://channel9.msdn.com/Blogs/Azure/Cognitive-Services-HDInsight-and-Power-BI-on-Azure-Government">Demo om Power BI US Government</a>
