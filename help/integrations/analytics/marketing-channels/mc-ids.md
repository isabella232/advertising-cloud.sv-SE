---
title: Använda Advertising Cloud-id:n för att skapa [!DNL Marketing Channels] regler
description: Lär dig hur du använder Advertising Cloud ID:n för att skapa bearbetningsregler för [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Använda Advertising Cloud-id:n för att skapa [!DNL Marketing Channels]-bearbetningsregler

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

Du kan använda Advertising Cloud ID:n ([AMO ID och EF ID](../ids.md)) för att konfigurera [!DNL Marketing Channels]-bearbetningsregler i Adobe Analytics. Använd Advertising Cloud ID:n för regler som är specifika för era Advertising Cloud-kampanjer.

## AMO-ID i bearbetningsregler

AMO-ID är den primära spårningskod som används för att rapportera Advertising Cloud-data inom [!DNL Analytics]. AMO-ID är en sammanfogning av dynamiska värden som hanteras av Adobe för att ge detaljerad rapportering inom [!DNL Analytics]. Den lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- eller rVar-dimension (AMO ID). AMO-ID kan anges i [!DNL Analytics] på två sätt:

* Klickspårning: Advertising Cloud anger frågesträngsparametern `s_kwcid` i en länk och [!DNL Analytics] hämtar parametern från landningssidans URL när en klickning inträffar.
* Direktspårning ([!DNL DSP] Endast): Den senaste händelsetjänsten identifierar en genomgång på serversidan och skickar AMO-ID:t till [!DNL Analytics]. I det här fallet innehåller URL-adressen inte någon `s_kwcid`-parameter.

De dynamiska värdena i AMO-ID:n anger marknadsföringskanalen som spårades:

* Prefixet i AMO-ID kan användas för att identifiera kanalen på den översta nivån i [!DNL Marketing Channels].

* Teckenfraser i texten för AMO-ID anger en mer specifik kampanjtyp.

* Suffixet&quot;vt&quot; finns för [!DNL DSP]-direkttrafik och kan användas för att skapa separata klicknings- och visningskanaler i [!DNL DSP].

Resten av AMO-ID kan ignoreras.

| AMO-ID | Kanal | Regellogik |
|--------|---------|--------------------|
| AL! (prefix) | [!UICONTROL Paid Search] | Börjar med |
| AC! (prefix) | [!UICONTROL DSP] | Börjar med |
| !g! (brödtext) | [!UICONTROL Google Search] | Innehåller |
| !s! (brödtext) | [!UICONTROL Search Partner] | Innehåller |
| !d! (brödtext) | [!UICONTROL Display Network] | Innehåller |
| !u! (brödtext) | [!UICONTROL Smart Shopping Campaign] | Innehåller |
| !ytv! (brödtext) | [!UICONTROL YouTube Video Ad] | Innehåller |
| !yts! (brödtext) | [!UICONTROL YouTube Search Ad] | Innehåller |
| !vp! (brödtext) | [!UICONTROL Google Video Partners] | Innehåller |
| !vt (suffix) | [!UICONTROL DSP View-through] | Slutar med |

### Exempel på bearbetningsregler som använder AMO-ID

Bearbetningsregeln [!DNL Marketing Channels] för kanalen [!UICONTROL Paid Search] kan se ut så här:

![Exempel på en  [!UICONTROL Paid Search] regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Bearbetningsregeln [!DNL Marketing Channels] för kanalen [!UICONTROL YouTube Video Ads] kan se ut så här:

![Exempel på en  [!UICONTROL YouTube Video Ads] regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Var noga med att köra reglerna i den ordning de är specifika. Om de två ovanstående reglerna var ordnade hamnar all videoannonstrafik i [!DNL YouTube]-kanalen under [!UICONTROL Paid Search] eftersom både AMO-ID:t skulle börja med &quot;AL!&quot; och innehåller &quot;!ytv!&quot;.

## EF ID in Processing Rules

AMO EF ID (EF ID) är den andra spårningskoden som används i [!DNL Analytics for Advertising Cloud]-integreringen. Dess främsta syfte är att spåra och skicka [!DNL Analytics] händelsedata till Advertising Cloud. Varje gång en klickning eller genomgång sker genereras ett unikt EF-ID, även om det är exakt samma annons för samma besökare. EF ID används inte i [!DNL Analytics]-rapportanvändargränssnittet eftersom det vanligtvis överskrider 500 kB-gränsen för unika värden per variabel i [!DNL Analytics], vilket gör det oanvändbart för rapportering. Advertising Cloud-mått och metadata tillämpas inte på EF-id:t. de tillämpas bara på AMO-ID:t. Spårning krävs för kampanjoptimering i Advertising Cloud, så båda ID:n krävs.

Trots att EF ID-dimensionen inte används direkt i [!DNL Analytics]-rapportering kan EF ID vara användbart när du skapar marknadsföringskanaler. EF ID-suffixet anger kanalen (visning eller sökning) och om besöket drivs av en klickfrekvens eller en genomgång. Avgränsaren i EF-ID är ett kolon i stället för utropstecknet i AMO-ID.

| EF ID-suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exempel på bearbetningsregler som använder EF-ID

#### Visa genomklickningsregel

Skapa en klickbar marknadsföringskanal för webbannonsering genom att endast klickningar görs. Eftersom AMO-ID:t är samma för både klickningar och genomgångar, använder den här regeln variabeln EF ID och frågesträngsparametern `ef_id`.

Ibland spåras klickningar via webbadressen (standardvärdet). I andra fall spåras klickningar via den senaste händelsetjänsten på serversidan, och därför innehåller URL-adressen inte parametern `ef_id`. Regeln kontrollerar därför om det finns villkor där variabeln EF ID eller frågesträngsparametern `ef_id` avslutas med &quot;:d&quot;. Använd operatorn `Any` eftersom du vill att den här regeln ska aktiveras för båda villkoren.

![Exempel på en klickningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visa genomskinlighetsregel

Om du vill skapa en visningskanal skapar du en regel där EF-ID:t avslutas med &quot;:i&quot;. Eftersom besökaren inte klickade på annonsen inkluderar inte den genomskinliga spårningen `ef_id` eller `s_kwcid` i URL:en. Därför behövs bara ett villkor.

![Exempel på en genomskärningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Varför olika kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Använda  [!DNL Analytics Marketing Channels] med Advertising Cloud Data](mc-ac-data.md)
>* [Video: Rapportera med Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)

