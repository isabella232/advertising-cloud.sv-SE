---
title: Bästa metoder för att skapa ett anpassat mål
description: Lär dig de bästa sätten att skapa anpassade mål för att definiera framgångsrika händelser.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Bästa metoder för att skapa ett anpassat mål

## Anpassade mål med en enda egenskap

I följande exempel visas hur du kan konfigurera mål som har en enda egenskap som mål (metrisk).

### Exempel på en kampanj med optimeringsmålet [!UICONTROL Highest ROAS - Custom Goal]

Om kampanjmålet är intäkt ([!UICONTROL Highest ROAS - Custom Goal]) kommer ditt anpassade mål (mål) att inkludera egenskapen [!UICONTROL Revenue] med en vikt på 1 (1).

![exempel på ett anpassat ROAS-mål med en enda egenskap](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> Ett [!UICONTROL Property Weight] på ett motsvarar värdet på ett för varje $1 av intäkt som spåras.
>
> En konvertering på 250 USD med vikten 1 rapporteras till exempel som 250 USD. Om konverteringsmåttet har tilldelats vikten 0,5, rapporteras konverteringen $250 som $125 i Advertising Cloud ($250 Conversion * 0.5 [!UICONTROL Property Weight] = $125).

### Exempel på en kampanj med optimeringsmålet [!UICONTROL Lowest CPA - Custom Goal]

Om kampanjmålet är den lägsta kostnaden per förvärv (CPA) och endast kräver en lyckad händelse, inkluderar du det måttet (i följande exempel&quot;Application Submit&quot;). Det bästa sättet är att ange vikten som ett (1).

![exempel på ett anpassat CPA-mål med en enda egenskap](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> Ett [!UICONTROL Property Weight] på ett är lika med värdet på ett för varje konvertering som spåras.
>
> Om till exempel 10 programsändningskonverteringar spåras rapporteras 10 programsändningskonverteringar.  Om konverteringsmåttet har tilldelats vikten 0,5 rapporteras 10 konverteringar som fem (5) i Advertising Cloud (10 Conversions * 0,5 [!UICONTROL Property Weight] = 5).

## Anpassade mål med flera egenskaper

Det finns två scenarier där du kan använda flera egenskaper i ett anpassat mål:

* Kampanjmålet har flera lyckade händelser. Du kanske till exempel annonserar för mer än en åtgärd på plats, och alla kan tillskrivas ditt mål med CPA. Följande exempelmål innehåller tre separata egenskaper (PDF-hämtning, kontakta oss och e-postregistrering), där var och en har vikten 1 (1), som anger att varje egenskap har samma vikt som [!DNL Adobe Sensei]-algoritmen. Om du inkluderar egenskaper med varierande kostnader eller prioritet kan du justera deras relativa vikt därefter.

   ![exempel på ett anpassat mål med flera egenskaper](/help/dsp/assets/custom-goal-multiple-properties.png)

* Den enda egenskapen i det anpassade målet har inte den lägsta konverteringsnivå på 10 per dag som krävs för optimerade prestanda. Detta kan bero på minimal daglig paketkostnad eller ett begränsat antal naturliga konverteringar. Genom att lägga till ytterligare stödegenskaper till det anpassade målet kan du uppnå tröskelvärdet på 10 konverteringar per dag. Tio stödhändelser kan hjälpa ett paket att uppnå tröskelvärdet 10/dag, även när varje vikt är under 1 (1). Men du kanske inte behöver lägga till så många händelser.

   När du lägger till stödegenskaper till ett anpassat mål ska du väga dem efter deras relativa betydelse för händelsen om det ska lyckas och tänka på mängden datapunkter. På så sätt kan Adobe Sensei-algoritmen balansera flera egenskaper och optimera mot ditt mål.

   Följande exempelmål innehåller tre egenskaper med olika vikt: Application Submit = 1, Application Start = 0.1 och Advertiser Landing Page = 0.01. Det innebär att varje konvertering av Application Submit har samma värde som i genomsnitt 10 konverteringar av Application Start och 100 konverteringar av Advertiser Landing Page.

   ![exempel på ett anpassat mål med flera egenskaper](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Om du i stället vägde besök för landningssidor lika mycket som i ansökningsformulär, kan det naturligt högre antalet besök på landningssidor överbelasta ditt mål och skevhet för besöken på landningssidor.<!--reword-->

>[!MORELIKETHIS]
>
>* [Om anpassade mål](custom-goal-about.md)
>* [Skapa ett anpassat mål](custom-goal-create.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)

