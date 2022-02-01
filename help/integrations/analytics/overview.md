---
title: Översikt över [!DNL Analytics for Advertising Cloud]
description: Översikt över [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Översikt över [!DNL Analytics for Advertising Cloud]

*Annonsörer med Advertising Cloud DSP och Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] integrerar Adobe Analytics och Adobe Advertising Cloud för att utöka och förbättra funktionerna i respektive produkt.

Tack vare integreringen kan annonsörer spåra klicknings- och genomskinlighetsinteraktioner på webbplatser i sina [!DNL Analytics] instanser, som gör det möjligt för varumärken att se hur deras annonskostnader leder till webbplatsengagemang och viktiga affärsmål.

Dessutom har Advertising Cloud tillgång till de omfattande förstahandsdata som [!DNL Analytics] samlingar med [!DNL Analytics] -taggar finns redan på platsen. Detta ger en mer robust hantering av resor, återmarknadsföring från första part och rapportering av betalda webbplatser. Advertising Cloud kan använda [!DNL Analytics] data för optimering av utgifter och bud.

När de är korrekt anställda, [!DNL Analytics for Advertising Cloud] oskarpa linjer mellan två traditionella roller: hantering av annonseringsresan (genom att skicka användare till webbplatsen via annonser) och förstå webbplatsengagemanget med hjälp av webbanalys.

Fördelar:

* Skicka [!DNL Analytics] direkt till Advertising Cloud för återmarknadsföring av förstahandswebbplatser.
* Använd [!DNL Analytics] anpassade händelser och standardhändelser som konverteringssignaler för optimering av betalmediereklam.
* Utnyttja [!DNL Analytics] Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden.
* Bättre samarbete mellan webbanalytiker och betalteam.
* Använd Advertising Cloud-ID:n för genomsökning och klickning i [!DNL Analytics] för att förstå webbplatsengagemang.
* Förbättra traditionella betalda medierapporter i Analysis Workspace med anpassade mätvärden, anpassade dimensioner och webbplatsaktivitet som inte är möjliga när du exporterar data eller pixlar till annonsservrar eller andra DSP.
* Utnyttja [!DNL Analytics] finns redan på er webbplats för att spåra och optimera inom Advertising Cloud.

>[!TIP]
>
> Se en [videointroduktion till [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Använda analyser för betald medierapportering

[!DNL Analytics for Advertising Cloud] ger bättre rapporter och insikt i hur annonserna påverkar webbplatsens beteende genom att göra det möjligt för er att:

* Använd Advertising Cloud-ID:n för genomsökning och klickning i [!DNL Analytics] för att förstå webbplatsengagemang.
* Utnyttja Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden. Ni har tillgång till dimensionella data och händelsedata för betalda medier, som innehåller namn på Advertising Cloud kampanjentiteter (inte bara för utplaceringar och annonser) och tillhörande värden, som klick, visningar och kostnader.

Används [!DNL Analytics] som ert betalda medierapporteringsverktyg behöver din organisation logga in på Experience Cloud med tillgång till Analysis Workspace. Advertising Cloud-teamet hjälper dig att kartlägga dina Advertising Cloud-data till enskilda rapporteringsprogram i Analysis Workspace. Du kan skicka Advertising Cloud-data till alla rapporteringsprogram, men du bör vara medveten om vilka rapportsviter som har mappats till Advertising Cloud och vilka som inte har det. Beroende på rapportsviten kan detta ändra rapporterade data.

[Advertising Cloud ID:n i [!DNL Analytics]](ids.md) fungerar som andra eVars-variabler med en anpassad, permanent förfallotid. Som standard är attributsökningsfönstret inställt på 60 dagar under Advertising Cloud-implementeringen. Om du vill ändra den här inställningen arbetar du med [!DNL Adobe] kontoteam.

Advertising Cloud-dimensioner läggs till med suffixet&quot;(AMO ID)&quot; (t.ex.&quot;Ad Type (AMO ID)&quot;). Se &quot;[Advertising Cloud Metrics in Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; för en lista över tillgängliga dimensioner.

>[!NOTE]
>
> När du visar Advertising Cloud-data (eller en datauppsättning) i [!DNL Analytics]ska du vara medveten om att mätvärden och rapporter baseras på de regler som anges i [!DNL Analytics]. Informationen kan skilja sig från vad du ser i andra rapporteringssystem, t.ex. annonsserverrapporter, [!DNL DSP] rapporter eller sökmotorrapporter. För att förstå datamatchskillnader i [!DNL Analytics]behöver ni veta när eVar upphör, vad som definierar ett besök, vad som betraktas som sista beröringsattribuering jämfört med total bestående attribuering och andra faktorer. Mer information finns i [Förväntade datavariationer mellan [!DNL Analytics] och Advertising Cloud](data-variances.md).

## Använda analyser för att driva Advertising Cloud Campaigns och Portfolio

Utan behov av ytterligare pixlar [!DNL Analytics for Advertising Cloud] ger bättre optimering och enklare målgruppssegmentering genom att skicka två huvudsignaler till Advertising Cloud:

* Konverteringsmått som ska användas som anbudssignaler:
   * standardvärden, som [!UICONTROL Revenue] och [!UICONTROL Cart Views].
   * mått för webbplatsengagemang, t.ex. sidvisning och besök.
   * anpassade intäktsmått.
   * reserverade intäktsmått.
* Segment skapade i [!DNL Analytics] och publiceras i Experience Cloud.

   Du kan använda [!DNL Analytics] segment för återmarknadsföring av förstahandswebbplatser i [!DNL DSP] och betalda sökannonser.

   (Endast Advertising Cloud Search) Annonsörer med [!DNL Analytics] men inte Audience Manager kan också skapa taggbaserade målgrupper (ommarknadsföringslistor) för Google webbplatser och kundmatchande målgrupper (kundlistor) från [!DNL Analytics] segment som delas med Experience Cloud.

### Webbplatskonverteringsmått som budsignaler

Du kan använda standardhändelser och anpassade händelser från [!DNL Analytics] bygga viktade mål i Advertising Cloud. Målen ligger till grund för era anbudsbeslut [!DNL DSP] paket och sökportfolior.

>[!NOTE]
>
> Du kan inte mappa beräknade värden från [!DNL Analytics] till Advertising Cloud.

Advertising Cloud-teamet hjälper dig att identifiera och kartlägga de händelser som gäller för betalmedieprestanda i Advertising Cloud, där de visas i [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Se &quot;[Analytics-statistik i Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; om du vill se en lista över tillgängliga mätvärden.

### Analyssegment för återmarknadsföring av webbplatser

Advertising Cloud kan importera [!DNL Analytics] segment för återmarknadsföring för Advertising Cloud DSP och [!DNL Search] annonser som använder Experience Cloud-målgruppsintegreringen mellan [!DNL Analytics] och Experience Cloud.

Så här öppnar du [!DNL Analytics] segment, ett annonserarkonto måste ha [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiverat. När ID-tjänsten är aktiverad, alla segment i Experience Cloud (inklusive segment skapade i [!DNL Analytics] och publiceras i Experience Cloud, segment skapade i Adobe Audience Manager, segment skapade i Experience Cloud med [!DNL People core service]och segment som skapats i Adobe Experience Platform och skickats till Advertising Cloud via Audience Manager) blir tillgängliga i Advertising Cloud så snart de bearbetas.

[!DNL Analytics] segmenten är tillgängliga inom 24 timmar och uppdateras dagligen.

Mer information om Publiktjänsten Experience Cloud finns i [Experience Cloud målgrupper](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exempel på hur du använder integreringen

### Använda Advertising Cloud-data i Analysis Workspace

Om du vill veta hur du kan använda dina Advertising Cloud-data för att skapa visuella rapporter i Analysis Workspace kan du titta på videon &quot;[Introduktion till arbetsyta och rapportering](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Skapa Advertising Cloud Dashboards

Se videon &quot;[Skapa Advertising Cloud Dashboards med Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Använda Advertising Cloud-id:t för analys av webbplatsposter

Se videon &quot;[Skapa Advertising Cloud Site Entry-rapporter](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Introduktion till [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud ID:n som används av Analytics](ids.md)
>* [JavaScript Code for Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Förväntade datavariationer mellan [!DNL Analytics] och Advertising Cloud](data-variances.md)
>* [Advertising Cloud Metrics in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

