---
title: Inställningar för mobilannonsering
description: Se beskrivningar av tillgängliga annonsinställningar för mobilannonser.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Inställningar för mobilannonsering

## [!UICONTROL Upload or Select Creative]

*Endast nya mobilvideoannonser*

**[!UICONTROL Vertical video]:** (Inte tillgängligt när  [!UICONTROL Custom Transcode] är markerat) Anger att videon är lodrät (stående läge).

**[!UICONTROL Transcode to]:** (Vissa användare, beroende på behörigheter; (valfritt) De format du vill inkludera i din VAST-tagg när utgivaren har särskilda krav på kreativa filer. Format som accepteras av de flesta utgivare är markerade som standard.

**[!UICONTROL Custom Transcode]:** (endast Beta-användare; inte tillgängligt när Lodrät video är valt) Anger att videon använder anpassad omkodning. Om du väljer det här alternativet anger du filformat, videobithastighet, zoom och dimensioner för upp till tre anpassade omkodningsversioner.

**[!UICONTROL XTrader]:** (Vissa användare, beroende på behörigheter) Anger att videon använder en eller flera  [!DNL X_TRADER] flöden.

**[!UICONTROL Upload Video]:** Så här överför du en Raw-resurs till DSP. Gör följande när du väljer det här:

1. Klicka på **[!UICONTROL Choose File]** och leta upp filen på enheten eller i nätverket.
1. Ange en titel för filen, som ska användas i vyn och rapporterna för [!UICONTROL Ads].
1. Klicka på **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** Om du vill välja en tidigare överförd kreativitet i rätt format på kontot.

**[!UICONTROL Advanced: VAST Tag URL]:** (Vissa annonstyper) Så här anger du en VAST-tagg från tredje part som innehåller kreativa resurser och spårar pixlar:

1. Klicka på ![pilen](/help/dsp/assets/compressed.png) bredvid **[!UICONTROL Advanced: VAST Tag URL]**.
1. Ange VAST-taggens URL i fältet **[!UICONTROL URL]**.
1. Ange ett **[!UICONTROL Title]**-värde för filen, som ska användas i vyn och rapporterna för [!UICONTROL Ads].

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]**. Om taggen är giltig visas en XML-fil som innehåller `<VAST>` nära överkanten.

**[!UICONTROL Advanced: 3rd party Ad Tag]:** (Vissa annonstyper) Så här anger du en annonsmarkering från tredje part som innehåller kreativa resurser och spårar pixlar:

1. Klicka på ![pilen](/help/dsp/assets/compressed.png) bredvid **[!UICONTROL Advanced: #3rd party Ad Tag]**.
1. Ange ett **[!UICONTROL Ad Title]**-värde för filen, som ska användas i vyn och rapporterna för [!UICONTROL Ads].
1. Ange taggen ad i fältet **[!UICONTROL Ad Tag]**.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Mobilvisningsannonser

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, som motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 300x250-spelare&quot;).

**\[Annonskälla\]**: Oavsett om Advertising Cloud DSP serverar annonsen (*[!UICONTROL Adobe served]*) eller du använder en annonsserver från tredje part (*[!UICONTROL 3rd party]*).

**[!UICONTROL Creative type]:** (endast annonser som hanteras i Adobe) Anger om resursen är en  *[!UICONTROL Image]* eller en  *[!UICONTROL HTML5]* tillgång.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (endast annonser som hanteras i Adobe) En bildfil eller zippad HTML5-resurs som ska överföras, beroende på vilken typ av projekt det är fråga om. Klicka på **[!UICONTROL Browse]** och leta reda på filen på enheten eller i nätverket. Klicka sedan på **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Endast annonser som visas i Adobe) Den URL som användaren kommer att hamna på när han/hon klickar på annonsen.

**[!UICONTROL Final Click URL]:** (endast annonser som tillhandahålls av Adobe; skrivskyddad) Klicka-URL:en med den nödvändiga  [Advertising Cloud DSP-spårningen ](/help/dsp/campaign-management/macros.md) makroinfogad, om tillämpligt.

**[!UICONTROL Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part. Alla [tidsstämpelparametrar] och [[tidsstämpel]] ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part, med den nödvändiga  [Advertising Cloud DSP-spårningen ](/help/dsp/campaign-management/macros.md) markerad, om tillämpligt.

### [!UICONTROL Basic]: Video Ads

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, som motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du bifogar annonsen till en placering, i annonsvyn och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek telefoninledning&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Player X]:** Annonsenhetens X-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Y]:** Annonsenhetens Y-koordinat. Behåll standardinställningen.

**[!UICONTROL Player Width]:** Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:Höjden** på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

Detta är samma som fältet **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Var ska annonsens videokontroller inkluderas?  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* eller  *[!UICONTROL None]* (standard).

**[!UICONTROL Preserve Aspect Ratio]:** Om bredd- och höjdproportionerna för videon ska behållas (*[!UICONTROL Yes]*) eller om videon ska sträckas ut så att den fyller det tillgängliga utrymmet (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Vissa annonstyper) Antal sekunder som stängningsknappens utseende ska fördröjas.

**[!UICONTROL Click URL]:** (Endast annonser som visas i Adobe) Den URL som användaren kommer att hamna på när han/hon klickar på annonsen.

**[!UICONTROL Final Click URL]:** (endast annonser som tillhandahålls av Adobe; skrivskyddad) Den  [!UICONTROL Click URL] med nödvändig  [Advertising Cloud DSP-spårning ](/help/dsp/campaign-management/macros.md) makroinfogad, om tillämpligt.

**[!UICONTROL VAST Tag]:** (annonser som endast använder VAST-taggar; skrivskyddad) Den VAST-tagg från tredje part som du angav som kreativ resurs.

**[!UICONTROL Final VAST Tag]:** (annonser som endast använder VAST-taggar; skrivskyddad) Den VAST-tagg från tredje part som du angav som den kreativa resursen med den nödvändiga  [Advertising Cloud DSP-spårningen ](/help/dsp/campaign-management/macros.md) makroinsatt, om tillämpligt.

**[!UICONTROL Wmode]:** (Vissa annonstyper) Fönsterläget:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* eller  *[!UICONTROL opaque]*.

### [!UICONTROL Teaser]

*Mobilformat för att peka och spela upp för DSP annonser*

**[!UICONTROL Asset]:** The teaser image or video asset:

* Om du vill välja en egen bild klickar du på **[!UICONTROL Choose File],** letar upp filen på enheten eller nätverket och klickar sedan på **[!UICONTROL Upload Image]**.

   Det bästa sättet är att använda en bild med samma dimensioner som annonsenheten.

* Klicka på **[!UICONTROL Choose Thumbnail]** om du vill välja en bild.

Krav för statiska bildteam:

* Format: GIF, JPEG, PNG
* Bildstorlek: 300x250
* Filstorlek: 50 kB eller mindre
* Rekommenderas: aktion, identifierbar bild, logotyp

Krav för videoutbildning:

* Filtyp: MOV, MP4
* Filstorlek: Mindre än 2 MB
* Varaktighet: 7-10 sek
* Rekommenderas: identifierbara bilder, ansikten, snabbklipp

### [!UICONTROL Overlays]

*Interaktiva interaktiva pre-roll- och Mobile-interaktiva och tap-to-play-format för annonser som DSP*

Följande inställningar gäller för alla övertäckningar som du skapar eller redigerar.

**[!UICONTROL Asset]:** (Endast Raw-resurser) Övertäckningsbildresursen. Filen måste vara i GIF-, JPG- eller PNG-format med en bildruta, och den maximala bildstorleken är mindre än 2 MB. Om du vill överföra resursen klickar du på **[!UICONTROL Browse]**, letar upp filen på enheten eller i nätverket och klickar sedan på **[!UICONTROL Upload]**.

>[!TIP]
>
>Se de [bästa sätten att utforma övertäckningar](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  Den webbadress som visningsprogrammet ska hamna på när de klickar på en övertäckning för annonsen.

**[!UICONTROL X]:X-** koordinaten för övertäckningen. Markera startpositionen för övertäckningen och ange sedan antalet pixlar från startpositionen (till exempel 10px från mitten). Det bästa sättet är att använda *From Center*, vilket förhindrar att övertäckningen flyttas med olika spelarstorlekar på utgivarwebbplatser.

**[!UICONTROL Y]:Y-** koordinaten för övertäckningen. Markera startpositionen för övertäckningen och ange sedan antalet pixlar från startpositionen (till exempel 10px uppifrån). Det bästa sättet är att ange en koordinat *[!UICONTROL From Bottom]* eller *[!UICONTROL From Top],* beroende på i vilken position du vill att övertäckningen ska visas på annonsen.

**[!UICONTROL Layer]:** Det lager som övertäckningen ska visas i. Videon och alla övertäckningar finns i separata lager.

* *[!UICONTROL 2 through 5]:* Framför videon men bakom andra övertäckningar.

* *[!UICONTROL 1]:* Framför videon.

* *[!UICONTROL 0]:* I samma lager som videon. Videon krymper för att fylla det återstående utrymmet. Rekommenderas inte för interaktiv inledning.

* *[!UICONTROL -1]:* Bakom videon.

* *[!UICONTROL -2 through -5]:* Bakom videon men framför andra övertäckningar.

* *[!UICONTROL Background]:* Bakom videon och andra övertäckningar. Övertäckningen skalas till videons hela bredd och höjd och proportionerna bevaras inte.

### [!UICONTROL Endcap]

Föråldrat

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov utifrån dina spårningsbehov.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en  *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil),  *[!UICONTROL HTML]* eller  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i rätt format för den angivna  [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det lättare att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* eller  *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Föråldrat

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [De bästa sätten att utforma övertäckningar](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

