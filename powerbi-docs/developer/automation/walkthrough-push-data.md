---
title: Overfør data til et datasæt
description: Overfør data til et Power BI-datasæt
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.date: 05/22/2019
ms.openlocfilehash: 932e458c90b248e01a88d45a849838cff27f6dcb
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "79488194"
---
# <a name="push-data-into-a-power-bi-dataset"></a>Overfør data til et Power BI-datasæt

Med Power BI-API'en, kan du overføre data til et Power BI-datasæt. I denne artikel viser vi dig, hvordan du kan overføre datasæt for SalesMarkering, der indeholder en produkttabel, til et eksisterende datasæt.

Inden du går i gang, skal du have en Azure AD- (Azure Active Directory) og [Power BI-konto](../embedded/create-an-azure-active-directory-tenant.md).

## <a name="steps-to-push-data-into-a-dataset"></a>Sådan overfører du data til et datasæt

* Trin 1: [Registrer en app med Azure AD](../embedded/register-app.md)
* Trin 2: [Hent et adgangstoken til godkendelse](walkthrough-push-data-get-token.md)
* Trin 3: [Opret et datasæt i Power BI](walkthrough-push-data-create-dataset.md)
* Trin 4: [Hent et datasæt for at føje rækker til en Power BI-tabel](walkthrough-push-data-get-datasets.md)
* Trin 5: [Indsæt rækker i en Power BI-tabel](walkthrough-push-data-add-rows.md)

Det næste afsnit er en generel beskrivelse af de handlinger i Power BI-API'en, der overfører data.

## <a name="power-bi-api-operations-to-push-data"></a>Handlinger i Power BI-API'en til overførsel af data

Med Power BI REST API'en kan du overføre datakilder til Power BI. Når en app føjer rækker til et datasæt, opdateres dashboardfelter automatisk med de nye data. Hvis du vil overføre data, skal du bruge handlingerne [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postdataset) og [PostRows](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows). Hvis du vil finde et datasæt, skal du bruge handlingen [Hent datasæt](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets). Du kan overføre et gruppe-id for alle disse handlinger, hvis du vil arbejde med en gruppe. Hvis du vil hente en gruppe-id-liste, skal du bruge handlingen [Get Groups](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups).

Her er de handlinger, du skal bruge for at overføre data til et datasæt:

* [PostDataset](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postdataset)
* [Hent datasæt](https://docs.microsoft.com/rest/api/power-bi/datasets/getdatasets)
* [Post Rows](https://docs.microsoft.com/rest/api/power-bi/pushdatasets/datasets_postrows)
* [Hent grupper](https://docs.microsoft.com/rest/api/power-bi/groups/getgroups)

Du kan oprette et datasæt i Power BI ved at overføre en JSON-streng (JavaScript Object Notation) til Power BI-tjenesten. Hvis du vil have mere at vide om JSON, skal du se [Om JSON](https://json.org/).

JSON-strengen til et datasæt har følgende format:

**Power BI-datasæt JSON-objekt**

    {"name": "dataset_name", "tables":
        [{"name": "", "columns":
            [{ "name": "column_name1", "dataType": "data_type"},
             { "name": "column_name2", "dataType": "data_type"},
             { ... }
            ]
          }
        ]
    }

For eksemplet med SalesMarketing-datasættet ville du overføre en JSON-streng som vist i nedenstående eksempel. I dette eksempel er **SalesMarketing** navnet på datasættet, og **Product** er navnet på tabellen. Når du har defineret tabellen, kan du definere tabelskemaet. For datasættet **SalesMarketing** indeholder tabelskemaet disse kolonner: ProductID, Manufacturer, Category, Segment, Product og IsCompete.

**Eksempeldatasæt JSON-objekt**

    {
        "name": "SalesMarketing",
        "tables": [
            {
                "name": "Product",
                "columns": [
                {
                    "name": "ProductID",
                    "dataType": "int"
                },
                {
                    "name": "Manufacturer",
                    "dataType": "string"
                },
                {
                    "name": "Category",
                    "dataType": "string"
                },
                {
                    "name": "Segment",
                    "dataType": "string"
                },
                {
                    "name": "Product",
                    "dataType": "string"
                },
                {
                    "name": "IsCompete",
                    "dataType": "bool"
                }
                ]
            }
        ]
    }

Hvis du har et Power BI-tabelskema, kan du bruge følgende datatyper.

## <a name="power-bi-table-data-types"></a>Power BI-tabeldatatyper

| **Datatype** | **Begrænsninger** |
| --- | --- |
| Int64 |Int64.MaxValue og Int64.MinValue er ikke tilladt. |
| Double |Værdierne Double.MaxValue og Double.MinValue er ikke tilladt. NaN understøttes ikke. +Infinity og -Infinity understøttes ikke i visse funktioner (f.eks. Min., Maks.). |
| Boolesk |Ingen |
| Datetime |Under indlæsning af data beregnes værdier baseret på brøkdele af dagen i hele multipler af 1/300 sekunder (3,33 ms). |
| Streng |Tillader i øjeblikket op til 128.000 tegn. |

## <a name="learn-more-about-pushing-data-into-power-bi"></a>Få mere at vide om at overføre data til Power BI

Du kan få hjælp til at komme i gang med at overføre data til et datasæt i [Trin 1: Registrer en app med Microsoft Azure Active Directory](../embedded/register-app.md) i navigationsruden.

## <a name="next-steps"></a>Næste trin

* [Tilmeld dig Power BI](../embedded/create-an-azure-active-directory-tenant.md)  
* [Introduktion til JSON](https://json.org/)  
* [Oversigt over Power BI REST-API](overview-of-power-bi-rest-api.md)  

Har du flere spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)