---
title: Använda [!DNL Last Event Service] JavaScript-bibliotek med [!DNL Web SDK]
description: Lär dig hur du byter från att använda [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising Cloud] implementering.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Använda [!DNL Last Event Service] JavaScript-bibliotek med Adobe Experience Platform [!DNL Web SDK]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

Om din organisation använder äldre Adobe Analytics `visitorAPI.js` för datainsamling kan du växla till [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) bibliotek (`alloy.js`), vilket gör att du kan interagera med de olika Experience Cloud-tjänsterna via [!DNL Edge Network].

The [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] JavaScript-bibliotek, i befintligt skick, registrerar händelserna view-through och click-through och sammanfogar dem till associerade konverteringar med ett extra ID (`SDID`). The [!DNL Web SDK] biblioteket har dock ingen [!DNL stitch ID]. Så här använder du [!DNL Web SDK] for [!DNL Analytics for Advertising Cloud]måste du ändra 1) [!DNL Last Event Service] tagga som du använder på dina webbsidor och 2) [!DNL Web SDK] `sendEvent` -kommandon.

## Steg 1: Redigera dina [!DNL Last Event Service] Tagg för att generera en `[!DNL StitchID]`

I [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] tagg som du använder på dina webbsidor, lägg till kod för att generera `[!DNL StitchID]` med den slumpmässiga ID-generatorn som paketeras i biblioteket.

**Äldre tagg:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Ny tagg:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Steg 2: Använd [!DNL Web SDK] Skicka [!DNL StitchID] som XDM-data för [!DNL Analytics]

Infoga följande egenskap i [!DNL Web SDK] `sendEvent` för att skicka [!DNL StitchID] till [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) data för [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] kommer att använda värdet som `SDID`.

**Egenskap som ska läggas till:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exempel:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [JavaScript-kod för [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/javascript.md)

