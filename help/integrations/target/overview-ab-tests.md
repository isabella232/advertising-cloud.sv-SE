---
title: Konfigurera A/B-tester för Advertising Cloud DSP Ads i Adobe Target
description: Lär dig hur du ställer in ett A/B-test i [!DNL Target] för era DSP annonser.
source-git-commit: e4d0ae194da063f04fc153f0b55488bdd60f30db
workflow-type: tm+mt
source-wordcount: '1660'
ht-degree: 0%

---

# Konfigurera A/B-tester för Advertising Cloud DSP Ads i Adobe Target

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Annonsörer endast med Advertising Cloud DSP*

Adobe Advertising Cloud DSP och Adobe Target gör det ännu enklare för marknadsförare att leverera en personaliserad och uppkopplad upplevelse i betalda medier och på-plats-meddelanden. Genom att dela signaler mellan de två produkterna kan du:

* Minska antalet fall på webbplatsen genom att länka kundernas exponering från DSP till deras upplevelser på plats.

* Upprätta A/B-tester genom att spegla webbplatsupplevelser med annonsmeddelanden med hjälp av Adobe Audience Manager exponeringsdata och click-to-feed Target-målgrupper.

* Mät effekten av enhetliga meddelanden på ett visst mål med enkla visualiseringar i Adobe Analytics för [!DNL Target].

I följande avsnitt finns information om krav och instruktioner för att ställa in klicknings- och genomskinlighetsspårning, implementera signaldelning mellan DSP och [!DNL Target] och konfigurera en A/B-testaktivitet och konfigurera [!DNL Analytics] Analysis Workspace för att visa testdata.

Om du har ytterligare frågor kan du kontakta adcloud_support@adobe.com.

## Förutsättningar

Det här användningsexemplet kräver följande produkter och integreringar:

* [!DNL Target]

* [[!DNL Analytics] för Advertising Cloud](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (krävs endast för genomsiktstestning)

## Steg 1: Konfigurera Click-through Framework {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Genomklickningsramverk](/help/integrations/assets/target-ct-framework.png)

När du lägger till DSP makron i en klicknings-URL (den URL som visas när en användare klickar på en annons och når landningssidan), DSP automatiskt placeringsnyckeln genom att inkludera ```${TM_PLACEMENT_ID}``` i klickbara URL:er. Det här makrot hämtar den alfanumeriska placeringsnyckeln och inte det numeriska placerings-ID:t.

![Genomklicknings-URL tillagd till landningssidans URL](/help/integrations/assets/target-ct-url.jpg)

### Lägg till DSP makron till klickbara URL:er

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Uppdatera klicknings-URL:en för varje annons manuellt i Google Campaign Manager 360, så att den innehåller de makron som krävs för att hämta AMO ID-variabler. AMO ID-variablerna används för att skicka klickdata till Adobe Analytics och för att dela placeringsnycklar för A/B-testning. Instruktioner finns på följande sidor:

* [Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Flashtalking] Annonstaggar](/help/integrations/analytics/macros-flashtalking.md)

* [Lägg till [!DNL Analytics for Advertising Cloud] Makron till [!DNL Google Campaign Manager 360] Annonstaggar](/help/integrations/analytics/macros-google-campaign-manager.md)

Kontakta DSP och Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) för att hämta den placeringsnyckel som krävs och slutföra konfigurationen, och för att se till att varje klicknings-URL är ifylld med placeringsnyckeln.

## Steg 2: Konfigurera visningsramverket med Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Genomskinligt ramverk](/help/integrations/assets/targetr-vt-framework.png)

Genom att lägga till en händelsepixel för Audience Manager i era annonstaggar och placeringsinställningar kan du skapa ett testsegment för ytterligare visningsmöjligheter.

1. Implementera en händelsepixel för Audience Manager-intryckning i dina annonstaggar och inställningar för DSP.

   Instruktioner finns i &quot;[Samla in data om medieexponering från Advertising Cloud DSP Campaigns](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Se till att du lägger till [DSP makron](/help/dsp/campaign-management/macros.md) för att samla in alla data som du vill att bilden ska skickas tillbaka, inklusive `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

   >[!NOTE]
   >
   >Klickspårnings-URL:er innehåller `${TM_PLACEMENT_ID}` makro för den alfanumeriska placeringsnyckeln i stället för `${TM_PLACEMENT_ID_NUM}` för det numeriska placerings-ID:t.

1. Konfigurera ett Audience Manager-segment utifrån DSP:

   1. Gå till **Audience Manager** > **Målgruppsdata** > **Signaler** och sedan väljer **Sök** överst till vänster.

   1. Ange **Nyckel** och **Värde** för signalen som bestämmer på vilken nivå segmentanvändarna grupperas. Använd en [nyckel som stöds](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) med ett värde som motsvarar ett makro som du har lagt till i Audience Manager-visningshändelsepixeln.

      Om du till exempel vill gruppera användare för en viss placering använder du `d_placement` nyckel. För värdet använder du ett numeriskt placerings-ID (till exempel 2501853 i skärmbilden ovan) som fångas av det DSP makrot `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Om fältet Totalt antal visar antalet användare för nyckelvärdepar, vilket anger att pixeln placerades korrekt och att data flödar, kan du fortsätta till nästa steg.
   ![Söksignaler](/help/integrations/assets/target-am-signals.png)

1. [Skapa ett regelbaserat varumärke](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) för att skapa segment i Audience Manager.

   1. Namnge egenskapen så att den är lätt att identifiera inom testaktiviteterna. Lagra egenskaperna i den mapp du föredrar.

   1. Från **Datakälla** nedrullningsbar meny, välja **Ad Cloud**.

   1. I uttrycksverktyget lägger du till ```d_event``` i fältet Key och ```imp``` i **Värde** fält, markera **Lägg till regel** och spara sedan tecknet.

   ![Skärmbild av ett regelbaserat varumärke](/help/integrations/assets/target-am-trait.png)

1. Ställ in ett testsegment i Audience Manager:

   1. Överst på sidan går du till **Målgruppsdata** > **Traits** och sök efter det fullständiga namnet. Markera kryssrutan intill namnet och klicka sedan på **Skapa segment**.

   1. Namnge segmentet, markera `Ad Cloud` som **Datakälla** och spara sedan segmentet.

      Audience Manager delar automatiskt upp segmentet i en kontrollgrupp som tar emot standardupplevelsen på landningssidan och en testgrupp som fått en personaliserad upplevelse på plats.
   ![Skärmbild av ett testsegment](/help/integrations/assets/target-am-segment.png)

## Steg 3: Ställ in en A/B-testaktivitet i mål

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

I följande anvisningar markeras information som gäller DSP användningsfall. Fullständiga anvisningar finns i &quot;[Skapa ett A/B-test](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html.&quot;

1. [Logga in på Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. Från **Verksamhet** lista, klicka på **Skapa aktivitet** > **A/B-test**.

   ![Skapa en A/B-testaktivitet](/help/integrations/assets/target-create-ab.png)

1. I **Ange aktivitets-URL*** anger du landningssidans URL för testet.

   ![Ange URL-fält för aktivitet](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Du kan använda flera URL:er för att testa en genomskinlig webbplatspost. Mer information finns i &quot;[Flersidig aktivitet](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Du kan enkelt identifiera de översta posterna per sid-URL genom att skapa en [Platsens anmälningsrapport](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) i Analytics.

1. I **Mål** anger du framgångsmåttet för testet.

   >[!NOTE]
   >
   >Se till att [!DNL Analytics] aktiveras som en datakälla i [!DNL Target]och att rätt rapportsvit har valts.

1. Ange **Prioritet** till `High` eller `999` för att förhindra konflikter när användare i testsegmentet får en felaktig upplevelse på plats.

1. Inom **Rapportinställningar** väljer du **Företag** och **Report Suite** är ansluten till ditt DSP.

   Ytterligare rapportips finns i &quot;[Rapportera bästa praxis och felsökning](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. I **Datumintervall** anger du lämpliga start- och slutdatum för testet.

1. Lägg till målgrupper i aktiviteten:

   1. Välj [segment som du tidigare skapat i Audience Manager för att testa genomsiktliga målgrupper](#view-through-framework).

      ![Lägg till målgrupper i aktiviteten](/help/integrations/assets/target-create-ab-audiences.png)

   1. Välj **Webbplatssidor** > **Landningssida** > **Fråga** och ange DSP placeringsnyckel i **Värde** om du vill använda Target-frågesträngsparametrarna för klickbara målgrupper.

      ![Skärmbild av en målgrupp med klickningar](/help/integrations/assets/target-click-audience.jpg)

1. För **Trafikallokeringsmetod**, markera **Manuell (standard)** och dela publiken 50/50.

1. Spara aktiviteten.

1. Använd [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) för att göra konstruktionsändringar i A/B-testsidans mall för landningssidor.

   * Upplevelse A: Redigera inte, eftersom det är standardupplevelsen/kontrollen av landningssidan utan personalisering.

   * Upplevelse B: Använd [!DNL Target] användargränssnitt för att anpassa landningssidans mall baserat på de tillgångar som ingår i testet (t.ex. rubriker, text, knappplacering och kreatörer).
   >[!NOTE]
   >
   >Exempel på användningsområden för kreativa tester kan vara att kontakta ditt kontoteam.

## Steg 4: Konfigurera [!DNL Analytics for Target] Analysis Workspace i [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) är en integrering med flera lösningar som gör att annonsörer kan skapa [!DNL Target] verksamhet som bygger på [!DNL Analytics] konverteringsstatistik och målgruppssegment och sedan mäta resultatet med [!DNL Analytics] som rapportkälla. All rapportering och segmentering för den aktiviteten baseras på [!DNL Analytics] datainsamling.

Mer information om [!DNL Analytics for Target], inklusive en länk till implementeringsanvisningar, se[Adobe Analytics som rapportkälla för Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Konfigurera [!DNL Analytics for Target] Panel

I Analysis Workspace konfigurerar du [!DNL Analytics for Target panel] för att analysera [!DNL Target] aktiviteter och upplevelser. Tänk på följande viktiga pekare och information om dina rapporter.

#### Mått

* Skapa en panel på arbetsytan som är specifik för den Advertising Cloud-kampanj, det paket eller den placering som testet kördes för. Använd sammanfattningsvisualiseringar för att visa Advertising Cloud-värden i samma rapport som Target-testets prestanda.

* Prioritera med hjälp av statistik på plats (som besök och konverteringar) för att mäta prestanda.

* Förstå att aggregerade mediemått från Advertising Cloud (t.ex. visningar, klick och kostnader) inte kan matchas mot Target-statistik.

#### Dimensioner

Följande dimensioner gäller för [!DNL Analytics for Target]:

* **Verksamheter**: A/B-testets namn

* **Målgrupper**: Namn på landningssidans upplevelser som används inom aktiviteten

* **Verksamhetens syfte?** > **Upplevelse**: Aktivitetsnamnet och upplevelsenamnet på samma rad

### Felsökningsanalys för [!DNL Target] Data

Om du inom Analysis Workspace märker att data om aktivitet och upplevelser är minimala eller inte är ifyllda gör du så här:

* Kontrollera att samma SDID (Additional Data ID) används för både Target och Analytics. Du kan verifiera SDID-värdena med [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) på landningssidan som kampanjen driver användarna till.

[SDID-värden (Additional Data ID) i Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* På samma landningssida kontrollerar du att a) värdnamnet som visas i Adobe Debugger under Solutions> Target matchar b) spårningsservern som visas i [!DNL Target] för aktiviteten (under Mål och inställningar > Rapporteringsinställningar).

   [!DNL Analytics For Target] kräver [!DNL Analytics] spårningsserver som ska skickas i samtal från [!DNL Target] till [!DNL Modstats] datainsamlingsserver för Analytics.&lt;!— just &quot;to Analytics?&quot;>

[Värdnamnsvärde i Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Spårningsservervärde i mål](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Ytterligare läsning

* [Integrera Target med Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Beskriver hur du ställer in Target-rapportering i Analysis Workspace.
* [A/B-testöversikt](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beskriver A/B-testaktiviteter, som du kan använda med DSP annonser.
* [Erfarenheter och erbjudanden](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Förklaringar [!DNL Target] verktyg för att avgöra vilket innehåll på plats som DSP testanvändare exponeras för.
* [Signaler, egenskaper och segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definierar några av Audience Manager-verktygen som kan användas för DSP-genomskinlighetstestning.
* [Översikt över Analytics för Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud/integrations/analytics/overview.html) - Vi presenterar Analytics för Advertising Cloud, som gör att ni kan spåra klicknings- och genomskinlighetsinteraktioner på webbplatsen i era Analytics-instanser.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->