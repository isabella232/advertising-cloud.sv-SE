---
title: Varumärkessäkerhet och mediakvalitet
description: Läs mer om varumärkessäkerhet och funktioner för mediekvalitet.
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 0%

---

# Varumärkessäkerhet och mediakvalitet

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP innehåller en uppsättning varumärkesskyddsfunktioner som säkerställer att alla era kampanjer når verkliga användare i en varumärkessäker miljö.

Vårt team för bedrägeriövervakning samarbetar nära med branschledande partner, som [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]och [!DNL WhiteOps], för att noggrant strukturera inventeringen på vår plattform. Genom en proaktiv hantering av vårt utbud säkerställer DSP att alla annonsörer på plattformen skyddas från icke-mänsklig trafik (botar, crawler, datacentralstrafik och bedrägeri) och endast levererar i varumärkessäkra sammanhang.

Förutom att tillhandahålla central kvalitetsstyrning anser vi att annonsörerna ska kunna utforma de kontroller som är anpassade till deras varumärke. DSP erbjuder integrering med [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]och [!DNL Peer39], som säkerställer att varje annonsör kan välja önskad nivå på bedrägeriskyddet, kontextuell filtrering och målgruppsanpassning för nyckelord.

## Kvalitetsinitiativ

### Lagerverifiering med [!DNL Ads.txt] Support

[[!DNL Ads.txt], som står för [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) är ett initiativ som [!DNL Interactive Advertising Bureau] ([!DNL IAB]) i juni 2017 för att underlätta en korrekt återgivning av lagret på den öppna marknaden och därmed motverka olagliga källor till trafik och domänförfalskning. Deltagande utgivare och distributörer offentliggör de företag som är auktoriserade att sälja sitt digitala lager, och vilken typ av relation det rör sig om, genom att upprätthålla en `ads.txt` på domänens översta nivå (t.ex. `example.com/ads.txt`).

DSP [!DNL ads.txt] genom att läsa varje utgivares `ads.txt` och ger dig möjlighet att köpa endast från verifierad [!DNL ads.txt] säljare. Genom att matcha säljarna ser vi till exempel åtkomst `nytimes.com` till New York Times&#39; `ads.txt` kan vi identifiera vilka som är berättigade och vilka som inte är det, och vi kommer att blockera förbrytarna om placeringen är konfigurerad att endast köpa från verifierade säljare. <!-- can we actually mention NY Times? -->

Du kan ange standard [!DNL ads.txt] kontroller för varje annonsör<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->och sedan valfritt [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) till:

* köpa lager endast från en domäns auktoriserade direktförsäljare

* köpa lager endast från en domäns auktoriserade direktförsäljare och återförsäljare

* prioritera att köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare

* köpa lager från alla säljare

### Övervakning av plattformsbedrägerier

DSP har byggt kraftfulla interna verktyg och system för att hantera bedrägerier på hela vår plattform, och samarbetar med ledande branschleverantörer som [!DNL Whiteops] och [!DNL Integral Ad Science].

Dessutom samarbetar Adobe nära med [!DNL IAB] och [!DNL TAG] för att säkra en stabil, branschledande blockering av bedrägerier för att skydda våra annonsörer, med hjälp av verktyg som [!DNL ads.txt] (se föregående avsnitt), [!DNL IAB] Listan med spindlar och [!DNL TAG] IP-lista för datacenter.

Genom vår flerdimensionella strategi för kvalitet övervakar vårt team avvikelser och ogiltiga trafikmönster, vilket säkerställer mindre än 3 % ogiltig trafik på skyddat lager. Alla lager som är misstänkta - inklusive lager på specifika domäner eller från specifika utgivare eller säljare - blockeras omedelbart på hela plattformen.

### Lagermappning, nivåindelning och kategorisering

Inventariemappning är den detaljerade process för granskning och introduktion som krävs för allt nytt lager innan det läggs till på vår plattform. Denna process är utformad för att säkerställa säkerheten och kvaliteten för alla DSP.

* **Mappning:** Inventeringsteamet granskar varje domän noggrant och utvärderar till exempel:

   * Varumärkessäkerhet

   * Annonstypverifiering

   * Allmänt innehåll, dubblettdomäner och fejkad annonsvisning

* **Niering:** Vi undersöker helhetsvarumärkets närvaro i det övergripande ekosystemet för att klassificera lager i olika nivåer. Du kan [rikta in dina placeringar](/help/dsp/campaign-management/placements/placement-settings.md) till dessa nivåer för önskad nivå av räckvidd:

   * **[!UICONTROL T1]** - Varumärkesnamn, internationellt identifierbara webbplatser

   * **[!UICONTROL T2]** - Perfekta webbplatser som är aktuella, aktuella, utan användargenererat innehåll och som vanligtvis saknar global igenkänning

   * **[!UICONTROL T3]** - Användargenererat innehåll och nischinnehåll

* **Webbplatskategorisering:** För att säkerställa enkel målinriktning och blockering av innehåll taggar vi varje egenskap med en DSP definierad webbplatskategori baserat på egenskapens innehåll. Du kan [mål eller utelämna dessa webbplatskategorier för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) utifrån placeringsmålen.

### Omfattande stöd för webbplatsblockering

DSP innehåller både en global lista över blockerade webbplatser och alternativet att skapa anpassade listor över blockerade webbplatser för annonsörer och konton.

#### DSP Globalt blockerade webbplatser {#global-blocked-sites}

DSP har en global lista över webbplatser som blockerats och som anses osäkra att köra annonser på. Den här listan innehåller webbplatser med stötande innehåll (till exempel hat eller terror) och webbplatser som infekterats med botar, falska förrullningsdomäner, felmatchade domäner och annan bedräglig aktivitet.

Som en del av vårt varumärkessäkerhetsinitiativ för att rota bort aktiviteter som lockar annonsörer, skärs alla webbplatser med hjälp av åtgärderna i listan över blockerade webbplatser. Alla webbplatser som inte godkänns i varumärkessäkerhetskontrollerna läggs till i listan över globalt blockerade platser. Eftersom DSP hanterar den här listan dynamiskt kan sajterna när som helst gå vidare på eller bort från listan baserat på den senaste varumärkessäkerhetsanalysen.

När du tar med en plats i den globalt blockerade platslistan som placeringsmål flaggas platsen med ett rött utropstecken (!). Detta anger att annonser inte kommer att köras på den flaggade webbplatsen.

>[!NOTE]
>
>Du kan också kringgå den globala listan över blockerade webbplatser för standarddisplayannonser som är kopplade till en betrodd privat affär genom att aktivera[!UICONTROL Allow unscreened sites]&quot; i [placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md). Om det behövs kan [!DNL Adobe] kontoteamet kan även inaktivera webbplatsblockering för ett offentligt (auktionsnivå) erbjudande i utgivarinställningarna för avtalet.

#### Blockerade webbplatslistor på kontonivå och annonsnivå

Användare kan också hantera blockerade webbplatser på kontonivå och annonsörnivå<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, som används automatiskt för alla placeringar. Listan Blockerade webbplatser på den lägre nivån används utöver listan Blockerade platser globalt.

## Tredjepartsintegreringar

### Sammanhangsbaserad filtrering

Med kontextuell filtrering kan du rikta eller blockera annonsmöjligheter baserat på kontexten på den sida som annonsen ska användas på. Adobe erbjuder kontextuell filtrering via integrering med ledande leverantörer i branschen: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39]. Exempel på aktuella filter är [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]och [!UICONTROL G-rated Sites].

Du kan ange standardinställningar för kontextuella filter för varje annonsör<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->och sedan valfritt [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![Comscore logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png) ![Peer39, logotyp](/help/dsp/assets/peer39-logo.png)

### Blockering av bedrägeri före köp

Utnyttja våra integreringar med andra leverantörer [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39] för att blockera icke-mänsklig trafik från era kampanjer. Dessa integreringar ger branschledande funktioner för att blockera före bud för att minimera både allmän och avancerad ogiltig trafik (GIVT och SIVT) i era kampanjer.

Du kan ange standardkontroller för spärra/knip för bedrägeri före bud för varje annonsörer<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->och sedan valfritt [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

Mer information om funktionalitet får du om du kontaktar en återförsäljare eller kontaktar [!DNL Adobe] kontoteam.

![Comscore logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png) ![Peer39, logotyp](/help/dsp/assets/peer39-logo.png)

### Visning före köp {#pre-bid-viewability}

Visningsfilter som tillhandahålls av våra branschledande partners [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]), och [!DNL Integral Ad Science] gör det möjligt för annonsörer att se till att deras kampanjer uppfyller de prestandamål de vill ha för visning i alla videoklipp och displayannonslager.

Du kan ange standardfilter för visning för varje annonsörer<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->och sedan valfritt [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising logo](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science logo](/help/dsp/assets/ias-logo.png)

### Målgruppsanpassning

DSP kan ni rikta in er på eller blockera nyckelordslistor genom att utnyttja våra branschledande sammanhangsbaserade partner [!DNL Comscore] och [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). Ämnesinriktningen hjälper er att se till att era annonser alltid får plats i en miljö som är anpassad efter ert varumärke, oavsett om det handlar om att blockera skadligt innehåll eller säkerställa utgifter i ett sammanhang som garanterar ett bättre resultat.

För målinriktning mot ämnen måste du skapa anpassade ämnessegment direkt med [!DNL Comscore] eller [!DNL Grapeshot] (med [!DNL Oracle Data Cloud]). När de har skapats på partnerplattformen kan du [mål eller exkludera ett segment-ID i [!UICONTROL Audience Targeting] sektion för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma för den här funktionen.

Så här skapar du anpassade ämnessegment:

* Skapa en [!DNL Comscore] konto och skapa anpassade segment, kan du begära inloggning för [!DNL Activation Segment Manager] på [https://agents.comscore.com](https://agents.comscore.com). Se [[!DNL Comscore] hjälpcenter](https://comscoreactivation.zendesk.com/hc/) om du vill ha fullständiga anvisningar om hur du ställer in anpassade segment. Avgifter för anpassade segment visas i [!DNL Segment Manager] när du skapar dem.

* Så här kommer du igång med [!DNL Oracle Data Cloud], kontakt [!DNL Oracle Data Cloud] eller [!DNL Adobe] kontoteam.

![Comscore logo](/help/dsp/assets/comscore-logo.png) ![Grapeshot logo](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP har samarbetat med [!DNL DoubleVerify] att erbjuda [!DNL Authentic Brand Safety] målgruppslösning, som gör att ni kan skapa en centraliserad uppsättning varumärkessäkerhetskrav för att nå ut till alla era inköpsplattformar för att vara enhetliga.

När du har byggt en [!DNL DoubleVerify] varumärkessäkerhetssegmentet med den nödvändiga målgruppsanpassningen kan ni använda det i DSP för att replikera era era regler för postbud med prebid-blockering i olika webbmiljöer.

Du kan ange en [!DNL DoubleVerify] segment-ID för varje annonsör<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->och sedan valfritt [aktivera eller inaktivera [!UICONTROL Authentic Brand Safety] för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). DSP fakturerar ditt konto för användning av segment-ID.

Mer information om funktioner finns i [!DNL DoubleVerify] direkt eller kontakta [!DNL Adobe] kontoteam.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
