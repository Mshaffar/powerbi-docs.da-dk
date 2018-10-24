---
title: Enkeltlogon i Power BI-mobilappen til Windows
description: Læs om enkeltlogon (SSO – Single Sign-On) i Power BI-mobilappen til Windows. SSO betyder, at du får adgang til alle programmer og ressourcer, du har brug for til din virksomhed, ved at logge på én gang, med en enkelt brugerkonto.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 09/17/2018
ms.author: maggies
ms.openlocfilehash: f13b6e0a6583bcb66da0fb0a27188c83c4bf6806
ms.sourcegitcommit: 698b788720282b67d3e22ae5de572b54056f1b6c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/17/2018
ms.locfileid: "45975029"
---
# <a name="single-sign-on-in-the-power-bi-mobile-windows-app"></a>Enkeltlogon i Power BI-mobilappen til Windows

Læs om enkeltlogon (SSO – Single Sign-On) i Power BI-mobilappen til Windows. SSO betyder, at du får adgang til alle programmer og ressourcer, du har brug for til din virksomhed, ved at logge på én gang, med en enkelt brugerkonto. Når du er logget på, kan du få adgang til alle disse programmer, uden at du skal godkende igen. 

Da Power BI-appen til Windows er integreret i Azure Active Directory, kan du bruge din primære organisationskonto til både at logge på dine domænetilsluttede enheder og Power BI-tjenesten uden problemer. Hvis du får vist Power BI på en Windows-telefon, skal du sørge for, at den konto, du bruger til Power BI, er konfigureret som en arbejds- eller skolekonto i enhedsindstillingerne.  

SSO er kun aktiveret for Windows-enheder, der administreres af Windows Azure Active Directory. 

## <a name="sign-in-with-sso"></a>Log på med SSO

Appen forsøger automatisk at godkende dig til Power BI-tjenesten ved hjælp af SSO, første gang du installerer appen, for at forenkle logonprocessen. Kun hvis denne proces ikke kan udføres, bliver du bedt om at angive dine legitimationsoplysninger til Power BI.  

Du kan også bruge SSO, hvis du allerede bruger Power BI-mobilappen til Windows, når du opgraderer til den nye version af appen. Log af appen, luk den, og åbn den igen. Når appen åbnes igen, forsøger den automatisk at bruge dine aktuelle Windows-legitimationsoplysninger til at godkende dig til Power BI-tjenesten. 

Hvis du ikke vil bruge dine aktuelle Windows-legitimationsoplysninger til den aktive session til at logge på Power BI, skal du blot gå til **indstillinger**, logge af og logge på med dine andre legitimationsoplysninger. 
 
## <a name="next-steps"></a>Næste trin

- [Kom i gang med Power BI-mobilappen til Windows 10](mobile-windows-10-phone-app-get-started.md)
- Har du spørgsmål? [Prøv at spørge Power BI-community'et](http://community.powerbi.com/)
