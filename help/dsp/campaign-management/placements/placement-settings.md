---
title: Placeringsinställningar
description: Se beskrivningar av tillgängliga placeringsinställningar.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: c2fbaf3381ca4380c18d55931e9f4f662da892af
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# Placeringsinställningar

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Placeringsnamnet.

>[!TIP]
>Använd en namnkonvention som passar ditt sätt att arbeta. En föreslagen namnkonvention är &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** Placeringsstatus: *[!UICONTROL Active]* (standard) eller *[!UICONTROL Paused]*.

>[!TIP]
>Det bästa sättet är att pausa placeringen tills du är redo att starta den.

**[!UICONTROL Details]:** (Skrivskyddat) Den tillämpliga annonstypen, det konto som skapar eller skapade placeringen samt den överordnade kampanjen. Om du vill visa mer information klickar du på **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Öppnar en lista över befintliga placeringsmallar. Så här fyller du i målinriktningsinställningar automatiskt från en mall:

1. Gör något av följande:

   * Om du vill återanvända alla mål från en mall markerar du kryssrutan bredvid mallnamnet.

   * Om du vill återanvända enskilda måltyper från en mall expanderar du mallnamnet och markerar kryssrutan bredvid de måltyper som du vill återanvända.

1. Klicka på **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Endast videoannonsformat) Specifikationerna för annonsens varaktighet och/eller annonsen, som används för att beräkna prognosprojektionen till höger. Fälten varierar beroende på annonstyp.

**[!UICONTROL Placement tags]:** (Valfritt) Nyckelord eller smeknamn som hjälper dig att hitta den här placeringen.

## Mål

**[!UICONTROL Package]:** (Valfritt) Ett paket som placeringen är tilldelad till. Klicka ![Redigera](/help/dsp/assets/edit.png) för att välja och skapa ett befintligt paket eller skapa ett nytt paket. När du tilldelar ett paket placeringen [!UICONTROL Goals] -avsnittet uppdateras med flygdatum, leveransmål och budget från paketet.

**[!UICONTROL Flight Dates]:** Startdatum och slutdatum för placeringen. Godkända annonser kan köras under flygningen när placeringen är aktiv och tilldelats ett aktivt paket eller en aktiv kampanj.

Datumen för paketet (om tillämpligt) eller kampanjen fylls i automatiskt som standard.

>[!NOTE]
>
>* Flightdatumen måste ingå i kampanjflygdatumen och paketflygdatumen.


### Placeringar tilldelade paket med paketnivåpacing

**[!UICONTROL Placement Funding]:** Så här budgeterar du placeringen:

* *[!UICONTROL Optimize based on performance]:* Styr budgeten på paketnivå.
* *[!UICONTROL Set a fixed budget cap]:* Gör att du kan ställa in en daglig, veckovis, månadsvis eller heltidsanställd ersättningsbudget. Ange ett värde och längden (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** Maximalt för 1 000 visningar.

**[!UICONTROL Placement Pre-bid Filters]:** Upp till fem KPI-trösklar (t.ex. ett minsta visbarhetsmått eller klickfrekvens) som måste uppfyllas för att budgivning ska ske. Ni kan använda filter före bud som optimeringsstrategier, men förstå att varje regel kan begränsa de möjligheter som den här placeringen kan erbjuda. Så här lägger du till eller redigerar filter:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Nästa till **[!UICONTROL Only bid if]**, väljer ett mått och anger sedan ett värde.
   * Om du vill ta bort ett filter klickar du på **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

Se beskrivningar av alla filter före bud på &quot;[Pre-Bid-filter på placeringsnivå och Så här använder du dem](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Alla andra placeringar

**[!UICONTROL Budget Goal]:** Bruttobudgetens övre gräns och budgetintervallet (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Placeringar i kampanjer med endast marginalledning) Bruttobudgetens övre gräns och budgetintervallet (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på &quot;[Optimeringsmål och Så här använder du dem](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Målet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Pace on]:** Vilken paketering kommer att baseras på:

* **[!UICONTROL Budget goal]:** (Standard) Det här alternativet ger så många avtryck som möjligt inom den tilldelade budgeten.

* **[!UICONTROL Impressions]:** Det här alternativet ger avtryck tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Maximalt för 1 000 visningar.

**[!UICONTROL Pacing Fill Strategy]:** (Paket med enbart paketnivåpaketering) Så här använder du plats för annonsleveranser:

* *[!UICONTROL Even]:* (Standardvärdet) Gör leveransen enhetlig under varje flygning, med ett mål på 50 % av leveransen under den första halvan av flygningen.

* *[!UICONTROL Frontload]:* Snabbare leverans så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Snabbare leverans så att den är 75-85 % klar halvvägs genom flygningen.

**[!UICONTROL Placement Pre-bid Filters]:** (Valfritt) Upp till fem filter måste uppfyllas för att budgivning ska ske. Du kan använda filter före bud som optimeringsstrategier, men tänk på att varje regel kan begränsa de möjligheter som den här placeringen kan ge. Så här lägger du till eller redigerar filter:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Så här lägger du till ett filter:
      1. Klicka på **[!UICONTROL Add Filter]**.
      1. Nästa till **[!UICONTROL Only bid if]**, väljer ett mått och anger sedan ett värde.
   * Om du vill ta bort ett filter klickar du på **[!UICONTROL X]** i filterraden.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Valfritt) Specifika platser där annonser ska inkluderas eller exkluderas i placeringen. Om du inte anger några platser anges alla platser som mål.

>[!NOTE]
>
>Ort och DMA-platser är inte tillgängliga för Roku-ersättningar.

Så här anger du platser:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Inkludera eller exkludera ett land, en stat, en stad, DMA, ett federala lagstiftningsdistrikt eller ett statligt lagstiftningsdistrikt:
      1. Välj platstyp i den vänstra kolumnen.
      1. (Vid behov) Klicka på en plats för att expandera den.
      1. Klicka på bredvid platsen *[!UICONTROL Include]* för att inkludera det som ett mål eller *[!UICONTROL Exclude]* för att exkludera den som ett mål.
   * Så här söker du efter ett postnummer och inkluderar eller exkluderar alla valda resultat:
      1. Klicka på **[!UICONTROL Search Postal Code]**.
      1. Välj land.
      1. Ange stadsnamnet och klicka sedan på ![Redigera](/help/dsp/assets/search.png).
      1. Klicka på rätt sökresultat.
      1. Klicka *[!UICONTROL Include All]* att inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Så här anger eller klistrar du in postnummer och inkluderar eller exkluderar dem alla:
      1. Klicka på **[!UICONTROL Paste Postal Code]**.
      1. Välj land.
      1. Ange eller klistra in upp till 1 000 postnummer.
Inkludera ett postnummer per rad eller ange flera värden avgränsade med kommatecken eller tabbar.
      1. Klicka *[!UICONTROL Include All]* att inkludera alla platser som mål eller *[!UICONTROL Exclude All]* om du vill utesluta alla platser som mål.
   * Ta bort en plats från [!UICONTROL Included] eller [!UICONTROL Excluded] lista, klicka på **[!UICONTROL X]** bredvid platsen i den högra kolumnen.
1. Klicka på **[!UICONTROL Done]**.

>[!NOTE]
>
>* Alla länder har inte delstat, ort eller postnummer.
>* DMA (angivet marknadsområde), federala lagstiftningsdistrikt och statliga lagstiftningsdistrikt är endast tillgängliga i USA.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Lagerkällor som ska inkluderas eller exkluderas som mål. För de flesta placeringstyper inkluderas alla lagertyper och alla källor för varje typ som standard. För [!DNL Roku] placeringar måste du ange lagertyp och källor. Du kan välja mellan följande lagertyper:

* [!UICONTROL Public]: (Alla placeringstyper utom Roku) Alla öppna börslager som Advertising Cloud har tillgång till. Du kan inkludera och exkludera offentligt lager.

   Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödets namn, flödesknapp eller en vald egenskapstagg.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Befintliga privata erbjudanden (eller befintliga privata) [!DNL Roku] erbjudanden för [!DNL Roku] ) med utgivare som du har konfigurerat i DSP. Du kan inkludera, men inte exkludera, offentligt lager.

   Du kan söka i listan efter nyckelord, nyckel, erbjudande-ID eller egen tagg.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alla [premie, ej garanterad [!UICONTROL On Demand] lager](/help/dsp/inventory/on-demand-inventory-about.md) (eller [!UICONTROL On Demand] [!DNL] Roku erbjuder [!DNL Roku] platser) som du prenumererar på [!DNL DSP]. Du kan inkludera och exkludera [!UICONTROL On Demand] lager.

   Du kan visa listan efter källa eller feed. När du visar listan efter feed kan du söka efter flödesnamn, flödesknapp eller en vald utgivarregion, kategoritagg eller karakteristisk tagg.

Så här anger du målinriktning för lager:

* Om du vill exkludera en lagertyp avmarkerar du kryssrutan bredvid namnet.
* Så här anger du en lagertyp som mål:
   1. Markera kryssrutan bredvid lagertypens namn.
   1. (Valfritt) Ändra källorna till:
      1. Klicka ![Redigera](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] och [!UICONTROL On Demand] lager) Klicka på *[!UICONTROL *View by Source]** eller **[!UICONTROL View by Feed]** om du vill ändra hur källorna visas.
      1. (I tillämpliga fall) Filtrera lagret efter behov.
      1. Ange de källor som ska inkluderas och exkluderas:
         * Ta med en [!UICONTROL Public] eller [!UICONTROL On Demand] källa, klicka på **[!UICONTROL Include]** bredvid källnamnet.
         * Inkludera [!UICONTROL Private] källor:
            * Om du vill inkludera allt lager i ett avtal klickar du **[!UICONTROL Include all]** bredvid avtalsnamnet.
            * Om du vill inkludera en enskild lagerkälla expanderar du avtalsnamnet och klickar sedan på kryssrutan bredvid källnamnet.
         * Så här exkluderar du [!UICONTROL Public] eller [!UICONTROL On ] källa, klicka på **[!UICONTROL Exclude]** bredvid källnamnet.
   1. (Valfritt) Om du vill hämta en CSV-fil med målinformation till hämtningsplatsen för webbläsaren klickar du på **[!UICONTROL Save & Export]**.
   1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>Om du prenumererar på [!UICONTROL On Demand] inventera men inte hitta de utgivare eller avtal som ska målgruppsanpassas och kontrollera sedan status för erbjudandena. Mer information om status finns i [Om [!DNL On Demand] Premiumlager](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Endast videopappningar) Utesluter trafik utanför strömmen.

Annonser utanför webben visas vanligtvis över innehållet som ett popup-fönster eller instoppat i innehåll (i den ursprungliga upplevelsen), i stället för som vanliga videoannonser i en videospelare.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** De typer av trafik som ska mål. Alternativen inkluderar **[!UICONTROL Websites]** och **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Kvaliteten på de webbplatser som ska målas. Nivåerna 1-3 är alla varumärkesskyddade och har godkänts av DSP kartteam.

* *[!UICONTROL Tier 1]:* Premium-sajter och -tillämpningar som är nationellt igenkännbara.
* *[!UICONTROL Tier 2]:* Målgrupper, nivå 1 samt webbplatser och applikationer som är mindre kända än nivå 1.
* *[!UICONTROL Tier 3]:* Målgrupper för Tiers 1-2 samt webbplatser och applikationer som är lagliga och varumärkessäkra och som passar en nischmålgrupp. Använd nivå 3 för målgruppsköp för räckvidd eller data.
* *[!UICONTROL All Sites]:* Målenheterna nivå 1-3 och nytt lager som inte har säkerhetskontrollerats eller kategoriserats, som du kan använda för att nå.

>[!NOTE]
>
>Lagret är specifikt för annonsenheterna i placeringen.

>[!TIP]
>
>För prestandakampanjer är det bästa sättet att välja *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Valfritt) tillgänglig när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatskategorier i de valda webbplatsnivåerna som antingen ska inkluderas eller exkluderas (men inte båda) som mål. Välj från lodräta webbplatslistor som Advertising Cloud har mappat baserat på webbplatsens ämne:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange de webbplatskategorier som ska inkluderas eller exkluderas:
   * Så här tar du med webbplatskategorier:
      1. Klicka på **[!UICONTROL Include categories]**.
      1. Markera kryssrutan bredvid varje kategori som du vill använda som mål.
   * Så här exkluderar du webbplatskategorier:
      1. Klicka på **[!UICONTROL Exclude categories]**.
      1. Markera kryssrutan bredvid varje kategori som ska uteslutas.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformation till hämtningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Valfritt) tillgänglig när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL Off]*) Webbplatser som ska uteslutas. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Välj de webbplatser som ska uteslutas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid den.
         * (När fler än 50 resultat är tillgängliga) Om du vill utesluta de första 50 resultaten klickar du på **[!UICONTROL Exclude these 50]**. Om du vill utesluta alla sökresultat klickar du på **[!UICONTROL Exclude these \<*NN *\>]**.
   * Så här anger du domännamn:
      1. Klicka på **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Exclude All]**.
1. Klicka **[!UICONTROL Done]** när du är klar.

>[!NOTE]
>
>* Listor över blockerade webbplatser på kontonivå och annonsörnivå används också, utöver Advertising Cloud DSP [globalt blockerad webbplatslista](/help/dsp/introduction/features/brand-safety-media-quality.md), som innehåller webbplatser som inte anses säkra för annonser.
>* Listor med blockerade webbplatser åsidosätter alltid målwebbplatslistor. Om en placering båda utesluter och innehåller samma mål för en annons, utesluts målet.


**[!UICONTROL Language]:** (Valfritt) Ett enda målspråk.

**[!UICONTROL Site List Preview]:** (Skrivskyddat) Alla målwebbplatser och blockerade webbplatser för placeringen.

Du kan också exportera listan med målwebbplatser och blockerade webbplatser som en kommaavgränsad värdefil (CSV). Om du vill exportera listan klickar du på **[!UICONTROL Export full site list]** och sedan öppna eller spara filen enligt webbläsarens normala procedur.

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** Gör att du bara kan ange specifika webbplatser som mål. När du aktiverar det här alternativet inaktiveras de andra alternativen för webbplatsanpassning.

**[!UICONTROL Sites]:** (Tillgängligt när **[!UICONTROL Paste list of targeted sites]** är *[!UICONTROL On]*) Webbplatser att rikta sig till. Du kan antingen söka efter och välja platser eller ange eller klistra in domännamn:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange platserna:
   * Så här söker du efter en plats:
      1. Klicka på **[!UICONTROL Search]**.
      1. Ange ett nyckelord, välj en webbplatsnivå och/eller välj en platskategori.
      1. Markera de webbplatser som ska inkluderas i sökresultaten:
         * Om du vill utesluta en enskild plats markerar du kryssrutan bredvid den.
         * (När fler än 50 resultat är tillgängliga) Om du vill inkludera de första 50 resultaten klickar du på **[!UICONTROL Include these 50]**. Om du vill inkludera alla sökresultat klickar du på **[!UICONTROL Include these \<*NN *\>]**.
   * Så här anger du domännamn:
      1. klicka **[!UICONTROL Paste]**.
      1. Ange ett eller flera domännamn på separata rader.
      1. Klicka på **[!UICONTROL Include All]**.
1. Klicka på **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alla målgrupper för placeringen, inklusive [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för alla valda segment och sparade målgrupper visas också. Du kan välja en befintlig målgrupp, skapa en ny målgrupp som du kan återanvända senare eller välja specifika målgruppssegment:

* Om du vill välja en befintlig målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Included Audiences]och sedan välja målgrupp.
* Om du vill skapa en ny målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Included Audiences]och sedan markera **[!UICONTROL + Create Audience]**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md), med början från steg 3.
* Om du vill markera specifika målgruppssegment klickar du på **[!UICONTROL Select segments for this placement only]**. Välj segmentlogik, för instruktioner, se steg 6 i &quot;[Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md).&quot; När du är klar klickar du på **Spara**.

**[!UICONTROL Excluded Audiences]:** Alla målgrupper som ska uteslutas för placeringen, inklusive målgrupper med [tredjepartssegment, förstapartssegment, Adobe-segment, anpassade segment och sparade målgrupper](/help/dsp/audiences/audience-settings.md). Den totala och aktiva borttagna dubblettstorleken för målgrupper visas också för alla uteslutna målgrupper. Du kan välja en befintlig målgrupp eller skapa en ny som du kan återanvända senare:

* Om du vill välja en befintlig målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Excluded Audiences]och sedan välja målgrupp.
* Om du vill skapa en ny målgrupp klickar du på ![Välj](/help/dsp/assets/chevron-down.png) nästa [!UICONTROL Excluded Audiences]och sedan markera **+ Skapa publik**. Instruktioner finns i [Skapa en återanvändbar publik](/help/dsp/audiences/reusable-audience-create.md), med början från steg 3.

**[!UICONTROL Cross Device Targeting]:** (Tillgängligt när du markerar minst ett segment eller en målgrupp och [kampanjen är konfigurerad för personbaserad målinriktning på olika enheter](/help/dsp/campaign-management/campaigns/campaign-settings.md). Gör att du kan utöka målanpassningen för alla kända enheter (enligt enhetsdiagrammet som anges i kampanjinställningarna), även enheter som inte finns i de angivna segmenten. Avgifterna kan tillkomma beroende på vilket diagram som har angetts för kampanjen. Enhetsdiagramdata är för närvarande bara tillgängliga i Nordamerika.

**[!UICONTROL Placement Cap]:** (Valfritt) Antalet gånger en unik enhet eller person (beroende på den angivna [!UICONTROL Cross Device Level]) kommer att få annonser från sin placering. Alternativen inkluderar *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Secondary Cap]:** (Valfritt) tillgängligt när du inkluderar ett numeriskt [!UICONTROL Placement Cap]) En ytterligare begränsning inom gränserna för det primära placeringsskyddet. Välj antalet visningar och tidsperioden (t.ex. 3 per 12 timmar).

**[!UICONTROL Day Parting]:** (Valfritt) Specifika veckodagar och klockslag då annonserna kan köras. Så här anger du dagdelningsintervall:
1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Välj tillämplig tidszon.
1. Ange intervallen:
   * Om du vill välja ett förinställt intervall klickar du på någon av intervallknapparna. Alternativen är *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*, eller *[!UICONTROL Prime]* (primetime).
   * Om du vill markera ett intervall manuellt klickar du inuti en cell och väljer intervallet genom att dra.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Valfritt) som är tillgängliga för annonsörer som konfigurerats med [!DNL Comscore] och [!DNL Grapeshot] segment) Specifika segmentnamn eller ID:n från [!DNL Comscore] och [!DNL Grapeshot] som ska inkluderas som mål. Ytterligare avgifter kan tillkomma för den här funktionen. Om du vill aktivera den här funktionen och konfigurera ämnessegment kontaktar du [!DNL Adobe] kontoteam.

Så här anger du målinriktning:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange de segment som ska målas:
   1. Välj partner i den vänstra kolumnen (*[!UICONTROL Comscore]* eller *[!UICONTROL Grapeshot]*).
   1. Ange segmentnamnen eller segmentens ID:n i indatafältet.
1. (Valfritt) Om du vill hämta en CSV-fil med ämnesinformationen till din webbläsares hämtningsplats klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

>[!TIP]
>
>* Ämnesinriktningen begränsar det lager där placeringen kan offereras, så använd Ämnesanpassning för endast en liten andel av hela köpet.
>
>* Ställ in negativ målgruppsanpassning inom segmentet på [!DNL Comscore] eller [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Valfritt) Specifik enhetsinformation, inklusive enhetstyper, tillverkare, operativsystem, webbläsare och anslutningstyper, som ska inkluderas och exkluderas som mål. Så här anger du målinriktning:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange den enhetsinformation som ska inkluderas och exkluderas:
   1. Välj kategori i den vänstra kolumnen.
   1. Ange mål:
      * Om du vill ta med ett värde klickar du på **[!UICONTROL Include]** bredvid värdenamnet.
      * Om du vill exkludera ett värde klickar du **[!UICONTROL Exclude]** bredvid värdenamnet.
1. (Valfritt) Om du vill hämta en CSV-fil med målinformation för enheten till nedladdningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Valfritt) Specifika internetleverantörer (ISP) kan antingen inkludera eller exkludera (men inte båda) som mål. Så här anger du ISP-mål:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Ange vilka Internet-leverantörer som ska inkluderas eller exkluderas:
   * Inkludera Internet-leverantörer:
      1. Klicka på **[!UICONTROL Include ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska användas som mål.
   * Så här exkluderar du Internet-leverantörer:
      1. Klicka på **[!UICONTROL Exclude ISPs]**.
      1. (Valfritt) Filtrera listan efter nyckelord.
      1. Markera kryssrutan bredvid varje Internet-leverantör som ska uteslutas.
1. (Valfritt) Om du vill ladda ned en CSV-fil med information om internetleverantörens mål till nedladdningsplatsen för webbläsaren klickar du på **[!UICONTROL Export]**.
1. Klicka på **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Typer av [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39] kontextuella filter som ska användas. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av lagerkontext som ska blockeras som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]:

   * **Målplatser som är:** (Valfritt) En eller flera typer av lagerattribut att rikta som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL ComScore]:

   * **Blockera webbplatser som är:** (Valfritt) En eller flera typer av lagerattribut att blockera som standard. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Valfritt) Graden av vuxeninnehåll som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Alcohol Content]:** (Valfritt) Den alkoholhalt som annonser ska blockeras för som standard: *[!UICONTROL Do Not Block]* (standard), *[!UICONTROL Standard]*, eller *[!UICONTROL Strict]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Pre-bid fraud blocking]:** Typer av webbplatser som ska blockeras baserat på bedräglig trafik och misstänkta aktiviteter som mäts via [!DNL DoubleVerify], [!DNL Integral Ad Science]och [!DNL Peer39]. Standardvärdena på annonsörnivå väljs för nya placeringar, men du kan ändra inställningarna:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Som standard blockeras all 100 % ogiltig trafik, inklusive trafik på överbelastade enheter, för nya placeringar. Ytterligare avgifter kan tillkomma.

   * **[!UICONTROL Also block sites with]:** (Valfritt) Ytterligare en nivå av bedrägeri och ogiltig trafik som gör att DSP blockerar annonser som standard:  *[!UICONTROL None]* (standard, som inte blockerar ytterligare trafik), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*, eller *[!UICONTROL >25% Average Fraud/IVT levels]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En eller flera typer av bedrägeri som gör att DSP blockerar annonser som standard: *[!UICONTROL Fraud]* (som blockerar alla webbplatser med bedrägeri), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* och/eller *[!UICONTROL Fraud: Zero Ads]*. Ytterligare avgifter kan tillkomma.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Valfritt) En typ av misstänkt webbplats- eller appaktivitet som gör att DSP blockerar annonser som standard: *[!UICONTROL None]* (standard, som inte blockerar annonser som baseras på misstänkt aktivitet), *[!UICONTROL Suspicious Activity - High Risk]*, eller *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Ytterligare avgifter kan tillkomma.

**[!UICONTROL Ads.txt filtering]:**

Vilken nivå av [Ads.txt](https://iabtechlab.com/ads-txt-about/) förfiltrera genom att utnyttja varje utgivares lista över auktoriserade digitala säljare. Standardvärdet på annonsörnivå är valt för nya placeringar, men du kan ändra inställningarna:

* *[!UICONTROL Opt out of ads.txt (default)]*: För att köpa lager från alla säljare.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Att prioritera inköp av lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare och återförsäljare.
* *[!UICONTROL Ads.txt sellers only]*: Att endast köpa lager från en domäns auktoriserade direktförsäljare.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Annonsörer konfigurerade med [!UICONTROL DoubleVerify Authentic Brand Safety] option) Aktiverar [!DNL DoubleVerify Authentic Brand Safety], som blockerar visningar efter bud med hjälp av anpassade varumärkessäkerhetsregler som konfigurerats för det angivna segment-ID:t. DSP fakturerar ditt konto för användning av det segment-ID som anges i annonserarens inställningar.

## [!UICONTROL Tracking]

>[!NOTE]
>
>([!DNL Roku] placements) Tredjepartsleverantörer för spårning som godkänts av [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]och [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Valfritt) Pixlar för händelsespårning från tredje part som bifogas som standard till alla nya annonser i placeringen. Så här anger du händelsepixlar:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en ny pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Pixel name]:** Pixelnamnet; får innehålla högst 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Pixel event fires on]:** Den händelse som utlöser pixeln som utlöses. Vilka händelser som är tillgängliga varierar beroende på annonstyp.
         * **[!UICONTROL Pixel type]:** Om pixeln är en *[!UICONTROL IMG URL]* (1 × 1 pixelbildfil), *[!UICONTROL HTML]*, eller *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Pixelbildens URL.
      1. Klicka på **[!UICONTROL Create and attach]**.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Valfritt) Pixlar för konverteringsspårning som bifogas som standard till alla nya annonser i placeringen. Så här anger du konverteringspixlar:

1. Klicka ![Redigera](/help/dsp/assets/edit.png).
1. Gör något av följande:
   * Om du vill markera en befintlig pixel markerar du kryssrutan på pixelraden.
   * Så här skapar du en ny pixel:
      1. Klicka på **[!UICONTROL Create]**.
      1. Ange följande information:
         * **[!UICONTROL Conversion pixel name]:** Pixelnamnet; får innehålla högst 500 tecken. Använd ett namn som gör det enkelt att identifiera pixeln.
         * **[!UICONTROL Conversion category]:** Typ av konvertering.
         * **[!UICONTROL Impression conversion window]:** Det antal dagar efter det att ett annonsintryck inträffar där intrycket kan tillskrivas en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Click conversion window]:** Det antal dagar efter att ett annonsklick inträffar där klickningen kan kopplas till en konvertering. Standardvärdet är 30 dagar.
         * **[!UICONTROL Notes]:** (Valfritt) En beskrivning eller annan information om pixeln.
      1. Klicka på **[!UICONTROL Create and attach]**.
      1. Implementera konverteringspixeln på relevanta webbsidor:
         1. På huvudmenyn går du till **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. Klicka på **[!UICONTROL edit]**.
         1. Kopiera värdena i [!UICONTROL HTML Tag] och [!UICONTROL Flash Tag] fält, efter behov, som ska tillhandahållas annonsören eller webbplatskontakten.

            Annonsörens IT-avdelning eller annan grupp kan behöva schemalägga, eller få information om, tagghanteringen.
   1. Klicka på **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad per tusen visningar. Standardvärdet på paketnivå används automatiskt för nya placeringar, om det är tillämpligt, såvida du inte anger ett annat värde.

>[!NOTE]
>
>Faktureringsbara avgifter återspeglas i [!UICONTROL Net CPM] mätvärden.

>[!MORELIKETHIS]
>
>* [Om Platshantering](placement-about.md)
>* [Skapa en placering](placement-create.md)
>* [Redigera en placering](placement-edit.md)
>* [Kortkommandon](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Vanliga frågor om kampanjhantering](/help/dsp/campaign-management/campaign-management-faq.md)

