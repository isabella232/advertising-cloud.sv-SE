---
title: ' [!DNL Analytics for Advertising Cloud]  [!DNL Google Campaign Manager 360] '
description: ' [!DNL Analytics for Advertising Cloud]  [!DNL Google Campaign Manager 360] '
feature: Integration with Adobe Analytics
source-git-commit: fe61dcd97d5509784a20bf8f68bea0ab2699dcfd
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud][!DNL Google Campaign Manager 360]

**

**

[!DNL Google Campaign Manager 360][`%p`](https://support.google.com/campaignmanager/table/6096962) `s_kwcid``ef_id`

[!DNL Campaign Manager 360][!DNL Analytics for Advertising Cloud]

* **[!DNL Adobe][!DNL Analytics for Advertising Cloud]**`s_kwcid``ef_id` However, using macros extends tracking to include click-based conversions when third-party cookies aren&#39;t supported. The best practice is to add the macros in the following sections to your ad tags to capture additional click-through data that isn&#39;t captured through the JavaScript code.

>[!NOTE]
>
>The JavaScript code is a solution for click tracking only while cookies are still available. Once cookies are discontinued, implementing the following macros will be necessary.

* **[!DNL Analytics for Advertising Cloud][!DNL Analytics]**

## [!DNL Google Campaign Manager 360]

[!DNL Google Campaign Manager 360]`%pamo=!;`

You can specify the landing page URL in several ways. Instructions for each option are included in the following subsections.

The following is an example of the landing page URL formatted with the suffix.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* `amo`
>* `amo` `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


## Configure the Advertiser-Level Landing Page URL Suffix

1. [!UICONTROL Advertisers]
1. Click the advertiser name.
1. [!UICONTROL Landing page URL suffix]`%pamo!;`[!UICONTROL URL suffix]

## Configure the Campaign-Level Landing Page URL Suffix

1. [!UICONTROL Campaigns]
1. Click the campaign name.
1. Klicka på [!UICONTROL Properties].
1. [!UICONTROL Landing page URL suffix]`%pamo!;`[!UICONTROL URL suffix]

## Configure the Creative-Level Landing Page URL Suffix

1. [!UICONTROL Campaigns]
1. Click the campaign name.
1. [!UICONTROL Views][!UICONTROL Creatives]
1. Click the creative name.
1. [!UICONTROL Click tags]`%pamo!;`[!UICONTROL Landing page]

## [!DNL Analytics for Advertising Cloud]

[!DNL Analytics for Advertising Cloud]`amo``ef_id``s_kwcid` `ef_id``s_kwcid`

[!DNL Google Campaign Manager 360][](https://support.google.com/campaignmanager/answer/6080468)

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

[!DNL Google Campaign Manager 360]`%pamo``amo`


>[!MORELIKETHIS]
>
>* [ [!DNL Analytics for Advertising Cloud]](overview.md)
>* [ [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [ [!DNL Analytics for Advertising Cloud]  [!DNL Flashtalking] ](macros-flashtalking.md)

