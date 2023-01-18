---
title: Importera Adobe Audience Manager-segment för annonsinriktning
description: Så här importerar du [!DNL Adobe] målgrupper i Advertising DSP and Search med Adobe Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Importera Adobe Audience Manager-segment för annonsinriktning

DSP och [!DNL Advertising Search] kan alla hämta in metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers [!DNL Adobe] målgrupper<!-- segments or audiences? Standardize terms per AAM's docs -->. Detta inkluderar data för:

* Adobe Audience Manager segment

* Adobe Analytics-segment som publiceras till Adobe Experience Cloud

* Segment som har skapats i Adobe Experience Cloud med [!DNL People core service]

* Segment som har skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager

För åtkomst [!DNL Adobe] målgrupper i DSP eller [!DNL Creative]måste ni importera målgrupperna till DSP. För åtkomst [!DNL Adobe] målgrupper i [!DNL [!DNL Search]] måste du importera målgrupperna till [!DNL [!DNL Search]].

## Förutsättningar

* Annonsören måste implementera [den [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) version 2.0 eller senare. The [!DNL Identity Service] ger ett universellt, beständigt ID som identifierar besökarna i alla lösningar i Experience Cloud.

   Implementeringen innefattar att lägga till [!DNL Identity service] koda till varje webbsida på annonsörens webbplatser.

* Organisationen måste vara [aktiverat för Experience Cloud-tjänster](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) och ha Experience Cloud [!DNL Organization ID] (kallades tidigare [!DNL IMS org ID]).

   The [!UICONTROL Organization ID] kan företag med flera Adobe Experience Cloud-produkter dela data mellan vissa av dessa produkter.

* (Annonsörer med [!DNL Analytics]) Annonsören måste [implementera [!DNL Analytics] använda `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) version 1.6.4 eller senare.

* Annonsörens webbplatsbesökare har inte så många [!DNL Apple Safari] -användare.

* (Rekommenderas när annonsören använder både Audience Manager och [!DNL Analytics]) Om du vill minska antalet anrop till varje webbsida tar du bort Audience Manager [!DNL Data Integration Library] kod för datainsamling och aktivera vidarebefordran på serversidan för varje [!DNL Analytics] istället. Mer information finns i &quot;[Översikt över vidarebefordran på serversidan](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Rekommenderas) Om du vill ha högre matchningsfrekvenser skickar du endast data från förstahandswebbplatser till Adobe Advertising. Om annonsören paketerar data från tredje part eller offlinedata från ett kundrelationshanteringssystem kan dataläckage minska matchningsfrekvensen.

## Importera målgrupper från Audience Manager till DSP

### Steg för att importera målgrupper till DSP

The [!DNL Adobe] Konto- och datahanteringsteamen utför följande steg.

1. The [!DNL Adobe] kontoteamet bör konfigurera inställningen på annonsörnivå &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. The [!DNL Adobe] kontoteamet ska skicka en förfrågan<!-- Submit a request as a JIRA task? --> till datahanteringsteamet<!-- implementation team? --> om du vill importera organisationens Audience Manager-segment med hjälp av Advertising DSP native API-integrering.

### Vilka förändringar ger Audience Manager?

API:t automatiskt:

* Skapar två DSP mål i Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mappar de två destinationerna till alla Audience Manager-segment, så att Audience Manager kan dela segmenten med det DSP annonskonto som är associerat med samma Experience Cloud [!DNL Organization ID] används för Audience Manager. <!-- Verify -->

   Organisationen kan även ta bort onödiga segment från destinationerna i Audience Manager.

* Lägger till följande cookie-synkpixel för utbyte i Audience Manager-behållaren för att öka kundkampanjernas räckvidd:

   * Adobe AdCloud: 411 (Detta levereras som standard och automatiskt som en del av [!DNL Identity Service] version 2.0. Organisationer med [!DNL Identity Service] i versioner under 2.0 bör den här pixeln läggas till i Audience Manager-behållaren.

## Importera målgrupper från Audience Manager till [!DNL Search]

### Steg för att importera målgrupper till [!DNL Search]

[!DNL Adobe] personalen utför de flesta eller alla av följande steg.

1. The [!DNL Adobe] kontogruppen ska skicka en begäran till datahanteringsteamet om att skapa en integrering mellan [!DNL Search] och Audience Manager. Inkludera namnen på de Audience Manager-segment som du vill exportera till [!DNL Search].

1. Konfigurera mål för Audience Manager [!DNL Search]:

   1. Skapa två nya mål: `[!UICONTROL Adobe Media Optimizer (HTTP)]` och `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] är ett tidigare namn för [!DNL Search].

   1. Ange segmenten för var och en av destinationerna.

      Med [!UICONTROL Automatically map all current and future segments] kan alla segment mappas och synkroniseras dagligen.

      The [!UICONTROL Manually map segments] gör att du kan mappa segmenten manuellt för att synkronisera med gruppmålet (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Inga segment behöver mappas manuellt till HTTP-målet.

1. Inom [!DNL Search], antingen [!DNL Search] implementeringsteamet eller en användare med klienthanterarrollen för direkt åtkomst bör initiera importen från [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Du måste ange organisationens Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]). ID:t måste vara samma som det som används för organisationens Audience Manager-konto.

### Vilka förändringar ger Audience Manager?

Organisationen kommer att se två [!DNL Search] destinationer i Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Datasynkronisering

Den inledande importen tar ca 24 timmar. Efter den första importen synkroniseras data i realtid med en fördröjning på en till två sekunder.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Var hittar du dina synkroniserade segment?

### I DSP

I DSP ordnas segmentnamnen efter Audience Manager-taxonomin och är tillgängliga med motsvarande antal segmentmedlemmar i:

* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): På [!UICONTROL Adobe Segments] -fliken i [!UICONTROL Audience Targeting] -avsnitt.

* I [målgruppsinställningar](/help/dsp/audiences/audience-settings.md): På [!UICONTROL Adobe Segments] -fliken.

### I reklambranschen

I [!DNL Creative], är segmenten tillgängliga i upplevelseinställningarna för målnoder.

### I [!DNL Advertising Search]

I [!DNL [!DNL Search]] är segmenten tillgängliga när du skapar en [!DNL Google] målgrupp med [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; från [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

För varje [!DNL Google] målgrupper som du skapar, [!DNL Google] används för att anpassa målgruppens storlek.

>[!MORELIKETHIS]
>
>* [Adobe reklamintegrering med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

