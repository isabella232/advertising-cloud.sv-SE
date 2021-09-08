---
title: Om annonshantering i Advertising Cloud DSP
description: Läs mer om annonshantering.
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Om annonshantering i Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP erbjuder två sätt att serva era annonser:

* Advertising Cloud DSP levererar annonserna kostnadsfritt när du överför ditt eget material (till exempel banners, videor, ljudfiler eller URL:er) direkt till DSP. För resurser som DSP hanteras har du tillgång till ytterligare funktioner, till exempel övertäckningar.

* Om du använder en annonsserver från tredje part (till exempel Google, Flashtalk eller Sizmek) kan du överföra dina tredjepartstaggar för annonsvisning till DSP enskilt eller gruppvis. För massöverföring måste du antingen a) överföra DoubleClick- och Flashtalk-taggmallar eller b) hämta en mall, ange dina taggar i mallen och sedan överföra mallen igen.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

När era annonser väl är klara måste ni bifoga varje annons till en placering, som inkluderar målinriktningsparametrar (som geo, målgrupp, enhet och målinriktning mot lager) som styr hur kampanjen kommer att leverera. Du kan bifoga en annons till en eller flera placeringar.

## Tillgängliga annonstyper

* Ljud
* Ansluten TV
* Visa
* Mobil
* Inbyggt
* Före rullning

Mer information om annonstyperna finns i [Tillgängliga annonstyper](ad-types.md) och den fullständiga [annonsspecifikationen](/help/dsp/assets/ad-specs.pdf).

## Special Ad Features

Följande funktioner är endast tillgängliga för annonser som DSP administreras.

### Companion Banners

Ledande banners serveras tillsammans med [pre-roll-ads](ad-settings-pre-roll.md) eller (med vissa utgivare) [ljudannonser](ad-settings-audio.md) och kan förstärka varumärkes- och meddelandekopplingen.

>[!NOTE]
>
>* Inte alla utgivare tillåter komplementbanners. Utgivare som tillåter banners ger inga garantier för banneravtryck.
>* Det är inte alltid möjligt att förhandsgranska hjälpbanners från annonstaggar från tredje part.


Du kan överföra din egen tillhörande banderollresurs eller överföra en iFrame- eller skriptbanderolltagg från en certifierad tredjepartsleverantör av annonstjänster.

### Övertäckningar

Övertäckningar hjälper till med beständig branding i hela videon och kan få fler klick. Överläggsfunktionen är tillgänglig för [interaktiva pre-roll-ads](ad-settings-pre-roll.md) och för [mobilannonser i interaktiva och tryck-för-spela-format](ad-settings-mobile.md).

Se de [bästa sätten att utforma övertäckningar](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Lärare

Ett teaser är en slående bild som lockar tittaren att spela upp en annons. Teasers apply only to mobile tap-to-play ad ad annonsformat.

## Advertising Cloud DSP Ad Approvals

När du skapar en annons granskar Advertising Cloud DSP den för att se om det finns känsliga kategorier, klickar på URL-funktionen och förhandsgranskar återgivningen.

Till att börja med visas en röd punkt i kolumnen [!UICONTROL Status]. Granskningsprocessen tar normalt 24-48 timmar. En trasig annons kan dock ha en väntande status i mer än 48 timmar, så du har tid att åtgärda fel innan annonsen refuseras. Avvisade annonser innehåller en orsak till refuseringen.

När DSP godkänner en annons visas en grön punkt i statuskolumnen.

![godkännandeindikator i  [!UICONTROL Status] kolumn](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Din annons kan endast användas om både DSP och SSP har godkänt den kreativa processen. Varje enskild SSP har sina egna krav och processer för godkännande.

>[!MORELIKETHIS]
>
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-third-party.md)
>* [Tillgängliga annonstyper](ad-types.md)
>* [Annonsspecifikationer](/help/dsp/assets/ad-specs.pdf)

