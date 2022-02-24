---
title: '"[!UICONTROL Simple Ad Serving] Avtalsinställningar"'
description: Läs mer om de tillgängliga inställningarna för [!UICONTROL Simple Ad Serving] erbjudanden.
feature: DSP Simple Ad Serving
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Avtalsinställningar

## Nytt [!UICONTROL Simple Ad Serving] Erbjudanden

### [!UICONTROL Select Ad Source]

| Parameter | Beskrivning |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Medietypen för det här erbjudandet: *[!UICONTROL Video],* *[!UICONTROL Display],* eller *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Namnet på utgivaren som säljer det här lagret. Sök efter en utgivare genom att ange minst de två första tecknen i namnet. Om du vill lägga till en utgivare som inte finns med i listan kontaktar du [!DNL Adobe] kontoteam. |
| **[!UICONTROL Advertiser]** | En enskild annonsör på kontot som har åtkomst till erbjudandet. Välj även den kampanj och (valfritt) det paket där erbjudandet är tillgängligt. |
| **[!UICONTROL Media Quality Assessment?]** | (Vissa användare) Gör att annonsen kan köras på en annan DSP för verifiering från tredje part. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | Det enda alternativet är *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Endast nya erbjudanden) Om du vill:<ul><li>*[!UICONTROL Create New]:* För att skapa en annons för det här erbjudandet.</li><li>*[!UICONTROL Select Ads]:* Att använda en befintlig annons för det här erbjudandet.</li></ul> |
| **[!UICONTROL Ad Type]** | Annonstypen för det här erbjudandet. Om du ska skapa nya annonser för erbjudandet ska du inkludera annonsstorleken eller -längden, enligt förfrågan. Vilka alternativ som är tillgängliga varierar beroende på medietyp. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(När du använder befintliga annonser) Annonserna som ska ingå i erbjudandet. Markera kryssrutan bredvid varje annons som ska inkluderas.

### [!UICONTROL Select & Upload [Media Type]]

(Endast nya annonser) Skärmar för att skapa en ny [förstahandsannons](/help/dsp/campaign-management/ads/ad-create.md) eller [annons från tredje part](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| Parameter | Beskrivning |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Kostnaden per tusen visningar (CPM), vilket framgår av priset för ditt kontrakt. Kontakta [!DNL Adobe] kontoteam för det här värdet. <br><br>Ange även valutan för erbjudandet. Alla användare kan välja USD eller, om SSP stöder ytterligare valutor, valutan för DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad och valutan för transaktionen.<br><br>Alla användare kan välja USD eller, om SSP stöder ytterligare valutor, valutan för DSP. **OBS!** Faktureringsbara avgifter återspeglas i [!UICONTROL Net CPM] mätvärden. |
| **[!UICONTROL Third Party Fee Description]** | (Valfritt) En beskrivning av tredjepartsavgifterna. |
| **[!UICONTROL Flight Dates]** | Start- och slutdatum för trafik som använder det här avtalet. Flygdatum måste inkluderas i kampanjflygdatum. Annonstaggarna returnerar bara ett svar under den angivna flygningen.<br><br> Det bästa sättet att skapa en separat enkel kampanj för annonsvisning med en ettårig varaktighet och att skapa spårningspixlar i den. |
| **[!UICONTROL Impressions]** | (Valfritt) Det uppskattade antalet visningar som du förväntar dig att kunna göra med det här erbjudandet. Detta värde används endast för spårningsändamål och för att flagga när leveransmålen uppfylls. utgivaren kontrollerar faktisk annonsleverans. Det bästa sättet är att ange ett stort antal visningar för att hålla taggen aktiv i DSP så att den kan förnyas eller utökas vid behov. |
| **[!UICONTROL Deal Name]** | Avtalsnamnet. Ange ett namn eller markera *[!UICONTROL Auto Generate Deal Name]* för att DSP ska kunna generera ett namn baserat på avtalsinformationen.<br><br>Exempel på ett namn som genererats automatiskt: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Skrivskyddat) Annonserna som ingår i erbjudandet. Om du vill redigera en annons klickar du på annonsens namn. Om du vill ta bort en annons från erbjudandet klickar du **[!UICONTROL X]** bredvid annonsnamnet. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Skapa en [!UICONTROL Simple Ad Serving] Erbjudande](simple-deal-create.md)
>* [Visa händelsespårningspixlar för en [!UICONTROL Simple Ad Serving] Erbjudande](simple-deal-show-pixels.md)

