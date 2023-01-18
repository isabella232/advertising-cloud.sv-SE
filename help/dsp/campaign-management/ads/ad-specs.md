---
title: Annonsspecifikationer
description: Referera till allmänna och utgivarspecifika annonsspecifikationer.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Specifikationer för annonstyper som stöds

## Video Ads (Pre-Roll, CTV och Universal Video)

### Skärmar som stöds

Annonserna levereras som standard på datorer, mobiler och anslutna tv-enheter. Enhetsanpassning är tillgängligt för att justera leveransen.

### Tredjeparts annonsservrar som stöds

Du kan använda märkordsblad från [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]och [!DNL Sizmek]. En fullständig lista över leverantörer som stöds finns i &quot;[Certifierade annonserande partners](certified-ad-servers.md).&quot;

### Krav för HD-videomaterial (obligatoriskt)

**Typ av videotagg:** VPAID 2.0 JavaScript eller VAST (CTV). Alla VPAID-annonsenheter måste följa [VPAID 2.0-specifikation](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) enligt definition av Interactive Advertising Bureau (IAB).

**Videokodek:** MP4/H.264

**Upplösning:** 1280x720 för 720p, 1920x1080 för 1080p

**Bithastighet:** 1500-2500 kbit/s för 720p, 2500-3500 kbit/s för 1080p

**H.264-profil/nivå:** Hög profil, nivå 3.1 för 720p; Hög profil, nivå 4.0 för 1080p

**Bildrutefrekvens för video:** 29,970 fps (kallas ofta 30 fps) för NTSC-länder, 25 fps för PAL-länder, 23,976 fps (kallas ofta 24 fps) för filmlook-innehåll

**Videofärgmodell:** 4:2:0 YUV-kromdelsampling

**Videosammanflätning:** Progressiv skanning, dvs. icke-sammanflätad. Ingen rörelse inom fältet (blandningsbildrutor) eller sammanflätning.

**Ledare (Slate):** Ej tillåtet

**Ljudkodek:** AAC-LC eller HE-AACv1

**Ljudbithastighet:** 128-192 kbit/s för AAC-LC, 64-128 kbit/s för HE-AACv1

**Ljudkanal:** 2-kanals stereomix

**Samplingsfrekvens för ljud:** 44,1 kHz eller 48 kHz, enligt källmaterial

**Ljudnivåer:** 24 LKFS (+/- 2,0 dB) i USA enligt ATSC A/85, 23 LUFS (+/- 1.0) i EU enligt EBU R128

#### Ytterligare utgivarkrav för anslutna TV-annonser

* **A+E-nätverk:** Se A+E-nätverkets [annonsspecifikationer](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Identifiering:** Se Identifierings [annonsspecifikationer](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (inkl. Hulu):** Se Disneys [annonsspecifikationer](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** Se HBO Max [annonsspecifikationer](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUnversal:**

   * [Digital Video](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livesream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Peacock](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Se Paramount&#39;s [annonsspecifikationer](https://www.paramount.com/digital-ads).

## Visa annonser

### Skärmar som stöds

Annonserna levereras som standard på datorer och mobila enheter. Enhetsanpassning är tillgängligt för att justera leveransen.

### Filtyper som stöds

**Bild:** GIF, JPG/JPEG, PNG

**HTML5:** Bildfiltyper: GIF, JPG/JPEG, PNG, SVG

### Krav för bildresurser (obligatoriskt)

Universell visning stöds.

**Rekommenderade annonsstorlekar:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Tredjeparts annonsservrar som stöds:** Du kan använda märkordsblad från [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]och [!DNL Sizmek]. En fullständig lista över leverantörer som stöds finns i &quot;[Certifierade annonserande partners](certified-ad-servers.md).&quot;

## Ljudannonser

### Skärmar som stöds

Stationär dator, mobil, surfplatta, smarta högtalare och ansluten TV

### Tredjeparts annonsservrar som stöds

Du kan använda märkordsblad från [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]och [!DNL Sizmek]. En fullständig lista över leverantörer som stöds finns i &quot;[Certifierade annonserande partners](certified-ad-servers.md).&quot;

### Krav för ljudresurser (obligatoriskt)

**Filtyp:** MP3, OGG, AAC

**Ledare (skiffer):**  Ej tillåtet

**Maximal filstorlek:** 2 MB

**Bithastighet:** 128

**Fillängd:** 0-60s

#### Ytterligare krav för utgivaren

* **[!DNL iHeartRadio]**
   * Längd: 5, 15, 30 eller 60 sekunder
   * Filtyp: MP3
   * Maximal filstorlek: 320 kbit/s
   * Volym: 44,1 kHz

* **[!DNL Pandora]**
   * Längd: 15 eller 30 sekunder
   * Filtyp: MP4 (i programmet), MP3 (skrivbord)
   * Maximal filstorlek: 2,2 MB

* **[!DNL SoundCloud]**
   * Längd: 6, 15 eller 30 sekunder
   * Filtyp: MP3
   * Maximal filstorlek: 5 MB

* **[!DNL Spotify]**
   * Längd: Upp till 30 sekunder
   * Filtyp: OGG
   * Maximal filstorlek: 500 MB
   * Volym: RMS normaliserat till -14; dBFS toppvärde normaliserat till -0,2 dBFS

* **[!DNL TargetSpot]**
   * Längd: 15, 30 eller 60 sekunder
   * Filtyp: MP3

* **[!DNL TuneIn]**
   * Längd: 10, 15 eller 30 sekunder
   * Filtyp: MP3, OGG
   * Volym: 44,1 kHz

### Krav för tilläggsbanderollannonser (valfritt)

**Storlekar som stöds:** 300x250, 500x500, 640x640, 1024x1024

#### Ytterligare krav för utgivaren

* **[!DNL iHeartRadio]:**
   * Filtyp: JPEG, JPG, PNG, GIF, SWF, HTML,
   * Maximal filstorlek: 2,2 MB
   * Dimensioner: 300x250

* **[!DNL Pandora]:**
   * Filtyp: JPEG, GIF
   * Maximal filstorlek: Storlek: 100 kB
   * Dimensioner: 300x250 (mobil eller stationär) eller 500x500 (stationär)

* **[!DNL SoundCloud]:**
   * Filtyp: Statisk JPG, PNG
   * Maximal filstorlek: Under 400 kB
   * Dimensioner: 1024x1024

* **[!DNL Spotify]:**
   * Filtyp: Statisk JPG, PNG
   * Maximal filstorlek: 200 kB
   * Dimensioner: 300x250

* **[!DNL TuneIn]:**
   * Filtyp: JPEG, JPG, PNG, GIF, HTML
   * Maximal filstorlek: 2 MB
   * Dimensioner: 300x250
 

## Inbyggda visningsannonser

Varje annons kan innehålla antingen en stillbild eller ett rörligt GIF (cinemparagraph).

### Skärmar som stöds

Annonserna levereras som standard på datorer och mobila enheter. Enhetsanpassning är tillgängligt för att justera leveransen.

### Nödvändiga resurser för alla interna format i feed

#### Bildresurs

**Upplösning:** Minst 600x600px; Rekommenderat minimum: 1 200 × 627 px

**Filtyp:** JPEG (bild- och videobildbild och omslagsbild), GIF (filmfotografi)

**Filstorlek:** Mindre än 1 MB (bilden ska vara fri från text.)

#### Advertiser-logotyp

**Upplösning:** Minst 80x80px; Rekommenderat minimum: 300x300px

**Filtyp:** JPEG eller PNG.

**Proportioner:**  1x1-förhållande

>[!NOTE]
>
>Beroende på vilken bild bilden täcker väljer du mellan ljusa och mörka logotyper.

#### Text/Kopiera

**Headline:** Högst 200 tecken; 25 tecken rekommenderas

**Bildtext:** Högst 200 tecken; 100 tecken rekommenderas

**Sponsrat av:** Högst 200 tecken; 30 tecken rekommenderas

**Call to Action (endast MoPub):** Max 15 tecken

>[!NOTE]
>
>Den slutliga layouten definieras av utgivaren vid körning. Om en annons överskrider det rekommenderade antalet tecken kanske vissa lagerleverantörer inte levererar annonsen, eller så kan utgivaren eller SSP trunkera texten.

#### URL för landningssida

Den klickbara URL:en med valfria klickningsspår.

Krav för klickningsspårare:

* Pixlar för visningsspårning från tredje part: Endast 1x1 bild-URL-format

* JavaScript-spårare för synlighet: Stöds endast för IAS. 1x1 bilder endast i JS.append-format

* Klickspårningspixlar från tredje part: Måste omdirigera till landningssidan som är inbäddad i URL:en (HTTP 302-omdirigering)

* Datahanteringsplattform (DMP), klickningsspårare med 200 eller fler svar stöds inte.

>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Skapa flera tredjepartsannonser](ad-create-multiple.md)
>* [Redigera en annons](ad-edit.md)

