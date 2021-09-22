---
title: Använda [!DNL Roku] Lager
description: 'Lär dig mer om DSP partnerskap med  [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]-specifika ersättningar. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Använda [!DNL Roku]-lager

Advertising Cloud DSP har unika funktioner för annonsering på [!DNL Roku].

## Advertising Cloud DSP och [!DNL Roku] Partnership

Roku och Advertising Cloud DSP har ett unikt partnerskap som matchar dina [!DNL DSP]-målgrupper med [!DNL Roku] ID:n för 1:1 deterministisk målgruppsanpassning på [!DNL Roku]-lager.

Utanför Rokus egna DSP (OneView) har Advertising Cloud DSP enda åtkomst till dessa målningsfunktioner. Advertising Cloud DSP är också den enda DSP som har tillstånd att mäta [!DNL Roku]-leveranser bredvid alla andra TV-lager med anslutning (CTV). Eftersom [!DNL Roku] inte delar alla standard-RTB och visningssignaler för pixlar, kan ingen annan DSP rikta eller mäta sig över den Roku-sålda CTV-leverantören.

## [!DNL Roku] Lageralternativ

Du kan antingen a) konfigurera privata avtal-ID:n direkt med [!DNL Roku] och sedan ange data för avtals-ID i DSP eller b) gå till [!DNL On Demand]-galleriet för att prenumerera på [!DNL Roku]-profiler:

>[!NOTE]
>
>[!DNL Roku] det finns inget tillgängligt lager på öppna marknadsplatser och börser.

* För dina privata avtal ska du [ange information om erbjudande-ID:n i DSP](/help/dsp/inventory/deal-id-create.md) och sedan ange [!UICONTROL Roku Network – Audience] och [!UICONTROL The Roku Channel – Audience] som mål på [!DNL Roku]-placeringar.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Du kan [prenumerera på följande [!DNL Roku] inventory within the [!DNL On Demand] galleri](/help/dsp/inventory/on-demand-inventory-subscribe.md) och sedan göra något av de godkända avtalen på [!DNL Roku]-platser:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; för lager i [!DNL Roku]-ekosystemet med partners för premiuminnehåll, som [!DNL The CW], [!DNL ABC] och [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; för [!DNL Roku] ägt och styrt (O&amp;O) appinnehåll.

### Fördelar med att anpassa privata marknadsplatser med [!DNL Roku]

Med privata avtal kan ni anpassa avtalsparametrarna efter era behov.

* **Förhandlat pris:** Samarbeta med  [!DNL Roku] säljteamet för att förhandla och strukturera ett avtal som uppfyller era kampanjbehov.

* **Skalprioritet:** Privata marknadsplatser (PMP) får högre prioritet än alltid gällande avtal (t.ex.  [!DNL On Demand] avtal).

* **Frekvenshantering:** Standardfrekvensen för  [!DNL Roku] frekvens är en (1) och per 30 minuter per användare, men du kan anpassa hatten efter timme, dag, vecka, månad eller hela flygperioden.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Datamål:** [!DNL Roku] målgrupper byggs av  [!DNL Roku] enhets- och tv-signaler, data spåras av  [!DNL The Roku Channel] (t.ex. tv-genre, direktuppspelad TV-funktion och kabelabonnemangsstatus) samt ytterligare data från CRM-systemet ( [!DNL Roku] customer relationship management).

* **[!DNL Roku]Målgruppsanpassning:** Privata avtal kan rikta in appar efter genre, appapplikationer med blockeringslista, säsongs- och interpoleringshändelser och program  [!DNL The Roku Channel] endast visas inom dessa områden.

## [!DNL Roku] Placeringar

I DSP kampanjer ska du [skapa [!DNL Roku]-specifika placeringar](/help/dsp/campaign-management/placements/placement-create.md) med placeringstypen &quot;[!UICONTROL Connected TV (Roku)].&quot; Du inkluderar [!DNL Roku]-placeringar i [!DNL Roku]-specifika paket med definierade mål.

Varje [!DNL Roku]-placering måste ha minst en [!DNL Roku]-affär eller -källa som mål. Om du vill utnyttja DSP unika målgruppsmatchning med [!DNL Roku] ska du ta med ett eller flera målgruppssegment som kan matchas mot [!DNL Roku] (opted-in)-deterministisk datamängd.

### [!DNL Roku]-Godkända tredjepartsleverantörer av spårning

[!DNL Roku] placeringar kan innehålla händelsepixlar från tredje part och konverteringspixlar från följande leverantörer:   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal]  [!DNL Oracle]  [!DNL Placed]  [!DNL Polk]  [!DNL Research Now]¥,¥,¥ och¥.

### Bästa praxis efter placeringsstrategi

Nedan följer de rekommenderade metoderna för [!DNL Roku]-specifika ersättningar.

Så här maximerar du inkrementell räckvidd:

* Utelämna exponerade målgrupper på [!DNL Roku O&O] genom att utesluta målgrupper som du redan har nått med [!DNL The Roku Channel].

* Utelämna exponerade målgrupper på [!DNL All Roku] genom att utesluta målgrupper som du redan har nått över [!DNL Roku]-plattformen.

För snabbaste konfiguration:

* Rikta in er på befintliga, alltid aktiverade erbjudanden för [!DNL The Roku Channel] i [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) för att snabbt få tillgång till [!DNL Roku] ägt och styrt lager.
* Rikta in er på befintliga, alltid aktiverade erbjudanden för [!DNL Roku Network] i [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) för att snabbt uppnå skalbarhet över [!DNL Roku]-plattformen.

Till maximal skala:

* Anpassa en [!DNL Roku] privat marknadsplats för prioriterad åtkomst till [!DNL Roku]-leverans till ett förhandlat pris.

>[!MORELIKETHIS]
>
>* [Skapa information om avtal-ID manuellt](/help/dsp/inventory/deal-id-create.md)
> * [Prenumerera och begär åtkomst  [!DNL On Demand] till Premium Inventory Deals](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Skapa en placering](/help/dsp/campaign-management/placements/placement-create.md)

