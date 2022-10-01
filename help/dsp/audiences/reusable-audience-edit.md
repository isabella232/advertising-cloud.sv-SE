---
title: Redigera en återanvändbar publik
description: Lär dig hur du redigerar en återanvändbar målgrupp.
feature: DSP Audiences
source-git-commit: 4310a5cb01fc1969ff28143c3a7cb652118b410e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Redigera en återanvändbar publik

När du redigerar en målgrupp som används på en plats eller i andra återanvändbara målgrupper tillämpas ändringarna omedelbart på dessa platser och målgrupper.<!-- verify -->

1. På huvudmenyn klickar du på **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. Håll markören över målgruppsraden och klicka **[!UICONTROL Edit]**.

1. Redigera målgruppsinställningarna på något av följande sätt:

   >[!NOTE]
   >
   >Om du redigerar målgruppssegmentslogiken, detaljerad [målgruppsstorleksdata](audience-about.md) uppdateras i den högra panelen.

   * (Valfritt) Redigera **[!UICONTROL Audience Name]** klicka ![Redigera](/help/dsp/assets/edit.png) bredvid målgruppsnamnet anger du ett unikt målgruppsnamn och klickar sedan på **[!UICONTROL Apply]**.

   * (Valfritt) Om du vill redigera segmentlogiken manuellt använder du segment som finns på [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]och [!UICONTROL Saved Audiences] tabbar](audience-settings.md)gör du följande.

      * Så här lägger du till ett segment i en befintlig segmentgrupp:
      1. Klicka på segmentgruppen på den högra panelen.

      1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, eller *[!UICONTROL Exclude All]*, efter behov.

         *[!UICONTROL Exclude All]* är inte tillgänglig för den första segmentgruppen. För en målgrupp som endast innehåller undantag, bygg denna målgrupp som *[!UICONTROL Include Any]* och sedan, på en plats, välja den publiken på menyn Uteslutna målgrupper.

      1. Leta reda på det nya segmentet i den vänstra panelen och markera kryssrutan bredvid segmentnamnet.

         Segmentgruppen uppdateras automatiskt med det nya segmentet.
   * Så här lägger du till en ny segmentgrupp:

      1. Klicka **[!UICONTROL + New Group]** i den högra panelen.

      1. (Valfritt) Ändra logiken mellan föregående grupp och den nya gruppen till *[!UICONTROL And]* eller *[!UICONTROL Or]*, efter behov.

      1. Leta reda på segmenten för den nya gruppen i den vänstra panelen och markera kryssrutorna bredvid segmentnamnen.

      1. (Valfritt) Ändra grupplogiken till *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, eller *[!UICONTROL Exclude All]*, efter behov.
   * Så här använder du segmentlogik från en befintlig målgrupp:

      1. Kopiera segmentlogiken från den befintliga målgruppen på något av följande sätt:

         * I vyn Alla målgrupper håller du markören över målgruppsraden och klickar sedan på **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Klicka på i inställningarna för den befintliga målgruppen längst upp på segmentlogikpanelen **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * I en textredigerare skapar du segmentlogiken manuellt med hjälp av alfanumeriska segment-ID:n och [Boolesk syntax](audience-segment-logic-syntax.md)och kopiera det till Urklipp.
      1. Klicka **[!UICONTROL paste in an audience rule to begin building]**, klistra in den befintliga segmentlogiken i indatafältet och klicka sedan på **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Om målgruppen redan innehåller någon segmentlogik skrivs den befintliga logiken över när du klistrar in den i den nya segmentlogiken.





1. Klicka på **[!UICONTROL Save]**.

1. Klicka på **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Duplicera en återanvändbar publik](reusable-audience-duplicate.md)
>* [Visa information om en återanvändbar publik](reusable-audience-view-details.md)
>* [Dela en återanvändbar målgrupp](reusable-audience-share.md)
>* [Exportera en återanvändbar publik](reusable-audience-export.md)
>* [Kopiera segmentnyckeln för en återanvändbar publik till Urklipp](reusable-audience-clipboard.md)
>* [Ta bort en återanvändbar publik](reusable-audience-delete.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Syntax för målgruppssegmentslogik](audience-segment-logic-syntax.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)

