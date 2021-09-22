---
title: Inställningar för annonsering före registrering
description: Se beskrivningar av tillgängliga annonsinställningar för förrollsannonser.
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Inställningar för annonsering före registrering

## [!UICONTROL Upload or Select Creative]

*Endast nya annonser*

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

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, som motsvarar den placeringstyp som annonsen kan kopplas till.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i vyn [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek före (pre-roll)&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** (Endast standard- och överhoppningsbara pre-roll-ads) Bredden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** (Endast standard- och överhoppningsbara pre-roll-ads) Höjden på hela annonsenheten. Det här alternativet kan vara låst beroende på vilken typ av annonsenhet du har valt.

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

**[!UICONTROL Wmode]:** (Endast interaktiv förrullning) Fönsterläge:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* eller  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Endast interaktiv pre-roll) Annonsspelarens format för potentiell inventering:  *[!UICONTROL VPAID]* eller  *[!UICONTROL VPAID & VAST]*. Visningsbarheten mäts alltid för VPAID, men VPAID och VAST inkluderar lager som inte tillåter visningsbarhetsmätning. Tänk på detta om mätvärden för visningsbarhet är viktiga för er kampanj.

**[!UICONTROL Clock Number]**: (Endast interaktiv förrullning. endast används i Förenade kungariket, är bara tillgängligt för användare med behörighet) En unik identifierare som används för att säkerställa att rätt annons sänds. Om den här inställningen inte är tillämplig lämnar du den tom.

### [!UICONTROL Companion]

*Endast DSP annonser*

Du kan också bifoga upp till tre kompletterande banderoller med en annons. Det bästa sättet är att där det är möjligt lägga till komplementbanderoller.

>[!NOTE]
>
> Inte alla utgivare tillåter komplementbanners. Utgivare som tillåter banners ger inga garantier för banneravtryck.
> Det är inte alltid möjligt att förhandsgranska hjälpbanners från annonstaggar från tredje part.

**\[kryssruta\]:** Innehåller den angivna tilläggsbanderollen med annonsen. När kryssrutan är inaktiverad inkluderas inte pekbanderollen.

**\[Banderollstorlek\]:** Den tillhörande banderollstorleken:  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*, som är den vanligaste annonsstorleken och rekommenderas för alla annonser,  *[!UICONTROL 300x60 (Small Banner)]*; eller  *[!UICONTROL 728x90 (Leaderboard)]*, vilket är en mindre vanlig annonsstorlek.

**\[Källa\]:** Om du överför en egen bannerresurs eller använder en tredjepartstagg.

**Tillgång:** (endast Raw-resurser) Den tillhörande banderollresursen. Klicka på **[!UICONTROL Browse]** och leta reda på filen på enheten eller i nätverket. Klicka sedan på **[!UICONTROL Upload]**.

**Ad-tagg]:[!UICONTROL ** (Lägger till med endast VAST-taggar) En URL till en tredjepartsbanderollkälla.

**[!UICONTROL Final Ad Tag]:** (Lägger endast till VAST-taggar) En URL till en källfil för tredjepartsbanderoller med den nödvändiga  [Advertising Cloud DSP-spårningen ](/help/dsp/campaign-management/macros.md) makroinfogad, om tillämpligt.

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

### [!UICONTROL Pixel]

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov utifrån dina spårningsbehov.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som utlöses på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]* för den här annonstypen.

**[!UICONTROL Pixel Type]:** Om pixeln är en  *[!UICONTROL IMG URL]* (1 x 1 pixelbildfil),  *[!UICONTROL HTML]* eller  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i rätt format för den angivna  [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det lättare att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* eller  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [De bästa sätten att utforma övertäckningar](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

