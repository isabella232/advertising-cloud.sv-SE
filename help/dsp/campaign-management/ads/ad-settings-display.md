---
title: Visa annonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för displayannonser.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Visa annonsinställningar

Följande inställningar gäller för vanliga displayannonser. Du kan också visa videobrev för att klicka-för-spela-annonser för webbannonser, men vi rekommenderar inte det eftersom det inte finns många utgivare som stöder dem.

## [!UICONTROL Ad Options]

### Grundläggande

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, som motsvarar den placeringstyp som annonsen kan kopplas till. Standardvärdet är *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering, i vyn [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 300x250-spelare&quot;).

**\[Annonskälla\]**: Oavsett om Advertising Cloud DSP serverar annonsen (*[!UICONTROL Adobe served]*) eller du använder en annonsserver från tredje part (*[!UICONTROL 3rd party]*).

**[!UICONTROL This is an expandable Banner]:** (Endast annonser från tredje part) Anger att annonsen är en utbyggbar banners. De relaterade expansionsinställningarna avgör vilket lager som ska köpas, så se till att de återspeglar annonsbeteendet.

**[!UICONTROL Expansion Method]:** (Endast expanderbara banners från tredje part) Om bannern utökas  *[!UICONTROL Click]* eller  *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Endast expanderbara banners från tredje part) Riktningen som annonsen utökas i:  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]* eller  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Endast utbyggbara banners från tredje part) Den certifierade leverantör som annonsen är tillgänglig för:  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]* eller  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part. Alla [tidsstämpelparametrar] och [[tidsstämpel]] ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part, med den nödvändiga  [Advertising Cloud DSP-spårningen ](/help/dsp/campaign-management/macros.md) markerad, om tillämpligt.

**[!UICONTROL Creative type]:** (endast annonser som hanteras i Adobe) Anger om resursen är en  *[!UICONTROL Image]* eller en  *[!UICONTROL HTML5]* tillgång.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (endast annonser som hanteras i Adobe) En bildfil eller zippad HTML5-resurs som ska överföras, beroende på vilken typ av projekt det är fråga om. Klicka på **[!UICONTROL Browse]** och leta reda på filen på enheten eller i nätverket. Klicka sedan på **[!UICONTROL Upload]** eller **[!UICONTROL Upload Image]**.

**[!UICONTROL Ad Size]:** Annonsens bredd och höjd. Det måste vara en [standardstorlek](/help/dsp/assets/ad-specs.pdf) som stöds för visning och visning. Du kan ange annonsstorleken manuellt innan du överför annonsen eller ange en [!UICONTROL Display Code]. Om du inte anger annonsstorleken anges dimensionerna för den överförda annonstaggen eller annonstaggen automatiskt som skrivskyddade. Observera att annonsen för bildskärm inte sparas om dimensionerna inte finns i standardvisning i storlekar - t.ex. 301x250 i stället för 300x250 i annonsstorlek.

>[!IMPORTANT]
>
> Annonsstorleken som deklareras i fälten för bredd och höjd matchas med inkommande anbudsförfrågningar. Leveransproblem kan uppstå om annonsens dimensioner inte matchar den deklarerade annonsstorleken.

**[!UICONTROL Click URL]:** (Endast annonser som visas i Adobe) Den URL som användaren kommer att hamna på när han/hon klickar på annonsen.

**[!UICONTROL Final Click URL]:** (endast annonser som tillhandahålls av Adobe; skrivskyddad) Den  [!UICONTROL Click URL] med nödvändig  [Advertising Cloud DSP-spårning ](/help/dsp/campaign-management/macros.md) makroinfogad, om tillämpligt.

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
>* [Visa en lista över placeringar som är kopplade till en annons](ad-list-placements.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

