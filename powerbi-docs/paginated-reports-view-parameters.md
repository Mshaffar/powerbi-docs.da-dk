---
title: Få vist parametre for sideinddelte rapporter i Power BI-tjenesten (eksempelvisning)
description: I denne artikel kan du læse om, hvordan du arbejder med parametre for sideinddelte rapporter i Power BI-tjenesten.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: report-builder
ms.topic: conceptual
ms.date: 11/05/2018
ms.author: maggies
ms.openlocfilehash: 404ec820b766716810b2881351f8be8e77902803
ms.sourcegitcommit: b03912343a5a214c6bb972aaa6aa051c2a5f4332
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2018
ms.locfileid: "52900146"
---
# <a name="view-parameters-for-paginated-reports-in-the-power-bi-service-preview"></a>Få vist parametre for sideinddelte rapporter i Power BI-tjenesten (eksempelvisning)

I denne artikel kan du læse om, hvordan du arbejder med parametre for sideinddelte rapporter i Power BI-tjenesten.  En rapportparameter gør muligt at filtrere rapportdata. Parametre tilbyder en liste over tilgængelige værdier, og du kan vælge en eller flere værdier. Nogle gange har parametre en standardværdi, og nogle gange skal du vælge en værdi, før du kan se rapporten.  

Når du får vist en rapport, der indeholder parametre, viser værktøjslinjen for rapportfremviseren de enkelte parametre, så du kan angive værdier interaktivt. I illustrationen nedenfor vises parameterområdet for en rapport med parametre for **Buying Group**, **Location**, **From Date** og **To Date**.  

## <a name="parameters-pane-in-the-power-bi-service"></a>Ruden Parameters i Power BI-tjenesten

![Få vist sideinddelt rapport med parametre](media/paginated-reports-view-parameters/power-bi-paginated-view-parameters.png)
  
1.  **Ruden Parameters** På værktøjslinjen i rapportfremviseren vises der en prompt, f.eks. "Required", eller en standardværdi for de enkelte parametre.    
  
2.  **Parametrene Invoices From/To Date** De to dataparametre har standardværdier. Hvis du vil ændre datoen, skal du angive en dato i tekstfeltet eller vælge en dato i kalenderen.  
  
3.  **Parameteren Location** Placeringsparameteren er angivet, så du kan vælge en, mange eller alle værdier. 
  
4.  **View Report** Når du har angivet eller ændret parameterværdier, skal du klikke på **View Report** for at køre rapporten. 

5. **Default values** Hvis alle parametre har standardværdier, køres rapporten automatisk ved første visning. Nogle parametre i denne rapport har ikke standardværdier, så du kan ikke se rapporten, før du vælger værdier.  

## <a name="next-steps"></a>Næste trin

[Opret parametre for sideinddelte rapporter i Power BI-tjenesten](paginated-reports-parameters.md)