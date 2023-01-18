---
title: Universella inställningar för videoreklam
description: Se beskrivningar av tillgängliga annonsinställningar för universella videoannonser.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Universella inställningar för videoreklam

*Öppna betafunktion*

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]:** VAST-taggens URL.

**[!UICONTROL Title]:** En rubrik för filen, som finns i [!UICONTROL Ads] visa och rapportera.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]** nyckel. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära toppen.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering i [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek universell video&quot;).

**[!UICONTROL Show Controls]:** Var videokontroller för annonsen ska inkluderas: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, eller *[!UICONTROL None]* (standard).

**[!UICONTROL Preserve Aspect Ratio]:** Om videons bredd- och höjdproportioner ska behållas (*[!UICONTROL Yes]*) eller för att sträcka ut videon så att den fyller ut det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Endast annonser som använder VAST-taggar. skrivskyddad) Den VAST-tagg från tredje part som du angav som annonskälla.

**[!UICONTROL Final VAST Tag]:** (Endast annonser som använder VAST-taggar. skrivskyddad) Den VAST-tagg från tredje part som du angav som annonskälla med den nödvändiga [Annonsera DSP spårningsmakron](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Wmode]:** Fönsterläge: *[!UICONTROL window]*, *[!UICONTROL transparent]*, eller *[!UICONTROL opaque]*. Om den här inställningen inte är tillämplig lämnar du den tom.

**[!UICONTROL Video Format]:** Annonsspelarens format för potentiell inventering: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*, eller *[!UICONTROL VAST]*. Synligheten mäts alltid för [!UICONTROL VPAID], men [!UICONTROL VPAID & VAST] innehåller lager som inte tillåter visningsmätning. Tänk på den här skillnaden om mätvärden för visningsbarhet är viktiga för er kampanj.

Använd *[!UICONTROL VAST]*, vilket inte tillåter visningsmätning, när du har en ansluten TV eller ett lager som endast kräver VAST-format (vanligtvis från leverantörer som Google Ad Manager, Appnexus, SpotX och Freewheel) som mål.

**[!UICONTROL Clock Number]**: (Används endast i Förenade kungariket.) är bara tillgängligt för användare med behörighet) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som aktiveras på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL, i lämpligt format för den angivna [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, eller *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [DSP makron](/help/dsp/campaign-management/macros.md)

