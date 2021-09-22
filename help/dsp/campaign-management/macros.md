---
title: Advertising Cloud DSP Macros
description: Referera till de tillgängliga makrona för allmän spårning och för att spåra klick på visningsannonser från tredje part.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Advertising Cloud DSP Macros

Ett makro är ett kort kommando eller en förkortning för en instruktion och följer vanligtvis formatet `${MACRO_NAME}`. Advertising Cloud DSP annonsserver kör makron när annonsen skickas eller klickas.

Makron används oftast vid handel med kod eller metadata från tredje part (t.ex. pixlar från tredje part).

## Spårningsmakron

Använd allmänna spårningsmakron för alla annons- och taggtyper för att skicka tillbaka specifika data efter behov.

| Makro | Beskrivning |
| --------------- | ---------------------- |
| `${USER_ID}` | Användaridentifierare för alla enhetstyper. |
| `${TM_RANDOM}` | Cachebuster: ett slumpmässigt tal mellan 1 och 100000 |
| `${TM_PLACEMENT_ID_NUM}` | Placerings-ID |
| `${TM_SITE_URL_URLENC}` | Den URL som skickades i anbudsförfrågan. URL-kodad |
| `${TM_SITE_DOMAIN_URLENC}` | Den sidunderdomän som tolkas från URL:en i anbudsförfrågan. URL-kodad |

{style=&quot;table-layout:auto&quot;}

## Klicka på Makron för visningsannonser från tredje part

För att kunna spåra klick efter annonser med hjälp av tredjepartstaggar måste DSP ha ett musklickningsmakro. Endast en version av makrot krävs. vilket makro det gäller beror på vilken typ av tagg det är.

| Makro | Beskrivning |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | Omdirigerings-URL som gör att annonsservrar kan spåra och räkna annonsklickningar på plattformen |
| `${TM_CLICK_URL_URLENC}` | Omdirigerings-URL som gör det möjligt för annonsservrar som kräver URL-kodning att spåra och räkna annonsklickningar på plattformen |

{style=&quot;table-layout:auto&quot;}

DSP infogar automatiskt klickmakron i en visningstagg när du:

* Exportera annonstaggar från en Advertising Cloud-annonsserverpartner <!-- [Needs PM confirmation.] -->
* Massöverföring [!DNL Flashtalking] eller [!DNL Google DoubleClick for Advertisers] annonstaggar direkt i DSP

Om ett klickande makro saknas när du skapar en visningsannons visas ett varningsmeddelande, som uppmanar dig att manuellt infoga rätt visningsklicksmakro i rätt område i taggen.

>[!MORELIKETHIS]
>
>* [Ljudannonsinställningar](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Inställningar för ansluten TV-annons](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Visa annonsinställningar](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Inställningar för mobilannonsering](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Inbyggda annonsinställningar](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Inställningar för annonsering före registrering](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

