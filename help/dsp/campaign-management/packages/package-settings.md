---
title: Paketinställningar
description: Se beskrivningar av tillgängliga paketinställningar.
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Paketinställningar

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Paketnamnet. Maxlängden är 60 tecken.

**[!UICONTROL Description]:** (Valfritt) En beskrivning av paketet.

**[!UICONTROL 3rd Party Billed Fees]:** (Valfritt) En statisk tredjepartsavgift som ska spåras som en icke fakturerbar kostnad:

>[!NOTE]
>
>Fakturerbara avgifter återspeglas i [!UICONTROL Net CPM]-måttet.
* **[!UICONTROL CPM]:** Kostnaden per 1 000 visningar (CPM).

* **[!UICONTROL CPM Description]:** En beskrivning av CPM-avgiften.

Du kan åsidosätta inställningen på paketnivå på [placeringsnivå](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Skrivskyddat för befintliga paket) På vilken nivå ska plats och fästpunkter placeras i paketet:

* **[!UICONTROL Package level pacing]:** Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar placeras och häftas som en  *grupp*. Denna strategi säkerställer att alla placeringar i ett givet paket optimeras helhetsbaserat på prestanda och skalning till utvalda nyckeltal (KPI).

* **[!UICONTROL Placement level pacing]:**  Den här paketeringsstrategin fungerar genom att alla inkluderade placeringar placeras  *var för sig*. Det bästa sättet är att endast använda denna strategi för att genomföra garanterade privata marknadsplatserbjudanden.

**[!UICONTROL Flight Dates]:** Paketets startdatum och slutdatum.

Om du vill skapa icke-jämna mellanrum för paketet väljer du *[!UICONTROL *Activate Custom Flighting]** och ställer in anpassade flygningar i [!UICONTROL Flighting]-avsnittet nedan. När du har aktiverat anpassad belysning och sparat paketet kan du inte inaktivera anpassad belysning.

>[!NOTE]
>
>* Flygdatum måste inkluderas i kampanjflygdatum. Dessutom måste flygdatum för alla placeringar som är tilldelade detta paket inkluderas i dessa datum.
> * Du kan inte redigera paketets startdatum när anpassad ljussättning aktiveras.


**[!UICONTROL Budget]:** (Paket med endast paketnivåpaketering) Bruttobudgetens övre gräns och budgetintervallet.

För paket med anpassad felsökning är budgetintervallet alltid *[!UICONTROL All time]*. För paket utan anpassad felsökning anger du budgetintervallet: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paket med enbart paketnivåpacing och dynamisk marginalhantering) Bruttobudgettaket för paketets varaktighet.

**[!UICONTROL Optimization Goal]:** (Paket med endast paketnivåpaketering) Optimeringsmålet för paketet. Se beskrivningar av varje optimeringsmål på [Optimeringsmål och Använda dem](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Paket med enbart anpassade optimeringsmål) Det  [anpassade ](/help/dsp/optimization/custom-goal-about.md) målet för paketet. Mer information om de effektivaste strategierna för anpassade mål och kampanjer som använder dem finns i [Bästa metoder för att skapa ett anpassat mål](/help/dsp/optimization/custom-goal-best-practices.md) och [Bästa metoder för att konfigurera prestandakampanjer](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** (Paket med enbart anpassade optimeringsmål) Paketets syfte. Med den här inställningen kan du avgöra hur paketet ska optimeras:

* *[!UICONTROL Prospecting]:* Prospecting packages fokuserar på att skaffa nya kunder.

* *[!UICONTROL Retargeting]:* Återmarknadsföring av paket fokuserar på att återexponera tidigare besökare eller kunder.

* *[!UICONTROL Other]:* Alla andra syften.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Paket med enbart anpassade optimeringsmål) Ett annat paket vars historiska data används som indata för optimering av paketet.

**[!UICONTROL Target]:** (Paket med endast paketnivåpaketering) Målet, som används för att spåra prestanda.

>[!NOTE]
>
>Detta fält är bara ett riktmärke och används inte för beslut.

**[!UICONTROL Frequency Cap]:** (Paket med endast paketnivåpaketering) Antal gånger en unik enhet eller person (beroende på angivet  [!UICONTROL Cross Device Level]värde) kan få annonser från paketet. Alternativen är *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
>* Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.
>* Det bästa sättet är att ange frekvensgränser för både prospektering och återmarknadsföring på paketnivå.
> * Högre frekvenshål ger högre utgifter och större intryck men lägre räckvidd. Lägre frekvenshål ger lägre kostnader och större intryck men större räckvidd.


**[!UICONTROL Pace on]:** (Paket med endast paketnivåpaketering) Vilken paketering baseras på:

* *[!UICONTROL Budget]:* (Standard) Det här alternativet ger så många avtryck som möjligt inom den allokerade paketbudgeten.

* *[!UICONTROL Impressions]:* Det här alternativet ger avtryck tills en angiven kvantitet nås inom ett angivet intervall. När du väljer det här alternativet anger du antalet visningar och intervallet: *All time,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* eller *[!UICONTROL Weekly]*.

**[!UICONTROL Pacing Fill Strategy]:** (Paket med enbart paketnivåpaketering) Så här lägger du ut annonseringstester:

* *[!UICONTROL Even]:* Gör resultatet enhetligt under varje flygning, med målet 50 % av leveranstiden under den första hälften av flygningen.

* *[!UICONTROL Slightly Ahead]:* (Standardvärdet) Accelererar leveransen så att den är 55-65 % klar halvvägs genom flygningens längd.

* *[!UICONTROL Frontload]:* Snabbar upp leveransen så att den är 65-75 % klar halvvägs genom flygningen.

* *[!UICONTROL Aggressive Frontload]:* Snabbar upp leveransen så att den är 75-85 % klar halvvägs genom flygningen.

## [!UICONTROL Flighting]

(Paket med paketnivåpaketering och med &quot;[!UICONTROL Activate Custom Flighting]&quot; aktiverat) Anpassade flygperioder inom det totala [!UICONTROL Flight Dates] som anges i [!UICONTROL Goals & Budget]-avsnittet.

Ange startdatum, slutdatum och målantal visningar för varje flygning. Klicka på **[!UICONTROL Add Flight]** om du vill lägga till en annan flight.

>[!MORELIKETHIS]
>
>* [Om pakethantering](package-about.md)
>* [Skapa ett paket](package-create.md)
>* [Redigera ett paket](package-edit.md)
>* [Koppla en placering till ett paket](package-attach-placement.md)
>* [Vanliga frågor om kampanjhantering](/help/dsp/campaign-management/campaign-management-faq.md)

