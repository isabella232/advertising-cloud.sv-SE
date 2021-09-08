---
title: Översikt över kampanjhantering i Advertising Cloud DSP
description: Lär dig mer om kampanjhanteringshierarkin och komponenter.
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Översikt över kampanjhantering i Advertising Cloud DSP

Advertising Cloud DSP-kampanjer har följande hierarki:

* Campaign
   * Paket
      * Placering(ar)
         * Annonser
            * Kreativa

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) Campaign är det övergripande ramverket för flyginställningar. Varje kampanj är konfigurerad med en annonsörer, start- och slutdatum, en övergripande budget, ett alternativ för målinriktning mellan olika enheter och standardfrekvens samt rapporteringsalternativ för visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering. Alla inställningar på kampanjnivå gäller automatiskt för varje paket och placering i kampanjen.

## [!UICONTROL Packages]

Varje kampanj kan innehålla ett eller flera [paket](/help/dsp/campaign-management/packages/package-about.md), där vart och ett innehåller en uppsättning placeringar.

Använd paket för att gruppera placeringar för leverans till en fast budget, prestationsmål och anpassad paketeringsstrategi. DSP optimerar paket genom att flytta budgeten till de bästa placeringarna i paketet. Du kan ordna paket efter placeringsformat, lagertyp, dataleverantör, persona eller andra särskiljbara egenskaper.

Paket är valfria men rekommenderas.

## [!UICONTROL Placements]

En [placering](/help/dsp/campaign-management/placements/placement-about.md) lagrar målparametrar för en eller flera annonser av samma annonstyp. Du kan skapa en placering för en enskild kampanj eller ett paket och sedan tilldela annonser till den.

## [!UICONTROL Ads]

[Lägg ](/help/dsp/campaign-management/ads/ad-about.md) in kreativt material och spåra URL:er. Du kan antingen överföra ditt kreativa material och DSP skicka annonser som använder dem kostnadsfritt, eller så kan du överföra annonsserverkod från tredje part.

När ni väl har ställt in era annonser måste ni bifoga varje annons på en plats. Du kan bifoga en annons till en eller flera ersättningar.

Alla aktiva, godkända annonser i en aktiv placering i en aktiv kampanj kan köras baserat på parametrarna för riktade placeringar.

## [!UICONTROL Creatives]

Du kan överföra ljud- och videofiler som ska användas i annonser för angivna kampanjer.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

Du kan omedelbart skapa en annons med den överförda kreativa annonsen eller skapa en annons senare från antingen vyn Creative Cloud eller vyn Ads.

>[!MORELIKETHIS]
>
>* [Om kampanjhantering](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Om pakethantering](/help/dsp/campaign-management/packages/package-about.md)
>* [Om Platshantering](/help/dsp/campaign-management/placements/placement-about.md)
>* [Om annonshantering](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checklista för kampanjstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Bästa metoder för att konfigurera resultatkampanjer](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Om rapporter på plattformen](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Om kampanjdatavyer](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

