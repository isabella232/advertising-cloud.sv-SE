---
title: Skicka en annons för ett PG-avtal till [!DNL FreeWheel]
description: Lär dig hur du begär godkännande av en annons för ett programmatiskt garanterat avtal med en utgivare på FreeWheel.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Skicka en annons för ett program med garanterad programmering till FreeWheel

*Konton med enbart  [!DNL FreeWheel] programbehörighet garanterad*

När du [har accepterat ett programmatiskt garanterat avtal med en utgivare på FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), inklusive att välja en annons och skapa den programmatiska standardplaceringen som ska användas för erbjudandet, måste du skicka annonsen till FreeWheel för godkännande.

>[!PREREQUISITES]
>
>Samarbeta med ditt Adobe-kontoteam för att säkerställa att ditt [!DNL DSP]-konto har behörighet att använda det programmatiska garanterade arbetsflödet [!DNL FreeWheel].

1. Kopiera annonstangenten för annonsen som används med erbjudandet FreeWheel:

   1. Klicka på kampanjens namn.

   1. Klicka på **[!UICONTROL Ads]** på undermenyn.

   1. Klicka på **[!UICONTROL ...]>[!UICONTROL Edit]** bredvid annonsnamnet.

   1. När annonsinställningarna är öppna kopierar du den alfanumeriska annonstangenten i den URL som visas i webbläsarens adressfält.

      I följande URL är annonsnyckeln `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. Skicka annonsen till FreeWheel:

   1. Leta reda på erbjudandet i vyn [!UICONTROL Deals].

   1. Klicka på ![Alternativ-menyn](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]** i avtalsraden.

   1. Verifiera erbjudande-ID, ange **[!UICONTROL Ad Key]** som du kopierade i steg 1 och klicka sedan på **[!UICONTROL Submit]**.

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status](freewheel-check-status.md) för annonsinlämning.

>[!MORELIKETHIS]
>
>* [Översikt över hur man ställer in garantierbjudanden i FreeWheel](freewheel-overview.md)
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Kontrollera status för annonser  [!DNL FreeWheel] för programmatiska erbjudanden](freewheel-check-status.md)
>* [Felkoder för FreeWheel Ad-överföringar](freewheel-error-codes.md)

