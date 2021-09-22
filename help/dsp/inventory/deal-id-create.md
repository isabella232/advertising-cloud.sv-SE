---
title: Skapa information om avtal-ID manuellt
description: Lär dig hur du manuellt anger information för ett avtal-ID.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Skapa information om avtal-ID manuellt

1. Klicka på **[!UICONTROL Inventory]> [!UICONTROL Deals] på huvudmenyn.**

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]** och väljer **[!UICONTROL Deal ID]**.

1. Ange [avtalsinställningarna](deal-id-settings.md):

   1. I avsnittet [!UICONTROL Deal ID basics] anger du avtalsinformation och vilka annonsörer som har tillgång till erbjudandet. För garanterade erbjudanden måste du även ange planerade flygdatum och uppskattat antal visningar, endast i spårningssyfte.

   1. (Endast administratörsanvändare; (valfritt) I avsnittet [!UICONTROL Technical] redigerar du standardinställningarna efter behov.

   1. Klicka på **[!UICONTROL Save]**.

1. (Garanterade erbjudanden) Välj de annonser som ska användas för erbjudandet och skapa en standardplacering med programgaranti (PG).

   Standardplaceringar av PG-paket ser till att ditt avtal alltid returnerar ett bud för varje anbudsförfrågan. Om du inte skapar en standardplacering i PDF-format kommer inga erbjudanden att skickas in om de inte är rätt konfigurerade. Du bör alltid skapa en standardplacering för PG. I vyn [!UICONTROL Placements] har PG-standardplaceringar kolumnvärdet [!UICONTROL Sub-type] [!UICONTROL PG Default].

   Du kan också använda erbjudandet som ett lagermål i ytterligare placeringar, men du måste konfigurera dem på rätt sätt för att placera offerter.

   1. I [!UICONTROL Ad & Campaign Selection]-inställningarna väljer du de annonser som ska användas för erbjudandet:

      1. Välj annonsören, kampanjen och annonstypen.

      1. Markera kryssrutan bredvid varje annons som ska användas för erbjudandet i listan över tillgängliga annonser.

      1. Klicka på **[!UICONTROL Apply]**.
   1. På skärmen för placeringsinställningar:

      1. Ange placeringsnamnet.

      1. (Valfritt) Redigera [placeringsinställningarna](/help/dsp/campaign-management/placements/placement-settings.md), inklusive att skriva över standarderbjudandet, som automatiskt fylls med CPM-värdet från erbjudandet. ändra datumintervallet, eller bifoga fler annonser.

      Avtalen anges automatiskt i avsnittet Inventeringsmål. Alla andra målinriktningsalternativ är inte tillämpliga.

      1. Klicka på **[!UICONTROL Create placement]**.



När du har skapat avtalet kan du använda det som ett lagermål för flera placeringar.

>[!NOTE]
>
> Du behöver inte skicka avtalstaggen till utgivaren för verifiering.

>[!TIP]
>
>* I vyn [!UICONTROL Inventory] > [!UICONTROL Deals] visar kolumnen [!UICONTROL Pacing & Budget] hur erbjudandet gäller för det angivna flygdatumet och det angivna visningsmålet.
>
>* Om leveransen är under- eller överbelagd kontaktar du utgivaren för att justera hur mycket av volymen den skickar genom erbjudandet.


>[!MORELIKETHIS]
>
>* [Manuella inställningar för avtal-ID](deal-id-settings.md)
>* [Ställ in en programgarantiavtal](programmatic-guaranteed-set-up.md)
>* [Skicka in en annons för en programmatisk garanterad affär med [!DNL FreeWheel]](freewheel-submit.md)
>* [Om programmatiska erbjudanden](programmatic-guaranteed-about.md)

