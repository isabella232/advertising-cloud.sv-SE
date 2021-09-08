---
title: Varumärkessäkerhet och mediakvalitet
description: Läs mer om varumärkessäkerhet och funktioner för mediekvalitet.
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# Varumärkessäkerhet och mediakvalitet

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP har en uppsättning funktioner för varumärkesskydd som säkerställer att alla era kampanjer når verkliga användare i en varumärkessäker miljö.

Vårt team för bedrägeriövervakning samarbetar nära med branschledande partners, som [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] och [!DNL WhiteOps], för att noggrant kunna strukturera inventeringen på vår plattform. Genom en proaktiv hantering av vårt utbud säkerställer DSP att alla annonsörer på plattformen skyddas från icke-mänsklig trafik (botar, crawler, datacentralstrafik och bedrägeri) och endast levererar i varumärkessäkra sammanhang.

Förutom att tillhandahålla central kvalitetsstyrning anser vi att annonsörerna ska kunna utforma de kontroller som är anpassade till deras varumärke. Adobe Advertising Cloud erbjuder integreringar med [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] och [!DNL Peer39], vilket säkerställer att alla annonsörer kan välja önskad nivå av bedrägeriskydd, kontextuell filtrering och nyckelordsanpassning.

## Advertising Cloud DSP kvalitetsinitiativ

### Lagerverifiering med stöd för [!DNL Ads.txt]

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) är ett initiativ som startades av  [!DNL Interactive Advertising Bureau] ([!DNL IAB]) i juni 2017 för att underlätta en korrekt återgivning av lager på den öppna marknaden och därmed motverka olagliga källor till trafik och domänförfalskning. Deltagande utgivare och distributörer deklarerar offentligt vilka företag som har rätt att sälja sitt digitala lager, och vilken typ av relation det rör sig om, genom att ha en `ads.txt`-sida på domänens högsta nivå (till exempel `example.com/ads.txt`).

DSP stöder [!DNL ads.txt] genom att läsa respektive utgivares `ads.txt`-fil och ger dig möjlighet att köpa endast från verifierade [!DNL ads.txt]-säljare. Genom att matcha de säljare vi ser med åtkomsten av `nytimes.com` till filen `ads.txt` i New York Times kan vi identifiera vilka som är berättigade och vilka som inte är det, och vi blockerar dem om placeringen är konfigurerad att endast köpa från verifierade säljare. <!-- can we actually mention NY Times? -->

Du kan ange standardkontroller för [!DNL ads.txt] för varje annonsörer<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan, om du vill [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) till:

* köpa lager endast från en domäns auktoriserade direktförsäljare

* köpa lager endast från en domäns auktoriserade direktförsäljare och återförsäljare

* prioritera att köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare

* köpa lager från alla säljare

### Övervakning av plattformsbedrägerier

DSP har byggt kraftfulla interna verktyg och system för att hantera bedrägerier på hela vår plattform och samarbetar med ledande branschleverantörer som [!DNL Whiteops] och [!DNL Integral Ad Science].

Dessutom samarbetar Adobe nära med [!DNL IAB] och [!DNL TAG] för att säkerställa en robust, branschstandard blockering av bedrägerier för att skydda våra annonsörer, med verktyg som [!DNL ads.txt] (se föregående avsnitt), listan [!DNL IAB] Bots and Spiders samt IP-listan för [!DNL TAG] Datacenter.

Genom vår flerdimensionella strategi för kvalitet övervakar vårt team avvikelser och ogiltiga trafikmönster, vilket säkerställer mindre än 3 % ogiltig trafik på skyddat lager. Alla lager som är misstänkta - inklusive lager på specifika domäner eller från specifika utgivare eller säljare - blockeras omedelbart på hela plattformen.

### Lagermappning, nivåindelning och kategorisering

Inventariemappning är den detaljerade process för granskning och introduktion som krävs för allt nytt lager innan det läggs till på vår plattform. Denna process är utformad för att säkerställa säkerheten och kvaliteten för alla DSP.

* **Mappning:** Vårt inventeringsteam granskar varje domän noggrant och utvärderar aspekter som:

   * Varumärkessäkerhet

   * Annonstypverifiering

   * Allmänt innehåll, dubblettdomäner och fejkad annonsvisning

* **nivåindelning:** Vi undersöker helhetshur varumärket finns i det övergripande ekosystemet för att klassificera lager i olika nivåer. Du kan [ange dina placeringar](/help/dsp/campaign-management/placements/placement-settings.md) som mål för dessa nivåer för önskad nivå av räckvidd:

   * **[!UICONTROL T1]** - Varumärkesnamn, internationellt identifierbara webbplatser

   * **[!UICONTROL T2]** - Perfekta webbplatser som är aktuella, aktuella, utan användargenererat innehåll och som vanligtvis saknar global igenkänning

   * **[!UICONTROL T3]** - Användargenererat innehåll och nischinnehåll

* **Webbplatskategorisering:** För att säkerställa enkel målinriktning och blockering av innehåll taggar vi varje egenskap med en Advertising Cloud-definierad webbplatskategori baserat på egenskapens innehåll. Du kan [ange eller utesluta dessa webbplatskategorier för varje placering](/help/dsp/campaign-management/placements/placement-settings.md) baserat på placeringsmålen.

### Omfattande stöd för webbplatsblockering

Advertising Cloud DSP tillhandahåller både en global lista över blockerade webbplatser och alternativet att skapa anpassade listor över blockerade webbplatser för annonsörer och konton.

#### Advertising Cloud DSP Global Blocked Sites List

Advertising Cloud DSP har en global lista över blockerade webbplatser som anses osäkra att köra annonser på. Den här listan innehåller webbplatser med stötande innehåll (till exempel hat eller terror) och webbplatser som infekterats med botar, falska förrullningsdomäner, felmatchade domäner och annan bedräglig aktivitet.

Som en del av vårt varumärkessäkerhetsinitiativ för att rota bort aktiviteter som lockar annonsörer, skärs alla webbplatser med hjälp av åtgärderna i listan över blockerade webbplatser. Alla webbplatser som inte godkänns i varumärkessäkerhetskontrollerna läggs till i listan över globalt blockerade platser. Eftersom Advertising Cloud DSP hanterar den här listan dynamiskt kan webbplatserna när som helst fortsätta eller lämna listan baserat på den senaste varumärkessäkerhetsanalysen.

När du tar med en plats i den globalt blockerade platslistan som placeringsmål flaggas platsen med ett rött utropstecken (!). Detta anger att annonser inte kommer att köras på den flaggade webbplatsen.

#### Blockerade webbplatslistor på kontonivå och annonsnivå

Användare kan också underhålla listor över blockerade webbplatser på kontonivå och annonsörnivå<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, som används automatiskt för alla placeringar. Listan Blockerade webbplatser på den lägre nivån används utöver listan Blockerade platser globalt.

## Tredjepartsintegreringar

### Sammanhangsbaserad filtrering

Med kontextuell filtrering kan du rikta eller blockera annonsmöjligheter baserat på kontexten på den sida som annonsen ska användas på. Adobe erbjuder kontextuell filtrering via integrering med ledande leverantörer i branschen: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39]. Exempel på aktuella filter är [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] och [!UICONTROL G-rated Sites].

Du kan ange standardinställningar för kontextuella filter för varje annonsörer<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan välja [att anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### Blockering av bedrägeri före köp

Utnyttja våra integreringar med [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] och [!DNL Peer39] för att blockera icke-mänsklig trafik från era kampanjer. Dessa integreringar ger branschledande funktioner för att blockera före bud för att minimera både allmän och avancerad ogiltig trafik (GIVT och SIVT) i era kampanjer.

Du kan ange standardinställningar för spärrkontroll före köp för varje annonsörer<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, och sedan välja [anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

Mer information om funktionalitet får du om du kontaktar en återförsäljare direkt eller kontaktar din kontoansvarige på Adobe.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoIntegral Ad Science ](/help/dsp/assets/ias-logo.png) ![logoPeer39 logo](/help/dsp/assets/peer39-logo.png)

### Visning före köp {#pre-bid-viewability}

Profilerade visningsfilter som bygger på våra branschledande partners [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) och [!DNL Integral Ad Science] gör det möjligt för annonsörer att se till att deras kampanjer uppfyller de önskade målen för visningsprestanda för video och displayannonser.

Du kan ange standardfilter för visningsbarhet för varje annonsörer<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan välja [att anpassa inställningarna för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma när du använder den här funktionen.

![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoOracle Advertising ](/help/dsp/assets/oracle-advertising-logo.png) ![logoIntegral Ad Science logo](/help/dsp/assets/ias-logo.png)

### Målgruppsanpassning

Med DSP inriktning på ämnen kan du målinrikta eller blockera nyckelordslistor genom att utnyttja våra branschledande sammanhangsberoende partner [!DNL Comscore] och [!DNL Oracle Data Cloud] ([!DNL Grapeshot]).

Ämnesinriktningen hjälper er att se till att era annonser alltid får plats i en miljö som är anpassad efter ert varumärke, oavsett om det handlar om att blockera skadligt innehåll eller säkerställa utgifter i ett sammanhang som garanterar ett bättre resultat.

Ämnesmål kräver att du skapar ämnessegment direkt med [!DNL Comscore] eller [!DNL Grapeshot] (med [!DNL Oracle Data Cloud]). När dessa har skapats i partnerplattformen kan du [ange eller utelämna ett segment-ID i [!UICONTROL  Audience Targeting]-avsnittet för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). Ytterligare avgifter kan tillkomma för den här funktionen.

Kontakta din leverantör eller kontohanteraren för Adobe för att komma igång.

![Comscore ](/help/dsp/assets/comscore-logo.png) ![logoGrapeshot logo](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP samarbetar med [!DNL DoubleVerify] för att kunna erbjuda sin [!DNL Authentic Brand Safety] målinriktningslösning, som gör att ni kan skapa en centraliserad uppsättning varumärkessäkerhetskrav för att nå enhetliga köpplattformar.

När du har byggt ett [!DNL DoubleVerify]-segment för varumärkessäkerhet med den nödvändiga målgruppsanpassningen kan du använda det i DSP för att replikera era era regler för blockering efter bud med förbud i olika webbmiljöer.

Du kan ange ett [!DNL DoubleVerify] segment-ID för varje annonsörer<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> och sedan välja [aktivera eller inaktivera [!UICONTROL Authentic Brand Safety] för varje placering](/help/dsp/campaign-management/placements/placement-settings.md). DSP fakturerar ditt konto för användning av segment-ID.

Om du vill ha mer information om funktionalitet kontaktar du [!DNL DoubleVerify] direkt eller kontaktar din kontoansvarige på Adobe.

![DoubleVerify-logotyp](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
