---
title: 'Project Online: Opret forbindelse til data via Power BI Desktop'
description: 'Project Online: Opret forbindelse til data via Power BI Desktop'
author: davidiseminger
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 04/01/2020
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 0f01a6da3bb0d829d396861814f71d33ba69f22f
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83291920"
---
# <a name="connect-to-project-online-data-through-power-bi-desktop"></a>Opret forbindelse til Project Online-data via Power BI Desktop
Du kan oprette forbindelse til data i Project Online via Power BI Desktop.

## <a name="step-1-download-power-bi-desktop"></a>Trin 1: Download Power BI Desktop
1. [Download Power BI Desktop](https://go.microsoft.com/fwlink/?LinkID=521662), og kør derefter installationsprogrammet for at få **Power BI Desktop** på din computer.

## <a name="step-2-connect-to-project-online-with-odata"></a>Trin 2: Opret forbindelse til Project Online med OData
1. Åbn **Power BI Desktop**.
2. På *velkomstskærmen* skal du vælge **Hent data**.
3. Vælg **OData-feed**, og vælg **Opret forbindelse**.
4. Angiv adressen til dit OData-feed i feltet til URL-adressen, og klik derefter på OK.
   
   Hvis adressen til dit Project Web App-websted ligner *https://\<tenantname\>.sharepoint.com/sites/pwa*, skal den adresse, du angiver for dit OData-feed, være *https://\<tenantname\>.sharepoint.com/sites/pwa/\_api/Projectdata*.
   
   I dette eksempel bruger vi:

    `https://contoso.sharepoint.com/sites/pwa/default.aspx`

5. Power BI Desktop beder dig om at blive godkendt med din Office 365-konto. Vælg Organisationskonto, og angiv derefter dine legitimationsoplysninger.
   
   ![](media/desktop-project-online-connect-to-data/image.png)

Den konto, du bruger til at oprette forbindelse til OData-feedet med, skal som minimum have Portfolio Viewer-adgang til Project Web App-webstedet. 

Herfra kan du vælge, hvilke tabeller du vil oprette forbindelse til, og lave en forespørgsel.  Vil du gerne vide, hvordan du kommer i gang?  I følgende blogindlæg kan du se, hvordan du opretter et burndown-diagram ud fra dine Project Online-data.  I blogindlægget henvises der til, hvordan du kan bruge Power Query til at oprette forbindelse til Project Online, men det gælder også for Power BI Desktop.

[Oprettelse af burndown-diagrammer til Project ved hjælp af Power Pivot og Power Query](https://blogs.office.com/2014/03/24/creating-burndown-charts-for-project-using-power-pivot-and-power-query/)
