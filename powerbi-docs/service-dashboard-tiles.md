---
title: Dashboardfelter i Power BI-tjeneste
description: Alt om dashboardfelter i Power BI. Det omfatter felter, der er oprettet fra SQL Server Reporting Services (SSRS).
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/3/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: f63f99004f9cb532821d6623ab2bdd3f805beafd
ms.sourcegitcommit: 07beb155ec0ea1cdcc741085251ed06d7bc8581c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/09/2018
ms.locfileid: "48874799"
---
# <a name="dashboard-tiles-in-power-bi"></a>Dashboardfelter i Power BI
Dashboards og dashboardfelter er en funktion i Power BI-tjenesten ikke Power BI Desktop. Selvom dashboardfelter ikke kan oprettes eller fastgøres i Power BI - Mobil, [kan de vises og deles](mobile-tiles-in-the-mobile-apps.md). Og i Power BI - Mobil kan du [føje billeder til dashboardet med iPhone-appen](mobile-iphone-app-get-started.md).

## <a name="dashboard-tiles"></a>Dashboardfelter
![Power BI-dashboard](media/service-dashboard-tiles/power-bi-dashboard.png)

Et felt er et snapshot af dine data, der er fastgjort til dashboardet. Et felt kan oprettes fra en rapport, et datasæt, et dashboard, fra feltet Spørgsmål og svar, Excel og fra SQL Server Reporting Services (SSRS) og mere.  Dette skærmbillede viser mange forskellige felter, der er fastgjort til et dashboard.

Ud over fastgørelse kan der oprettes separate felter direkte på dashboardet ved hjælp af [Tilføj felt](service-dashboard-add-widget.md). Separate felter omfatter: tekstfelter, billeder, videoer, streamingdata og webindhold.

Har du brug for hjælp til at forstå de komponenter, der udgør Power BI?  Se [Power BI – Grundlæggende begreber](service-basic-concepts.md).

> [!NOTE]
> Hvis den oprindelige visualisering, der blev brugt til at oprette feltet, ændres, er det ikke tilfældet med feltet.  Hvis du f.eks. har fastgjort et kurvediagram fra en rapport, og du derefter har ændret kurvediagrammet til et søjlediagram, fortsætter dashboardfeltet med at vise et kurvediagram. Dataene opdateres, men visualiseringstypen bliver ikke.
> 
> 

## <a name="pin-a-tile-from"></a>Fastgør et felt fra...
Der er mange forskellige måder at føje (fastgøre) et felt til et dashboard på. Felter kan fastgøres fra:

* [Power BI Spørgsmål og svar](service-dashboard-pin-tile-from-q-and-a.md)
* [en rapport](service-dashboard-pin-tile-from-report.md)
* [et andet dashboard](service-pin-tile-to-another-dashboard.md)
* [Excel-projektmappe på OneDrive for Business](service-dashboard-pin-tile-from-excel.md)
* [Power BI Publisher til Excel](publisher-for-excel.md)
* [Quick Insights](service-insights.md)
* [SSRS](https://msdn.microsoft.com/library/mt604784.aspx)

Og separate felter til billeder, tekstfelter, videoer, streamingdata og webindhold kan oprettes direkte på dashboardet ved hjælp af [Tilføj felt](service-dashboard-add-widget.md).

  ![Ikonet Tilføj felt](media/service-dashboard-tiles/add_widgetnew.png)

## <a name="interacting-with-tiles-on-a-dashboard"></a>Interager med felter på et dashboard
### <a name="move-and-resize-a-tile"></a>Flyt og tilpas størrelsen på et felt
Tag et felt, og [flyt det rundt på dashboardet](service-dashboard-edit-tile.md). Peg, og vælg håndtaget ![håndtag](media/service-dashboard-tiles/resize-handle.jpg) for at tilpasse størrelsen på feltet.

### <a name="hover-over-a-tile-to-change-the-appearance-and-behavior"></a>Peg på et felt for at ændre udseende og funktionalitet
1. Peg på feltet for at vise ellipsen.
   
    ![feltellipse](media/service-dashboard-tiles/ellipses_new.png)
2. Vælg ellipsen for at åbne menuen med felthandlinger.
   
    ![ellipseikon](media/service-dashboard-tiles/power-bi-tile-menu.png)
   
    Herfra kan du:
   
   * [Åbne den rapport, der blev brugt til at oprette dette felt ](service-reports.md) ![rapportikon](media/service-dashboard-tiles/chart-icon.jpg)  
   
   * [Åbne det regneark, der blev brugt til at oprette dette felt ](service-reports.md) ![regnearksikon](media/service-dashboard-tiles/power-bi-open-worksheet.png)  
     
    * [Få vist i fokuseringstilstand ](service-focus-mode.md) ![fokusikon](media/service-dashboard-tiles/fullscreen-icon.jpg)  
     * [Eksportere data, der bruges i feltet](visuals/power-bi-visualization-export-data.md) ![eksportér data-ikon](media/service-dashboard-tiles/export-icon.png)
     * [Redigere titel og undertitel, tilføje et link](service-dashboard-edit-tile.md) ![redigeringsikon](media/service-dashboard-tiles/pencil-icon.jpg)
     * [Køre indsigt](service-insights.md) ![indsigtsikon](media/service-dashboard-tiles/power-bi-insights.png)
     * [Fastgøre feltet til et andet dashboard ](service-pin-tile-to-another-dashboard.md)
       ![fastgørelsesikon](media/service-dashboard-tiles/pin-icon.jpg)
     * [Fjerne feltet](service-dashboard-edit-tile.md)
     ![sletningsikon](media/service-dashboard-tiles/trash-icon.png)
3. Vælg et tomt område på canvasset for at lukke handlingsmenuen.

### <a name="select-click-a-tile"></a>Vælg (klik på) et felt
Når du vælger et felt, afhænger næste handling af, hvordan feltet blev oprettet, og om det har et [brugerdefineret link](service-dashboard-edit-tile.md). Hvis det har et brugerdefineret link, føres du til linket ved at vælge feltet. Ellers føres du til rapporten, Excel Online-projektmappen, SSRS-rapporten, der er i det lokale miljø, eller spørgsmål i Spørgsmål og svar, der blev brugt til at oprette feltet.

> [!NOTE]
> Undtagelsen til dette er videofelter, der er oprettet direkte på dashboardet ved hjælp af **Tilføj felt**. Hvis du vælger et videofelt (der blev oprettet på denne måde), afspilles videoen direkte på dashboardet.   
> 
> 

## <a name="considerations-and-troubleshooting"></a>Overvejelser og fejlfinding
* Hvis den rapport, der blev brugt til at oprette visualiseringen, ikke blev gemt, sker der ikke noget, når feltet vælges.
* Hvis feltet blev oprettet fra en projektmappe i Excel Online, og du ikke som minimum har læserettigheder til denne projektmappe, åbnes projektmappen ikke i Excel Online, når du vælger feltet.
* For felter, der er oprettet direkte på dashboardet ved hjælp af **Tilføj felt**, og hvis et brugerdefineret hyperlink er angivet, åbnes denne URL-adresse, når titlen, undertitlen eller feltet vælges.  Ellers medfører det som standard ingen handling at vælge et af disse felter oprettet direkte på dashboardet for et billede, en webkode eller et tekstfelt.
* Hvis du ikke har tilladelse til rapporten i SSRS, vil valget af et felt oprettet ud fra SSRS producere en side, der angiver, at du ikke har adgang (rsAccessDenied).
* Hvis du ikke har adgang til netværket, hvor SSRS-serveren er placeret, vil valget af et felt oprettet ud fra SSRS producere en side, der angiver, at serveren ikke blev fundet (HTTP 404). Enheden skal have netværksadgang til rapportserveren for at få vist rapporten.
* Hvis den oprindelige visualisering, der blev brugt til at oprette feltet, ændres, er det ikke tilfældet med feltet.  Hvis du f.eks. har fastgjort et kurvediagram fra en rapport, og du derefter ændrer kurvediagrammet til et søjlediagram, fortsætter dashboardfeltet med at vise et kurvediagram. Dataene opdateres, men visualiseringstypen bliver ikke.

## <a name="next-steps"></a>Næste trin
[Opret et kort (felt med stort tal) til dit dashboard](power-bi-visualization-card.md)

[Dashboards i Power BI](service-dashboards.md)  

[Opdatering af data](refresh-data.md)

[Power BI – Grundlæggende begreber](service-basic-concepts.md)

[Eksportér et felt til Power Point](http://blogs.msdn.com/b/powerbidev/archive/2015/09/28/integrating-power-bi-tiles-into-office-documents.aspx)

[Fastgør Reporting Services-elementer til Power BI-dashboards](https://msdn.microsoft.com/library/mt604784.aspx)

Har du flere spørgsmål? [Prøv at spørge Power BI-community'et](http://community.powerbi.com/)
