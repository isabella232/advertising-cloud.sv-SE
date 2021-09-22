---
title: Om rapporter på plattformen
description: Läs mer om rapportdata som ingår i kampanjhanteringsvyer.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: c1441fb6fddf56a0f0346a967da49efa0fb602ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Om rapporter på plattformen

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Vyerna för kampanjhantering omfattar omfattande rapportdata. De tillgängliga rapporterna hjälper dig att identifiera de paket och placeringar som fungerar bra och de som behöver din uppmärksamhet. Snabba åtgärdsknappar gör dig också mer produktiv.

## Alla kampanjlistor

Vyn [!UICONTROL Campaigns] öppnas med en lista över alla kampanjer i ditt konto. Raden [!UICONTROL Subtotals] visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

![Kampanjlista](/help/dsp/assets/campaigns-list.png)

Som standard innehåller varje kampanjrad pacing- och leveransstatistik. Paketmätvärden inkluderar [!UICONTROL Gross Spend (Lifetime)], som inkluderar en mätare för den faktiska utgiften på målet jämfört med den förväntade kostnaden på målet för alla paket i kampanjen, så att ni snabbt kan identifiera underpresterande kampanjer. Du kan även [ändra kolumnvyn](column-view-change.md) eller till och med [skapa en anpassad kolumnvy](column-view-create.md).

Du kan ytterligare [anpassa datatabellerna](campaign-data-views-about.md) på ytterligare sätt och [filtrera synliga data](campaign-data-filter.md).

Klicka på kampanjnamnet om du vill visa en mer detaljerad kampanj.

## Single Campaign Reporting

Inom en kampanj kan ni filtrera data baserat på kampanjentiteten: [!UICONTROL Packages], [!UICONTROL Placements] och [!UICONTROL Ads]. Du kan ytterligare [filtrera synliga data](campaign-data-filter.md) så att endast de paket, placeringar eller annonser som du vill se inkluderas.

![Kampanjentitetsflikar](/help/dsp/assets/campaign-subtabs.png)

På varje enhetsflik innehåller varje rad som standard plats- och leveransmått, men du kan [ändra kolumnvyn](column-view-change.md) eller till och med [skapa en anpassad kolumnvy](column-view-create.md) som ska användas på alla underflikar för kampanjen. Du kan ytterligare [anpassa datatabellerna](campaign-data-views-about.md) på andra sätt. Varje datatabell innehåller en [!UICONTROL Subtotals]-rad som visar antingen summan eller det genomsnittliga värdet för varje mätvärde över alla synliga rader.

För varje kampanj kan ni också anpassa trenddiagram för tidsserier med tre mätvärden, som är tillgängliga i varje enhetsvy. Som standard ingår data för [!UICONTROL Net Spend], [!UICONTROL Impressions] och [!UICONTROL Net CPM] i separata diagram (trellis-diagram). Du kan ändra måtten om du vill.

![separata trenddiagram för tre mätvärden](/help/dsp/assets/trend-chart-separate.png)

Du kan också täcka över de tre mätvärdena för att enkelt upptäcka avvikelser och områden där du kan förbättra skalan eller prestandan.

![trenddiagram med övertäckning](/help/dsp/assets/trend-chart.png)

Du kan [anpassa trenddiagram](campaign-data-visualization-manage.md) efter kampanj, och samma mätvärden bevaras för alla trenddiagram för kampanjen.

### Placement Inspector

För varje placering kan du [öppna en (detaljvy [!UICONTROL Inspector])](placement-details-view.md), som innehåller följande djupgående data:

* **[!UICONTROL Sites]:** Alla webbplatser där placeringen har fått intrycket.

   Fliken [!UICONTROL Sites] innehåller sök- och filterfunktioner, samma standardvy och anpassade kolumnvisningsalternativ som finns på huvudsidan samt en [!UICONTROL Exclude]-knapp i varje rad så att du snabbt kan utesluta en webbplats från placeringen.

* **[!UICONTROL Ads]:** Alla annonser på platsen.

   Fliken [!UICONTROL Ads] innehåller sök- och filterfunktioner, samma standardvy och anpassade kolumnvisningsalternativ som finns på huvudsidan samt snabbåtgärdsknappar i varje rad, till exempel [!UICONTROL Pause] (så att du snabbt kan pausa en annons).

* **[!UICONTROL Frequency]:** Data för varje annonsfrekvensnivå för placeringen, inklusive:
   * annonsfrekvensen (t.ex. &quot;1&quot; för alla tillfällen då användaren såg en annons en gång)
   * det uppskattade unika antalet enheter/webbläsare eller personer (beroende på den angivna [!UICONTROL Cross Device Level] för placeringen) som fick visningar på den angivna frekvensnivån
   * det uppskattade antalet avtryck på den angivna frekvensnivån
   * den uppskattade genomsnittliga frekvensen för den angivna frekvensnivån. Detta värde är lika med (Estimated Impressions)/(Estimated Uniques).

* **[!UICONTROL Inventory]:** Information om alla erbjudanden som gäller för placeringen i en enda vy.

Fliken Lager innehåller sök- och filterfunktioner, samma standardvy och anpassade kolumnvisningsalternativ som finns på huvudsidan samt snabbåtgärdsknappar i varje rad, till exempel Redigera och Visa rapport. Fliken Inventering hjälper dig att snabbt felsöka genom att visa prestandatillstånd som auktioner, bud, Win Rate osv.

# Felsökning av lager

| Problem | Möjlig orsak | Åtgärder att vidta |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Publisher har inte börjat skicka anbudsförfrågningar | Kontakta utgivaren för att aktivera erbjudandet |
|  | Problem med avtalsinställningar som att ange ett felaktigt externt avtal-ID osv. | Bekräfta avtalsinformationen och redigera erbjudandet |
| [!UICONTROL Non-zero Auctions but no Bids] | Placeringsmålet matchar inte inkommande anbudsförfrågningar från avtal. <br><br> Till exempel kan placeringen ha en annan geografisk inriktning än vad som krävs enligt erbjudandet | Redigera placeringsinställningar på lämpligt sätt för att undvika felmatchningar med avtal |
|  | Placeringen har ingen aktiv annons eller rätt medietyp som krävs enligt avtal | Skapa/bifoga annonser med rätt medietyp till placeringen |
|  | Placeringen har inte tillräcklig budget | Redigera placeringsbudget på lämpligt sätt för att tillåta offerter på inkommande begäranden |
|  | Flightdatum för placeringen överlappar inte med leveransdatum för intrycket enligt avtal | Redigera flygdatum för placeringen |
| [!UICONTROL Low Win Rate] | Det högsta anbudet vid positionen ligger under det lägsta belopp som krävs för erbjudandet (golv eller fast) | Redigera maximalt bud vid placering |
|  | I placeringen används filter som begränsar | Sänk tröskelvärdena för filter före bud för att möjliggöra fler budgivningar |
|  | Målgruppsanpassning vid placering är för restriktiv | Kontrollera att de angivna målgruppsmålen har tillräckligt många aktiva användare och utöka målgruppen om möjligt |

![placeringsinspektör](/help/dsp/assets/placement-inspector-sites.png)

Du kan exportera data på fliken [!UICONTROL Sites], [!UICONTROL Ads] eller [!UICONTROL Frequency] till webbläsarens standardmapp för hämtning som en rapport i XLSM-format.

### Andra typer av kampanjnivårapportering

Om du vill ha mer information läser du [de äldre rapportsidorna](/help/dsp/campaign-management/campaigns/campaign-view-report.md) på kampanjnivå från [!UICONTROL Campaigns Classic]. Den äldre rapporten innehåller avsnitt om [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] och [!UICONTROL Audience Performance]-data.

>[!MORELIKETHIS]
>
>* [Visa Sites, Ads och Frequency Details för en placering](placement-details-view.md)
>* [Om kampanjdatavyer](campaign-data-views-about.md)
>* [Skapa en anpassad kolumnvy](column-view-create.md)
>* [Ändra kolumnvyn](column-view-change.md)
>* [Hantera datavisualiseringar](campaign-data-visualization-manage.md)
>* [Exportera data från en kampanjhanteringsvy](campaign-export-data.md)
>* [Visa en detaljerad rapport för en kampanj](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

