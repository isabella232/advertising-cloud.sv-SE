---
title: Samla in klicknings- och imponeringsdata från Advertising Cloud DSP Campaigns
description: Lär dig hur du fångar in cookie-baserat intryck och klickar på händelser från Advertising Cloud DSP-annonser med hjälp av Audience Manager-pixlar
feature: Integration with Adobe Audience Manager
source-git-commit: b4dae983d390aaa5476951aa0c4c39648f07975c
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Samla in data om medieexponering från Advertising Cloud DSP Campaigns

*Annonsörer endast med Advertising Cloud DSP*

*Annonsörer med endast Advertising Cloud-Adobe Audience Manager-integrering*

I det här dokumentet beskrivs hur du taggar Advertising Cloud DSP-annonser för att fånga in cookie-baserat intryck och klickningshändelser med hjälp av Audience Manager-pixlar, och ytterligare åtgärder som krävs för att använda data.

Händelsepixlarna fångar inte in händelser som inträffar i cookie-fria miljöer, som mobilappar och ansluten TV (CTV).

## Steg 1: Konfigurera en datakälla i Audience Manager {#set-up-data-source}

Skapa en [datakälla](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) för DSP och klicka på data. Inkludera datakällans ID [i varje händelsetagg](#implement-dsp-pixels) så att alla spårade händelser kan hänföras till datakällan.

>[!NOTE]
> Det är möjligt att samla in alla intryckta data och klickdata för annonskampanjer som körs på flera DSP i en enda datakälla.

## Steg 2: Implementera Impression och klicka på händelsepixlar på webbsidor {#implement-dsp-pixels}

Annonsörer kan skapa och implementera händelsetaggar för sina egna varumärken. Kontakta vid behov Adobe Audience Manager eller [!DNL Adobe] kontoansvarig för support.

>[!NOTE]
>
>Om din organisation använder [!DNL Analytics] spårning behöver du kanske inte spåra Audience Manager-klickningar. Adobe Analytics tar klicksignaler och kan skicka dem till Audience Manager via [vidarebefordran på serversidan](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Pixelsyntax

Händelsepixlar måste innehålla följande parametrar.

**Pixlar för Impression-tracking:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}` Med [valfria ytterligare parametrar](#parameters) prefix med `&`

**Klickspårningspixlar:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}` med [valfria ytterligare parametrar](#parameters) prefix med `&`

Var:

* `[Audience Manager customer domain]` är det domännamn som ska skicka intrycket eller klickhändelser till [!DNL Adobe].

* `[source id]` är ID:t för [datakälla](#set-up-data-source) där du kan spåra DSP och klicka på data.

* `[redirect URL]` är den dubbelkodade omdirigerings-URL:en. Om du använder ett kodningsverktyg online, t.ex. www.urlencoder.org, kör du strängen genom kodaren och kodar om resultatet.

* `${TM_CAMPAIGN_ID_NUM}` är det numeriska kampanj-ID:t i DSP. Om du vill hårdkoda ett enskilt kampanj-ID i stället för att använda det DSP makrot ska du leta reda på ID:t i kampanjinställningarna.

* Varje [parameter](#key-value-pairs) är prefix med `&` och har formatet `d_parameter=parameter_id`, där `parameter` ersätts med nyckelvärdepar för det nya fältet. Exempel: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parametrar som nyckelvärdepar {#parameters}

**Format:**  `d_parameter=parameter_id`

    där:
    
    * parametern prefixeras med `&amp;`
    
    * &quot;parameter&quot; ersätts med nyckelvärdepar för det nya fältet
    
    Exempel: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Båda pixeltyperna kan innehålla ytterligare parametrar som *nyckelvärdepar* för att samla in egenskaper eller för att tillhandahålla kampanjmetadata (t.ex. ett placeringsnamn eller ett kampanjnamn) för andra rapporter. Ett nyckelvärdepar består av två relaterade element: a *key*, som är en konstant som definierar datauppsättningen och en *value*, som är en variabel som tillhör uppsättningen.

I nyckelvärdepar kan värdevariabeln vara antingen ett hårdkodat ID eller ett *makro*, som är en liten enhet med självständig kod som dynamiskt ersätts med motsvarande värden när annonstaggen läses in för kampanj- och användarspårning. För kampanjrelaterade parametrar kan du använda [DSP makron](/help/dsp/campaign-management/macros.md) i stället för Audience Manager-makron för att skicka kampanjattribut tillsammans med motsvarande intryck eller klicka på data till Audience Manager, med en enda pixel i alla annonser. De DSP makron som du infogar i händelsepixlarna måste vara lämpliga värden för de nyckel/värde-par som du inkluderar i pixlarna. För `d_placement` använder du DSP `${TM_PLACEMENT_ID_NUM}` som värdet för att hämta placerings-ID:n som genereras av Advertising Cloud-makrot.

En lista över makron som Audience Manager stöder för att visa händelsepixlar finns i &quot;[Samla in data för kampanjexponering via pixelanrop](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

En lista över makron som Audience Manager stöder för klickningshändelsepixlar finns i &quot;[Samla in data för kampanjklickningar via pixelanrop](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* Det bästa sättet är att inkludera kampanj-, placerings-, kreativa (annons) och webbplats-ID:n så att du kan använda kampanjattributen för att skapa Audience Manager.
>* Ytterligare parametrar krävs för att skapa rapporter från Audience Optimization.
>* Ersätt värdena i nyckelvärdepar med relevanta [DSP makron](/help/dsp/campaign-management/macros.md) så att ni kan använda en enda pixel i alla annonser i alla kampanjer. Ändra till exempel `d_campaign=[%campaignID%]`till `d_campaign=${TM_CAMPAIGN_ID_NUM}` för att hämta kampanj-ID:n som genererats av Advertising Cloud-makrot.
>* Om det behövs kan du skapa egna parametrar med hårdkodade värden. Exempel: `d_DSP=AdCloud`


Exempel på en visningshändelsepixel:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Var ska pixlarna läggas till?

#### Impression-Tracking Pixel

Bifoga en pixel för att spåra intryckshändelser till alla annonser i [!DNL DSP] kampanjer. Du kan göra det på följande platser:

* På placeringsnivån, som tillämpar pixeln som standard på alla annonser i placeringen. Lägg till pixeln i [[!UICONTROL Event pixels] fält](/help/dsp/campaign-management/placements/placement-settings.md).

* På annonsnivån, som åsidosätter händelsepixlar på placeringsnivå. I annonsinställningarna [skapa en händelsepixel på [!UICONTROL Pixel] tab](/help/dsp/campaign-management/ads/ad-edit.md).

* (För annonser på en annonsserver från tredje part) På annonsnivån i annonsservern.

#### Click-Tracking Pixel

På annonsservern infogar du klickhändelsepixeln (med den kodade URL:en tillagd) på det ställe där du normalt infogar annonsens klicknings-URL.

## Steg 3: Åtgärder efter implementering

När händelsetaggarna implementeras flödar data in i Audience Manager datainsamlingsservrar. Utför följande åtgärder innan du kan använda data i rapporter.

### Skapa en [!DNL Amazon S3] Bucket och datakälla

När data finns på Audience Manager-servrarna måste du skapa en [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) och sedan en datakälla som alla pixeldata skickas till. Kontakta din Audience Manager-konsult eller [Kundtjänst](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) om du behöver support.

### Skapa Audience Manager-traits och segment

Dina händelsedata flödar in i Audience Manager som [oanvända signaler](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Skapa manuellt [regelbaserade egenskaper](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) från inkapslade data och sedan skapa [segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) med dessa egenskaper, innan du kan använda data i rapporter.

Exempeldiagram som fyller i användarnivådata för användare som exponeras för en viss kreativ i DSP:

1. Identifiera händelsen som `d_event = imp`.
1. Identifiera det kreativa ID:t i DSP kampanj och mappa det sedan till egenskapen som `d_creative=[Creative ID]`.

![Skärm för att skapa spår](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud DSP Macros](/help/dsp/campaign-management/macros.md)
>* [Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager](overview.md)
>* [Användningsexempel](use-cases.md)

