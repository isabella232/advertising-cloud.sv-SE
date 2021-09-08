---
title: Visa diagnostikrapporter för placering
description: Lär dig hur du diagnostiserar problem med placeringskonfiguration och placering.
feature: Placements
exl-id: d64406b6-83b5-4ae7-984c-98610fc1ee40
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Visa diagnostikrapporter för placering

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Följande verktyg kan hjälpa dig att diagnostisera problem med placeringskonfiguration och paketering när en kampanj är aktiv:

* **[!UICONTROL Change Log]:** Visar ändringar i inställningar för nyckelplacering, t.ex. namn, status och högsta bud. Varje post innehåller datum och användarnamn för den person som gjorde ändringen.
* **[!UICONTROL Ad Approvals]:** Visar om annonser har godkänts eller avvisats av lagerleverantörerna. Du kan ändra status för en annons (t.ex. pausa en avvisad annons) eller öppna annonsinställningarna.
* **[!UICONTROL Non Bids]:** Visar varför DSP inte lade något bud.

1. Öppna diagnostikrapporten:
   1. Öppna placeringsinställningarna:
      1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.
      1. Klicka på kampanjens namn och klicka sedan på **[!UICONTROL Placements]**.
      1. Klicka på **[!UICONTROL ...]>[!UICONTROL Edit]** bredvid placeringsnamnet.
   1. Klicka på ![Placeringsdiagnostik](/help/dsp/assets/placement-diagnostics.png) eller **[!UICONTROL Diagnostic]** i det övre högra hörnet.
1. Gör något av följande:
   * Så här visar du ändringsloggen:
      1. Klicka på **[!UICONTROL Change Log]**.
      1. (Valfritt) Filtrera rapportresultaten:
         * Ändra rapportperioden från de senaste 14 dagarna till en annan punkt på datummenyn (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* eller *[!UICONTROL Last 1 year]*).
         * I den vänstra menyn filtrerar du rapporten med ett specifikt användarnamn.
         * På den högra menyn filtrerar du rapporten efter en specifik placeringsinställning.
   * Så här visar du status för annonsgodkännanden:
      1. Klicka på **[!UICONTROL Ad Approvals]** i det övre högra hörnet.
      1. (Valfritt) Om du vill pausa eller aktivera annonsen klickar du på statusväxeln (![statusväxel](/help/dsp/assets/status-switch.png)) i annonskolumnen).
      1. (Valfritt) Om du vill öppna inställningarna för en annons klickar du på **[!UICONTROL View Ad]** bredvid annonsen.
   * För att se varför DSP inte lade något bud på utplaceringen:
      1. Klicka på **[!UICONTROL Non Bids]** i det övre högra hörnet.
      1. (Valfritt) Om du vill ändra datumintervallet klickar du i datumfältet och väljer ett annat datum eller datumintervall.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Om rapporter på plattformen](campaign-reports-about.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

