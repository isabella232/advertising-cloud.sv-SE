---
title: Skapa en återanvändbar publik
description: Lär dig hur du skapar återanvändbara målgrupper som består av målgruppssegment och andra sparade målgrupper.
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 37e5a4fbb7e2ccda77ab0afd49054ec4d1dabf76
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Skapa en återanvändbar publik

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Ni kan spara och hantera återanvändbara målgrupper, som är grupper av målgruppssegment och till och med andra sparade målgrupper, som ni kan använda som mål eller exkluderingar för flera platser.

1. På huvudmenyn klickar du på **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. Ovanför datatabellen klickar du på **[!UICONTROL Create]**.

1. Ange ett unikt [!UICONTROL Audience Name].

1. (Valfritt) Avmarkera alternativet till **[!UICONTROL Share with all advertisers in my account]**.

   När ni delar en publik blir målgruppen tillgänglig som mål eller exkludering för alla annonsörer på kontot. De enskilda segmenten i målgruppen är dock bara tillgängliga för användare som segmenten delas med. Om du till exempel delar en publik som innehåller Adobe Analytics-segment med en annonsörer som inte är mappad till samma [!DNL Analytics] kommer segmentet inte att förhandsgranskas för den annonsören. Endast de segment som är tillgängliga för den annonsören förhandsgranskas i målgruppen.

1. Klicka på **[!UICONTROL Save]**.

1. Bygg målgruppen:

   >[!NOTE]
   >
   >När ni bygger upp målgruppen, detaljerat [målgruppsstorleksdata](audience-about.md) uppdateras i den högra panelen

   * Skapa segmentlogiken manuellt med hjälp av segment som finns på [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]och [!UICONTROL Saved Audiences] tabbar](audience-settings.md)gör du följande.

      * Om du vill lägga till det första segmentet letar du reda på segmentet i den vänstra panelen och markerar kryssrutan bredvid segmentnamnet.

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




1. Klicka på **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Om Audience Management](audience-about.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Syntax för målgruppssegmentslogik](audience-segment-logic-syntax.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)
>* [Skapa och implementera ett anpassat segment](custom-segment-create.md)
>* [Skapa och implementera en [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

