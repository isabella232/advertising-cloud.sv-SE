---
title: Ljudannonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för ljudannonser.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Ljudannonsinställningar

## [!UICONTROL Insert Ad Tag]

*Endast nya annonser*

**[!UICONTROL URL]**: VAST-taggens URL.

**[!UICONTROL Title]**: Ett namn för filen som ska användas i [!UICONTROL Ads] visa och rapportera.

>[!TIP]
>
> Om du vill kontrollera giltigheten för en VAST-tagg klistrar du in den i en webbläsare och trycker på **[!UICONTROL Enter]** nyckel. Om märkordet är giltigt visas en XML-fil som innehåller `<VAST>` nära toppen.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Skrivskyddat) Annonstypen som du skapar, vilket motsvarar den placeringstyp som annonsen kan kopplas till. Standardvärdet är *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Annonsnamnet. Resursens titel används som standard, men du kan ändra namnet.

>[!TIP]
>
> Använd ett namn som är lätt att hitta när du kopplar annonsen till en placering i [!UICONTROL Ads] och i rapporter. Beskriv t.ex. enhetstypen och några nyckelattribut (t.ex. Helgdagsproduktförhandsvisning: 30 sek-ljud&quot;).

**[!UICONTROL Ad Duration]:** Längden på ljudfilen. Det anges automatiskt som antingen [!UICONTROL 15] eller [!UICONTROL 30], beroende på vald annonsenhet.

Det här fältet kanske visas eller inte, beroende på kontobehörigheterna.

**[!UICONTROL VAST Tag]:** (Lägger till annonser med enbart VAST-taggar) En URL för en annonskälla från tredje part. Kontrollera att VAST-taggen bara innehåller ljudmediefiler.

**[!UICONTROL Final VAST Tag]:** (Endast annonser som använder VAST-taggar) URL:en för annonskällan från tredje part med nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Select Rate]:** (Användare med endast tillstånd) En förförhandlad avgift som faktureras via Adobe, eller en av de priser som du har förhandlat och som faktureras via leverantören. Om du vill lägga till en frekvens kontaktar du [!DNL Adobe] kontoteam.

### Pixel

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov, baserat på din spårningsbehov för den enskilda annonsen.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som aktiveras på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG UR]L* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det enkelt att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, eller *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Annonsspecifikationer](ad-specs.md)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

