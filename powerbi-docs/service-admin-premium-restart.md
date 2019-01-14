---
title: Genstart en Power BI Premium-kapacitet
description: Få mere at vide om, hvordan du genstarter en Power BI Premium-kapacitet for at løse problemer med ydeevnen.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 12/10/2018
ms.author: mblythe
LocalizationGroup: Premium
ms.openlocfilehash: ea36b9aabe3d721a1eeb476507b6e6079397add8
ms.sourcegitcommit: 750f0bfab02af24c8c72e6e9bbdd876e4a7399de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/04/2019
ms.locfileid: "54009006"
---
# <a name="restart-a-power-bi-premium-capacity"></a>Genstart en Power BI Premium-kapacitet

Som Power BI-administrator skal du muligvis genstarte en Premium-kapacitet. I denne artikel forklarer vi, hvordan du genstarter en kapacitet og besvarer flere spørgsmål om genstart og ydeevne.

## <a name="why-does-power-bi-provide-this-option"></a>Hvorfor rummer Power BI denne mulighed?

Power BI giver brugerne mulighed for at udføre komplekse analyser af enorme mængder data. Desværre kan brugerne forårsage problemer med ydeevnen ved at overlæsse Power BI-tjenesten med job, skrive alt for avancerede forespørgsler, oprette cirkulære referencer osv.

Delt kapacitet i Power BI tilbyder beskyttelse mod sådanne situationer ved at angive grænser for filstørrelser, opdatere tidsplaner og andre aspekter af tjenesten. I en Power BI Premium-kapacitet er de fleste af disse begrænsninger dog fjernet. En enkelt rapport med et forkert DAX-udtryk eller en meget kompleks model kan derfor medføre betydelige problemer med ydeevnen. Når en rapport behandles, kan den forbruge alle de tilgængelige ressourcer i kapaciteten. 

Power BI forbedrer konstant, hvordan brugere af Premium-kapacitet beskyttes mod sådanne problemer. Vi giver også administratorer værktøjer til at analysere, hvornår kapaciteter er overbelastede og hvorfor. Du kan finde flere oplysninger i vores [korte træningssession](https://www.youtube.com/watch?v=UgsjMbhi_Bk&feature=youtu.be) og [lange træningssession](https://www.microsoft.com/businessapplicationssummit/video/BAS2018-2174). Du skal også være i stand til at afhjælpe betydelige problemer, når de opstår. Den hurtigste måde at afhjælpe disse problemer på er ved at genstarte kapaciteten.

## <a name="is-the-restart-process-safe-will-i-lose-any-data"></a>Er det sikkert at genstarte? Mister jeg nogen data?

Alle de gemte data, definitioner, rapporter og dashboards på din kapacitet forbliver intakte efter genstart. Når du genstarter en kapacitet, stoppes alle igangværende planlagte opdateringer og ad hoc-opdateringer. Opdateringer genstartes, når kapaciteten er tilgængelig. De brugere, der interagerer med kapaciteten, mister det arbejde, der ikke er gemt. De skal opdatere deres browsere, når genstarten er fuldført.

## <a name="how-do-i-restart-a-capacity"></a>Hvordan genstarter jeg en kapacitet?

Følg denne fremgangsmåde for at genstarte en kapacitet.

1. I Power BI-administrationsportalen skal du på fanen **Kapacitetsindstillinger** gå til din kapacitet. 

1. Føj **funktionsflaget** *CapacityRestart* til kapacitetens URL-adresse: https://app.powerbi.com/admin-portal/capacities/<YourCapacityId>? capacityRestartButton = true.

1. Under **Avancerede indstillinger** > **CAPACITY RESTART** skal du vælge **Genstart kapacitet**.

    ![Genstart kapacitet](media/service-admin-premium-restart/restart-capacity.png)

1. I dialogboksen **Genstart kapacitet** skal du vælge **Ja, genstart kapacitet**.

    ![Bekræft genstart](media/service-admin-premium-restart/confirm-restart.png)

## <a name="how-can-i-prevent-issues-from-happening-in-the-future"></a>Hvordan kan jeg undgå problemer i fremtiden?

Den bedste måde at undgå problemer på er at lære brugerne om effektiv datamodellering. Du kan finde flere oplysninger i vores [træningssession](https://www.microsoft.com/businessapplicationssummit/video/BAS2018-2170).

Vi anbefaler også, at du [overvåger kapaciteterne](service-admin-premium-monitor-capacity.md) jævnligt for tendenser, der indikerer, at der er underliggende problemer. Vi planlægger jævnligt versioner af appen til overvågning og andre værktøjer, så du kan overvåge og administrere kapaciteterne mere effektivt.

## <a name="next-steps"></a>Næste trin

[Hvad er Power BI Premium?](service-premium.md)

Har du flere spørgsmål? [Prøv at spørge Power BI-community'et](http://community.powerbi.com/)