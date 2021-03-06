---
title: Filtrer og del en Power BI-rapport
description: Få mere at vide om, hvordan du filtrerer Power BI-rapporter og deler dem med kolleger i din organisation.
author: maggiesMSFT
ms.reviewer: lukaszp
featuredvideoid: 0tUwn8DHo3s
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 01/29/2020
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 636aaf59a3a949b5b3571012d12cecc234e9763b
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83347947"
---
# <a name="filter-and-share-a-power-bi-report"></a>Filtrer og del en Power BI-rapport
*Deling* er velegnet til at give nogle få personer adgang til dine dashboards og rapporter. Hvad nu hvis du vil dele en filtreret version af en rapport? Måske vil du have, at der kun vises data for en bestemt by eller sælger eller et bestemt år, i rapporten. I denne artikel forklares det, hvordan du filtrerer en rapport og deler den filtrerede version af rapporten. En anden måde at dele en filtreret rapport på er at [føje forespørgselsparametre til rapportens URL-adresse](service-url-filters.md). I begge tilfælde filtrers rapporten, når modtagerne åbner den. De kan rydde filtervalgene i rapporten.

![Filtreret rapport](media/service-share-reports/power-bi-share-filter-pane-report.png)

Med Power BI får du [andre måder at samarbejde om og distribuere dine rapporter på](service-how-to-collaborate-distribute-dashboards-reports.md). Til deling skal du og dine modtagere bruge en [Power BI Pro-licens](../fundamentals/service-features-license-type.md), eller indholdet skal være i en [Premium-kapacitet](../admin/service-premium-what-is.md). 

## <a name="follow-along-with-sample-data"></a>Følg med via eksempeldataene

I denne artikel bruges appen med eksempelskabelonen Marketing and Sales. Vil du prøve det? 

1. Installer [appen med eksempelskabelonen Marketing and Sales](https://appsource.microsoft.com/product/power-bi/microsoft-retail-analysis-sample.salesandmarketingsample?tab=Overview).
2. Vælg appen, og vælg **Udforsk app**.

   ![Udforsk eksempeldata](media/service-share-reports/power-bi-sample-explore-data.png)

3. Vælg blyantsikonet for at åbne det arbejdsområde, du installerede sammen med appen.

    ![Appredigeringsblyant](media/service-share-reports/power-bi-edit-pencil-app.png)

4. Vælge **Rapporter** på listen med indhold i arbejdsområdet, og vælg derefter rapporten **PBIX-eksempelfilen Sales and Marketing**.

    ![Åbn eksempelrapporten](media/service-share-reports/power-bi-open-sample-report.png)

    Nu er du klar til at følge med.

## <a name="set-a-filter-in-the-report"></a>Angiv et filter i rapporten

Åbn en rapport i [redigeringsvisning](../consumer/end-user-reading-view.md), og anvend et filter.

I dette eksempel filtrerer vi siden YTD Category i skabeloneksemplet Marketing & Sales for kun at få vist de værdier, hvor **Region** er lig med **Central**. 
 
![Ruden Rapportfilter](media/service-share-reports/power-bi-share-report-filter.png)

Gem rapporten.

## <a name="share-the-filtered-report"></a>Del den filtrerede rapport

1. Vælg **Del**.

   ![Vælg Del](media/service-share-reports/power-bi-share.png)

2. Ryd **Send meddelelse via mail til modtagere**, så du kan sende et filtreret link i stedet ved at vælge **Del rapport med aktuelle filtre og udsnitsværktøjer**, og vælg derefter **Del**.

    ![Del rapport med filtre](media/service-share-reports/power-bi-share-with-filters.png)

4. Vælg **Del** igen.

   ![Vælg Del](media/service-share-reports/power-bi-share.png)

5. Vælg fanen **Adgang**, og vælg derefter **Administrer delte rapportvisninger**.

    ![Administrer delte rapportvisninger](media/service-share-reports/power-bi-manage-shared-report-views.png)

6. Højreklik på den ønskede URL-adresse, og vælg **Kopiér link**.

    ![Kopiér filtreret link](media/service-share-reports/power-bi-copy-filtered-link.png)

7. Når du deler dette link, kan modtagerne se din filtrerede rapport. 


## <a name="next-steps"></a>De næste trin
* [Måder at dele dit arbejde på i Power BI](service-how-to-collaborate-distribute-dashboards-reports.md)
* [Del et dashboard](service-share-dashboards.md)
* Har du flere spørgsmål? [Prøv Power BI-community'et](https://community.powerbi.com/).
* Har du feedback? Indsend dine forslag på [webstedet for Power BI-community'et](https://community.powerbi.com/).
