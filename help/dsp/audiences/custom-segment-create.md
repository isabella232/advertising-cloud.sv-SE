---
title: Skapa och implementera ett anpassat segment
description: Lär dig hur du skapar och implementerar ett anpassat segment för att spåra användare som exponeras för annonser eller användare som besöker dina webbsidor.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: bc8e476e1218681140a1748998c19f1f6c5c0866
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Skapa och implementera ett anpassat segment

Ni kan samla in era egna data från förstapartsmålgrupper genom att skapa och implementera ett anpassat Advertising Cloud-segment. Du kan använda segmentet för att spåra a) användare som exponeras för annonser från datorer, mobila enheter och CTV-enheter och b) användare som besöker specifika webbsidor. Du kan senare rikta om användare i segmentet med ytterligare annonser eller hindra användare i segmentet från att få ytterligare annonser.

>[!NOTE]
>
>Om du vill spåra användar-ID:n från förfrågningar om avanmälan till försäljning på din webbplats, enligt California Consumer Privacy Act (CCPA), skapar du en [CCPA Avanmäl segmentet](ccpa-opt-out-segment-create.md).

1. Skapa segmentet:

   1. På huvudmenyn klickar du på **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**.

   1. Ange ett unikt **[!UICONTROL Segment Name]**.

   1. För [!UICONTROL Segment Type], markera **[!UICONTROL Custom]**.

   1. Ange segmentfönstret, vilket är antalet dagar som en användares cookie stannar kvar i segmentet.

      Standardfönstret är 45 dagar. Ange ett värde mellan 1 och 365.

   1. Klicka på **[!UICONTROL Save]**.

1. Kopiera och implementera taggar för att spåra segmentet efter behov:

   1. Återgå till **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Håll markören över segmentraden och klicka **[!UICONTROL Get pixel]**.

      * Så här spårar du besökare på en webbsida:

         1. Kopiera spårningstaggen för sidvyn, som har etiketten[!UICONTROL Desktop or mobile websites].&quot;

         1. Ge annonsören eller webbplatskontakten taggen för distribution.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.
      * Så här spårar du användare som exponeras för en annonsenhet på datorer, mobila enheter eller CTV-enheter:

         1. Kopiera taggen för visningsspårning, som har etiketten &quot;[!UICONTROL Desktop or mobile ads].&quot;

         1. Lägg till taggen i antingen [!UICONTROL Pixel] flik för varje relevant annons eller för [!UICONTROL Event Pixels] i [[!UICONTROL Tracking] inställningar för varje relevant placering](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).


När du har implementerat en spårningstagg kan du använda segmentet i målgruppen eller exkluderingarna för alla placeringar.

>[!TIP]
>
>Håll reda på segmentstorleken när användarna spåras.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
