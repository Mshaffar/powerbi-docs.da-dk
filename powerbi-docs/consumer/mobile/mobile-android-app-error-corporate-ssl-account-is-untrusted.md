---
title: Løsning af "Der er ikke tillid til din virksomheds SSL-certifikat"
description: Når du logger på Power BI-appen til Android, kan du få vist meddelelsen "Godkendelsen lykkedes ikke, da denne enhed ikke har tillid til din virksomheds SSL-certifikat
.": ''
author: paulinbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 03/11/2020
ms.author: painbar
ms.openlocfilehash: a68644c63d3d5eaeb54a71683629af01817d62a7
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2020
ms.locfileid: "79114612"
---
# <a name="fixing-corporate-ssl-certificate-is-untrusted---power-bi"></a>Løsning af "Der er ikke tillid til din virksomheds SSL-certifikat" – Power BI
Når du logger på Microsoft Power BI-appen til Android, kan du få vist meddelelsen "Godkendelsen lykkedes ikke, da denne enhed ikke har tillid til din virksomheds SSL-certifikat. Kontakt virksomhedens it-administrator". 

Løsningen afhænger af, hvilket operativsystem du har på din Android-enhed, men der er en række andre problemer, der kan medføre denne fejl.

## <a name="on-android-7-or-later"></a>På Android 7 eller senere
Se efter en opdatering til appen **Chrome**, og installér opdateringen.

## <a name="on-android-6-and-earlier"></a>På Android 6 eller tidligere
Du skal muligvis installere en opdateret version af System Webview på enheden. Den kan være installeret på din enhed, og du skal muligvis blot klikke på **Opdater**.

Hvis System Webview ikke er installeret på din enhed:

1. Luk Power BI på din Android-enhed.
2. Åbn Google Play Butik, og søg efter **System Webview** af Google Inc.
3. Installér appen.
4. Genstart Power BI-appen, og log på.

## <a name="time-zone-settings"></a>Indstillinger for tidszone
Tidszonen kan være angivet forkert på din enhed. 

Gå til **Indstillinger** > **System** > **Dato og klokkeslæt** for at se indstillingerne.

## <a name="custom-authentication-server"></a>Brugerdefineret godkendelsesserver
Hvis du bruger en brugerdefineret godkendelsesserver, kan det skyldes, at certifikatet i virksomhedens godkendelsesserver ikke er gyldigt. Arbejd sammen med din organisations it-afdeling for at teste virksomhedens konfiguration af godkendelsesserveren ved hjælp af vejledningen i [denne artikel](https://support.microsoft.com/help/3203929/using-adal-to-authenticate-from-android-devices-fails-if-additional-ce).

## <a name="next-steps"></a>De næste trin
* [Download Android-appen](https://go.microsoft.com/fwlink/?LinkID=544867) fra Android App Store.
* Har du nogen spørgsmål? [Prøv at spørge Power BI-community'et](https://community.powerbi.com/) 

