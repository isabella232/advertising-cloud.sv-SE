---
title: Om Audience Management i Advertising Cloud DSP
description: Läs om funktioner för målgruppshantering.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 3b44e8e019bfc4bab2ee65ac028313752cb4a0e0
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# Om Audience Management i Advertising Cloud DSP

I Advertising Cloud DSP kan du skapa och hantera målgruppssegment och målgruppsuppsättningar som du kan använda som mål för dina ersättningar:

* Ni kan samla in era egna data från förstapartsmålgrupper genom att skapa och implementera segment. Du kan senare rikta om användare i segmentet med annonser eller hindra användare i segmentet från att ta emot annonser. Du kan skapa följande typer av segment:

   * [Egna segment](/help/dsp/audiences/custom-segment-create.md) för att spåra a) användare som exponeras för annonser från datorer, mobila enheter och CTV-enheter och b) användare som besöker specifika webbsidor.

   * [CCPA-segment för avstående från försäljning](/help/dsp/audiences/ccpa-opt-out-segment-create.md) för att spåra användar-ID:n från förfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA). Du kan hämta månadsrapporter om användar-ID:n från begäranden om att avanmäla dig.

      Mer information om Advertising Cloud stöd för CCPA-begäran om avanmälan finns i [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* Du kan skapa ett målgruppsbibliotek med [återanvändbara målgrupper](/help/dsp/audiences/reusable-audience-create.md). Sparade målgrupper består av alla era tillgängliga målgruppssegment och alla era andra sparade målgrupper. Alla ändringar du gör för en sparad målgrupp tillämpas automatiskt på alla placeringar som riktar sig till eller utesluter målgruppen och på alla andra målgrupper som inkluderar den sparade målgruppen.

   Med sparade målgrupper kan mediemanners gruppera målgrupper efter behov genom att inkludera och exkludera flera segment med komplex boolesk logik. Storleken på varje enskilt segment och den totala målgruppsstorleken anges när du skapar en målgrupp. Kampanjcheferna kan sedan välja en eller flera sparade målgrupper som placeringsmål i stället för att manuellt konfigurera målgrupper för varje placering.

Det finns även andra typer av målgrupper att tillgå för riktad marknadsföring.

## Importera datasegment från första och tredje part

DSP kan importera egna datasegment från första part från datahanteringsplattformen (DMP) och tillhandahålla dem till alla typer av annonsörer efter behov.

DSP är ett integrerat mål för [den [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)så att ni kan dela autentiserade förstahandssegment med godkända annonsörer och användare för kampanjaktivering. Mer information om Real-Time CDP-integrationen finns i [Avsnittet Källor](/help/dsp/audiences/sources/source-about.md).

DSP kan även importera egna tredjepartssegment, inklusive komplexa kombinationer av tredjepartssegment. Ni kan vid behov tillhandahålla segmenten till valfri uppsättning annonsörer.

Kontakta [!DNL Adobe] kontoteam för mer information.

## Målgrupper som är tillgängliga som placeringsmål

Du kan rikta dina placeringar till alla följande typer av målgrupper.

* Alla användarskapade målgruppsuppsättningar som sparades i DSP.

* Alla användarskapade målgruppssegment som skapades i DSP:

   * Anpassade segment för användare som besökte specifika webbsidor och användare som exponerats för visningar av specifika annonser.

   * CCPA-målgruppssegment för avanmälan av försäljning för användare som lämnat in begäran om avanmälan av försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA).

* Alla importerade datasegment från första part.

* Alla importerade anpassade datasegment från tredje part.

* (Endast praktik i USA) [Alla tredjepartsdatasegment som är tillgängliga för DSP kunder från över 30 leverantörer](/help/dsp/audiences/third-party-data-providers.md), inklusive [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]och många fler.

   Du kan rikta in dig på specifika segment, som riktar sig till användare baserat på målgruppsdata (t.ex. användare med specifika demografiska profiler, intressen eller avsikter samt/eller beteendeprofiler). Du kan bläddra efter dataleverantör och kategori, söka efter segment efter namn eller segment-ID eller filtrera resultaten efter dataleverantör, total segmentstorlek, webbläsarantal eller antal enheter.

   Extra avgifter tillkommer för segment från tredje part, vilket anges bredvid varje segmentnamn.

* (Annonsörer med Adobe Experience Platform och [!DNL Real-Time CDP], Adobe Audience Manager eller Adobe Analytics som endast använder Advertising Cloud JavaScript-konverteringstaggar) Alla tillgängliga första-, andra- eller tredjepartssegment som skapats i [!DNL Real-Time CDP], skapat i Audience Manager eller publicerat till Adobe Experience Cloud från Audience Manager eller [!DNL Analytics].

   Priset för segmenten är förförhandlat och syns inte i DSP.

   Segment från [!DNL Analytics] är tillgängliga ungefär en timme efter att du har skapat eller publicerat dem som Experience Cloud-målgrupper. Segment som kommer direkt från Audience Manager eller [!DNL Real-Time CDP] är tillgängliga inom 24 timmar efter att du delat dem.

   >[!NOTE]
   >
   >Läs dokumentationen för [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analyser](https://experienceleague.adobe.com/docs/analytics.html)och [den [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) för information om hur du ställer in och samlar in data för segment i dessa lösningar.

## Målgruppsstorleksdata

Inom sparade målgruppsinställningar och placeringsinställningar kan du se detaljerade data om målgruppsstorlek:

* Den totala och aktiva borttagna dubblettstorleken för alla valda segment och sparade målgrupper visas, och du kan visa information per enhetstyp (webbläsare, mobil eller ansluten TV).

   ![den kombinerade målgruppsstorleken](/help/dsp/assets/audience-size.png)

* För enskilda segment och sparade målgrupper visas den totala målgruppsstorleken och CPM (om tillämpligt) bredvid segmentnamnet. Du kan visa mer information om segmentet, inklusive storleken per enhetstyp (webbläsare, mobil eller ansluten TV). För sparade målgrupper är den totala storleken den deduplicerade summan.

   ![den enskilda segmentstorleken](/help/dsp/assets/audience-size-segment.png)

## Målgruppsvyer

### Vyn Alla målgrupper

I [!UICONTROL All Audiences] för , eller Audience Library, kan ni spara och hantera återanvändbara målgrupper, som innefattar grupper av målgruppssegment och till och med andra sparade målgrupper. Du kan använda målgrupper som mål för flera placeringar. Antalet placeringar där varje målgrupp används anges bredvid placeringsnamnet.

Du kan redigera, klona, ta bort, exportera och dela vilken målgrupp som helst.

### Segmentvyn

I [!UICONTROL Segments] kan alla användare skapa ytterligare anpassade segment.

The [!UICONTROL Segments] I visas även följande segmenttyper:

* Alla användarskapade anpassade segment är tillgängliga för användaren.

   Du kan visa spårningstaggar för alla anpassade segment som du har skapat och dela dessa segment med andra användare. Du kan också redigera eller ta bort de anpassade segment som du har skapat.

   Du kan inte redigera eller dela anpassade segment som andra användare har delat med dig.

* Alla importerade förstapartssegment som är tillgängliga för användaren.

   Du kan inte redigera eller dela egna segment som delats med dig. Kontakta [!DNL Adobe] kontoteam om ni behöver dela förstahandssegment med andra användare.

* Alla anpassade tredjepartssegment som är tillgängliga för användaren.

   Du kan inte redigera eller dela tredjepartssegment som delats med dig. Kontakta [!DNL Adobe] kontoteam om ni behöver dela segment från tredje part med andra användare.

>[!MORELIKETHIS]
>
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Syntax för målgruppssegmentslogik](audience-segment-logic-syntax.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

