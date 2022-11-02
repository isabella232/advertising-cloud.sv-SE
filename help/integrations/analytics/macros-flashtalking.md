---
title: Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Flashtalking] Annonstaggar
description: Lär dig varför och hur du lägger till [!DNL Analytics for Advertising Cloud] makron till [!DNL Flashtalking] annonstaggar
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: ae516c1947d2b163ebd97dd05fb4e2870a1450d2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Flashtalking] Annonstaggar

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

*Gäller endast Advertising Cloud DSP*

Om du använder annonstaggar från [!DNL Flashtalking] för era Advertising Cloud DSP-annonser, lägg till parametrar för Analytics for Advertising Cloud i era URL:er för landningssidor. Parameterposten `s_kwcid` och `ef_id` frågesträngsparametrar i landningssidans URL, vilket gör att Advertising Cloud kan skicka klickdata för annonserna till Adobe Analytics.

Använd makron för [!DNL Flashtalking] webbannonser och videoannonser för följande typer av [!DNL Analytics for Advertising Cloud] implementeringar:

* **Annonsörer med [!DNL Adobe] [!DNL Analytics for Advertising Cloud] JavaScript-kod som implementeras på deras webbplatser**: JavaScript-koden registrerar redan `s_kwcid` och `ef_id` frågesträngsparametrar. Om du använder makron utökas dock spårningen så att den omfattar klickbaserade konverteringar när cookies från tredje part inte stöds. Det bästa sättet är att lägga till makron i följande avsnitt i dina annonstaggar för att hämta ytterligare klickdata som inte fångas in via JavaScript-koden.

>[!NOTE]
>
>JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När cookies har upphört måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder [!DNL Analytics for Advertising Cloud] JavaScript-kod och förlita dig istället på [!DNL Analytics] vidarebefordran på serversidan endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickningsaktiviteter på plats som har gjorts av annonser som du köper via Advertising Cloud.

## Visa annonstaggar

I [!DNL Flashtalking] lägg till följande makro i slutet av klicknings-URL:en i dialogrutan `Clicktag` fält:

```html
?[ftqs:[AdobeAMO]]
```

Exempel:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![Exempel på [!DNL Flashtalking] inställningar för annonstaggar](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Video Ad-taggar

I [!DNL Flashtalking] lägg till följande makro i slutet av klicknings-URL:en i dialogrutan `Clicktag` fält:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exempel:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![Exempel på [!DNL Flashtalking] inställningar för annonstaggar](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md)

