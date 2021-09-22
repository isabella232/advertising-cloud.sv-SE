---
title: Om [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter
description: Lär dig hur du skapar segment för att spåra ID:n från CCPA-förfrågningar om att avanmäla sig från försäljning och hur du hämtar rapporter om ID:n.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Om [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter

Du kan spåra användar-ID:n från förfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA), genom att [skapa och implementera ett CCPA-segment för avanmälan från försäljning](ccpa-opt-out-segment-create.md). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar Advertising Cloud samla in en pool med ID:n för annonsörens räkning.

## Rapporter om avanmälan till konsumenter

Advertising Cloud genererar månadsrapporter om ID:n som kunder har skickat in för att avanmäla sig från försäljning för kontot. Data konsoliderar begäranden som samlats in med CCPA-segment för avanmälan från försäljning som skapats i Advertising Cloud DSP och alla överföringar som gjorts via Privacy Service-API:t.  Rapporterna skapas den första i varje månad för föregående månad. Till exempel är användarlistan för juni tillgänglig den 1 juli.

Varje rapport är tillgänglig som en tabbseparerad textfil komprimerad till GZIP-format. Användar-ID:n som används i CCPA-segment för avanmälan identifieras av segment och annonsörer.

Du kan [hämta länkar till de månadsrapporter](ccpa-opt-out-segment-report-retrieve.md) som skapades under de senaste tre månaderna, antingen från Advertising Cloud DSP eller med Advertising Cloud [!DNL Trafficking API]. Varje länk gäller i sju dagar, men uppdateras varje gång en kund försöker hämta en länk.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Skapa och implementera ett  [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Hämta rapporter om konsumentavanmälan](ccpa-opt-out-segment-report-retrieve.md)
>* [Om Audience Management](audience-about.md)

