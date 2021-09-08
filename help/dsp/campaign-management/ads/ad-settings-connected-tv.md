---
title: Inställningar för ansluten TV-annons
description: Se beskrivningar av tillgängliga annonsinställningar för anslutna TV-annonser.
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Inställningar för ansluten TV-annons

## [!UICONTROL Upload or Select Creative]

*Endast nya annonser*

**[!UICONTROL Upload Audio]:** Så här överför du en Raw-resurs till DSP. Gör följande när du väljer det här:

1. Klicka på **[!UICONTROL Choose File]** och leta upp filen på enheten eller i nätverket.
1. Ange en titel för filen, som ska användas i vyn och rapporterna för [!UICONTROL Ads].
1. Klicka på **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Om du vill välja en tidigare överförd kreativitet i rätt format på kontot.

**[!UICONTROL Advanced: VAST Tag URL]:** (Vissa annonstyper) Så här anger du en VAST-tagg från tredje part som innehåller kreativa resurser och spårar pixlar:

1. Klicka på ![pilen](/help/dsp/assets/compressed.png) bredvid **[!UICONTROL Advanced: VAST Tag URL]**.
1. Ange VAST-taggens URL i fältet **[!UICONTROL URL]**.
1. Ange en **[!UICONTROL Title]** för filen, som ska användas i annonsvyn och rapporter.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära överkanten.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, som motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i vyn [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height | Ad Unit Height]:Höjden** på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** Annonsenhetens X-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Annonsenhetens Y-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:Höjden** på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Var ska annonsens videokontroller inkluderas?  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* eller  *[!UICONTROL None]* (standard).

**[!UICONTROL Preserve Aspect Ratio]:** Om bredd- och höjdproportionerna för videon ska behållas (*[!UICONTROL Yes]*) eller om videon ska sträckas ut så att den fyller det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL Click URL]:** (Endast annonser som visas i Adobe) Den URL som användaren kommer att hamna på när han/hon klickar på annonsen.

**[!UICONTROL Final Click URL]:** (endast annonser som tillhandahålls av Adobe; skrivskyddad) Den  [!UICONTROL Click URL] med nödvändig  [Advertising Cloud DSP-spårning ](/help/dsp/campaign-management/macros.md) makroinfogad, om tillämpligt.

**[!UICONTROL VAST Tag]:** (annonser som endast använder VAST-taggar; skrivskyddad) Den VAST-tagg från tredje part som du angav som annonskälla.

**[!UICONTROL Final VAST Tag]:** (annonser som endast använder VAST-taggar; skrivskyddad) Den VAST-tagg från tredje part som du angav som annonskälla med den nödvändiga  [Advertising Cloud DSP tracking-](/help/dsp/campaign-management/macros.md) makrosignerad, om tillämpligt.

**[!UICONTROL Clock Number]**: (Används endast i Förenade kungariket.) är bara tillgängligt för användare med behörighet) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov utifrån dina spårningsbehov.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en  *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil),  *[!UICONTROL HTML]* eller  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det lättare att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* eller  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

