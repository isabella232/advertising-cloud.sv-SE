---
title: Advertising Cloud ID:n som används av [!DNL Analytics]
description: Advertising Cloud ID:n som används av [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising Cloud ID:n som används av [!DNL Analytics]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

*Gäller Advertising Cloud DSP och Advertising Cloud Search*

Advertising Cloud använder två ID:n för prestandaspårning på plats:  EF ID och AMO ID.

När ett annonsintryck inträffar skapar Advertising Cloud värdena för AMO ID och EF ID och lagrar dem. När en besökare som har sett en annons komma in på webbplatsen utan att klicka på en annons anropar [!DNL Analytics] dessa värden från Advertising Cloud via JavaScript-koden [!DNL Analytics for Advertising Cloud]. För genomsynstrafik genererar [!DNL Analytics] ett extra ID (`SDID`) som används för att sammanfoga EF-ID och AMO-ID till [!DNL Analytics]. För genomklickningstrafik inkluderas dessa ID:n i landningssidans URL med hjälp av frågesträngsparametrarna `s_kwcid` och `ef_id`.

Advertising Cloud skiljer mellan klickbara eller genomskinliga poster på webbplatsen enligt följande kriterier:

* En genomsiktspost hämtas när en användare besöker webbplatsen efter att ha visat en annons, men inte klickat på den. [!DNL Analytics] spelar in en genomskinlig vy om två villkor uppfylls:
   * Besökaren har inga klickningar för en [!DNL DSP] eller [!DNL Search]-annons under [klickningsfönstret](#lookback-a4adc).
   * Besökaren har sett minst en [!DNL DSP]-annons under [visningsfönstret](#lookback-a4adc). Det sista intrycket skickas som en genomgång.
* En klickbar post hämtas när en besökare klickar på en annons innan han/hon kommer in på webbplatsen. [!DNL Analytics] hämtar en klickning genom när något av följande inträffar:
   * URL:en innehåller ett EF-ID och AMO-ID som har lagts till i Advertising Cloud-URL:en för landningssidan.
   * URL:en innehåller inga spårningskoder, men Advertising Cloud JavaScript-koden hittar ett klick inom de senaste två minuterna.

![Advertising Cloud vybaserade  [!DNL Analytics] integrering](/help/integrations/assets/a4adc-view-through-process.png)

*Bild 1: Advertising Cloud vybaserade  [!DNL Analytics] integrering*

![Advertising Cloud click URL-based  [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Bild 2: Advertising Cloud click URL-based  [!DNL Analytics] integration*

## Advertising Cloud EF ID:n

EF ID är en unik variabel som Advertising Cloud använder för att koppla aktiviteter till en onlineklickning eller annonsexponering. EF-id:t lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- eller rVar-dimension (reserverad eVar) (Advertising Cloud EF-id) och spårar varje annonsklickning eller exponering på den enskilda webbläsarnivån eller enhetsnivån. EF ID:n fungerar främst som nycklar för att skicka [!DNL Analytics]-data till Advertising Cloud för rapportering och budoptimering inom Advertising Cloud.

### EF ID-format

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

där:

* &lt;>Advertising Cloud besökar-ID *> är ett unikt ID per besökare (till exempel EhKVaAABCkJ0mDt).* Ringde även *surfer-ID*.

* &lt;>tidsstämpel *> är tiden i formatet YYYMMDDHMMSS (t.ex. 20190821192533 för År 2019, månad 08, dag 21, tid 19:25:33).*

* &lt;>kanaltyp *> är den kanaltyp som ansvarar för klickningen eller exponeringen:*

   * `d` för ett klick på en DSP (visa klickbar bild)
   * `i` för ett intryck av en DSP displayannons (visningsvy)
   * `s` för att klicka på en sökannons (sök-klickning).

Exempel `EF `ID: WcmibgAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID:n är skiftlägeskänsliga. Om en [!DNL Analytics]-implementering tvingar URL-spårning till gemener, kommer Advertising Cloud inte att känna igen EF-ID:t. Detta påverkar Advertising Cloud budgivning och rapportering men påverkar inte Advertising Cloud rapportering inom [!DNL Analytics].

### EF ID-Dimensionen i [!DNL Analytics]

I [!DNL Analytics]-rapporter kan du hitta EF ID-data genom att söka efter dimensionen [!UICONTROL EF ID] och använda måttet [!UICONTROL EF ID Instance].

`EF IDs` omfattas av den unika identifierargränsen på 500 kB i Analysis Workspace. När 500 kB-värdet har nåtts rapporteras alla nya spårningskoder under rubriken &quot;[!UICONTROL Low Traffic]&quot;. På grund av risken att rapporteringsföljsamhet saknas klassificeras inte `EF IDs` och du bör inte använda dem för segment eller rapporter i [!DNL Analytics].

## Advertising Cloud AMO ID

AMO-ID spårar varje unik annonskombination på en mindre detaljerad nivå och används för [!DNL Analytics]-dataklassificering och inmatning av reklamstatistik (t.ex. visningar, klick och kostnader) från Advertising Cloud. AMO-ID:t lagras i en [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- eller rVar-dimension (AMO-ID) och används uteslutande för rapportering i [!DNL Analytics].

AMO-ID:t kallas även `s_kwcid`, som ibland kallas för&quot;bläckfisken&quot;.

### AMO ID-format för [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

där:

* &lt;>Kanal-ID *> kan vara:*

   * `AC` = Advertising Cloud DSP
   * `AL` för Advertising Cloud Search

* &lt;>Annons-ID *> används som en unik identifierare som skapats av Advertising Cloud för en annons.* Det fungerar som en nyckel för översättning av Advertising Cloud-entitetsmetadata till läsbara [!DNL Analytics]-dimensioner.

* &lt;>Placement ID *> är en Advertising Cloud-genererad unik identifierare för en placering.* Det fungerar som en nyckel för översättning av Advertising Cloud-entitetsmetadata till läsbara [!DNL Analytics]-dimensioner.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

Exempel på AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO ID-format för [!DNL Search]

AMO-ID:n för [!DNL Search] följer ett distinkt format för varje sökmotor. Formatet för alla sökmotorer börjar med följande:

```AL!{ef_userid}!{ef_sid}```

där:

* `AL` är kanal-ID för sökkanalen.
* `{ef_userid}` är det unika numeriska användar-ID som Advertising Cloud tilldelar annonsören.
* `{ef_sid}` är det numeriska ID som Advertising Cloud använder för den angivna sökmotorn, till exempel  `3` för  [!DNL Google Ads] eller  `10` för  [!DNL Microsoft Advertising].

Nedan följer de fullständiga AMO ID-formaten för ett par sökmotorer. Om du har AMO ID-format för andra sökmotorer kontaktar du kontohanteraren för Adobe.

AMO ID-format för [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

där:

* `{creative}` är det  [!DNL Google Ads] unika numeriska ID:t för den kreativa.
* `{matchtype}` är matchningstypen för nyckelordet som utlöste annonsen:  `e` för exakta,  `p` för fras eller  `b` för breda.
* `{placement}` är domännamnet för den webbplats där annonsen klickades. Det finns ett värde för annonser i riktade kampanjer och för annonser i kampanjer riktade mot nyckelord som visas på innehållswebbplatser.
* `{network}` anger nätverket som klickningen inträffade från:   `g` för  [!DNL Google] sökning (endast för nyckelordsriktade annonser),  `s` för en sökpartner (endast för nyckelordsriktade annonser) eller  `d` för visningsnätverket (för antingen nyckelordsriktade eller placeringsriktade annonser).
* `{keyword}` är antingen det specifika nyckelord som utlöste din annons (på sökwebbplatser) eller det bästa matchande nyckelordet (på innehållswebbplatser).

AMO ID-format för [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

där:

* `{AdId}` är det  [!DNL Microsoft Advertising] unika numeriska ID:t för den kreativa.
* `{OrderItemId}` är det  [!DNL Microsoft Advertising] numeriska ID:t för nyckelordet.

### AMO ID-Dimension i [!DNL Analytics]

I analysrapporter kan du hitta AMO ID-data genom att söka efter dimensionen [!UICONTROL AMO ID] och använda måttet [!UICONTROL AMO ID Instance]. Dimensionen [!UICONTROL AMO ID] lagrar alla AMO ID-värden som fångats, medan måttet [!UICONTROL AMO ID Instance] anger hur ofta ett AMO ID-värde hämtades av platsen. Om till exempel samma sökannons klickades fyra gånger men Analytics spårade sju webbplatsposter, skulle [!UICONTROL AMO ID Instance] vara sju (7) och [!UICONTROL Clicks] vara fyra (4).

För alla rapporter och granskningar inom [!DNL Analytics] är det bästa sättet att använda AMO-ID tillsammans med motsvarande instans. Mer information finns i &quot;[Dataverifiering för [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; i &quot;Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud.&quot;

## Om analysklassificeringar

I [!DNL Analytics] är en [klassificering](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) en del metadata för en viss spårningskod, till exempel Konto, Kampanj eller Annons. Advertising Cloud kategoriserar Advertising Cloud-rådata med hjälp av klassificeringar så att du kan visa data på olika sätt (t.ex. efter annonstyp eller Campaign) när du genererar rapporter. Klassifikationer utgör grunden för Advertising Cloud-rapportering i [!DNL Analytics] och kan användas med AMO-mått, som [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions] och [!UICONTROL AMO Clicks], samt med anpassade händelser och standardhändelser på plats som [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] och [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Förväntade datavariationer  [!DNL Analytics] mellan och Advertising Cloud](data-variances.md)

