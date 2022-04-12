---
title: Mobile Ad Settings
description: Se beskrivningar av tillgängliga annonsinställningar för mobilannonser.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Mobile Ad Settings

## [!UICONTROL Insert Ad Tag]

*Endast nya mobilvideoannonser*

**[!UICONTROL URL]** eller **[!UICONTROL Ad Tag]**: En VAST-annonstagg eller annonstagg från tredje part som innehåller kreativa resurser och spårar pixlar

**[!UICONTROL Ad Title]** eller **[!UICONTROL Title]**: Ett namn för annonsen som används i [!UICONTROL Ads] visa och rapportera.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]** nyckel. Om märkordet är giltigt visas en XML-fil som innehåller `<VAST>` nära toppen.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Mobile Display Ads

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 300x250-spelare&quot;).

**\[Annonskälla\]**: (Skrivskyddad) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** URL:en för den kreativa resursen från tredje part. Alla [tidsstämpel] och [[tidsstämpel]]-parametrar ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** URL:en för det kreativa materialet från tredje part, med nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

### [!UICONTROL Basic]: Video Ads

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek telefoninledning&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** X-koordinaten för annonsenheten. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Y-koordinaten för annonsenheten. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma sak som **[!UICONTROL Width]** fält.

**[!UICONTROL Player Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma sak som **[!UICONTROL Height]** fält.

**[!UICONTROL Show Controls]:** Var videokontroller för annonsen ska inkluderas: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, eller *[!UICONTROL None]* (standard).

**[!UICONTROL Preserve Aspect Ratio]:** Om videons bredd- och höjdproportioner ska behållas (*[!UICONTROL Yes]*) eller för att sträcka ut videon så att den fyller ut det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Vissa annonstyper) Antalet sekunder som stängningsknappens utseende ska fördröjas.

**[!UICONTROL VAST Tag]:** (Endast annonser som använder VAST-taggar. skrivskyddad) Den VAST-tagg från tredje part som du angav som kreativ resurs.

**[!UICONTROL Final VAST Tag]:** (Endast annonser som använder VAST-taggar. skrivskyddad) Den VAST-tagg från tredje part som du angav som den kreativa resursen med den nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Wmode]:** (Vissa annonstyper) Fönsterläget: *[!UICONTROL window]*, *[!UICONTROL transparent]*, eller *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som aktiveras på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL, i lämpligt format för den angivna [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, eller *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Föråldrat

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

