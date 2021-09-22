---
title: Översikt över konfiguration av PG-erbjudanden i FreeWheel
description: 'Lär dig mer om förutsättningarna och de extra steg som krävs för att köra annonser för programmatiska annonsköp med utgivare på FreeWheel. '
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Översikt över hur man ställer in garantierbjudanden i FreeWheel

Att konfigurera programmatiska, garanterade avtal med utgivare på FreeWheel kräver extra behörigheter och steg.

>[!PREREQUISITES]
>
>Samarbeta med ditt Adobe-kontoteam för att säkerställa att ditt [!DNL DSP]-konto har följande behörigheter.
>
>1. Behörighet att använda det programmatiska garanterade arbetsflödet [!DNL FreeWheel], som krävs för att skicka en annons för ett programmatiskt erbjudande till [!DNL FreeWheel].
>
>1. (Om du arbetar med utgivare i Storbritannien som behöver ett Clearcast-klocknummer med varje annons) Tillstånd att inkludera klocknummer i dina annonser.


## Arbetsflöde

1. Skapa en annons med medietypen som anges i erbjudandet.

   För vissa utgivare i Storbritannien måste du inkludera ett Clearcast-klocknummer tillsammans med din annons.

1. [Godkänn det ](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) avtals-ID som du redan har förhandlat med en utgivare på FreeWheel med hjälp av Inkorgen för ditt avtal-ID.

   När du har godkänt erbjudandet följer du instruktionerna för 1) väljer annonsen som ska användas för erbjudandet och 2) skapar en programmatisk garanterad standardplacering för annonsen.

1. [Skicka annonsen till FreeWheel](freewheel-submit.md)

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status](freewheel-check-status.md) för annonsinlämning.

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Skicka en annons för ett program med garanterad programmering till FreeWheel](freewheel-submit.md)
>* [Kontrollera status för annonser  [!DNL FreeWheel] för programmatiska erbjudanden](freewheel-check-status.md)
>* [Felkoder för FreeWheel Ad-överföringar](freewheel-error-codes.md)

