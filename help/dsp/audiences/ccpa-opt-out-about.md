---
title: Om [!UICONTROL CCPA Opt-out-of-Sale] Segment och rapporter
description: Lär dig hur du skapar segment för att spåra ID:n från CCPA-förfrågningar om att avanmäla sig från försäljning och hur du hämtar rapporter om ID:n.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Om [!UICONTROL CCPA Opt-out-of-Sale] Segment och rapporter

Du kan spåra användar-ID:n från förfrågningar om att avanmäla dig från försäljning på din webbplats enligt California Consumer Privacy Act (CCPA) genom att [skapa och implementera ett avanmälningssegment för CCPA](ccpa-opt-out-segment-create.md). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar annonseringen i Adobe samla in en pool med ID:n för annonsörens räkning.

## Rapporter om avanmälan till konsumenter

Adobe Advertising genererar månatliga rapporter om ID:n som kunder har skickat in för att avanmäla sig från försäljning för kontot. Data konsoliderar begäranden som samlats in med CCPA-segment för avanmälan från försäljning som skapats i DSP och alla inskickade data via Privacy Service-API.  Rapporterna skapas den första i varje månad för föregående månad. Till exempel är användarlistan för juni tillgänglig den 1 juli.

Varje rapport är tillgänglig som en tabbseparerad textfil komprimerad till GZIP-format. Användar-ID:n som används i CCPA-segment för avanmälan identifieras av segment och annonsörer.

Du kan [hämta länkar till månadsrapporter](ccpa-opt-out-segment-report-retrieve.md) som skapades de senaste tre månaderna, antingen från DSP eller genom att använda DSP [!DNL Trafficking API]. Varje länk gäller i sju dagar, men uppdateras varje gång en kund försöker hämta en länk.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](/help/privacy/ccpa-opt-out-of-sale.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Hämta rapporter om konsumentavanmälan](ccpa-opt-out-segment-report-retrieve.md)
>* [Om Audience Management](audience-about.md)

