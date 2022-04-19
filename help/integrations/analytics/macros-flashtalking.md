---
title: Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Flashtalking] Annonstaggar
description: Lär dig varför och hur du lägger till [!DNL Analytics for Advertising Cloud] makron till [!DNL Flashtalking] annonstaggar
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Flashtalking] Annonstaggar

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

*Gäller endast Advertising Cloud DSP*

Om du använder annonstaggar från [!DNL Flashtalking] för era Advertising Cloud DSP-annonser, lägg till parametrar för Analytics for Advertising Cloud i era URL:er för landningssidor. Med parametrarna kan Advertising Cloud skicka klickdata för annonserna till Adobe Analytics.

Använd makron för [!DNL Flashtalking] webbannonser och videoannonser för följande typer av [!DNL Analytics for Advertising Cloud] implementeringar:

* **Annonsörer med [!DNL Adobe] [!DNL Analytics for Advertising Cloud] JavaScript-kod som implementeras på deras webbplatser**: Du bör se klickdata i Adobe Analytics från annonser som du köper via Advertising Cloud, utan extra makron. Om du vill hämta klickningsdata i webbläsare som inte stöder cookies från tredje part och därför inte kan fångas via JavaScript-koden lägger du till makrona i följande avsnitt i [!DNL Flashtalking] annonstaggar.

>[!NOTE]
>
>JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När Advertising Cloud upphör med cookies måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder [!DNL Analytics for Advertising Cloud] JavaScript-kod och förlita dig istället på [!DNL Analytics] vidarebefordran på serversidan endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickningsaktiviteter på plats som har drivits av annonser som du köper via Advertising Cloud.

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


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
