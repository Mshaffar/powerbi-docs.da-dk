---
title: Hvor findes min Power BI-lejer?
description: Find ud af, hvor din Power BI-lejer er placeret, og hvordan denne placering markeres. Dette er vigtigt at forstå, da det kan påvirke de interaktioner, du har med tjenesten.
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/09/2019
ms.author: kfollis
LocalizationGroup: Administration
ms.openlocfilehash: 4a763b31333004a8cdecda5262967473817bc983
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83136025"
---
# <a name="where-is-my-power-bi-tenant-located"></a>Hvor findes min Power BI-lejer?

<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

Find ud af, hvor din Power BI-lejer er placeret, og hvordan denne placering markeres. Det er vigtigt at forstå placeringen, da det kan påvirke de interaktioner, du har med tjenesten.

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a>Sådan afgør du, hvor din Power BI-lejer er placeret

Følg disse trin, for at finde det område din lejer befinder sig i.

1. Vælg hjælp ( **?** ) i den øverste menu i Power BI, og vælg derefter **Om Power BI**.

1. Søg efter værdien ud for **Dine data er lagret i**. Dette er det område, din lejer er placeret i. Værdien er også det område, hvor dine data er gemt, medmindre du bruger dedikerede kapaciteter i forskellige områder til dine arbejdsområder.

    ![Dataområde](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a>Sådan vælges dataområdet

Dataområdet er baseret på det land, du vælger, når du opretter lejeren. Dette valg gælder for tilmelding til Office 365 og Power BI, da disse oplysninger deles. Hvis dette er en ny lejer, skal du vælge det relevante land på listen, når du tilmelder dig.

![Valg af land](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

Power BI vælger et dataområde, der er tættest på dette valg, hvilket afgør, hvor data for din lejer lagres.

> [!IMPORTANT]
> Du kan ikke ændre valget, efter du har oprettet lejeren.

Har du flere spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)

