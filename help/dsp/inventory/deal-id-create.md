---
title: Skapa information om avtal-ID manuellt
description: Lär dig hur du manuellt anger information för ett avtal-ID.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Skapa information om avtal-ID manuellt

1. På huvudmenyn klickar du på **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]** och sedan markera **[!UICONTROL Deal ID]**.

1. Ange [inställningar](deal-id-settings.md):

   1. I [!UICONTROL Deal ID basics] , ange avtalsinformation och vilka annonsörer som har tillgång till erbjudandet. För garanterade erbjudanden måste du även ange planerade flygdatum och det uppskattade antalet avtryck, endast i spårningssyfte.

   1. (Endast administratörsanvändare; valfritt) [!UICONTROL Technical] redigerar du standardinställningarna efter behov.

   1. Klicka på **[!UICONTROL Save]**.

1. (Garanterade erbjudanden) Välj de annonser som ska användas för erbjudandet och skapa en standardplacering med programgaranti (PG).

   Standardplaceringar av PG-paket ser till att ditt avtal alltid returnerar ett bud för varje anbudsförfrågan. Om du inte skapar en standardplacering i PG-format lägger inte eventuella placeringar som är avsedda för erbjudandet anbud om de inte är rätt konfigurerade. Du bör alltid skapa en standardplacering för PG. I [!UICONTROL Placements] vy, standardplaceringar i PG har en [!UICONTROL Sub-type] kolumnvärde för &quot;[!UICONTROL PG Default].&quot;

   Du kan också använda erbjudandet som ett lagermål i ytterligare placeringar, men du måste konfigurera dem på rätt sätt för att placera offerter.

   1. I [!UICONTROL Ad & Campaign Selection] väljer du de annonser som ska användas för erbjudandet:

      1. Välj annonsören, kampanjen och annonstypen. Du kan också välja en annonsstatus att filtrera annonserna med.

      1. I listan med tillgängliga annonser markerar du kryssrutan bredvid varje annons som ska användas för erbjudandet.

      1. Klicka på **[!UICONTROL Apply]**.
   1. På skärmen för placeringsinställningar:

      1. Ange placeringsnamnet.

      1. (Valfritt) Redigera [placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md), inklusive att skriva över standardanbudet, som automatiskt fylls i med CPM-värdet från affären, ändra datumintervallet, eller bifoga fler annonser.

      Avtalen anges automatiskt i avsnittet Inventeringsmål. Alla andra målinriktningsalternativ är inte tillämpliga.

      1. Klicka på **[!UICONTROL Create placement]**.



När du har skapat avtalet kan du använda det som ett lagermål för flera placeringar.

>[!NOTE]
>
> Du behöver inte skicka avtalstaggen till utgivaren för verifiering.

>[!TIP]
>
>* I [!UICONTROL Inventory] > [!UICONTROL Deals] visa [!UICONTROL Pacing & Budget] kolumn visar hur erbjudandet gäller det angivna flygdatumet och det angivna visningsmålet.
>
>* Om leveransen är under- eller överbelagd kontaktar du utgivaren för att justera hur mycket av volymen den skickar genom erbjudandet.


>[!MORELIKETHIS]
>
>* [Manuella inställningar för avtal-ID](deal-id-settings.md)
>* [Ställ in en programgarantiavtal](programmatic-guaranteed-set-up.md)
>* [Skicka in en annons för en programmatisk garanterad affär med [!DNL FreeWheel]](freewheel-submit.md)
>* [Om programmatiska erbjudanden](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->