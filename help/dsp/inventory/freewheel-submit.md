---
title: Skicka en annons för ett PG-avtal till [!DNL FreeWheel]
description: Lär dig hur du begär godkännande av en annons för ett programmatiskt garanterat avtal med en utgivare på FreeWheel.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: c2caed80f0afc0cbe3572d01dc2c89f13ed13712
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Skicka en annons för ett program med garanterad programmering till FreeWheel

*Konton med [!DNL FreeWheel] Programmatiskt garanterad behörighet*

En gång [acceptera ett programmatiskt garanterat avtal med en utgivare på FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), inklusive att välja en annons och skapa den programmatiska standardplaceringen som ska användas för erbjudandet, måste du skicka annonsen till FreeWheel för godkännande.

>[!PREREQUISITES]
>
>Arbeta med dina [!DNL Adobe] kontoteam för att säkerställa att [!DNL DSP] kontot har behörighet att använda [!DNL FreeWheel] programmatiskt garanterat arbetsflöde.

## Kopiera en annonsnyckel att använda med [!DNL FreeWheel] Erbjudande {#copy-ad-key}

1. Klicka på kampanjens namn.

1. Klicka på **[!UICONTROL Ads]**.

1. Klicka  **[!UICONTROL ...]>[!UICONTROL Edit]** bredvid annonsnamnet.

1. När annonsinställningarna är öppna kopierar du den alfanumeriska annonstangenten i den URL som visas i webbläsarens adressfält.

I följande URL är annonsnyckeln `3NtNC5ZbaGZtqbei8jD3`

`https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

## Skicka en annons från [!UICONTROL Ads] Visa

1. [Kopiera annonsnyckeln för annonsen](#copy-ad-key).

1. Klicka på bredvid annonsnamnet  **[!UICONTROL ...]>[!UICONTROL submit to FreeWheel]**.

1. Verifiera erbjudande-ID, ange [den **[!UICONTROL Ad Key]**](#copy-ad-key)och klicka sedan på&#x200B;**[!UICONTROL Submit]**.

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status för annonsinlämning](freewheel-check-status.md).

## Skicka en annons från [!UICONTROL Deals] Visa

1. [Kopiera annonsnyckeln för annonsen](#copy-ad-key).

1. Klicka på **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Klicka på ![Alternativ-menyn](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to FreeWheel]**.

1. Verifiera erbjudande-ID, ange [den **[!UICONTROL Ad Key]**](#copy-ad-key)och klicka sedan på&#x200B;**[!UICONTROL Submit]**.

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status för annonsinlämning](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Översikt över hur man ställer in garantierbjudanden i FreeWheel](freewheel-overview.md)
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Kontrollera status för annonserna [!DNL FreeWheel] Programmatiska garanterade erbjudanden](freewheel-check-status.md)
>* [Felkoder för FreeWheel Ad-överföringar](freewheel-error-codes.md)

