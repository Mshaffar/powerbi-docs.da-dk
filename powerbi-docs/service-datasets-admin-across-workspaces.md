---
title: Styr brugen af datasæt på tværs af arbejdsområder (prøveversion) – Power BI
description: Lær, hvordan du begrænser flowet af oplysninger i Power BI-lejeren.
author: maggiesMSFT
manager: kfile
ms.reviewer: chbraun
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/31/2019
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 363bf9b107722b3993ed7ac43138c73da03f410a
ms.sourcegitcommit: 7c426a5209d4fdd1360fc3d0442d57991be1984d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2019
ms.locfileid: "66461781"
---
# <a name="control-the-use-of-datasets-across-workspaces-preview"></a>Styr brugen af datasæt på tværs af arbejdsområder (prøveversion)

Brug af datasæt på tværs af arbejdsområder er en effektiv måde at drive datakultur og datademokratisering i en organisation på. Hvis du er Power BI-administrator vil du måske nogle gange begrænse flowet af oplysninger i Power BI-lejeren. Ved hjælp af lejerindstillingen **Brug datasæt på tværs af arbejdsområder** kan du begrænse genbrug af datasæt enten helt eller delvist for hver sikkerhedsgruppe.

![Indstillinger for arbejdsområde for Power BI-administrator](media/service-datasets-admin-across-workspaces/power-bi-admin-workspace-settings.png)

Hvis du slår denne indstilling fra, kan du her se effekten på forfattere af rapporter:

- Knappen til at kopiere rapporter på tværs af arbejdsområder er ikke tilgængelig. 
- I en rapport, der er baseret på et delt datasæt, er knappen **Rediger rapport** ikke tilgængelig.
- I Power BI-tjenesten vises der kun datasæt for det aktuelle arbejdsområde i forbindelse med søgningsoplevelsen.
- I Power BI Desktop vises der kun datasæt fra arbejdsområder, hvor du er medlem, i forbindelse med søgningsoplevelsen.
- I Power BI Desktop får brugerne vist en fejlmeddelelse, hvor de bliver bedt om at oprette forbindelse til et andet datasæt, hvis de åbner en .pbix-fil med en direkte forbindelse til et datasæt uden for et hvilket som helst arbejdsområde.

## <a name="provide-a-link-for-the-certification-process"></a>Angiv et link til certificeringsprocessen

Som lejeradministrator kan du angive en URL-adresse for linket **Få mere at vide** på siden med indstillingen **Godkendelse**.  Dette link kan føre til dokumentation om certificeringsprocessen. Hvis du ikke angiver en destination for linket **Få mere at vide**, peger det som standard på artiklen om [certificering af datasæt](service-datasets-certify.md).

![Få mere at vide om certificering af datasæt](media/service-datasets-certify-promote/power-bi-dataset-learn-more-certification.png)

## <a name="next-steps"></a>Næste trin

- [Brug datasæt på tværs af arbejdsområder (prøveversion)](service-datasets-across-workspaces.md)
- Har du spørgsmål? [Prøv at spørge Power BI-community'et](http://community.powerbi.com/)