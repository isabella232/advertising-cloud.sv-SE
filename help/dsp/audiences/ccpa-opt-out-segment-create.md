---
title: Skapa och implementera ett CCPA-segment för avanmälan vid försäljning
description: Lär dig hur du skapar och implementerar ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning.
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Skapa och implementera ett CCPA-segment för avanmälan vid försäljning

Du kan skapa ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar annonseringen i Adobe samla in en pool med ID:n för annonsörens räkning.

>[!NOTE]
>
>* Mer information om hur du kan kommunicera CCPA-begäran om att avanmäla sig från försäljning till Adobe Advertising med Adobe Experience Platform Privacy Service API finns i [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* Skapa en [anpassat segment](/help/dsp/audiences/custom-segment-create.md).


1. Skapa segmentet:

   1. På huvudmenyn klickar du på **Publiker > Segment**.

   1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**.

   1. Ange ett unikt **[!UICONTROL Segment Name]**.

      Rekommenderat segmentnamn: &quot;&lt;*Advertiser-namn*> - CCPA Opt Out of Sale (t.ex. &quot;Acme - CCPA Opt Out of Sale&quot;)

   1. För [!UICONTROL Segment Type], markera **[!UICONTROL CCPA Opt-out of sale]**.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera en pixeltagg för att spåra segmentet:

   1. Återgå till **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Håll markören över det nya segmentet på segmentraden och klicka **[!UICONTROL Get pixel]**.

   1. Kopiera bildpixeln (börja med `<img src="https://rtd-tm.everesttech.net"`) för att samla in användar-ID:n för dator- och mobilbesökare på en webbsida.

   1. Ange taggen till annonsören eller webbplatskontakten för distribution med hjälp av den mekanism som företaget använder för att spåra förfrågningar om att avanmäla sig från försäljning (till exempel med hjälp av en plattform för hantering av samtycke).

      Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      När pixeln har implementerats börjar annonseringen i Adobe samla in en pool med ID:n för annonsörens räkning.

      Även om det är annonsörerna som bestämmer implementering och logik är det här ett exempel på hur en annonsör kan tända ut pixeln:

      1. En konsument hamnar på annonsörens hemsida.
      1. Konsumenten hittar och klickar på annonserarens&quot;CCPA opt out of sales&quot;-knapp.
      1. Konsumenten får en lista över tjänsteleverantörer som annonsören arbetar med.
      1. Konsumenten markerar rutan för att avanmäla sig från att sälja data till Adobe Advertising.

         Den här åtgärden aktiverar pixeln och samlar in konsumentens cookie-ID inom den angivna[!UICONTROL CCPA Opt-out of sale]&quot; segment.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](/help/privacy/ccpa-opt-out-of-sale.md)
>* [Om [!UICONTROL CCPA Opt-out-of-Sale] Segment och rapporter](ccpa-opt-out-about.md)
>* [Hämta rapporter om konsumentavanmälan](ccpa-opt-out-segment-report-retrieve.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Om Audience Management](audience-about.md)

