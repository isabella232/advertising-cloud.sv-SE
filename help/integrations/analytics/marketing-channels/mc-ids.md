---
title: Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] Regler
description: Lär dig hur du använder Adobe Advertising ID:n för att skapa bearbetningsregler för [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] Bearbetar regler

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

Du kan använda Adobe Advertising ID:n ([AMO ID och EF ID](../ids.md)) för att konfigurera [!DNL Marketing Channels] bearbetningsregler i Adobe Analytics. Använd Adobe Advertising ID:n för regler som är specifika för era annonskampanjer i Adobe.

## AMO-ID i bearbetningsregler

AMO-ID är den primära spårningskod som används för att rapportera Adobe-annonsdata i [!DNL Analytics]. AMO-ID är en sammanfogning av dynamiska värden som hanteras av Adobe för att ge detaljerad rapportering inom [!DNL Analytics]. Den lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) eller rVar dimension (AMO ID). AMO-ID:t kan anges i [!DNL Analytics] på två sätt:

* Klickspårning: Adobe Advertising ställer in `s_kwcid` frågesträngsparametern i en länk, och [!DNL Analytics] hämtar parametern från landningssidans URL när en klickning inträffar.
* Direktspårning ([!DNL DSP] Endast): Den senaste händelsetjänsten identifierar en genomgång på serversidan och skickar AMO-ID:t till [!DNL Analytics]. I det här fallet innehåller URL-adressen inte något `s_kwcid` parameter.

De dynamiska värdena i AMO-ID:n anger marknadsföringskanalen som spårades:

* Prefixet i AMO-ID kan användas för att identifiera kanalen på den översta nivån i [!DNL Marketing Channels].

* Teckenfraser i texten för AMO-ID anger en mer specifik kampanjtyp.

* suffixet&quot;vt&quot; finns för [!DNL DSP] direkttrafik och kan användas för att skapa separat klickbar och genomskinlig [!DNL DSP] kanaler.

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

The [!DNL Marketing Channels] bearbetningsregel för [!UICONTROL Paid Search] kanalen kan se ut så här:

![Exempel på en [!UICONTROL Paid Search] regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

The [!DNL Marketing Channels] bearbetningsregel för [!UICONTROL YouTube Video Ads] kanalen kan se ut så här:

![Exempel på en [!UICONTROL YouTube Video Ads] regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Var noga med att köra reglerna i den ordning de är specifika. Om de två ovanstående reglerna är i ordning, kommer [!DNL YouTube] video- och trafik faller under [!UICONTROL Paid Search] eftersom både AMO-ID:t börjar med&quot;AL!&quot; och innehåller &quot;!ytv!&quot;.

## EF ID in Processing Rules

AMO EF ID (EF ID) är den andra spårningskoden som används i [!DNL Analytics for Advertising] integrering. Det främsta syftet är att spåra och passera [!DNL Analytics] händelsedata till Adobe Advertising. Varje gång en klickning eller genomgång sker genereras ett unikt EF-ID, även om det är exakt samma annons för samma besökare. EF ID används inte i [!DNL Analytics] rapporterar användargränssnitt eftersom det vanligtvis överstiger gränsen på 500 kB unika värden per variabel i [!DNL Analytics], vilket gör det oanvändbart för rapportering. Marknadsföringsstatistik och metadata för Adobe tillämpas inte på EF-id:t. de tillämpas bara på AMO-ID:t. Spårning krävs för kampanjoptimering i Adobe Advertising, så båda ID:n krävs.

Trots att EF ID-dimensionen inte används direkt i [!DNL Analytics] rapporter kan det vara användbart att använda ett EF-ID för att skapa marknadsföringskanaler. EF ID-suffixet anger kanalen (visning eller sökning) och om besöket drivs av en klickfrekvens eller en genomgång. Avgränsaren i EF-ID är ett kolon i stället för utropstecknet i AMO-ID.

| EF ID-suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exempel på bearbetningsregler som använder EF-ID

#### Visa genomklickningsregel

Skapa en klickbar marknadsföringskanal för webbannonsering genom att endast klickningar görs. Eftersom AMO-ID:t är samma för både klickningar och genomvisningar används variabeln EF ID och `ef_id` frågesträngsparameter.

Ibland spåras klickningar via webbadressen (standardvärdet). I andra fall spåras klickningar via tjänsten för senaste händelse på serversidan, och därför innehåller URL:en inte `ef_id` parameter. Regeln kontrollerar därför om det finns villkor där variabeln för EF-id eller `ef_id` frågesträngsparametern slutar med &quot;:d&quot;. Använd &quot;`Any`&quot; eftersom du vill att den här regeln ska aktiveras för båda villkoren.

![Exempel på en klickningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Visa genomskinlighetsregel

Om du vill skapa en visningskanal skapar du en regel där EF-ID:t avslutas med &quot;:i&quot;. Eftersom besökaren inte klickade på annonsen inkluderar inte genomsiktsspårningen `ef_id` eller `s_kwcid` i URL:en, så regeln kräver bara ett villkor.

![Exempel på en genomskärningsregel för visning](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Varför kanaldata kan variera mellan Adobe och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Använda [!DNL Analytics Marketing Channels] med Adobe Advertising Data](mc-ac-data.md)
>* [Video: Använda [!DNL Marketing Channels] för Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)

