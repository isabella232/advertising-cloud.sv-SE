---
title: Bifoga en annons till en placering
description: Lär dig hur du bifogar en annons till en placering.
feature: DSP Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 1%

---

# Bifoga en annons till en placering

## Bifoga en ny annons från vyn [!UICONTROL Ads]

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.
1. Klicka på kampanjens namn.
1. Klicka på **[!UICONTROL Ads]** på undermenyn.
1. Klicka på **bredvid annonsnamnet.. >[!UICONTROL Add to Placements]**.
1. Gör något av följande på skärmen Montera annons:
   * Så här skapar du en ny placering för annonsen:
      1. Klicka på **[!UICONTROL Create New Placement]**.
      1. Ange [placeringsinställningarna](/help/dsp/campaign-management/placements/placement-settings.md) och klicka sedan på **[!UICONTROL Create Placement]**.
   * Så här lägger du till annonsen på en eller flera befintliga placeringar:
      1. Klicka på **[!UICONTROL Select a Placement].**
      1. Gör något av följande:
         * Så här lägger du till en annons i taget:
            1. Klicka på **[!UICONTROL Select]bredvid annonsnamnet.**
            1. (Valfritt) För varje ytterligare annons som du vill bifoga klickar du på **[!UICONTROL Attach to Other Placement]**. Klicka på **[!UICONTROL Select]bredvid annonsnamnet.**
         * Så här bifogar du annonsen till upp till 20 placeringar i taget:
            1. Markera kryssrutan bredvid **Välj flera.&quot;
            1. Markera kryssrutan bredvid varje placering som annonsen ska kopplas till.
            1. Klicka på **[!UICONTROL Attach]**.
      1. Välj något av följande på fliken Slutför och granska:
         * Klicka på **[!UICONTROL I'm done for now]** om du vill återgå till annonsvyn.
         * Klicka på **[!UICONTROL Attach To Other Placement]** om du vill bifoga annonsen till en annan placering.

## Bifoga en ny eller befintlig annons från vyn [!UICONTROL Placements]

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.
1. Klicka på kampanjens namn.
1. Klicka på **[!UICONTROL Placements]** på undermenyn.
1. Klicka på **bredvid placeringsnamnet.. > [!UICONTROL Attach Ads].**
1. Gör något av följande på skärmen [!UICONTROL Add Ad to Placement]:
   * Så här skapar du en ny annons:
      1. Klicka på **[!UICONTROL Create a New Ad]**.
      1. Ange annonsinställningarna för [ljudannonser](ad-settings-audio.md), [ansluten TV](ad-settings-connected-tv.md), [visningsannonser](ad-settings-display.md), [mobilannonser](ad-settings-mobile.md), [inbyggda annonser](ad-settings-native.md) eller [pre-roll-annonser](ad-settings-pre-roll.md).
      1. Klicka på **[!UICONTROL Save & Submit for Review]**.

         [Reklamgranskningen](ad-about.md) för den nya annonsen tar 24-48 timmar och innehåller kontroller för känsliga kategorier, klicka på URL-funktionen och förhandsgranska rendering. Kolumnen [!UICONTROL Status] anger om DSP har godkänt annonsen. Brutna annonser kan ha en väntande status i mer än 24-48 timmar, så du har tid att åtgärda fel innan de avvisas.

         >[!NOTE]
         >
         >Din annons kan endast användas om både DSP och SSP har godkänt den kreativa processen. Varje enskild SSP har sina egna krav och processer för godkännande.
   * Så här väljer du befintliga annonser:
      1. Klicka på **[!UICONTROL Select an Ad].**
      1. Ange annonserna:
         * Så här lägger du till en annons i taget:
            1. Klicka på **[!UICONTROL Select]bredvid annonsnamnet.**
            1. (Valfritt) För varje ytterligare annons som du vill bifoga klickar du på **[!UICONTROL Add Another Ad]**. Klicka på **[!UICONTROL Select]bredvid annonsnamnet.**
         * Så här lägger du till upp till 20 annonser i taget:
            1. Markera kryssrutan bredvid **[!UICONTROL Bulk Select]**.&quot;
            1. Markera kryssrutan bredvid varje annons som ska läggas till.
            1. Klicka på **[!UICONTROL Attach]**.
      1. (Valfritt) Om du vill åsidosätta standardflygperioden och annonsrotationen för specifika annonser i placeringen:
         1. Klicka på **[!UICONTROL Custom Schedule Ads]**.
         1. Gör något av följande:
            * Om du vill lägga till en flygning klickar du på **[!UICONTROL Add Flight]** och anger sedan start- och slutdatum.
            * Om du vill lägga till en befintlig flygning i en annons klickar du på **[!UICONTROL +]** i annonsraden för flygkolumnen.
            * Om du vill ta bort en befintlig flygning från en annons klickar du på **[!UICONTROL x]** i annonsraden för flygkolumnen.
            * (När flera annonser har samma flygning) Om du vill rotera annonserna ojämnt klickar du på **[!UICONTROL Even Rotation]** i flyginformationen och anger sedan den relativa vikt som varje annons ska roteras med, i procent.
Den totala vikten måste vara lika med 100.
         1. Klicka på **[!UICONTROL Continue]** i det övre högra hörnet.
         1. Granska flyginformationen och klicka sedan på **[!UICONTROL Save & Finish]**.
      1. Klicka på **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [Om annonshantering](ad-about.md)
>* [Skapa en annons](ad-create.md)
>* [Redigera en annons](ad-edit.md)
>* [Visa en lista över placeringar som är kopplade till en annons](ad-list-placements.md)
>* [Redigera annonsschemat för en placering](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

