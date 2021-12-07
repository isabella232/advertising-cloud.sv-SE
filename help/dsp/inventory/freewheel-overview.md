---
title: Översikt över konfiguration av PG-erbjudanden i [!DNL Freewheel]
description: 'Läs om förutsättningarna och de extra steg som krävs för att köra annonser för programmatiska annonsköp med utgivare på [!DNL Freewheel]. '
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Översikt över hur man ställer in garantierbjudanden för programmatiska inköp i [!DNL Freewheel]

Konfigurera programmatiska garanterade avtal med utgivare på [!DNL Freewheel] kräver extra behörigheter och steg.

>[!PREREQUISITES]
>
>Arbeta med dina [!DNL Adobe] kontoteam för att säkerställa att [!DNL DSP] kontot har följande behörigheter.
>
>1. Behörighet att använda [!DNL FreeWheel] programmatiskt garanterat arbetsflöde, som krävs för att skicka in en annons för ett programmatiskt garanterat erbjudande till [!DNL FreeWheel].
>
>1. (Om du arbetar med utgivare i Storbritannien som behöver en [!DNL Clearcast] klocknummer med varje annons) Tillstånd att inkludera klocknummer i annonserna.


## Arbetsflöde

1. Skapa en annons med medietypen som anges i erbjudandet.

   För vissa utgivare i Storbritannien måste du inkludera en [!DNL Clearcast] telefonnummer med annonsen.

1. [Godkänn erbjudande-ID](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) du redan har förhandlat med en utgivare på [!DNL Freewheel] med hjälp av Inkorgen för avtal-ID.

   När du har godkänt erbjudandet följer du instruktionerna för 1) väljer annonsen som ska användas för erbjudandet och 2) skapar en programmatisk garanterad standardplacering för annonsen.

1. [Skicka annonsen till [!DNL Freewheel]](freewheel-submit.md)

   Annonsen måste skickas och godkännas innan den kan köras.

1. [Kontrollera status för annonsinlämning](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Skicka in en annons för en programmatisk garanterad affär till [!DNL Freewheel]](freewheel-submit.md)
>* [Kontrollera status för annonserna [!DNL FreeWheel] Programmatiska garanterade erbjudanden](freewheel-check-status.md)
>* [Felkoder för [!DNL Freewheel] Annonsmaterial](freewheel-error-codes.md)

