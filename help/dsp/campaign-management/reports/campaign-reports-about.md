---
title: Om rapporter på plattformen
description: Läs mer om rapportdata som ingår i kampanjhanteringsvyer.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: b2393d5e66ba5d3d2dc9816825c05eda076eaad1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Om rapporter på plattformen

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Vyerna för kampanjhantering omfattar omfattande rapportdata. De tillgängliga rapporterna hjälper dig att identifiera de paket och placeringar som fungerar bra och de som behöver din uppmärksamhet. Snabba åtgärdsknappar gör dig också mer produktiv.

## Alla kampanjlistor

The [!UICONTROL Campaigns] visas en lista med alla kampanjer på ditt konto. The [!UICONTROL Subtotals] raden visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

![Kampanjlista](/help/dsp/assets/campaigns-list.png)

Som standard innehåller varje kampanjrad pacing- och leveransstatistik. Mellanrumsmått innehåller [!UICONTROL Gross Spend (Lifetime)], som inkluderar en mätare av de faktiska utgifterna på målet jämfört med de förväntade utgifterna på målsidan för alla paket i kampanjen, så att ni kan identifiera underpresterande kampanjer i en enda gång. Du kan också [ändra kolumnvyn](column-view-change.md) eller jämn [skapa en anpassad kolumnvy](column-view-create.md).

Du kan fortsätta [anpassa datatabellerna](campaign-data-views-about.md) på ytterligare sätt och [filtrera synliga data](campaign-data-filter.md).

Klicka på kampanjnamnet om du vill visa en mer detaljerad kampanj.

## Single Campaign Reporting {#single-campaign-reporting}

Inom en kampanj kan ni filtrera data baserat på kampanjentiteten: [!UICONTROL Packages], [!UICONTROL Placements]och [!UICONTROL Ads]. Du kan fortsätta [filtrera synliga data](campaign-data-filter.md) om du bara vill inkludera de paket, placeringar eller annonser som du vill se.

![Kampanjentitetsflikar](/help/dsp/assets/campaign-subtabs.png)

På varje enhetsflik innehåller varje rad som standard värden för avstånd och leverans, men du kan [ändra kolumnvyn](column-view-change.md) eller jämn [skapa en anpassad kolumnvy](column-view-create.md) som ska gälla alla underflikar för kampanjen. Du kan fortsätta [anpassa datatabellerna](campaign-data-views-about.md) på ytterligare sätt. Varje datatabell innehåller en [!UICONTROL Subtotals] rad, som visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

För varje kampanj kan ni också anpassa trenddiagram för tidsserier med tre mätvärden, som är tillgängliga i varje enhetsvy. Som standard används data för [!UICONTROL Net Spend], [!UICONTROL Impressions]och [!UICONTROL Net CPM] ingår i separata diagram (trellis charts). Du kan ändra måtten om du vill.

![separata trenddiagram för tre mätvärden](/help/dsp/assets/trend-chart-separate.png)

Du kan också täcka över de tre mätvärdena för att enkelt upptäcka avvikelser och områden där du kan förbättra skalan eller prestandan.

![trenddiagram med övertäckning](/help/dsp/assets/trend-chart.png)

Du kan [anpassa trenddiagram](campaign-data-visualization-manage.md) efter kampanj, och samma mätvärden bevaras för alla trenddiagram för kampanjen.

### Placement Inspector

För varje placering kan du [öppna en (detaljvy) [!UICONTROL Inspector])](placement-details-view.md), som innehåller följande detaljerade data:

* **[!UICONTROL Sites]:** Alla platser där placeringen har haft avtryck.

   The [!UICONTROL Sites] -fliken innehåller sök- och filterfunktioner, samma standardalternativ och anpassade kolumnvisningsalternativ som finns på huvudsidan, och en [!UICONTROL Exclude] i varje rad så att du snabbt kan utesluta en plats från placeringen.

* **[!UICONTROL Ads]:** Alla annonser på platsen.

   The [!UICONTROL Ads] -fliken innehåller sök- och filterfunktioner, samma standardalternativ och anpassade kolumnvisningsalternativ som finns på huvudsidan samt snabbåtgärdsknappar på varje rad, som [!UICONTROL Pause] (så att du snabbt kan pausa en annons).

* **[!UICONTROL Frequency]:** Uppgifter för varje annonsfrekvensnivå för placeringen, inklusive
   * annonsfrekvensen (t.ex. &quot;1&quot; för alla tillfällen då användaren såg en annons en gång)
   * det uppskattade unika antalet enheter/webbläsare eller personer (beroende på angivet [!UICONTROL Cross Device Level] för placeringen) som fick intrycket på den angivna frekvensnivån
   * det uppskattade antalet avtryck på den angivna frekvensnivån
   * den uppskattade genomsnittliga frekvensen för den angivna frekvensnivån. Detta värde är lika med (Estimated Impressions)/(Estimated Uniques).

![placeringsinspektör](/help/dsp/assets/placement-inspector-sites.png)

Du kan exportera data på [!UICONTROL Sites], [!UICONTROL Ads], eller [!UICONTROL Frequency] som en rapport i XLSM-format.

### Andra typer av kampanjnivårapportering

Om du vill se andra databrytningar [de äldre rapportsidorna på kampanjnivå](/help/dsp/campaign-management/campaigns/campaign-view-report.md) från [!UICONTROL Campaigns Classic]. Den äldre rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]och [!UICONTROL Audience Performance] data.

>[!MORELIKETHIS]
>
>* [Visa Sites, Ads och Frequency Details för en placering](placement-details-view.md)
>* [Om kampanjdatavyer](campaign-data-views-about.md)
>* [Skapa en anpassad kolumnvy](column-view-create.md)
>* [Ändra kolumnvyn](column-view-change.md)
>* [Hantera datavisualiseringar](campaign-data-visualization-manage.md)
>* [Exportera data från en kampanjhanteringsvy](campaign-export-data.md)
>* [Visa en detaljerad rapport för en kampanj](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

