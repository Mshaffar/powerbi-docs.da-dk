---
title: 'DAX: DIVIDE-funktion vs. divisionsoperator (/)'
description: Vejledning til, hvornår du skal bruge DAX DIVIDE-funktionen.
author: peter-myers
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 09/09/2019
ms.author: v-pemyer
ms.openlocfilehash: b792c7d9f6200544188e9f9fe711cd1394e8b921
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "83279566"
---
# <a name="dax-divide-function-vs-divide-operator-"></a>DAX: DIVIDE-funktion vs. divisionsoperator (/)

Som dataudformer, kan du vælge at bruge funktionen [DIVIDE](/dax/divide-function-dax) eller divisionsoperatoren (/ – skråstreg), når du skriver et DAX-udtryk for at dele en tæller med en nævner.

Når du bruger funktionen DIVIDE, skal du overføre udtryk for tæller og nævner. Du kan også overføre en værdi, der repræsenterer et _alternativt resultat_.

```dax
DIVIDE(<numerator>, <denominator> [,<alternateresult>])
```

Funktionen DIVIDE er designet til automatisk at håndtere division med nul. Hvis et alternativt resultat ikke overføres, og nævneren er nul eller TOM, returnerer funktionen TOM. Hvis der sendes et alternativt resultat, returneres det i stedet for TOM.

Funktionen DIVIDE er praktisk, fordi udtrykket ikke først behøver at teste nævnerværdien. Funktionen er også bedre optimeret til at teste nævnerværdien end funktionen [IF](/dax/if-function-dax). Gevinsten ved ydeevnen er markant, da kontrol af division med nul er dyr. Derudover resulterer brug af DIVIDE også i et mere præcist og elegant udtryk.

## <a name="example"></a>Eksempel

Følgende målingsudtryk producerer sikker division, men det involverer brug af fire DAX-funktioner.

```dax
Profit Margin =
IF(
    OR(
        ISBLANK([Sales]),
        [Sales] == 0
    ),
    BLANK(),
    [Profit] / [Sales]
)
```

Dette målingsudtryk opnår samme resultat, men er endnu mere effektivt og elegant.

```dax
Profit Margin =
DIVIDE([Profit], [Sales])
```

## <a name="recommendations"></a>Anbefalinger

Vi anbefaler, at du bruger funktionen DIVIDE, når nævneren er et udtryk, der _kan_ returnere nul eller TOM.

Hvis nævneren er en konstant værdi, anbefaler vi, at du bruger divisionsoperatoren. I dette tilfælde gennemføres divisionen, og dit udtryk kører bedre, da unødvendige test undgås.

Overvej nøje, om funktionen DIVIDE skal returnere en alternativ værdi. I forbindelse med målinger er det normalt et bedre design, at de returnerer TOM. Returnering af TOM er bedre, fordi rapportvisualiseringer som standard fjerner grupperinger, når opsummeringer er TOMME. Det gør det muligt for visualiseringen at fokusere på grupper, der indeholder data. Når det er nødvendigt, kan du konfigurere visualiseringen til at vise alle grupper (der returnerer værdier eller er TOMME) i filterkonteksten ved at aktivere indstillingen [Vis elementer uden data](../create-reports/desktop-show-items-no-data.md).

## <a name="next-steps"></a>Næste trin

Du kan finde flere oplysninger om denne artikel i følgende ressourcer:

- [Henvisning til DAX (Data Analysis Expressions)](/dax/)
- Har du spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/)

