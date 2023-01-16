---
title: Översikt över Campaign Management i DSP
description: Lär dig mer om kampanjhanteringshierarkin och komponenter.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Översikt över Campaign Management i DSP

DSP har följande hierarki:

* Campaign
   * Paket
      * Placering(ar)
         * Annonser

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Kampanjer](/help/dsp/campaign-management/campaigns/campaign-about.md) är det övergripande ramverket för flyginställningar. Varje kampanj är konfigurerad med en annonsörer, start- och slutdatum, en övergripande budget, ett alternativ för målinriktning mellan olika enheter och standardfrekvens samt rapporteringsalternativ för visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering. Alla inställningar på kampanjnivå gäller automatiskt för varje paket och placering i kampanjen.

## [!UICONTROL Packages]

Varje kampanj kan innehålla en eller flera [paket](/help/dsp/campaign-management/packages/package-about.md), som alla innehåller en uppsättning placeringar.

Använd paket för att gruppera placeringar för leverans till en fast budget, prestationsmål och anpassad paketeringsstrategi. DSP optimerar paket genom att flytta budgeten till de bästa placeringarna i paketet. Du kan ordna paket efter placeringsformat, lagertyp, dataleverantör, persona eller andra särskiljbara egenskaper.

Paket är valfria men rekommenderas.

## [!UICONTROL Placements]

A [placering](/help/dsp/campaign-management/placements/placement-about.md) lagrar målparametrar för en eller flera annonser av samma annonstyp. Du kan skapa en placering för en enskild kampanj eller ett paket och sedan tilldela annonser till den.

## [!UICONTROL Ads]

[Annonser](/help/dsp/campaign-management/ads/ad-about.md) innehåller kreativa resurser och spårnings-URL:er. Du kan överföra tredjepartsannonser som servar taggar individuellt eller gruppvis med hjälp av partnertaggmallar eller bulktaggmallen. Du kan också skapa inbyggda displayannonser manuellt för DSP.

När ni väl har ställt in era annonser måste ni bifoga varje annons på en plats. Du kan bifoga en annons till en eller flera ersättningar.

Alla aktiva, godkända annonser i en aktiv placering i en aktiv kampanj kan köras baserat på parametrarna för riktade placeringar.

>[!MORELIKETHIS]
>
>* [Om Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Om pakethantering](/help/dsp/campaign-management/packages/package-about.md)
>* [Om Platshantering](/help/dsp/campaign-management/placements/placement-about.md)
>* [Om annonshantering](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checklista för kampanjstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Bästa metoder för att konfigurera resultatkampanjer](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Om rapporter på plattformen](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Om kampanjdatavyer](/help/dsp/campaign-management/reports/campaign-data-views-about.md)
>* [Video: DSP kontostruktur och användargränssnitt](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/ui.html)

