---
title: Användningsexempel
description: Läs mer om användningsexempel för att dela dina annonsdata DSP media med Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 21d80cf6-f817-495a-bae4-fc9e44f1eda4
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Använd exempel för att hämta medieexponeringsdata i Adobe Audience Manager

*Annonsörer med endast DSP*

*Annonsörer med endast Adobe Advertising-Adobe Audience Manager Integration*

Nedan följer några sätt som du kan dra nytta av när du hämtar in dina annonsdata DSP medieexponeringsdata <!-- ad impression data? --> i Audience Manager.

## Hantering av senaste och frekvenser

Genom att samla in visningsdata i Audience Manager kan ni förbättra frekvenshanteringen genom att skapa segment med användare som har exponerats för en viss annons eller kampanj. Du kan använda de här segmenten för annonsinriktning om du vill öka frekvensen eller för annonsundertryckning om du vill begränsa frekvensen.

Dessutom, med Audience Manager [!DNL Segment Builder]kan du använda [Regler för senaste och frekvenser](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) till [regelbaserade egenskaper](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) som innehåller användbara signaler. På så sätt kan du till exempel begränsa hur många gånger en användare visas som en viss kreativ del i en mediekampanj. Läs &quot;[Direkt undertryckning av olika enheter](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; för att lära sig hur man gör detta.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sekventiellt meddelande

Genom att samla in visningsdata kan du skapa ett segment med användare som har exponerats för en kampanj eller annons och använda det här segmentet för sekventiella meddelanden eller undertryckande. Du kan till exempel återannonsera användare som ser kreativa `123` men klickade inte eller konverterade genom att visa dem kreativa `456`.

Så här kör du det här exemplet i Audience Manager:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Skapa ett varumärke för att fånga användare som såg den kreativa sidan.

   Om du till exempel vill namnge egenskapen `Creative Trait 123`använder du följande trait-regel:

   `d_creative == 123 AND d_event == imp`

1. Skapa en egenskap för att fånga in användare som klickar eller konverterar.

   Om du till exempel vill namnge den här egenskapen `Click and Converter`använder du följande trait-regel:

   `d_event == click OR d_event=conv`

1. Skapa ett segment som kallas `Retarget Users` för att fylla i med användare som såg kreativa `123` men klickade eller konverterade inte. Använd följande trait-regel:

   `Creative Trait 123 AND NOT Click and Converter`

1. Mappa segmentet `Retarget Users` till en destination och målanvändare på destinationen med kreativa `456`.

## [!DNL Adobe Audience Analytics] och kampanjexponeringsdata

När kampanjens intryck och klickdata är tillgängliga i Audience Manager kan ni skapa egenskaper och segment för användare som exponerats för, eller interagerats med, en viss kampanj eller taktik. Med [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)kan dina Audience Manager-segment synkroniseras med [!DNL Analytics] för ytterligare analys. Exempel på användningsområden är följande:

* **Interaktionsanalys mellan DSP och [!DNL Adobe Advertising Search] annonser:** Standarden [[!DNL Analytics for Advertising] integration](/help/integrations/analytics/overview.md) ger inte insikter i interaktionen mellan DSP och [!DNL [!DNL Search]] eftersom båda kanalerna använder AMO-ID:n som följer attribueringsreglerna för AMO-ID, där ett sökklick åsidosätter en visningsvy. Genom att skapa ett DSP exponeringssegment i Audience Manager kan du använda [!DNL Audience Analytics] för att analysera interaktionen mellan DSP och [!DNL [!DNL Search]] annonser i [!DNL Analytics].

* **Frekvensanalys:** Du kan skapa segment i Audience Manager baserat på hur många gånger en användare exponerades för en viss annons eller kampanj. Sedan kan du analysera de olika exponeringssegmenten i Analytics för att se hur användarbeteendet ändras beroende på antalet DSP exponeringar.

## [!DNL Audience Optimization Reports]

Du kan utnyttja [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) för att identifiera potentiella resultatmöjligheter för segment i era kampanjer. Dessa rapporter kombinerar kampanjexponering, klickfrekvens och konverteringsdata med segmentstatistik för att skapa segmentbaserade optimeringar och en effektiv kanalmix.

### Typer av relevanta Audience Optimization-rapporter

| Rapport | Beskrivning |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Jämför mappade och omappade segment med visningar och konverteringsgrader. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Rapporter]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Returnera data om visningar, klickfrekvens och konverteringar för ett stort antal olika annonsdimensioner. |
| [[!UICONTROL Optimal Frequency] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Hjälper er att hitta den optimala balansen mellan antalet betjänade visningar och konverteringar. Det gör att du kan justera antalet visningar som ska visas innan du börjar se minskande avkastning. |
| [[!UICONTROL Unique User Reach] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Ett bubbeldiagram där varje bubbla storleksanpassas i direkt proportion till antalet unika användare för den valda dimensionen. |

### Överväganden

* If [!DNL Audience Optimization Reports] -användare har rollbaserade åtkomstkontroller (RBAC), och [!DNL Adobe Customer Care] måste konfigurera en mappning mellan Advertiser-ID:t och integreringskoden för organisationens Audience Manager-datakälla. Administratörsanvändare kan sedan tillhandahålla RBAC-rättigheter till olika användare.

* Konverteringsrapportering i [!DNL Audience Optimization Reports] kräver att slutanvändaren har konfigurerat något. Användarna måste fylla i metadatafiler.

* [!DNL Audience Optimization Reports] stöder inte ändringar i kampanjmetadata (till exempel kampanjnamn eller placeringsnamn).

* Klicka på sökannonser finns i [!DNL Audience Optimization Reports] bara när de är korrelerade med exponeringar. Med andra ord behandlas klickningar som konverteringar efter visningar. Därför kanske inte många sökklick tas med i [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager](overview.md)
>* [Samla in data om klick och tryck från annonskampanjer DSP kampanjer](collect.md)

