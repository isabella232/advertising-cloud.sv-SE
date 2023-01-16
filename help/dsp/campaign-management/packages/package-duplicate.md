---
title: Duplicera ett paket
description: Lär dig hur du duplicerar ett paket.
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Duplicera ett paket

Duplicera ett paket om du vill skapa ett paket med liknande inställningar. Du kan:

* Duplicera paketet inom den ursprungliga annonseraren och kampanjen eller inom olika
* Du kan även duplicera placeringarna i paketet
* (För duplicerade paket inom de ursprungliga kampanjerna) Duplicera alternativt de ursprungliga annonserna och händelsepixlarna på placeringsnivå
* Ändra flygdatum för det nya paketet

Se &quot;[Vad som inte är duplicerat](#package-not-duplicated)&quot; för en lista med placeringsinställningar som inte är duplicerade.

1. På huvudmenyn klickar du på **[!UICONTROL Campaigns]**.

1. Klicka på namnet på kampanjen för att öppna [!UICONTROL Packages] vy.

1. Klicka på bredvid paketnamnet  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Ange de nya paketinställningarna:

   1. Ange det nya paketnamnet.

   1. (Valfritt) Ändra standardinställningarna.

      Som standard:

      * Det nya paketet tilldelas den ursprungliga annonsören och kampanjen.

      * Det nya paketet aktiveras på den aktuella dagen.<!-- and the flight continues for NN  days. -->

      * Placeringar i originalpaketet kopieras till det nya paketet.

      * Annonserna och händelsepixlarna på placeringsnivå kopieras inte till det nya paketet.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#package-not-duplicated}

Alla inställningar från den ursprungliga placeringen dupliceras förutom:

* Experimentera
* (Om du ändrar flygdatum) Anpassad annonsplanering
* (Om du inte bifogar annonser) Anpassad annonseringskoefficient och schemaläggning
* Standardplaceringar för köp av programmatiska annonsköp (PG) för [!UICONTROL Simple Ad Serving] erbjudanden
* (Om du kopierar praktik till en annan kampanj):
   * Geografiska mål
   * Händelsepixlar
   * Annonser
   * Placeringsnivå [!DNL DoubleVerify Authentic Brand Safety] segment (som åsidosätter segment på annonsörnivå)

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Visa ändringsloggen för ett paket](package-change-log.md)
>* [Paketinställningar](package-settings.md)

