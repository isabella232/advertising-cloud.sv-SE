---
title: Visa diagnostikrapporter för placering
description: Lär dig hur du diagnostiserar problem med placeringskonfiguration och placering.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Visa diagnostikrapporter för placering

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Följande verktyg kan hjälpa dig att diagnostisera problem med placeringskonfiguration och paketering när en kampanj är aktiv:

* **[!UICONTROL Change Log]:** Visar ändringar av inställningar för nyckelplacering, t.ex. namn, status och högsta bud. Varje post innehåller datum och användarnamn för den person som gjorde ändringen.
* **[!UICONTROL Ad Approvals]:** Visar om annonser har godkänts eller avvisats av lagerleverantörerna. Du kan ändra status för en annons (t.ex. pausa en avvisad annons) eller öppna annonsinställningarna.
* **[!UICONTROL Non Bids]:** Visar varför DSP inte lade något bud.

1. Öppna diagnostikrapporten:
   1. Öppna placeringsinställningarna:
      1. På huvudmenyn klickar du på **[!UICONTROL Campaigns]**.
      1. Klicka på kampanjens namn och klicka sedan på **[!UICONTROL Placements]**.
      1. Klicka på bredvid placeringsnamnet  **[!UICONTROL ...]>[!UICONTROL Edit]**.
   1. Klicka på uppe till höger ![Placement Diagnostics](/help/dsp/assets/placement-diagnostics.png) eller **[!UICONTROL Diagnostic]**.
1. Gör något av följande:
   * Så här visar du ändringsloggen:
      1. Klicka på **[!UICONTROL Change Log]**.
      1. (Valfritt) Filtrera rapportresultaten:
         * Ändra rapportperioden från de senaste 14 dagarna till en annan period på menyn Datum (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* eller *[!UICONTROL Last 1 year]*).
         * I den vänstra menyn filtrerar du rapporten med ett specifikt användarnamn.
         * På den högra menyn filtrerar du rapporten efter en specifik placeringsinställning.
   * Så här visar du status för annonsgodkännanden:
      1. Klicka på uppe till höger **[!UICONTROL Ad Approvals]**.
      1. (Valfritt) Om du vill pausa eller aktivera annonsen klickar du på statusväxeln (![Statusväxel](/help/dsp/assets/status-switch.png)) i kolumnen Ad.
      1. (Valfritt) Om du vill öppna inställningarna för en annons klickar du på **[!UICONTROL View Ad]** bredvid annonsen.
   * För att se varför DSP inte lade något bud på utplaceringen:
      1. Klicka på uppe till höger **[!UICONTROL Non Bids]**.
      1. (Valfritt) Om du vill ändra datumintervallet klickar du i datumfältet och väljer ett annat datum eller datumintervall.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Om rapporter på plattformen](campaign-reports-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

