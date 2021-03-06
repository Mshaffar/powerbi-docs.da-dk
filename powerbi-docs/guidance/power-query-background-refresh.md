---
title: Deaktiver baggrundsopdatering i Power Query
description: Vejledning til deaktivering af baggrundsopdatering i Power Query.
author: peter-myers
manager: asaxton
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 09/26/2019
ms.author: v-pemyer
ms.openlocfilehash: 59cb62a9186da03a265fc3a8711d7275c3772af3
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "75623055"
---
# <a name="disable-power-query-background-refresh"></a>Deaktiver baggrundsopdatering i Power Query

Denne artikel er henvendt til udviklere af importdatamodeller, der arbejder med Power BI Desktop.

Når Power Query importerer data, cachelagres der som standard også op til 1000 rækker med eksempeldata for hver forespørgsel. Eksempeldataene er en hjælp, så du kan få en hurtig visning af kildedata og resultater af transformationer for hvert trin i dine forespørgsler. De gemmes separat på disken og ikke i Power BI Desktop-filen.

Når Power BI Desktop-filen indeholder mange forespørgsler, kan hentning og lagring af eksempeldata imidlertid forlænge den tid, det tager at fuldføre en opdatering.

## <a name="recommendation"></a>Anbefaling

Du opnår en hurtigere opdatering ved at indstille Power BI Desktop-filen til at opdatere eksempelcachen _i baggrunden_. Du aktiverer den i Power BI Desktop ved at vælge _Filer > Indstillinger og indstillinger > Indstillinger_ og derefter vælge siden _Dataindlæsning_. Du kan derefter aktivere indstillingen **Tillad, at forhåndsvisning af data downloades i baggrunden**. Bemærk, at denne indstilling kun kan angives for den aktuelle fil.

![Indstillinger for Power BI Desktop-baggrundsdata](media/power-query-background-refresh/power-query-options-background-data.png)

Aktivering af baggrundsopdatering kan resultere i, at eksempeldata bliver forældede. Hvis det sker, får du en meddelelse med den følgende advarsel i Power Query-editor:

![Advarsel fra Power Query-editor om gamle eksempeldata](media/power-query-background-refresh/power-query-preview-data-old.png)

Det er altid muligt at opdatere eksempelcachen. Du kan opdatere den til en enkelt forespørgsel eller til alle forespørgsler ved hjælp af kommandoen **Opdater eksempel**. Du finder den på båndet **Hjem** i Power Query-editor.

![Kommandoer i Power Query-editor til opdatering af eksempeldata](media/power-query-background-refresh/power-query-refresh-preview-data.png)

## <a name="next-steps"></a>De næste trin

Du kan finde flere oplysninger, der er relateret til denne artikel, i følgende ressourcer:

- [Power Query-dokumentation](/power-query/)
- Har du nogen spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)
