---
title: Kolumner i hämtade/överförda kalkylblad
description: Referera kolumnerna i hämtade och överförda Excel QA-kalkylblad.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 12056598ae436123a867e6eaefde47657242dc73
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Kolumner i hämtade/överförda kalkylblad

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> I ett nedladdat kalkylblad markeras alla redigerbara kolumner med blått.

| Avsnitt | Kolumn | Beskrivning | Redigerbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Placeringens numeriska ID. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Placeringens namn. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Etiketter som används för rapportering. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | En länk för att öppna placeringen i redigeringsläget. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Placeringsstatus: *[!UICONTROL active]* eller *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Placeringstypen. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Namnet på det överordnade paketet, om tillämpligt. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Placeringens startdatum. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Placeringens slutdatum. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Om dagen paration är *[!UICONTROL ON]* eller *[!UICONTROL OFF]*.<br><b>Obs!</b> Om du vill kontrollera det faktiska sommarschemat öppnar du placeringsinställningarna i [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Placeringsbudgeten, om det finns en sådan. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Budgetintervallet: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, eller *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Paketets syfte. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Målvärdet för målet. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Om placeringen är i linje med *[!UICONTROL Budget]* eller *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Det högsta anbudet för placeringen. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Flygpaketeringsstrategi för placeringen: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, eller *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Intraday-paketeringsstrategi för placeringen: *[!UICONTROL Even]* eller *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Eventuella filtervillkor före bud som ska tillämpas. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Om budgivningsreglerna (inaktuella) är *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Det primära frekvensskyddet för placeringen under den angivna [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervallet för det primära frekvensskyddet: *[!UICONTROL Day]*, *[!UICONTROL Week]*, eller *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Det sekundära frekvensskyddet för placeringen under den angivna [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Intervalltyp för sekundär frekvensbegränsning: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, eller *[!UICONTROL Minute]*. Det tillämpliga antalet veckor, dagar, timmar eller minuter anges av [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Antalet veckor, dagar, timmar eller minuter som [!UICONTROL Secondary Frequency Cap] gäller. Om det sekundära taket till exempel är tre avtryck per sex timmar blir värdet här <b>6&lt;/>. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Antalet målinriktade geografiska platser. *[!UICONTROL All]*, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | De avgränsade geografiska platserna, avgränsade med semikolon, eller *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Antalet uteslutna geografiska platser eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | de uteslutna geografiska platserna, åtskilda med semikolon, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Antalet riktade offentliga inventeringserbjudanden, om sådana finns, *[!UICONTROL All]*, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Antalet uteslutna offentliga inventeringserbjudanden, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Antalet riktade privata lageraffärer, om sådana finns, *[!UICONTROL All]*, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Antalet uteslutna privata lageraffärer, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Antalet mål [!UICONTROL On-Demand Inventory] eventuella erbjudanden, *[!UICONTROL All]*, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Antalet uteblivna erbjudanden om behovsstyrda inventeringar, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Måltyp för trafik: *[!UICONTROL Website]* och/eller *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Om alternativet Målinriktning för lager ska exkludera trafik utanför strömmen är &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* eller *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Annonser utanför webben visas vanligtvis över innehållet som ett popup-fönster eller instoppat i innehåll (i den ursprungliga upplevelsen), i stället för som vanliga videoannonser i en videospelare. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Kvaliteten på de webbplatser som ska mål: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, eller *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | antalet målwebbplatskategorier, om sådana finns, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Antalet uteslutna webbplatskategorier, om sådana finns, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | de utelämnade platserna, om sådana finns specificerade, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Målwebbplatsspråken. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Endast standardbildskärmsplaceringar) Om annonsleverans ska tillåtas på webbplatser som inte är granskade eller inte: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. När placeringen avser privat lager kan det här alternativet leverera annonser på blockerade webbplatser. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | antalet målwebbplatser, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | målgrupperna, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | de uteslutna målgrupperna, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Om eller inte [!DNL Comscore] demografiska segment är aktiverade för placering (och andra placeringar i kampanjen): *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. Den här funktionen kan bara aktiveras för kampanjer för vilka [!DNL Audience Verification] funktionen är aktiverad för [!DNL Nielsen] och/eller [!DNL Comscore].  Det medför ytterligare avgifter. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Om ni vill utöka annonseringen för olika enheter eller inte: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*. Målinriktning på flera enheter utökar er målinriktning på alla en persons kända enheter, enligt det enhetsdiagram som anges i kampanjinställningarna. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Inkluderat # | Antalet riktade ämneskoder, om sådana finns, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Antalet uteslutna ämneskoder, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | antalet mål för målenheten, om sådana har angetts, eller *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Antalet uteslutna enhetsmål, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Antalet riktade ISP-providers, om sådana finns, eller *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Antalet utelämnade leverantörer av Internet-leverantörer, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Antalet säkerhetsfilter för varumärket, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Antalet filter för att blockera bedrägerier före bud, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | antalet filter för förhandsgranskning som kan användas, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Om Site Safety Block är aktiverat eller inte: *[!UICONTROL ON]* eller *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Antalet pixlar för händelsespårning från tredje part som är kopplade till placeringen, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Antalet pixlar för konverteringsspårning som är kopplade till placeringen, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per 1000 visningar, om tillämpligt. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Antalet annonser som är kopplade till placeringen, om sådana finns, eller *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Namnen på annonserna som är kopplade till placeringen, om sådana finns, eller *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Om att korrigera placeringsinställningar för en kampanj med kalkylblad](qa-about.md)
>* [Hämta placeringsinställningar för en kampanj](qa-sheet-download.md)
>* [Överför placeringsinställningar för en kampanj](qa-sheet-upload.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

