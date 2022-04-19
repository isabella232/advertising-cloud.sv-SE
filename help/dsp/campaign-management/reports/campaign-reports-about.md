---
title: Om rapporter på plattformen
description: Läs mer om rapportdata som ingår i kampanjhanteringsvyer.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 2f985d9ae8343ea0005f1aa9c33acd603d514f1d
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Om rapporter på plattformen

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Vyerna för kampanjhantering omfattar omfattande rapportdata. De tillgängliga rapporterna hjälper dig att identifiera de paket och placeringar som fungerar bra och de som behöver din uppmärksamhet. Snabba åtgärdsknappar gör dig också mer produktiv.

## Vyn Alla kampanjer

The [!UICONTROL Campaigns] visas en lista med alla kampanjer på ditt konto. &lt;!— [!UICONTROL Subtotals] raden visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader. — Finns det fortfarande en rad med delsummor? Jag ser ingen. —>

### Diagramvy {#chart-view}

Du kan [anpassa trenddiagram för tidsserier](campaign-data-visualization-manage.md) för alla kampanjer med tre mätvärden. Som standard används data för [!UICONTROL Net Spend], [!UICONTROL Impressions]och [!UICONTROL Net CPM] ingår i separata diagram (trellis charts). Du kan ändra måtten om du vill. Om du vill aktivera timdata i trenddiagram för tidsserier ändrar du datumvalet till en enda dag ([!UICONTROL Today], [!UICONTROL Yesterday], eller en viss dag).

![separata trenddiagram för tre mätvärden](/help/dsp/assets/trend-chart-separate.png)

Du kan också täcka över de tre mätvärdena för att enkelt upptäcka avvikelser och områden där du kan förbättra skalan eller prestandan.

![trenddiagram med övertäckning](/help/dsp/assets/trend-chart.png)

### Tabellvy

![Kampanjlista](/help/dsp/assets/campaigns-list.png)

Som standard innehåller varje kampanjrad pacing- och leveransstatistik. Mellanrumsmått innehåller [!UICONTROL Gross Spend (Lifetime)], som inkluderar en mätare av de faktiska utgifterna på målet jämfört med de förväntade utgifterna på målsidan för alla paket i kampanjen, så att ni kan identifiera underpresterande kampanjer i en enda gång. Du kan också [ändra kolumnvyn](column-view-change.md) eller jämn [skapa en anpassad kolumnvy](column-view-create.md).

Du kan fortsätta [anpassa datatabellerna](campaign-data-views-about.md) på ytterligare sätt och [filtrera synliga data](campaign-data-filter.md).

Klicka på kampanjnamnet om du vill visa en mer detaljerad kampanj.

## Single Campaign Reporting {#single-campaign-reporting}

Inom en kampanj kan ni filtrera data baserat på kampanjentiteten: [!UICONTROL Packages], [!UICONTROL Placements]och [!UICONTROL Ads]. Du kan fortsätta [filtrera synliga data](campaign-data-filter.md) om du bara vill inkludera de paket, placeringar eller annonser som du vill se.

![Kampanjentitetsflikar](/help/dsp/assets/campaign-subtabs.png)

### Diagramvy

För varje kampanj kan ni [anpassa trenddiagram för tidsserier](campaign-data-visualization-manage.md) med tre mätvärden som är tillgängliga i varje enhetsvy. Samma mätvärden används för alla trenddiagram för kampanjen.

Se [Diagramvy om kampanjstatistik](#chart-view) för mer information.

### Tabellvy

På varje enhetsflik innehåller varje rad som standard värden för avstånd och leverans, men du kan [ändra kolumnvyn](column-view-change.md) eller jämn [skapa en anpassad kolumnvy](column-view-create.md) som ska gälla alla underflikar för kampanjen. Du kan fortsätta [anpassa datatabellerna](campaign-data-views-about.md) på ytterligare sätt. Varje datatabell innehåller en [!UICONTROL Subtotals] rad, som visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

### Placement [!UICONTROL Inspector] {#placement-inspector}

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

* **[!UICONTROL Inventory]:** Information om alla avtal som är inriktade på placeringen.

   The [!UICONTROL Inventory] -fliken innehåller sök- och filterfunktioner, samma standardalternativ och anpassade kolumnvisningsalternativ som finns på huvudsidan samt snabbåtgärdsknappar på varje rad, som [!UICONTROL Edit] och [!UICONTROL View Report]. The [!UICONTROL Inventory] -fliken möjliggör snabb felsökning genom att visa prestandastatistik, som [!UICONTROL Auctions], [!UICONTROL Bids]och [!UICONTROL Win Rate].

#### Felsökning av lager

| Problem | Möjlig orsak | Åtgärder att vidta |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Utgivaren har inte börjat skicka anbudsförfrågningar. | Kontakta utgivaren för att aktivera erbjudandet. |
|  | Avtalet ställdes in felaktigt, till exempel genom att ett felaktigt externt avtal-ID angavs. | Bekräfta avtalsinformationen och redigera erbjudandet. |
| [!UICONTROL Auctions but no Bids] | Placeringsmålet matchar inte inkommande anbudsförfrågningar för erbjudandet. <br><br> En placering kan till exempel vara inriktad på en geografi som inte är berättigad till erbjudandet. | Redigera placeringsmålen efter behov för att undvika felaktiga målmatchningar. |
|  | Placeringen har ingen aktiv annons med den medietyp som krävs för erbjudandet. | Skapa och bifoga en annons med rätt medietyp till placeringen. |
|  | Placeringen har inte tillräcklig budget. | Öka placeringsbudgeten för att tillåta offerter på inkommande begäranden. |
|  | Flightdatumen för placeringen överlappar inte leveransdatumen för erbjudandet. | Redigera placeringens flygdatum efter behov. |
| [!UICONTROL Low Win Rate] | Placeringens högsta bud (golv eller fast) ligger under det minimiantal som krävs för erbjudandet. | Öka placeringens [!UICONTROL Max Bid] efter behov. |
|  | I placeringen används filter som begränsar budgivning. | Sänk tröskelvärdena för föranbudsfiltren så att fler budgivningar tillåts. |
|  | Målgruppsanpassningen för placeringen är för restriktiv. | Kontrollera om de angivna målgruppsmålen har tillräckligt många aktiva användare och utöka målgruppen om möjligt. |

![placeringsinspektör](/help/dsp/assets/placement-inspector.png)

Du kan exportera data på [!UICONTROL Sites], [!UICONTROL Ads], eller [!UICONTROL Frequency] som en rapport i XLSM-format.

### Andra typer av kampanjnivårapportering

Om du vill se andra databrytningar [rapportsidor på kampanjnivå](/help/dsp/campaign-management/campaigns/campaign-view-report.md). The <!--legacy --> rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]och [!UICONTROL Audience Performance] data.

>[!MORELIKETHIS]
>
>* [Visa Sites, Ads och Frequency Details för en placering](placement-details-view.md)
>* [Om kampanjdatavyer](campaign-data-views-about.md)
>* [Skapa en anpassad kolumnvy](column-view-create.md)
>* [Ändra kolumnvyn](column-view-change.md)
>* [Hantera datavisualiseringar](campaign-data-visualization-manage.md)
>* [Exportera data från en Campaign Management-vy](campaign-export-data.md)
>* [Visa en detaljerad rapport för en kampanj](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

