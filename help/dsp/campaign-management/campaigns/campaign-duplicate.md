---
title: Duplicera en kampanj
description: Lär dig hur du duplicerar en kampanj.
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Duplicera en kampanj

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplicera en kampanj för att skapa en ny kampanj med liknande inställningar. Du kan:

* Duplicera kampanjen för den ursprungliga annonsören eller för en annan
* Duplicera originalpaketen och -placeringarna om du vill
* Ändra flygdatum för den nya kampanjen

Se &quot;[Vad som inte är duplicerat](#campaign-not-duplicated)&quot; för en lista över placeringsinställningar som inte är duplicerade.

1. Klicka på **[!UICONTROL Campaigns]** på huvudmenyn.
1. Klicka på **bredvid kampanjnamnet... >[!UICONTROL Duplicate]**.
1. Ange de nya kampanjinställningarna:
   1. Ange det nya kampanjnamnet och slutflygdatumet.
   1. (Valfritt) Ändra standardinställningarna.

      Som standard tilldelas den nya kampanjen till den ursprungliga annonsören, har ett flygschema som börjar den aktuella dagen och innehåller originalpaketen och -placeringarna.

1. Klicka på **[!UICONTROL Submit]**.

## Vad som inte är duplicerat {#campaign-not-duplicated}

Alla inställningar från den ursprungliga placeringen dupliceras förutom:

* Experimentera
* (Om du ändrar flygdatum) Anpassad annonsplanering
* (Om du inte bifogar annonser) Anpassad annonseringskoefficient och schemaläggning
* Standardersättningar för köp med programgaranti (PG) för [!UICONTROL Simple Ad Serving]-erbjudanden
* (Om du kopierar praktik till en annan kampanj):
   * Geografiska mål
   * Händelsepixlar
   * Annonser
   * Segment på placeringsnivå [!DNL DoubleVerify Authentic Brand Safety] (som åsidosätter segmenten på annonsörnivå)

>[!MORELIKETHIS]
>
>* [Om kampanjhantering](campaign-about.md)
>* [Skapa en kampanj](campaign-create.md)
>* [Redigera en kampanj](campaign-edit.md)
>* [Kampanjinställningar](campaign-settings.md)

