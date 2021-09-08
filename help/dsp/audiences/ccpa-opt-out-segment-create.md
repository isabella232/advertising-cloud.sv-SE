---
title: Skapa och implementera ett CCPA-segment för avanmälan vid försäljning
description: Lär dig hur du skapar och implementerar ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning.
feature: CCPA, Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Skapa och implementera ett CCPA-segment för avanmälan vid försäljning

Du kan skapa ett segment för att spåra användar-ID:n från konsumentförfrågningar om att avanmäla sig från försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA). Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

När segmentets pixeltagg har implementerats börjar Advertising Cloud samla in en pool med ID:n för annonsörens räkning.

>[!NOTE]
>
>* Mer information om hur du kan kommunicera CCPA-begäran om att avanmäla dig till Advertising Cloud med Adobe Experience Platform Privacy Service API finns i [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).
>* Skapa ett [anpassat segment](/help/dsp/audiences/custom-segment-create.md) för att spåra användare som besöker webbsidor för syften som inte är relaterade till avanmälningshändelser för CCPA, samt användare som exponeras för annonser från datorer, mobiler och CTV-enheter.


1. Skapa segmentet:

   1. På huvudmenyn klickar du på **Publiker > Segment**.

   1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**.

   1. Ange ett unikt **[!UICONTROL Segment Name]**.

      Rekommenderat segmentnamn: &quot;&lt;*Advertiser name*> - CCPA Opt Out of Sale&quot; (t.ex. &quot;Acme - CCPA Opt Out of Sale&quot;)

   1. Välj **[!UICONTROL CCPA Opt-out of sale]** för [!UICONTROL Segment Type].

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera en pixeltagg för att spåra segmentet:

   1. Gå tillbaka till **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Håll markören över det nya segmentet i segmentraden och klicka på **[!UICONTROL Get pixel]**.

   1. Kopiera bildpixeln (med början från `<img src="https://rtd-tm.everesttech.net"`) för att samla in användar-ID:n för dator- och mobilbesökare på en webbsida.

   1. Ange taggen till annonsören eller webbplatskontakten för distribution med hjälp av den mekanism som företaget använder för att spåra förfrågningar om att avanmäla sig från försäljning (till exempel med hjälp av en plattform för hantering av samtycke).

      Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.

      När pixeln är implementerad börjar Advertising Cloud samla in en pool med ID:n för annonsörens räkning.

      Även om det är annonsörerna som bestämmer implementering och logik är det här ett exempel på hur en annonsör kan tända ut pixeln:

      1. En konsument hamnar på annonsörens hemsida.
      1. Konsumenten hittar och klickar på annonserarens&quot;CCPA opt out of sales&quot;-knapp.
      1. Konsumenten får en lista över tjänsteleverantörer som annonsören arbetar med.
      1. Konsumenten markerar kryssrutan för att avanmäla sig från att sälja data till Adobe Advertising Cloud.

         Den här åtgärden aktiverar pixeln och samlar in konsumentens cookie-ID inom det angivna [!UICONTROL CCPA Opt-out of sale]-segmentet.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Om  [!UICONTROL CCPA Opt-out-of-Sale] segment och rapporter](ccpa-opt-out-about.md)
>* [Hämta rapporter om konsumentavanmälan](ccpa-opt-out-segment-report-retrieve.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Om Audience Management](audience-about.md)

