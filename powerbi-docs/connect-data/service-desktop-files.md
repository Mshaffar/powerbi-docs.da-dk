---
title: Hent data fra Power BI Desktop-filer
description: Få mere at vide, hvordan du henter data og rapporter fra Power BI Desktop til Power BI
author: davidiseminger
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Data from files
ms.openlocfilehash: 5368370cc25e12fdeab333b42a064ec4db66c301
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83347372"
---
# <a name="get-data-from-power-bi-desktop-files"></a>Hent data fra Power BI Desktop-filer
![](media/service-desktop-files/pbid_file_icon.png)

**Power BI Desktop** gør business intelligence og rapportering let. Uanset om du opretter forbindelse til mange forskellige datakilder, forespørger om og transformerer data, modellerer dine data og opretter effektive og dynamiske rapporter, gør **Power BI Desktop** business intelligence-opgaver intuitive og hurtige. Hvis du ikke har erfaring med **Power BI Desktop**, kan du se under [Introduktion til Power BI Desktop](../fundamentals/desktop-getting-started.md).

Når du overfører data til **Power BI Desktop** og opretter nogle få rapporter, skal du hente den gemte fil ind i **Power BI-tjenesten**.

## <a name="where-your-file-is-saved-makes-a-difference"></a>Det gør en forskel, hvor du gemmer din fil
**Lokalt** – Hvis du gemmer din fil på et lokalt drev på din computer eller på en anden placering i din organisation, kan du *importere* filen, eller du kan *publicere* fra Power BI Desktop for at hente dens data og rapporter ind i Power BI. Filen forbliver på den lokale harddisk, så det er ikke hele filen, der reelt flyttes til Power BI. Der sker det, at et nyt datasæt oprettes i Power BI, og data og datamodellen fra Power BI Desktop-filen indlæses i datasættet. Hvis filen indeholder rapporter, vises de på Power BI-webstedet under Rapporter.

**OneDrive – erhverv** – Hvis du har OneDrive for Business, og du logger på med den samme konto, du bruger til at logge på Power BI, er det den klart mest effektive metode til at holde dit arbejde i Power BI Desktop synkroniseret med datasæt, rapporter og dashboards i Power BI. Da både Power BI og OneDrive findes i cloudmiljøet, opretter Power BI *forbindelse* til din fil på OneDrive ca. hver time. Hvis der findes ændringer, opdateres datasættet, rapporter og dashboards automatisk i Power BI.

**OneDrive – personlig** – Hvis du gemmer dine filer på din egen OneDrive-konto, får du mange af de samme fordele som med OneDrive for Business. Den største forskel er, at når du første gang opretter forbindelse til din fil (med funktionen Hent data > Filer > OneDrive - personlig), skal du logge på OneDrive med din Microsoft-konto, som normalt er forskellig fra, hvad du bruger til at logge på Power BI. Når du logger på med OneDrive med din Microsoft-konto, skal du sørge for at vælge indstillingen Forbliv logget på. På denne måde kan Power BI oprette forbindelse til din fil ca. hver time og sikre, at dit datasæt i Power BI er synkroniseret.

**SharePoint – teamwebsteder** – Lagring af dine Power BI Desktop-filer på SharePoint – Teamwebsteder er stort set det samme som at gemme på OneDrive for Business. Den største forskel er, hvordan du opretter forbindelse til filen fra Power BI. Du kan angive en URL-adresse, eller du kan oprette forbindelse til rodmappen.

## <a name="import-or-connect-to-a-power-bi-desktop-file-from-power-bi"></a>Importér eller opret forbindelse til en Power BI Desktop-fil fra Power BI
>[!IMPORTANT]
>Den maksimale filstørrelse, du kan importere til Power BI, er 1 GB.

1. I Power BI skal du klikke på **Hent data** i navigationsruden.
   
   ![](media/service-desktop-files/pbid_get_data_button.png)
2. Under **Filer** skal du klikke på **Hent**.
   
   ![](media/service-desktop-files/pbid_files_get.png)
3. Find din fil. Power BI Desktop-filer har filtypeendelsen .PBIX.
   
   ![](media/service-desktop-files/pbid_find_your_file.png)

## <a name="publish-a-file-from-power-bi-desktop-to-your-power-bi-site"></a>Publicer en fil fra Power BI Desktop på dit Power BI-websted
Når du bruger Publicer fra Power BI Desktop fungerer det på samme måde som funktionen Hent Data i Power BI, når du importerer din fil fra et lokalt drev eller opretter forbindelse til den på OneDrive.  Her er en kort vejledning, men du kan se under [Publicer fra Power BI Desktop](../create-reports/desktop-upload-desktop-files.md) for at få mere at vide.

1. I Power BI Desktop skal du klikke på **Filer** > **Publicer** > **Publicer på Power BI** eller klikke på **Publicer** på båndet.
   
   ![](media/service-desktop-files/pbid_publish.png)
2. Log på Power BI. Det skal du kun gøre første gang.
   
   Når du er færdig, får du et link, du kan bruge til at åbne rapporten på Power BI-webstedet.
   
   ![](media/service-desktop-files/pbid_publishing.png)

## <a name="next-steps"></a>Næste trin
**Udforsk dine data** – Når du har hentet data og rapporter fra din fil til Power BI, er det tid til at udforske dem. Hvis din fil allerede indeholder rapporter, vises de i navigationsruden **Rapporter**. Hvis din fil kun indeholder data, kan du oprette nye rapporter. Du skal bare højreklikke på det nye datasæt og derefter klikke på **Udforsk**.

**Opdater eksterne datakilder** – Hvis din Power BI Desktop-fil opretter forbindelse til eksterne datakilder, kan du konfigurere planlagt opdatering for at sikre dig, at datasættet altid er ajour. Konfigurationen af planlagt opdatering er i de fleste tilfælde meget nem at udføre, men de nærmere detaljer ligger uden for emnet af denne artikel. Se [Opdatering af data i Power BI](refresh-data.md) for at få mere at vide.
