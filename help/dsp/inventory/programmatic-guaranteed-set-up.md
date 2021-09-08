---
title: Ställ in en programgarantiavtal
description: Lär dig hur du skapar ett programmatiskt garantiavtal (PG) som du har förhandlat fram med en utgivare.
feature: Private Inventory, Deal IDs, Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Ställ in en programgarantiavtal

*[Endast plattformar som stöds](programmatic-guaranteed-about.md)*

När du har förhandlat om en programmatisk garanti (PG) med en utgivare som stöds, kan du konfigurera avtalet inom DSP antingen med hjälp av [!DNL Deal ID inbox] eller genom att ange avtalsinformationen manuellt.

>[!NOTE]
>
> För PG-avtal hanterar utgivaren allt budgetutrymme, budgetbegränsning och målinriktning. Alla SSP:er som tillåter PG via DSP bekräftar att utgivaren kan ställa in budgetbegränsning.
>
> Om du vill konfigurera programmatiska, garanterade avtal med utgivare på [!DNL FreeWheel] måste du ha extra behörigheter och steg. Mer information finns i &quot;[Översikt över hur du ställer in garantierbjudanden för programmering i [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Ställ in en programmatisk garanterad affär med [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Detta är den metod som rekommenderas för [!DNL FreeWheel], [!DNL Google Authorized Buyers] och [!DNL Rubicon].

1. [Acceptera erbjudandet](deal-id-inbox-accept.md).

1. När du har sparat erbjudandet väljer du de annonser som ska användas för erbjudandet och skapar en programmatisk standardplacering (PG) enligt uppmaningen.

   Det är obligatoriskt att skapa en standardplacering för PG-paketet för att få 100 % av köpet. Den här typen av placering har ingen inriktning så DSP kan returnera ett bud till alla anbudsförfrågningar från utgivaren.

   * Om du bara tecknar ett enstaka erbjudande omdirigeras du automatiskt till arbetsflödet för att skapa standardplaceringar i PG.

      Alla [!DNL FreeWheel]-erbjudanden föreslås som ett enda avtal.

   * Om du godkänner ett förslag med flera PDF-avtal-ID:n ska du identifiera varje PG-standardplacering som du måste skapa. När du har skapat alla obligatoriska placeringar aktiveras knappen Fortsätt.

1. (Valfritt) Rikta in dig på PG-erbjudandet i andra placeringar än PG.

## Ställ in en programmatisk garanterad affär manuellt

Använd den här metoden för alla andra SSP:er.

1. [Ställ in information](deal-id-create.md) om erbjudande-ID manuellt.

1. När du har sparat erbjudandet väljer du de annonser som ska användas för erbjudandet och skapar en standardplacering för PG, enligt uppmaningen.

   Det är obligatoriskt att skapa en PG-standardplacering för erbjudandet för att få 100 % av köpet. Den här typen av placering har ingen inriktning så DSP kan returnera ett bud till alla anbudsförfrågningar från utgivaren.

1. (Valfritt) Rikta in dig på PG-erbjudandet i andra placeringar än PG.

>[!MORELIKETHIS]
>
>* [Om programmatiska erbjudanden](programmatic-guaranteed-about.md)
>* [Tips för att förhandla om ett program med garanterad programmering](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Skicka in en annons för en programmatisk garanterad affär med [!DNL FreeWheel]](freewheel-submit.md)
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Skapa information om avtal-ID manuellt](deal-id-create.md)
>* [SSP-partners](ssp-partners.md)
>* [Översikt över inventeringsfunktioner](inventory-overview.md)

