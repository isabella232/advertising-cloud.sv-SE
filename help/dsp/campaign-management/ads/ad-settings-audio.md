---
title: Ljudannonsinställningar
description: Se beskrivningar av tillgängliga annonsinställningar för ljudannonser.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Ljudannonsinställningar

## [!UICONTROL Upload or Select Creative]

*Endast nya annonser*

**[!UICONTROL Upload Audio]:** Så här överför du en råresurs till DSP. Gör följande när du väljer det här:

1. Klicka **[!UICONTROL Choose File]** och hitta filen på din enhet eller ditt nätverk.
1. Ange en rubrik för filen som ska användas i [!UICONTROL Ads] visa och rapportera.
1. Klicka på **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Om du vill välja ett tidigare överfört kreativt format i rätt format på kontot.

**[!UICONTROL Advanced: VAST Tag URL]:** Så här anger du en VAST-tagg från tredje part som innehåller kreativa resurser och spårar pixlar:

1. Klicka ![pil](/help/dsp/assets/compressed.png) nästa **[!UICONTROL Advanced: VAST Tag URL]**.
1. I **[!UICONTROL URL]** anger du VAST-taggens URL-adress.
1. Ange **[!UICONTROL Title]** för filen som ska användas i [!UICONTROL Ads] visa och rapportera.

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

**[!UICONTROL Click URL]:** (Annonser som använder råmaterial och endast annonser. (valfritt) Den URL som visningsprogrammet kommer att hamna på när de klickar på en visningsbanderoll som medföljer annonsen.

**[!UICONTROL Final Click URL]:** (Annonser som använder råmaterial och endast annonser. skrivskyddad) [!UICONTROL Click URL] med nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL VAST Tag]:** (Lägger till annonser med enbart VAST-taggar) En URL för en annonskälla från tredje part. Kontrollera att VAST-taggen bara innehåller ljudmediefiler.

**[!UICONTROL Final VAST Tag]:** (Endast annonser som använder VAST-taggar) URL:en för annonskällan från tredje part med nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Select Rate]:** (Användare med endast tillstånd) En förförhandlad avgift som faktureras via Adobe, eller en av de priser som du har förhandlat och som faktureras via leverantören. Om du vill lägga till en frekvens kontaktar du [!DNL Adobe] kontoteam.

### [!UICONTROL Companion]

*Endast DSP annonser*

Du kan också bifoga upp till tre kompletterande banderoller med en annons. Det bästa sättet är att där det är möjligt lägga till komplementbanderoller.

>[!NOTE]
>
>* Inte alla utgivare tillåter komplementbanners. Utgivare som tillåter banners ger inga garantier för banneravtryck.
>* Det är inte alltid möjligt att förhandsgranska hjälpbanners från annonstaggar från tredje part.


**\[Kryssruta\]:** Innehåller den angivna komplementbanderollen med annonsen. När kryssrutan är inaktiverad inkluderas inte pekbanderollen.

**\[Banderollstorlek\]:** Den tillhörande banderollstorleken: *[!UICONTROL 300x250]* (används för [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]och [!DNL TuneIn]), *[!UICONTROL 640x640]* (används för [!DNL Spotify), or *1024x1024]* (används för [!DNL SoundCloud]).

**\[Källa\]:** Källan till den tillhörande banderollresursen:

* *[!UICONTROL Upload My Own Asset]:* För att överföra din egen resurs.
* *[!UICONTROL Use a Third Party Tag]:* Att ange en iFrame- eller script-tagg från en certifierad tredjepartsannons som servar partner.

Använd en tagg från tredje part när du vill spåra tredjeparts banneravtryck.

**[!UICONTROL Asset]:** (Endast Raw-resurser) Den tillhörande banderollresursen i GIF, JPG eller PNG-format. Klicka **[!UICONTROL Browse]** och leta upp filen på din enhet eller ditt nätverk och klicka sedan på **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Endast Raw-resurser) Den URL som visningsprogrammet kommer att hamna på när de klickar på den tillhörande banderollen för annonsen. Den kan innehålla en klickomdirigering med hjälp av en klickspårning från tredje part.

**[!UICONTROL Final Click URL]:** (Endast råtillgångar) skrivskyddad) Klicka-URL:en med den [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

**[!UICONTROL Ad Tag]:** (Endast annonser som använder annonstaggar från tredje part) En iFrame- eller skriptbanderolltagg för en tredjeparts extern banderollkälla. Det måste komma från en certifierad tredjepartsleverantör.

**[!UICONTROL Final Ad Tag]:** (Endast annonser som använder annonstaggar från tredje part) Annonstaggen med de nödvändiga [Advertising Cloud DSP tracking macros](/help/dsp/campaign-management/macros.md) infogad, om tillämpligt.

### Pixel

Alla befintliga pixlar för händelsespårning för placeringen bifogas automatiskt. Du kan frigöra befintliga pixlar och skapa nya vid behov utifrån dina spårningsbehov.

Följande inställningar gäller för varje pixel som du skapar eller redigerar.

**[!UICONTROL Integration Event]:** Den händelse som utlöser pixeln som utlöses. Använd pixlar som aktiveras på *[!UICONTROL Impression]* eller *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Om pixeln är en *[!UICONTROL IMG UR]L* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Pixelbildens URL i lämpligt format för den angivna pixeltypen.

**[!UICONTROL Pixel Name]:** Pixelnamnet. Använd ett namn som gör det lättare att identifiera pixeln.

**[!UICONTROL Pixel Provider]:** Pixelprovidern: *[!UICONTROL None]*, *[!UICONTROL Nielsen]*, eller *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Visa en lista över placeringar som är kopplade till en annons](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)

