---
title: ' [!DNL Analytics for Advertising Cloud]  [!DNL Flashtalking] '
description: ' [!DNL Analytics for Advertising Cloud]  [!DNL Flashtalking] '
feature: Integration with Adobe Analytics
source-git-commit: c95dc72fa42b47ecea0c27bd59a2df4cd9c20233
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud][!DNL Flashtalking]

**

**

[!DNL Flashtalking] `s_kwcid``ef_id`

[!DNL Flashtalking][!DNL Analytics for Advertising Cloud]

* **[!DNL Adobe][!DNL Analytics for Advertising Cloud]**`s_kwcid``ef_id` However, using macros extends tracking to include click-based conversions when third-party cookies aren&#39;t supported. The best practice is to add the macros in the following sections to your ad tags to capture additional click-through data that isn&#39;t captured through the JavaScript code.

>[!NOTE]
>
>The JavaScript code is a solution for click tracking only while cookies are still available. Once cookies are discontinued, implementing the following macros will be necessary.

* **[!DNL Analytics for Advertising Cloud][!DNL Analytics]**

## Display Ad Tags

[!DNL Flashtalking]`Clicktag`

```html
?[ftqs:[AdobeAMO]]
```

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![[!DNL Flashtalking]](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Video Ad Tags

[!DNL Flashtalking]`Clicktag`

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![[!DNL Flashtalking]](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [ [!DNL Analytics for Advertising Cloud]](overview.md)
>* [ [!DNL Analytics]](/help/integrations/analytics/ids.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
