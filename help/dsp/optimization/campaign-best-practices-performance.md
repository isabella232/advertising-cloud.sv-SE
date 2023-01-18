---
title: Bästa metoder för att konfigurera resultatkampanjer
description: Lär dig de bästa sätten att skapa prestandainriktade kampanjer, som bland annat innehåller placeringar som är optimerade för det lägsta CPA-värdet eller det högsta ROAS-värdet.
feature: DSP Optimization, DSP Best Practices
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Bästa metoder för att konfigurera resultatkampanjer

DSP kan optimera era prestandainriktade kampanjer för praktik med lägsta kostnad per förvärv (CPA) eller högsta avkastningen på annonskostnaderna (ROAS).

Se följande metodtips för prestandakampanjer:

* Steg 1 - Definiera ditt mål
* Steg 2 - Definiera er strategi
* Steg 3 - Skapa paket
* Steg 4 - Skapa placeringsstruktur
* Steg 5 - Använd rätt kreativa resurser

## Steg 1 - Definiera ditt mål

Det är viktigt att förstå om kampanjens mål är att uppnå högsta möjliga avkastning på investerat kapital eller lägsta möjliga CPA. För varje paket i kampanjen anger ni målmålet i enlighet med detta antingen *[!UICONTROL Highest ROAS - Custom Goal]* eller *[!UICONTROL Lowest CPA - Custom Goal]*.

![optimeringsmål](/help/dsp/assets/optimization-goals.png)

Du måste också fastställa vilka framgångshändelser som ska leda till det övergripande målet och skapa anpassade mål utifrån detta. För varje paket anger du ett anpassat mål som ska användas med det övergripande optimeringsmålet för rapportering och algoritmisk optimering med [!DNL Adobe Sensei]. Mer information om hur du skapar anpassade mål finns i [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md).

![anpassade mål](/help/dsp/assets/objective-goals.png)

## Steg 2 - Definiera er strategi

### Nya strategier

Paket med huvudtratt omfattar praktik med mycket bred målinriktning för att nå ut till nya konsumenter.

#### Rekommenderade placeringsstrategier för potentiell kund

* Hitta nya målgrupper som kan konvertera med hjälp av följande taktiker:

   * Look-alike-modellering från en datahanteringsplattform (DMP), som Adobe Audience Manager.
   * Beteendeanpassning med hjälp av data från tredje part.
   * Sammanhangsbaserad målinriktning.
   * Målinriktning för webbplats/kategori.

* Använd RON-målinriktning (Run of Network): Det är viktigt att inkludera en mängd nätverksplaceringar utan målgruppsanpassning och med bred målinriktning på lagret. Detta gör att [!DNL Adobe Sensei] algoritm för att hitta värdefulla användare som kan ha nyare cookies som ännu inte har kategoriserats till en målgrupp.

### Återmarknadsföringsstrategier

Lägre trattpaket innehåller placeringar som riktar sig till användare som redan har varit på annonsörens webbsida eller för vilka annonsören har CRM-data.

#### Rekommenderade placeringsstrategier för återmarknadsföring

* Om annonsören är kund hos Adobe Analytics eller Adobe Audience Manager kan ni skapa förstahandssegment (som besökare på hemsidan, produktsidor eller övergivna varukorgar) och använda dem som placeringsmål i DSP.

* Undvik att tilldela för mycket budget till en målgruppsanpassad placering. Generellt gäller att du budgeterar 30 USD per 1 000 användare per månad.

## Steg 3 - Skapa paket

Det bästa sättet är att skapa separata paket för prospektering med övre kanalen och för återmarknadsföring med lägre kanal. Optimering sker på paketnivå, så att prestandadata från alla placeringar i ett paket samlas. Därför bör du gruppera placeringar i paket med liknande förväntade prestanda.

![exempel på separata paket för prospektering och återmarknadsföring](/help/dsp/assets/p-r.png)

Använd även följande inställningar.

### Mål och budget

* **Pacing &amp; Capping:** Om du vill välja ett mål för CPA- eller ROAS-optimering måste paketnivåpaketeringen användas. Detta garanterar att alla placeringar i paketet optimeras för att distribuera utgifter baserat på prestanda och skalas efter de valda målen.

* **Flygdatum:** (Prospecting packages) När kampanjen pågår längre än 25 dagar använder du [!UICONTROL Activate Custom Flighting] -funktion. Först ställer du in en anpassad flygresa för de första 10 dagarna på ungefär 75 % av den nödvändiga dagliga budgeten för att minska utgifterna under *inlärningsfas*. Ange sedan en andra anpassad flygning för resten av budgeten.

   Om du till exempel har 100 000 USD att spendera på 30 dagar anger du budgeten för Flight 1 (Dagar 1-10) till 25 000 USD (75 % x $100 000/30 dagar = $2 500 per dag). Använd den återstående budgeten på 75 000 USD för Flight 2 (Dagarna 11-30).

* **Budget:** DSP försöker alltid fördela 100 % av paketbudgeten jämnt mellan alla placeringar i ett paket. Om en placering har låga utgifter eller inga utgifter rekommenderar vi att placeringen begränsas så att mer av budgeten kan allokeras till utplaceringar i stor skala. Tillåt 24-48 timmar för budgetändringar att kalibrera.

* **Optimeringsmål:** Använd ett av de två målen för prestandaoptimering, *[!UICONTROL Highest ROAS]* eller *[!UICONTROL Lowest CPA]*, beroende på paketets mål. Dessa mål optimerar paketet automatiskt mot den högsta ROAS- respektive den lägsta CPA-placeringen.

* **Anpassade mål:**
   * Om ett nytt paket har samma mål som ett befintligt paket kan du länka det befintliga paketet så att algoritmen kan använda befintliga maskininlärningsdata.
   * Ange lämplig [!UICONTROL Target CPA] eller [!UICONTROL Target ROAS].

* **Flight Pacing och Intraday Pacing:** Välj *[!UICONTROL Even]* för att maximera era era prestationsmål genom att paketera enhetligt under alla dagar och under hela flygningen.

   >[!CAUTION]
   >
   >Använd *[!UICONTROL FrontLoad]* och *[!UICONTROL Aggressive Front Load]* för flygpaketering och *[!UICONTROL ASAP]* pacing for intraday pacing only when you are fully priority of delivery and cost over performance optimization because those Strategy can impact your önskad performance KPIs.

## Steg 4 - Skapa placeringsstruktur

Mindre är mer. Om du kan ställa in färre än sex placeringar per paket kan den tillgängliga budgeten dynamiskt flyttas till de mest effektiva placeringarna.

Se även till att lägga till varje placering i ett paket med måltypen paket *[!UICONTROL Prospecting]* eller *[!UICONTROL Retargeting]*, beroende på vad som är lämpligt.

Nedan följer de rekommenderade placeringsinställningarna för prestandakampanjer.

### Mål

Du konfigurerar CPA- eller ROAS-optimering på paketnivå (se Steg 3 - Skapa paket), men du kan lägga till ytterligare inställningar på placeringsnivå.

* **Max. bud:**
   * Använd ett lågt maximalt bud ($5) för prospekteringsplaceringar.
   * Använd ett högt maximalt bud ($12) för återmarknadsföring.

* **Föranbudsfilter:** Minimera, eller helst undvik, att ställa in aggressiva förbudsfilter, som förhindrar att placeringen når skala. De bästa sätten är följande:

   * Använd ett (1) pre-bid filter per placering. Flera föranbudsfilter kräver att båda uppfylls, vilket minskar skalan.

   * Överväg att ställa in mindre strikta förbudsfilter om ytterligare målgruppsanpassning (som målgruppsanpassning, geolokalisering och webbplatsanpassning) tillämpas.

Se beskrivningar av när varje pre-bid-filter ska användas på [Pre-Bid-filter på placeringsnivå och Så här använder du dem](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Lager

Om du vill maximera skalan använder du [!UICONTROL Public] (Open Exchange) och [!UICONTROL On Demand] lager.

### Webbplatsmål

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] endast
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Målgruppsanpassning

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * För prospekteringsplaceringar kan du gruppera liknande målgruppskategorier och liknande målgruppsstorlekar på en och samma plats. Gör sedan något av följande beroende på prestanda:
      * Ta bort underpresterande målgrupper från befintliga placeringar.
      * Flytta högpresterande målgrupper till en separat plats för bättre budgetkontroll.
   * För återannonsplaceringar bör du helst inkludera ett målgruppssegment per placering för att enkelt kunna styra anbud och budget.

>[!NOTE]
>
>Dina annonser fungerar bäst om en användare bara kan nås på ett ställe. Betydande överlappning mellan användare på olika platser kan leda till konkurrens, vilket leder till en cykel med ständigt ökande bud, vilket ökar kostnaden per användare. Om du inkluderar flera målgrupper måste du därför se till att de inte består av överlappande användare/målgruppsmedlemmar.
>
> Ni kan undvika överlappande målgrupper genom att skapa era målgrupper i lager så att ni kan utelämna de högre, mer omfattande nivåerna från placeringar efter behov.

* **[!UICONTROL Frequency Capping]:**
   * För prospekteringsplaceringar ska du använda täta frekvensändar (ett intryck per dag).
   * För retargetingplaceringar ställer du in det primära placeringshöljet på 6-10 visningar per dag och det sekundära locket på ett intryck per timme.

* **[!UICONTROL Device Targeting]**:
   * Inkludera [!UICONTROL Computer], [!UICONTROL Mobile]och [!UICONTROL Tablet].
   * Rikta inte [!UICONTROL Firefox] och [!UICONTROL Safari] på grund av begränsningar i målinriktning och mätning. Kontakta [!DNL Adobe] kontoteam för mer information om [!DNL Adobe] stöd för [!DNL Safari ITP].
   * Inaktivera alla webbläsare utom [!UICONTROL Chrome] och [!UICONTROL Edge].

### Varumärkessäkerhet och mediakvalitet

Använda kontextuell filtrering, blockering av bedrägeri före bud och/eller [!UICONTROL Ads.txt] filtreringen begränsar storleken på placeringarna, men använder dem vid behov.

## Steg 5 - Använd rätt kreativa resurser

* Det bästa sättet är att inkludera så många unika annonsstorlekar som möjligt för att maximera räckvidden. Med den universella visningsmallen kan du överföra alla standardstorlekar för visning och visning.
* Kontrollera att alla placeringar innehåller *minst* alla de primära bildskärmsannonserna (300x250, 728x90, 160x600, 300x600, 320x50 och 300x50).
* Uppdatera kreatörerna ofta för att förhindra kreativ trötthet.

>[!MORELIKETHIS]
>
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Pre-Bid-filter på placeringsnivå och Så här använder du dem](optimization-pre-bid-filters.md)
>* [Checklista för kampanjstart](/help/dsp/campaign-management/campaign-launch-checklist.md)

