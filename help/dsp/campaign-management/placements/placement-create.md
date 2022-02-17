---
title: Skapa en placering
description: Lär dig hur du skapar en placering.
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: a30f3bffaf63a79bb7aead69e52524419ed54ed0
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# Skapa en placering

>[!TIP]
>
>Skapa praktik baserat på specifika kampanjmål eller rapporteringsbehov.

1. På huvudmenyn klickar du på **[!UICONTROL Campaigns]**.

1. Klicka på namnet på kampanjen där placeringen ska inkluderas.

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**. I [!UICONTROL Placement Types] klickar du på placeringstypen.

   Placeringstypen bestämmer annonstypen som placeringen kan inkludera.

1. Ange [placeringsinställningar](placement-settings.md):

   1. Ange [!UICONTROL Basics] inställningar.

   1. I [!UICONTROL Goals] -avsnittet, ange [!UICONTROL Gross Budget] och, om du vill, ange ytterligare placeringsmål.

      Vissa fält har standardvärden som du kan åsidosätta.

      Om paketet som placeringen är tilldelad till har paketnivåpacing, kommer dina mål och paketinställningar att återspegla paketinställningarna.

   1. (Valfritt) I dialogrutan [!UICONTROL Geo-Targeting] avgränsar du de platser som är inkluderade eller exkluderade.

      Om du inte identifierar specifika platser anges alla platser som mål.

      >[!NOTE]
      >
      >Ort och DMA-platser är inte tillgängliga för Roku-ersättningar.

   1. I [!UICONTROL Inventory Targeting] kan du begränsa vilka lagerkällor som ska inkluderas eller exkluderas.

      För de flesta placeringstyper inkluderas alla lagertyper och alla källor för varje typ som standard. För [!DNL Roku] placeringar måste du ange lagertyp och källor.

   1. (Valfritt) I dialogrutan [!UICONTROL Site Targeting] avgränsar du de webbplatser som du vill ha som mål och anger de webbplatser som du vill utesluta.

   1. (Valfritt) I dialogrutan [!UICONTROL Audience Targeting] avsnitt:

      1. Begränsa publiken. Detta inkluderar att välja målgruppssegment att inrikta sig på inom placeringen.

         För [!DNL] Roku-placeringar, du kan använda [DSP unika målgruppsmatchning med [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) genom att inkludera ett eller flera målgruppssegment som kan matchas mot [!DNL Roku] (opted-in) deterministic dataset.
   1. (För kampanjer med enhetsövergripande målinriktning på personnivå. När placeringen är avsedd för en eller flera specifika målgrupper kan du aktivera personbaserad målinriktning på flera enheter för placeringen.

      Personbaserad målinriktning på olika enheter tillhandahålls av [!DNL LiveRamp] endast med data från USA. Tjänsten är tillgänglig för alla annonsörer på $0,35 CPM för visningar som levereras med [!DNL LiveRamp] enhetsdiagram (d.v.s. för enheter som inte hittas inom målgruppssegmenten).

   1. (Valfritt) I dialogrutan [!DNL Brand Safety and Media Targeting] kan du lägga till begränsningar för varumärkesskydd för dina placeringar.

   1. (Valfritt) I dialogrutan [!DNL Tracking] anger du händelsepixlar från tredje part eller konverterar pixlar för annonser i placeringen.

      >[!NOTE]
      >
      >([!DNL Roku] placements) Tredjepartsleverantörer av pixlar som godkänts av [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]och [!DNL Research Now].


1. Klicka på **[!UICONTROL Create Placement]**.

1. (Valfritt) Lägg till annonser på placeringen:

   1. Klicka på **[!UICONTROL Attach an ad]**.

   1. Gör något av följande:
   * Så här skapar du en ny annons:

      1. Klicka på **[!UICONTROL Create a New Ad].**

      1. Ange annonsinställningar för [ljudannonser](/help/dsp/campaign-management/ads/ad-settings-audio.md), [ansluten TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [displayannonser](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobilannonser](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [inbyggda annonser](/help/dsp/campaign-management/ads/ad-settings-native.md), eller [pre-roll ads](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md).

      1. Klicka på **[!UICONTROL Save & Submit for Review]**.

      1. (Valfritt) För varje ytterligare annons som du vill skapa för placeringen klickar du på **[!UICONTROL Attach Another Ad]** och sedan upprepa steg 1-3.

      1. Om du inte vill bifoga några annonser klickar du på **[!UICONTROL I'm done for now]**.
   * Så här bifogar du befintliga annonser i kampanjen:

      1. Klicka på **[!UICONTROL Select an Ad]**.
      1. Gör något av följande:
         * Så här lägger du till en annons i taget:
            1. Klicka på bredvid annonsnamnet **[!UICONTROL Select].**
            1. (Valfritt) För varje ytterligare annons som du vill bifoga klickar du på **[!UICONTROL Attach Another Ad]** och sedan upprepa processen.
         * Så här lägger du till upp till 20 annonser i taget:
            1. Markera kryssrutan ovanför annonslistan.
            1. Markera kryssrutan bredvid varje annons som ska läggas till.
            1. Klicka på **[!UICONTROL Attach]**.
            1. Klicka på bredvid annonsnamnet **[!UICONTROL Select]**.
      1. (Valfritt) Om du vill åsidosätta standardflygperioden och annonsrotationen för specifika annonser i placeringen:
         1. Klicka på **[!UICONTROL Custom Schedule Ads]**.

         1. Gör något av följande:

            * Klicka på **[!UICONTROL Add Flight]** och ange sedan startdatum och slutdatum.

            * Om du vill lägga till en befintlig flygning i en annons klickar du på **[!UICONTROL +]** i annonsraden för flygkolumnen.

            * Om du vill ta bort en befintlig flygning från en annons klickar du på **[!UICONTROL x]** i annonsraden för flygkolumnen.

            * (När flera annonser har samma plan) Om du vill rotera annonserna ojämnt klickar du på **[!UICONTROL Even Rotation]** i flyginformationen och ange sedan den relativa vikt som varje annons ska roteras med, i procent.

               Den totala vikten måste vara lika med 100.
         1. Klicka på uppe till höger **[!UICONTROL Continue]**.

         1. Granska flyginformationen och klicka sedan på **[!UICONTROL Save & Finish]**.




>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Redigera en placering](placement-edit.md)
>* [Redigera annonsschemat för en placering](placement-edit-ad-schedule.md)
>* [Pausa eller aktivera en placering](placement-pause-activate.md)
>* [Placeringsinställningar](placement-settings.md)
>* [Kortkommandon](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Felsökningsprestanda](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: Så här skapar du en standardbildskärmsplacering](https://video.tv.adobe.com/v/340454)

