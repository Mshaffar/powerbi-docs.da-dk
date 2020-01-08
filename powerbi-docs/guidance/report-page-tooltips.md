---
title: Udvidelse af visualiseringer med værktøjstip til rapportsider
description: Vejledning til arbejde med værktøjstip for rapportsider.
author: peter-myers
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 11/24/2019
ms.author: v-pemyer
ms.openlocfilehash: b7256a04ccdca107ef0cd8e24af8b3170a3d68cc
ms.sourcegitcommit: e492895259aa39960063f9b337a144a60c20125a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2019
ms.locfileid: "74834718"
---
# <a name="extending-visuals-with-report-page-tooltips"></a>Udvidelse af visualiseringer med værktøjstip til rapportsider

Denne artikel henvender sig til rapportforfattere, der designer Power BI-rapporter. Den indeholder forslag og anbefalinger til oprettelse af [værktøjstip til rapportsider](../desktop-tooltips.md).

## <a name="suggestions"></a>Forslag

Værktøjstippene til rapportsiden kan forbedre oplevelsen for dine rapportbrugere. Sideværktøjstip gør det muligt for rapportbrugerne hurtigt og effektivt at få dybere indsigt fra et visual. De kan knyttes til forskellige rapportobjekter:

- **Visuals:** Du kan for hvert visual konfigurere, hvilke visuals der skal vise sideværktøjstippet. Det er muligt for hvert visual at få vist ingen værktøjstip, visualværktøjstip (standard og konfigureret i ruden med visualfelter) eller et bestemt sideværktøjstip.
- **Visualheadere:** Du kan konfigurere bestemte visuals til at vise et sideværktøjstip. Rapportbrugerne kan se værktøjstippet til siden, når de holder markøren over ikonet for visuaheaderen. Sørg for at fortælle dine brugere om dette ikon.

> [!NOTE]
> Et rapportvisual kan kun vise et sideværktøjstip, når filtrene for værktøjstipsiden er kompatible med visualdesignet. Et visual, der grupperer efter _produkt_, er f. eks. kompatibelt med en værktøjstipside, der filtrerer efter _produkt_.
>
> Sideværktøjstip understøtter ikke interaktivitet. Hvis rapportbrugerne skal interagere, kan du i stedet oprette en [detaljeadgangsside](../desktop-drillthrough.md).
>
> Brugerdefinerede visuals understøtter ikke sideværktøjstip.

Her er nogle forslag til designscenarier:

- [Andet perspektiv](#different-perspective)
- [Tilføj detalje](#add-detail)
- [Tilføj Hjælp](#add-help)

### <a name="different-perspective"></a>Andet perspektiv

Et sideværktøjstip kan visualisere de samme data som kildevisual'et. Det gøres ved at bruge de samme visual- og pivoteringsgrupper eller ved at bruge forskellige visualtyper. Sideværktøjstip kan også anvende andre filtre end de filtre, der anvendes på kildevisual'et.

I følgende eksempel kan du se, hvad der sker, når rapportbrugeren holder markøren over værdien **EnabledUsers**. Filterkonteksten for værdien er Yammer i november 2018.

![Et matrixvisual viser et gitter med værdier, der er grupperet efter år og måned, for rækkerne. Rapportbrugeren holder markør over en enkelt værdi. Der vises et sideværktøjstip.](media/report-page-tooltips/suggestion-different-perspective.png)

Der bliver vist et sideværktøjstip. Det viser et andet datavisual (kurvediagram og grupperet søjlediagram) og anvender et andet tidsfilter. Bemærk, at filterkonteksten for datapunktet er november 2018. Men sideværktøjstippet viser tendensen i _alle måneder i et år_.

### <a name="add-detail"></a>Tilføj detalje

Et sideværktøjstip kan vise flere detaljer og tilføje kontekst.

I følgende eksempel kan du se, hvad der sker, når rapportbrugeren holder markøren over værdien **Average of Violation Points** for postnummeret 98022.

![Et tabelvisual viser et gitter med værdier, og tabellen indeholder tre kolonner. Der vises et sideværktøjstip.](media/report-page-tooltips/suggestion-add-details.png)

Der bliver vist et sideværktøjstip. Det viser bestemte attributter og statistikker for postnummeret 98022.

### <a name="add-help"></a>Tilføj Hjælp

Visualheadere kan konfigureres til at vise sideværktøjstip til visualheadere. Du kan føje Hjælp-indhold til et sideværktøjstip ved hjælp af RTF-formaterede tekstfelter. Det er også muligt at tilføje billeder og figurer.

Der kan også vises sideværktøjstip til visualheadere i knapper, billeder, tekstfelter og figurer.

I følgende eksempel kan du se, hvad der sker, når rapportbrugeren holder markøren over ikonet for visualheaderen.

![En rapportbruger holder markøren over ikonet for visualheaderen (ikonet med spørgsmålstegnet). Der vises et RTF-formateret værktøjstip.](media/report-page-tooltips/suggestion-add-help.png)

Der bliver vist et sideværktøjstip. Det viser RTF-formateret tekst, som beskriver de målinger, der vises i visual'et. Værktøjstippet indeholder også en figur (linje).

## <a name="recommendations"></a>Anbefalinger

Vi anbefaler følgende fremgangsmåder på tidspunktet for oprettelse af rapportdesignet:

- **Sidestørrelse:** Konfigurer side tippet til at være lille. Du kan bruge den indbyggede indstilling **Værktøjstip** (320 pixel bredt, 240 pixel højt). Eller du kan angive brugerdefinerede dimensioner. Vær forsigtig med ikke at bruge en sidestørrelse, der er for stor – det kan skjule de visuelle elementer på kildesiden.
- **Sidevisning:** I rapportdesigneren skal du angive sidevisningen til **Faktisk størrelse** (sidevisning er som standard til **Tilpas til side**). På denne måde kan du se den naturlige størrelse på side værktøjstippet, når du designer det.
- **Typografi:** Overvej at designe dit sideværktøjstip, så du kan bruge samme tema og typografi som i rapporten. På denne måde føler brugerne, at de ser den samme rapport. Du kan også designe en anden typografi til dine værktøjstip og anvende dette format på alle sideværktøjstip.
- **Værktøjstipfiltre:** Tildel filtre til sideværktøjstippet, så du kan få vist et virkelighedstro resultat, når du designer det. Sørg for at fjerne disse filtre, før du publicerer rapporten.
- **Sidesynlighed:** Skjul altid værktøjstipsider – brugerne bør ikke navigere direkte til dem.

## <a name="next-steps"></a>Næste trin

Du kan finde flere oplysninger, der er relateret til denne artikel, i følgende ressourcer:

- [Opret værktøjstip på basis af rapportsider i Power BI Desktop](../desktop-tooltips.md)
- [Tilpasning af værktøjstip i Power BI Desktop](../desktop-custom-tooltips.md)
- Videoen Guy in a Cube: [Værktøjstip til rapportside i Power BI – Sådan opretter du et i Power BI Desktop](https://www.youtube.com/watch?v=URTA7JZsAtw)
- Har du spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)