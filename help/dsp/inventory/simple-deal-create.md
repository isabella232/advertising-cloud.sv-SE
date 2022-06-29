---
title: '"Skapa en [!UICONTROL Simple Ad Serving] Erbjudande"'
description: '"Lär dig hur du skapar en spårningspixel för en [!UICONTROL Simple Ad Serving] affär."'
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: 089d91f7d1b06e29d27ac95a46834127d19c141d
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Skapa en [!UICONTROL Simple Ad Serving] Erbjudande

1. På huvudmenyn klickar du på **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]** och sedan markera **[!UICONTROL Simple Ad Serving]**.

1. Ange [inställningar](simple-deal-settings.md):

   1. I [!UICONTROL Select Ad Source] , ange information om utgivaren, annonsören och kampanjen samt annonstyp och klicka sedan på **[!UICONTROL Next]**.

   1. I [!UICONTROL Select Ad(s)] anger du en annons som ska användas som proxy i DSP:

      1. Gör något av följande:

         * För befintliga annonser väljer du de annonser som ska användas.

         * Skapa en proxy för nya annonser [annons från tredje part](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP betjänar inte de annonser du anger. Utgivaren står för annonsen.

      1. Klicka på **[!UICONTROL Next]**.
   1. Redigera flödesinformationen i Feed Details och klicka sedan på **[!UICONTROL Next]**.

      Advertising Cloud DSP genererar automatiskt en placering med namnet&quot;SAS-placering - &lt;*transaktionsnamn*>,&quot; för annonsen. I placeringen anges erbjudandet automatiskt i [!UICONTROL Inventory Targets] -avsnitt. Alla andra målinriktningsalternativ är inte tillämpliga.



1. Skicka pixlar för händelsespårning till utgivaren för implementering på något av följande sätt:

   * (Valfritt) Från [!UICONTROL Activate Tag with Publisher] skickar du avtalstaggen till utgivaren.

      När du är klar med de föregående stegen genererar DSP ett e-postmeddelande som du kan skicka till utgivaren. Meddelandet innehåller avtalsinformationen, en länk från vilken du kan hämta avtalstaggen och en auktoriseringskod för länken.

      1. Granska avtalsinformationen och gör sedan något av följande:

         * Klistra in informationen i ett e-postmeddelande i ett e-postprogram på enheten genom att klicka på **[!UICONTROL Email & Done]** och välj e-postprogrammet. The [!UICONTROL CC:] fältet är förifyllt med ett [!DNL Adobe] supportadress. Du kan sedan skicka meddelandet till lämplig kontakt för utgivaren.

         * Om du vill kopiera informationen till Urklipp klickar du på **[!UICONTROL Copy Email].** Du kan sedan klistra in innehållet manuellt i ett e-postmeddelande och skicka det till lämplig kontakt för utgivaren. Du måste inkludera en kopia (CC:) för att `publisher-support-global@adobe.com`. När du är klar med kopieringen av meddelandet klickar du på **[!UICONTROL Email & Done]**.
      1. (Om det behövs) Följ upp med utgivaren för att se om taggen innehåller rätt makron så att taggen fungerar med utgivarens annonsserver.
   * (Valfritt) Skicka pixlarna för händelsespårning manuellt till utgivaren:

      1. I avtalsraden i [!UICONTROL Deals] visa, klicka ![Alternativ-menyn](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Händelsepixlarna innehåller en [!UICONTROL Clickthrough] pixel och en [!UICONTROL Impression] pixel. Video- och ljudannonser innehåller även händelsepixlar per kvartil (från [!UICONTROL 25% Complete] till [!UICONTROL 100% Complete]).

      1. Kopiera pixlarna för händelsespårning och skicka dem till din utgivare.



>[!MORELIKETHIS]
>
>* [Om [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Inställningar](simple-deal-settings.md)
>* [Visa en detaljerad rapport för ett avtal](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
