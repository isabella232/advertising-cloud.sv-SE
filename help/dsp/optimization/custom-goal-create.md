---
title: Skapa ett anpassat mål
description: Skapa ett anpassat mål
feature: Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Skapa ett anpassat mål

>[!TIP]
>
>Tips om hur du konfigurerar dina anpassade mål finns i [de bästa sätten att skapa anpassade mål](custom-goal-best-practices.md).

1. Logga in på Advertising Cloud Search på (amerikanska företag) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) eller (företag i alla andra länder) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Kontrollera att de mätvärden du vill inkludera i ditt mål har spårats, att de är tillgängliga i produkten och att de innehåller ett visningsnamn:
   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]** på huvudmenyn.
   1. Leta reda på måttet och se till att **[!UICONTROL Show in UI and Reports]** är aktiverat för måttet.
   1. Om måttet inte har något värde i kolumnen **[!UICONTROL Display Name]** klickar du i cellen, anger visningsnamnet och klickar sedan på **[!UICONTROL Apply].**
1. Skapa det anpassade målet som ett *mål*:
   1. Klicka på **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]** på huvudmenyn.
   1. Klicka på **[!UICONTROL Create objective]i verktygsfältet.**
   1. Ange målinställningarna:
      1. Ange målnamnet i fältet **[!UICONTROL Change Objective Name]**.

         Målnamnet visas i listan [!UICONTROL Custom Goals] i Advertising Cloud DSP-paketinställningar.

      1. Associera egenskaper med målet:

         >[!NOTE]
         >
         > Alla transaktionsegenskaper som spåras för annonsören listas som standard i listan [!UICONTROL Available Properties].

         * Om du vill importera en CSV-fil med egenskaper och deras vikt klickar du på **[!UICONTROL Import]** och letar reda på filen som ska importeras.

            De importerade egenskaperna måste redan finnas för annonsören. namnen inte är skiftlägeskänsliga.

            De importerade egenskaperna ersätter alla befintliga egenskaper som har angetts.

         * Om du vill ange den första egenskapen manuellt med standardbredden (1) väljer du i en lista över alla transaktionsegenskaper som spåras för annonsören.

         * Om du vill lägga till en annan egenskap med standardbredden (1) manuellt klickar du på **[!UICONTROL +]** .

            >[!TIP]
            >
            > Om du vill söka efter en egenskap i listan anger du en sträng var som helst i egenskapsnamnet.

         * Om du vill lägga till flera egenskaper manuellt klickar du på **[!UICONTROL Add Multiple Properties].** För varje egenskap som du vill lägga till klickar du på egenskapsnamnet i  [!UICONTROL Available Properties] kolumnen och drar den till  [!UICONTROL Added Properties] kolumnen. När du är klar med att lägga till egenskaper klickar du på **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Om du vill söka efter en egenskap i listan anger du en sträng var som helst inom egenskapsnamnet i indatafältet.
            >* Om du vill filtrera listan så att den exkluderar egenskaper som har exkluderats i rapporter väljer du alternativet **[!UICONTROL Hide properties excluded from reports].**


         * (Om målet innehåller flera egenskaper) Om du vill ändra vikten för en egenskap i förhållande till de andra egenskaperna i målet anger du värden i **[!UICONTROL Weight]**-fälten.
      1. Klicka på **[!UICONTROL Save]** längst ned i inställningarna.


När du har skapat ett mål kan du tilldela det till ett Advertising Cloud DSP-paket som ett anpassat mål när optimeringsmålet är [!UICONTROL Highest ROAS - Custom Goal] eller [!UICONTROL Lowest CPA - Custom Goal].

>[!TIP]
>
>För optimerade <!-- optimum? Or optimization won't happen at all w/out it? -->prestanda måste de kombinerade mätvärdena i det anpassade målet (mål) totalt innehålla minst 10 konverteringar per dag. Om de inte gör det är det bästa sättet att lägga till ytterligare stödhändelser (transaktionsegenskaper), som produktsidor eller program som startar, i målet. Mer information finns i [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md).

>[!MORELIKETHIS]
>
>* [Om anpassade mål](custom-goal-about.md)
>* [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)

