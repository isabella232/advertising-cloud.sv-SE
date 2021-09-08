---
title: Advertising Cloud Metrics in Analysis Workspace
description: Advertising Cloud Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Advertising Cloud Metrics in Analysis Workspace

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

>[!NOTE]
>
>* Advertising Cloud skickar trafikstatistik och dimensioner till [!DNL Analytics] dagligen.
>* [!DNL Analytics] fångar upp Advertising Cloud klickningar och genomgångar i realtid.


## Trafikstatistik från Advertising Cloud

>[!NOTE]
>
>Alla Advertising Cloud trafikstatistik i [!DNL Analytics] börjar med AMO.

| Trafikmått | Beskrivning |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Antalet Advertising Cloud-visningar. |
| [!UICONTROL AMO Clicks] | Det totala antalet Advertising Cloud-klick. |
| [!UICONTROL AMO Cost] | Advertising Cloud spenderar pengar i rapporteringsprogrammets valuta. |
| [!UICONTROL AMO ID Instance] | Antalet gånger som Advertising Cloud-id:t anges. |
| [!UICONTROL AMO Minutes Viewed] | Hur många minuter en Advertising Cloud-video visades. |
| [!UICONTROL AMO Views] | Antalet visningar på en annons. En vy räknas när visningsprogrammet startar Advertising Cloud-videon. |
| [!UICONTROL AMO Views 25% Complete] | Antalet vyer som minst 25 % av en Advertising Cloud-video har tittat på. |
| [!UICONTROL AMO Views 50% Complete] | Antalet vyer som minst 50 % av en Advertising Cloud-video har tittat på. |
| [!UICONTROL AMO Views 75% Complete] | Antalet visningar som minst 75 % av en Advertising Cloud-video har tittat på. |
| [!UICONTROL AMO Views 100% Complete] | Antalet vyer som 100 % av en Advertising Cloud-video bevakades för. |
| [!UICONTROL AMO Viewable Impressions] | Antalet avtryck som har mätts så att de kan visas enligt placeringskonfigurationen. |
| [!UICONTROL AMO Not Viewable Impressions] | Antalet visningar som inte kunde visas. Värdet beräknas som ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Antalet visningar som har opererats och för vilka visningspotentieringen har initierats. Detta värde beräknas som (instrumenterade avtryck - antalet omätbara avtryck). |

## Användbara anpassade beräknade värden för Advertising Cloud

Överväg att skapa följande mätvärden för dina Advertising Cloud-data.

* Klicka på instansen av startsidan ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Detta är andelen personer som klickade på annonsen och gjorde den till landningssidan.
* Mätbar hastighet ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Synlig impressionshastighet ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kostnad per vy ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kostnad per klick ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Advertising Cloud-Dimensioner

>[!NOTE]
>
>Alla Advertising Cloud-dimensioner i [!DNL Analytics] följs av &quot;(AMO ID)&quot;.

| Dimension | Tillämpliga Advertising Cloud-data | Beskrivning |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Advertising Cloud DSP eller sökmotorns namn |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] och  [!DNL Search] data | Kontonamnet. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | RTB ([!DNL DSP]) eller annonsnätverksnamnet ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Kampanjnamnet. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Paketets ([!DNL DSP]) eller portföljens ([!DNL Search]) namn. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Placeringsnamnet. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Annonsgruppens namn. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Nyckelordet. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Sökmatchningstypen. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Nyckelordet och matchningstypen. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Annonstypen, till exempel `text`, `video`, `display` eller `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Annonstypen ([!DNL DSP]) eller annonsrubriken ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Annonsbeskrivningen ([!DNL DSP]) eller annonstexten ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Den URL som visas i annonsen. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | Annonsens mål-URL. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] och  [!DNL Search] data | Anger om landningssidan var en genomsiktlig eller klickbar. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Produktmålet för en produktlistad annons. |

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Data i Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

