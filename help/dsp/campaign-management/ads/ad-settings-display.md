---
title: Visa annonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för displayannonser.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Visa annonsinställningar

Följande inställningar gäller för vanliga displayannonser.

## [!UICONTROL Ad Options]

### Grundläggande

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till. Standardvärdet är *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering i [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 300x250-spelare&quot;).

**\[Annonskälla\]**: (Skrivskyddad) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Endast annonser från tredje part) Anger att annonsen är en utbyggbar banners. De relaterade expansionsinställningarna avgör vilket lager som ska köpas, så se till att de återspeglar annonsbeteendet.

**[!UICONTROL Expansion Method]:** (Endast utbyggbara banners från tredje part) Om bannern utökas *[!UICONTROL Click]* eller *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Endast expanderbara banners från tredje part) Riktningen som annonsen utökas i: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, eller *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Endast utbyggbara banners från tredje part) Den certifierade leverantör som annonsen är tillgänglig för: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, eller *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part. Alla [tidsstämpel] och [[tidsstämpel]]-parametrar ersätts med faktiska värden.

**[!UICONTROL Final Display Code]:** (Endast annonser från tredje part) URL:en för den kreativa resursen från tredje part, med nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Ad Size]:** Annonsens bredd och höjd. Det måste vara en [stöd för standardstorlek](/help/dsp/assets/ad-specs.pdf). Du kan ange annonsstorleken manuellt innan du överför annonsen eller ange en [!UICONTROL Display Code]. Om du inte anger annonsstorleken anges dimensionerna för den överförda annonstaggen eller annonstaggen automatiskt som skrivskyddade. Observera att annonsen för bildskärm inte sparas om dimensionerna inte finns i standardvisning i storlekar - t.ex. 301x250 i stället för 300x250 i annonsstorlek.

>[!IMPORTANT]
>
> Annonsstorleken som deklareras i fälten för bredd och höjd matchas med inkommande anbudsförfrågningar. Leveransproblem kan uppstå om annonsens dimensioner inte matchar den deklarerade annonsstorleken.

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
>* [Visa en lista över placeringar som är kopplade till en annons](ad-list-placements.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

