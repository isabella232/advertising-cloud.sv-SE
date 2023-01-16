---
title: Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar
description: Lär dig varför och hur du lägger till [!DNL Analytics for Advertising] makron till [!DNL Google Campaign Manager 360] annonstaggar
feature: Integration with Adobe Analytics
exl-id: 05084a85-5890-4a82-b3eb-4520f44f9d66
source-git-commit: 7c467f7a6eb2522fb998539ba01ceef8c89c3853
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Google Campaign Manager 360] Annonstaggar

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

*Gäller endast DSP*

Om du använder annonstaggar från [!DNL Google Campaign Manager 360] för era DSP annonser, lägg till [!DNL Analytics for Advertising] parametrar till landningssidans URL:er med [`%p` makro](https://support.google.com/campaignmanager/table/6096962). Parameterposten `s_kwcid` och `ef_id` frågesträngsparametrar i landningssidans URL, vilket gör att Adobe Advertising kan skicka klickdata för annonserna till Adobe Analytics.

Använd makron för [!DNL Campaign Manager 360] webbannonser och videoannonser för följande typer av [!DNL Analytics for Advertising] implementeringar:

* **Annonsörer med [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript-kod som implementeras på deras webbplatser**: JavaScript-koden registrerar redan `s_kwcid` och `ef_id` frågesträngsparametrar. Om du använder makron utökas dock spårningen så att den omfattar klickbaserade konverteringar när cookies från tredje part inte stöds. Det bästa sättet är att lägga till makron i följande avsnitt i dina annonstaggar för att hämta ytterligare klickdata som inte fångas in via JavaScript-koden.

>[!NOTE]
>
>JavaScript-koden är bara en lösning för klickspårning medan cookies fortfarande är tillgängliga. När cookies har upphört måste följande makron implementeras.

* **Annonsörer vars webbplatser inte använder [!DNL Analytics for Advertising] JavaScript-kod och förlita dig istället på [!DNL Analytics] vidarebefordran på serversidan endast för klickbara data** (utan genomskinliga data): Följande makron krävs för att rapportera klickningsaktiviteter på plats som styrs av annonser som du köper via Adobe Advertising.

## Lägg till makron i [!DNL Google Campaign Manager 360] Annonser

Inom [!DNL Google Campaign Manager 360], lägg till följande parameter till landningssidans URL för var och en av era annonser för skärm och video: `%pamo=!;`

Du kan ange landningssidans URL på flera sätt. Instruktioner för varje alternativ finns i följande underavsnitt.

Följande är ett exempel på landningssidans URL-adress formaterad med suffixet.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* Om landningssidans URL innehåller en hash-symbol (#), som inte är vanlig, placerar du `amo` parametern före hash-symbolen.
>* Om inga andra parametrar inkluderas efter `amo` lägger du sedan till en parameter (till exempel &amp;a=b) efter den. Exempel:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### Konfigurera URL-suffixet för marknadsföringsnivålandningssida

1. Se [instruktioner för att öppna annonsörsegenskaperna](https://support.google.com/campaignmanager/answer/2829344).
1. I [!UICONTROL Landing page URL suffix] inställningar, inkludera `%pamo!;` i [!UICONTROL URL suffix] fält.

### Konfigurera URL-suffixet för landningssida på kampanjnivå

1. Se [instruktioner för att öppna kampanjegenskaperna](https://support.google.com/campaignmanager/answer/2838056#set).
1. I [!UICONTROL Landing page URL suffix] inställningar, inkludera `%pamo!;` i [!UICONTROL URL suffix] fält.

### Konfigurera URL-suffixet för landningssida på Creative-nivå

1. Öppna de kreativa egenskaperna.
1. I [!UICONTROL Click tags] inställning, inkludera `%pamo!;` i [!UICONTROL Landing page] kolumn för click-taggen.

## Hur [!DNL Analytics for Advertising] Makron utökas i DSP

I DSP, när du skapar en annons som innehåller [!DNL Analytics for Advertising] parameter (`amo`), `ef_id` och `s_kwcid` makron läggs automatiskt till i klickwebbadressen. Det bästa sättet är att checka in DSP för att säkerställa att `ef_id` och `s_kwcid` makron finns.

Följande är ett exempel på en [!DNL Google Campaign Manager 360] [taggen ins](https://support.google.com/campaignmanager/answer/6080468) som det visas i DSP.

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

När en användare klickar på annonsen [!DNL Google Campaign Manager 360] ser `%pamo` i URL-suffixet och infogar dynamiskt värdet för `amo` i URL:en.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Lägg till [!DNL Analytics for Advertising] Makron till [!DNL Flashtalking] Annonstaggar](macros-flashtalking.md)

