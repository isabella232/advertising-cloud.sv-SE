---
title: Använda [!DNL Roku] Lager
description: Läs om DSP partnerskap med [!DNL Roku], inklusive lageralternativ, godkända tredjepartsleverantörer av spårning och bästa praxis för [!DNL Roku]-specifika placeringar.
feature: DSP On Demand Inventory, DSP Private Inventory
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Använda [!DNL Roku] Lager

DSP erbjuder unika funktioner för annonsering på [!DNL Roku].

## DSP och [!DNL Roku] Partnerskap

Roku och DSP har ett unikt samarbete som matchar dina [!DNL DSP] målgrupper till [!DNL Roku] ID:n för 1:1 deterministisk målgruppsanpassning på [!DNL Roku] lager.

Utanför Rokus egna DSP (OneView) har Advertising DSP tillgång till dessa målningsfunktioner. DSP är också den enda DSP som har tillstånd att mäta [!DNL Roku] leverans bredvid alla andra TV-lager (med internetanslutning). För [!DNL Roku] delar inte alla standard-RTB- och visningssignaler i pixlar, och ingen annan DSP kan rikta eller mäta sig med den Roku-sålda CTV-leverantören.

## [!DNL Roku] Lageralternativ

Du kan antingen a) konfigurera privata avtal-ID:n direkt med [!DNL Roku] och ange sedan avtals-ID-data i DSP eller b) gå till [!DNL On Demand] Galleri att prenumerera på [!DNL Roku] profiler:

>[!NOTE]
>
>[!DNL Roku] det finns inget tillgängligt lager på öppna marknadsplatser och börser.

* För era privata erbjudanden [konfigurera information om erbjudande-ID:n i DSP](/help/dsp/inventory/deal-id-create.md) och sedan ange &quot;[!UICONTROL Roku Network – Audience]&quot; och &quot;[!UICONTROL The Roku Channel – Audience]&quot; inom [!DNL Roku] placeringar.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Du kan [prenumerera på följande [!DNL Roku] lager inom [!DNL On Demand] Galleri](/help/dsp/inventory/on-demand-inventory-subscribe.md)och därefter rikta in er på något av de godkända erbjudandena inom [!DNL Roku] placeringar:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; för lager i hela [!DNL Roku] ekosystem med partners för premiuminnehåll, som [!DNL The CW], [!DNL ABC]och [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; for [!DNL Roku] App-innehåll som ägs och drivs (O&amp;O).

### Fördelar med att anpassa privata marknadsplatser med [!DNL Roku]

Med privata avtal kan ni anpassa avtalsparametrarna efter era behov.

* **Förhandlat pris:** Arbeta med [!DNL Roku] säljarna för att förhandla och strukturera ett avtal som uppfyller era kampanjbehov.

* **Skalprioritet:** Privata marknadsplatser (PMP) får högre prioritet än alltid pågående avtal (som [!DNL On Demand] erbjudanden).

* **Frekvenshantering:** The [!DNL Roku] Standardfrekvensen för frekvens är en (1) och 30 minuter per användare, men du kan anpassa ändpunkten efter timme, dag, vecka, månad eller hela flygperioden.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Målgruppsinriktning:** [!DNL Roku] målgrupper bygger på [!DNL Roku] enhets- och tv-signaler, data som spåras av [!DNL The Roku Channel] (som tillhörighet till tv-genre, beteende för direktuppspelad TV och kabelabonnemangsstatus) och ytterligare data från [!DNL Roku] CRM-system (customer relationship management).

* **[!DNL Roku]Målgruppsanpassning:** Privata erbjudanden kan rikta in appar efter genre, app-blockeringslista, säsongshändelser och interpoleringshändelser samt program inom [!DNL The Roku Channel] endast.

## [!DNL Roku] Placeringar

DSP kampanjer [skapa [!DNL Roku]-specifika placeringar](/help/dsp/campaign-management/placements/placement-create.md) med placeringstypen &quot;[!UICONTROL Connected TV (Roku)].&quot; Inkludera [!DNL Roku] placeringar i [!DNL Roku]-specifika paket med definierade mål.

Varje [!DNL Roku] placeringen måste ha minst ett mål [!DNL Roku] erbjudande eller källa. Använd DSP unika målgruppsmatchning med [!DNL Roku], innehåller ett eller flera målgruppssegment som kan matchas mot [!DNL Roku] (opted-in) deterministic dataset.

### [!DNL Roku]-Godkända tredjepartsleverantörer av spårning

[!DNL Roku] placeringar kan innehålla händelsepixlar från tredje part och konverteringspixlar från följande leverantörer:  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]och [!DNL Research Now].

### Bästa praxis efter placeringsstrategi

Följande metoder rekommenderas för [!DNL Roku]-specifika placeringar.

Så här maximerar du inkrementell räckvidd:

* Utelämna exponerade målgrupper på [!DNL Roku O&O] genom att utesluta målgrupper som du redan har nått med [!DNL The Roku Channel].

* Utelämna exponerade målgrupper på [!DNL All Roku] genom att utesluta målgrupper som ni redan har nått på andra sidan [!DNL Roku] plattform.

För snabbaste konfiguration:

* Anpassa befintliga, alltid aktiverade erbjudanden för [!DNL The Roku Channel] in [[!DNL On Demand] Lager](/help/dsp/inventory/on-demand-inventory-subscribe.md) för snabb åtkomst [!DNL Roku] egna och styrda inventarier.
* Anpassa befintliga, alltid aktiverade erbjudanden för [!DNL Roku Network] in [[!DNL On Demand] Lager](/help/dsp/inventory/on-demand-inventory-subscribe.md) för att snabbt få skala över [!DNL Roku] plattform.

Till maximal skala:

* Anpassa en [!DNL Roku] privat marknadsplats för prioriterad åtkomst till [!DNL Roku] till ett förhandlat pris.

>[!MORELIKETHIS]
>
>* [Skapa information om avtal-ID manuellt](/help/dsp/inventory/deal-id-create.md)
> * [Prenumerera och begär åtkomst till [!DNL On Demand] Premium Inventory Devices](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Skapa en placering](/help/dsp/campaign-management/placements/placement-create.md)

