---
title: Om anpassade mål
description: Läs mer om anpassade mål för att definiera framgångshändelser i paket som är optimerade för det lägsta CPA eller högsta ROAS.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Om anpassade mål

Anpassade mål definierar vilka framgångshändelser en annonsörer behöver för att uppfylla sina affärsmål. Varje paket som använder optimeringsmålen [!UICONTROL Highest ROAS - Custom Goal] eller [!UICONTROL Lowest CPA - Custom Goal] måste innehålla ett anpassat mål som hjälper till att uppnå det övergripande optimeringsmålet. Du kan skapa anpassade mål som *mål* i Advertising Cloud Search.

![anpassade mål](/help/dsp/assets/objective-goals.png)

Varje anpassat mål består av ett eller flera mått, eller *transaktionsegenskaper*, och de relativa vikterna för dessa transaktionsegenskaper. De tillgängliga transaktionsegenskaperna innehåller alla mätvärden som spåras med Advertising Cloud konverteringspixel och Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] dimensioner och segment är inte tillgängliga för Advertising Cloud-optimering.
>* Om du vill använda Analytics-händelser i DSP samarbetar du med din kontohanterare i Adobe för att konfigurera en integrering på annonsörnivå.
>* [!DNL Analytics] anpassade händelser följer den här namnkonventionen:  `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exempel: `custom_event_16_examplersid`


Anta till exempel att tre mätvärden (transaktionsegenskaper) är relevanta för ett visst paket i en av era kampanjer: &quot;PDF Download&quot;, som värderas till 20 USD, &quot;Email Registrup&quot; som värderas till 30 USD och &quot;Order Confirmation&quot; som värderas till 40 USD. Om du vill ge tyngd i enlighet med det engångs-monetära värdet av kundåtgärden, blir egenskapernas relativa vikter 1, 2 och 1,5.

Tips om hur du konfigurerar dina anpassade mål finns i [de bästa sätten att skapa anpassade mål](custom-goal-best-practices.md).

När du [skapar ett anpassat mål](custom-goal-create.md) kan du [tilldela det till ett paket](/help/dsp/campaign-management/packages/package-settings.md) för rapportering och algoritmisk optimering med Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Skapa ett anpassat mål](custom-goal-create.md)
>* [Bästa metoder för att skapa ett anpassat mål](custom-goal-best-practices.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)

