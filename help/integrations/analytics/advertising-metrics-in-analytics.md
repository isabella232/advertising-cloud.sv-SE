---
title: Adobe Advertising Metrics in Analysis Workspace
description: Adobe Advertising Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Adobe Advertising Metrics in Analysis Workspace

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

>[!NOTE]
>
>* Adobe Advertising överför trafikstatistik och dimensioner till [!DNL Analytics] varje dag.
>* [!DNL Analytics] tar klickningar och genomvisningar för Adobe Advertising i realtid.


## Trafikstatistik från Adobe Advertising

>[!NOTE]
>
>Alla Adobe Advertising trafik metrics in [!DNL Analytics] börja med &quot;AMO&quot;.

| Trafikmått | Beskrivning |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Antalet Adobe Advertising-visningar. |
| [!UICONTROL AMO Clicks] | Det totala antalet annonsklickningar i Adobe. |
| [!UICONTROL AMO Cost] | Adobe Advertising-utgifterna i rapporteringsprogrammets valuta. |
| [!UICONTROL AMO ID Instance] | Antalet gånger som Adobe Advertising ID anges. |
| [!UICONTROL AMO Minutes Viewed] | Hur många minuter en Adobe Advertising-video visades. |
| [!UICONTROL AMO Views] | Antalet visningar på en annons. En vy räknas när visningsprogrammet startar Adobe-reklamvideon. |
| [!UICONTROL AMO Views 25% Complete] | Antalet vyer för vilka minst 25 % av en Adobe-reklamvideo bevakades. |
| [!UICONTROL AMO Views 50% Complete] | Antalet vyer för vilka minst 50 % av en Adobe-reklamvideo bevakades. |
| [!UICONTROL AMO Views 75% Complete] | Antalet vyer för vilka minst 75 % av en Adobe-reklamvideo bevakades. |
| [!UICONTROL AMO Views 100% Complete] | Antalet vyer som 100 % av en Adobe-reklamvideo bevakades för. |
| [!UICONTROL AMO Viewable Impressions] | Antalet avtryck som har mätts så att de kan visas enligt placeringskonfigurationen. |
| [!UICONTROL AMO Not Viewable Impressions] | Antalet visningar som inte kunde visas. Detta värde beräknas som ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Antalet visningar som har opererats och för vilka visningspotentieringen har initierats. Detta värde beräknas som (instrumenterade avtryck - antalet omätbara avtryck). |

## Användbara beräknade värden för Adobe-annonsering

Överväg att skapa följande mätvärden för era Adobe-annonsdata.

* Klicka på instansen av landningssidan ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Detta är andelen personer som klickade på annonsen och gjorde den till landningssidan.
* Mätbar hastighet ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Synlig tryckhastighet ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kostnad per vy ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kostnad per klick ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe Advertising Dimensions

>[!NOTE]
>
>Alla Adobe-reklamdimensioner i [!DNL Analytics] följs av &quot;(AMO-ID)&quot;.

| Dimension | Tillämpliga Adobe-reklamdata | Beskrivning |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] och [!DNL Search] data | Kontonamnet. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] och [!DNL Search] data | RTB ([!DNL DSP]) eller annonsnätverksnamnet ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Kampanjnamnet. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Paketet ([!DNL DSP]) eller portfölj ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Placeringsnamnet. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Annonsgruppens namn. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Nyckelordet. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Sökmatchningstypen. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Nyckelordet och matchningstypen. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Annonstypen, som `text`, `video`, `display`, eller `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Annonstypen ([!DNL DSP]) eller annonsrubrik ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Annonsbeskrivningen ([!DNL DSP]) eller reklamtext ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Den URL som visas i annonsen. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | Annonsens mål-URL. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] och [!DNL Search] data | Anger om landningssidan var en genomsiktlig eller klickbar. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Produktmålet för en produktlistad annons. |

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Data i Adobe-reklam](/help/integrations/analytics/analytics-data-in-advertising.md)

