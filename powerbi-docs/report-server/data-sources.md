---
title: Power BI-rapportdatakilder på Power BI-rapportserver
description: Power BI-rapporter kan oprette forbindelse til en række datakilder. Der er adgang til forskellige datakilder, afhængigt af hvordan dataene bruges.
author: maggiesMSFT
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 04/08/2020
ms.author: maggies
ms.openlocfilehash: 166f72a717c99457e1d6b8e9a1f30535a9b4686f
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "80979839"
---
# <a name="power-bi-report-data-sources-in-power-bi-report-server"></a>Power BI-rapportdatakilder på Power BI-rapportserver
Power BI-rapporter kan oprette forbindelse til en række datakilder. Der er adgang til forskellige datakilder, afhængigt af hvordan dataene bruges. Dataene kan importeres, eller der kan foretages forespørgsler om data direkte ved hjælp af DirectQuery eller en direkte forbindelse til SQL Server Analysis Services.

Disse datakilder gælder kun for Power BI-rapporter, der bruges på Power BI-rapportserver. Du kan finde oplysninger om de datakilder, der understøttes sammen med sideinddelte rapporter (.rdl), under [Datakilder, der understøttes af Reporting Services](https://docs.microsoft.com/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs).

> [!IMPORTANT]
> Alle datakilder i en Power BI Desktop-rapport skal understøtte konfiguration af planlagt opdatering.
>  

## <a name="list-of-supported-data-sources"></a>Liste over understøttede datakilder

Det er muligt, at andre datakilder fungerer, selvom de ikke står på listen over understøttede datakilder.

| **Datakilde** | **Cachelagrede data** | **Planlagt opdatering** | **Live/DirectQuery** |
| --- | --- | --- | --- |
| SQL Server-database |Ja |Ja |Ja |
| SQL Server Analysis Services |Ja |Ja |Ja |
| Azure SQL Database |Ja |Ja |Ja |
| Azure SQL Data Warehouse |Ja |Ja |Ja |
| Excel |Ja |Ja |Nej |
| Access-database |Ja |Ja |Nej |
| Active Directory |Ja |Ja |Nej |
| Amazon Redshift |Ja |Nej |Nej |
| Azure Blob Storage |Ja |Ja |Nej |
| Azure Data Lake Store |Ja |Nej |Nej |
| Azure HDInsight (HDFS) |Ja |Nej |Nej |
| Azure HDInsight (Spark) |Ja |Nej |Nej |
| Azure Table Storage |Ja |Ja |Nej |
| Dynamics 365 (online) |Ja |Nej |Nej |
| Facebook |Ja |Nej |Nej |
| Mappe |Ja |Ja |Nej |
| Google Analytics |Ja |Nej |Nej |
| Hadoop-fil (HDFS) |Ja |Nej |Nej |
| IBM DB2-database |Ja |Ja |Nej |
| Impala |Ja |Nej |Nej |
| JSON |Ja |Ja |Nej |
| Microsoft Exchange |Ja |Nej |Nej |
| Microsoft Exchange Online |Ja |Nej |Nej |
| MySQL Database |Ja |Ja |Nej |
| OData-feed |Ja |Ja |Nej |
| ODBC |Ja |Ja |Nej |
| OLE DB |Ja |Ja |Nej |
| Oracle-database |Ja |Ja |Ja |
| PostgreSQL-database |Ja |Ja |Nej |
| Power BI-tjenesten |Nej |Nej |Nej |
| R Script |Ja |Nej |Nej |
| Salesforce-objekter |Ja |Nej |Nej |
| Salesforce-rapporter |Ja |Nej |Nej |
| SAP Business Warehouse-server |Ja |Ja |Ja |
| SAP HANA-database |Ja |Ja |Ja |
| SharePoint-mappe (i det lokale miljø) |Ja |Ja |Nej |
| SharePoint-liste (i det lokale miljø) |Ja |Ja |Nej |
| SharePoint Online-liste |Ja |Nej |Nej |
| Snowflake |Ja |Nej |Nej |
| Sybase-database |Ja |Ja |Nej |
| Teradata |Ja |Ja |Ja |
| Tekst/CSV |Ja |Ja |Nej |
| Web |Ja |Ja |Nej |
| XML |Ja |Ja |Nej |
| appFigures (beta) |Ja |Nej |Nej |
| Azure Analysis Services-database |Ja |Nej |Ja |
| Azure Cosmos DB (beta) |Ja |Nej |Nej |
| Azure HDInsight Spark (beta) |Ja |Nej |Nej |
| Common Data Service (beta) |Ja |Nej |Nej |
| comScore Digital Analytix (beta) |Ja |Nej |Nej |
| Dynamics 365 for Customer Insights (beta) |Ja |Nej |Nej |
| Dynamics 365 for Financials (beta) |Ja |Nej |Nej |
| GitHub (beta) |Ja |Nej |Nej |
| Google BigQuery (beta) |Ja |Nej |Nej |
| IBM Informix-database (beta) |Ja |Nej |Nej |
| IBM Netezza (beta) |Ja |Nej |Nej |
| Kusto (beta) |Ja |Nej |Nej |
| MailChimp (beta) |Ja |Nej |Nej |
| Microsoft Azure Consumption Insights (beta) |Ja |Nej |Nej |
| Mixpanel (beta) |Ja |Nej |Nej |
| Planview Enterprise (beta) |Ja |Nej |Nej |
| Projectplace (beta) |Ja |Nej |Nej |
| QuickBooks Online (beta) |Ja |Nej |Nej |
| Smartsheet |Ja |Nej |Nej |
| Spark (beta) |Ja |Nej |Nej |
| SparkPost (beta) |Ja |Nej |Nej |
| SQL Sentry (beta) |Ja |Nej |Nej |
| Stripe (beta) |Ja |Nej |Nej |
| SweetIQ (beta) |Ja |Nej |Nej |
| Troux (beta) |Ja |Nej |Nej |
| Twilio (beta) |Ja |Nej |Nej |
| tyGraph (beta) |Ja |Nej |Nej |
| Vertica (beta) |Ja |Nej |Nej |
| Visual Studio Team Services (beta) |Ja |Nej |Nej |
| Webtrends (beta) |Ja |Nej |Nej |
| Zendesk (beta) |Ja |Nej |Nej |

> [!IMPORTANT]
> Sikkerhed på rækkeniveau, der er konfigureret på datakilden, skal fungere for bestemte DirectQuery-forbindelser (SQL Server, Azure SQL Database, Oracle og Teradata) og direkte forbindelser, hvis vi antager, at Kerberos er konfigureret korrekt i dit miljø.
> 
> 

## <a name="list-of-supported-authentication-methods-for-model-refresh"></a>Liste over understøttede godkendelsesmetoder i forbindelse med opdatering af modellen

Power BI-rapportserver understøtter ikke OAuth-baseret godkendelse i forbindelse med opdatering af modellen. Nogle datakilder, f.eks. Excel- eller Access-databaser, gør brug af et separat trin som Filer eller Web til at oprette forbindelse til data.

| **Datakilde** | **Anonym godkendelse** | **Nøglegodkendelse** | **Brugernavn og adgangskode** | **Windows-godkendelse** |
| --- | --- | --- | --- | --- |
| SQL Server-database |Nej |Nej |Ja |Ja |
| SQL Server Analysis Services |Nej |Nej |Ja |Ja |
| Web |Ja |Nej |Ja |Ja |
| Azure SQL Database |Nej |Nej |Ja |Nej |
| Azure SQL Data Warehouse |Nej |Nej |Ja |Nej |
| Active Directory |Nej |Nej |Ja |Ja |
| Amazon Redshift |Nej |Nej |Nej |Nej |
| Azure Blob Storage |Ja |Ja |Nej |Nej |
| Azure Data Lake Store |Nej |Nej |Nej |Nej |
| Azure HDInsight (HDFS) |Nej |Nej |Nej |Nej |
| Azure HDInsight (Spark) |Nej |Nej |Nej |Nej |
| Azure Table Storage |Nej |Ja |Nej |Nej |
| Dynamics 365 (online) |Nej |Nej |Nej |Nej |
| Facebook |Nej |Nej |Nej |Nej |
| Mappe |Nej |Nej |Nej |Ja |
| Google Analytics |Nej |Nej |Nej |Nej |
| Hadoop-fil (HDFS) |Nej |Nej |Nej |Nej |
| IBM DB2-database |Nej |Nej |Ja |Ja |
| Impala |Nej |Nej |Nej |Nej |
| Microsoft Exchange |Nej |Nej |Nej |Nej |
| Microsoft Exchange Online |Nej |Nej |Nej |Nej |
| MySQL Database |Nej |Nej |Ja |Ja |
| OData-feed |Ja |Ja |Ja |Ja |
| ODBC |Ja |Nej |Ja |Ja |
| OLE DB |Ja |Nej |Ja |Ja |
| Oracle-database |Nej |Nej |Ja |Ja |
| PostgreSQL-database |Nej |Nej |Ja |Nej |
| Power BI-tjenesten |Nej |Nej |Nej |Nej |
| R Script |Nej |Nej |Nej |Nej |
| Salesforce-objekter |Nej |Nej |Nej |Nej |
| Salesforce-rapporter |Nej |Nej |Nej |Nej |
| SAP Business Warehouse-server |Nej |Nej |Ja |Nej |
| SAP HANA-database |Nej |Nej |Ja |Ja |
| SharePoint-mappe (i det lokale miljø) |Ja |Nej |Nej |Ja |
| SharePoint-liste (i det lokale miljø) |Ja |Nej |Nej |Ja |
| SharePoint Online-liste |Nej |Nej |Nej |Nej |
| Snowflake |Nej |Nej |Nej |Nej |
| Sybase-database |Nej |Nej |Ja |Ja |
| Teradata |Nej |Nej |Ja |Ja** |
| appFigures (beta) |Nej |Nej |Nej |Nej |
| Azure Analysis Services-database (beta) |Nej |Nej |Nej |Nej |
| Azure Cosmos DB (beta) |Nej |Nej |Nej |Nej |
| Azure HDInsight Spark (beta) |Nej |Nej |Nej |Nej |
| Common Data Service (beta) |Nej |Nej |Nej |Nej |
| comScore Digital Analytix (beta) |Nej |Nej |Nej |Nej |
| Dynamics 365 for Customer Insights (beta) |Nej |Nej |Nej |Nej |
| Dynamics 365 for Financials (beta) |Nej |Nej |Nej |Nej |
| GitHub (beta) |Nej |Nej |Nej |Nej |
| Google BigQuery (beta) |Nej |Nej |Nej |Nej |
| IBM Informix-database (beta) |Nej |Nej |Nej |Nej |
| IBM Netezza (beta) |Nej |Nej |Nej |Nej |
| Kusto (beta) |Nej |Nej |Nej |Nej |
| MailChimp (beta) |Nej |Nej |Nej |Nej |
| Microsoft Azure Consumption Insights (beta) |Nej |Nej |Nej |Nej |
| Mixpanel (beta) |Nej |Nej |Nej |Nej |
| Planview Enterprise (beta) |Nej |Nej |Nej |Nej |
| Projectplace (beta) |Nej |Nej |Nej |Nej |
| QuickBooks Online (beta) |Nej |Nej |Nej |Nej |
| Smartsheet |Nej |Nej |Nej |Nej |
| Spark (beta) |Nej |Nej |Nej |Nej |
| SparkPost (beta) |Nej |Nej |Nej |Nej |
| SQL Sentry (beta) |Nej |Nej |Nej |Nej |
| Stripe (beta) |Nej |Nej |Nej |Nej |
| SweetIQ (beta) |Nej |Nej |Nej |Nej |
| Troux (beta) |Nej |Nej |Nej |Nej |
| Twilio (beta) |Nej |Nej |Nej |Nej |
| tyGraph (beta) |Nej |Nej |Nej |Nej |
| Vertica (beta) |Nej |Nej |Nej |Nej |
| Visual Studio Team Services (beta) |Nej |Nej |Nej |Nej |
| Webtrends (beta) |Nej |Nej |Nej |Nej |
| Zendesk (beta) |Nej |Nej |Nej |Nej |

** Brug af LDAP-godkendelse med Teradata (aktiveret i Power BI Desktop ved hjælp af kommandoprompten 'setx PBI_EnableTeradataLdap true') understøttes ikke i forbindelse med opdatering af modellen.

## <a name="list-of-supported-authentication-methods-for-directquery"></a>Liste over understøttede godkendelsesmetoder i forbindelse med DirectQuery

Power BI-rapportserver understøtter ikke OAuth-baseret godkendelse i forbindelse med DirectQuery.

| **Datakilde** | **Anonym godkendelse** | **Nøglegodkendelse** | **Brugernavn og adgangskode** | **Windows-godkendelse** | **Integreret Windows-godkendelse** |
| --- | --- | --- | --- | --- | --- |
| SQL Server-database |Nej |Nej |Ja |Ja |Ja |
| SQL Server Analysis Services |Nej |Nej |Ja |Ja |Ja |
| Azure SQL Database |Nej |Nej |Ja |Nej |Nej |
| Azure SQL Data Warehouse |Nej |Nej |Ja |Nej |Nej |
| Oracle-database |Nej |Nej |Ja |Ja |Ja |
| SAP Business Warehouse-server |Nej |Nej |Ja |Nej |Nej |
| SAP HANA-database |Nej |Nej |Ja |Ja |Ja** |
| Teradata |Nej |Nej |Ja |Ja |Ja |

**SAP HANA understøtter kun DirectQuery med integreret Windows-godkendelse, når det bruges som en relationsdatabase i den publicerede Power BI Desktop-fil (.pbix).

## <a name="next-steps"></a>De næste trin
Nu, hvor du har oprettet forbindelse til datakilden, kan du [oprette en rapport](quickstart-create-powerbi-report.md) ved hjælp af dataene fra denne datakilde.

Har du flere spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)
