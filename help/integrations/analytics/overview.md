---
title: Översikt över [!DNL Analytics for Advertising Cloud]
description: Översikt över [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Översikt över [!DNL Analytics for Advertising Cloud]

*Annonsörer med Advertising Cloud DSP och Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] integrerar Adobe Analytics och Adobe Advertising Cloud för att utöka och förbättra funktionerna i respektive produkt.

Tack vare integreringen kan annonsörer spåra klicknings- och genomsiktsinteraktioner på webbplatser i sina [!DNL Analytics]-instanser, vilket gör att varumärken kan se hur deras annonsutgifter leder till webbplatsengagemang och viktiga affärsmål.

Dessutom kan Advertising Cloud komma åt de omfattande förstahandsdata som [!DNL Analytics] samlar in med [!DNL Analytics]-taggar som redan finns på webbplatsen. Detta ger en mer robust hantering av resor, återmarknadsföring från första part och rapportering av betalda webbplatser. Advertising Cloud kan använda [!DNL Analytics]-data ytterligare för optimering av utgifter och bud.

När [!DNL Analytics for Advertising Cloud] används på rätt sätt blir linjerna mellan två traditionella roller oskarpa: hantering av annonseringsresan (genom att skicka användare till webbplatsen via annonser) och förstå webbplatsengagemanget med hjälp av webbanalys.

Fördelar:

* Skicka [!DNL Analytics]-segment direkt till Advertising Cloud för återmarknadsföring av förstahandswebbplatser.
* Använd [!DNL Analytics] anpassade händelser och standardhändelser som konverteringssignaler för att optimera betalmediereklam.
* Använd [!DNL Analytics] Analysis Workspace för att få en bättre förståelse för webbplatsens startpunkter och besöksbeteenden.
* Bättre samarbete mellan webbanalytiker och betalteam.
* Använd beständiga Advertising Cloud-ID:n för genomgång och klickning i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Förbättra traditionella betalda medierapporter i Analysis Workspace med anpassade mätvärden, anpassade dimensioner och webbplatsaktivitet som inte är möjliga när du exporterar data eller pixlar till annonsservrar eller andra DSP.
* Utnyttja den [!DNL Analytics]-kod som redan finns på webbplatsen för att spåra och optimera inom Advertising Cloud.

>[!TIP]
>
> Se en [videopresentation till [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Använda analyser för betald medierapportering

[!DNL Analytics for Advertising Cloud] ger bättre rapporter och insikt i hur annonserna påverkar webbplatsens beteende genom att göra det möjligt för er att:

* Använd beständiga Advertising Cloud-ID:n för genomgång och klickning i [!DNL Analytics] för att förstå webbplatsengagemanget.
* Utnyttja Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden. Ni har tillgång till dimensionella data och händelsedata för betalda medier, som innehåller namn på Advertising Cloud kampanjentiteter (inte bara för utplaceringar och annonser) och tillhörande värden, som klick, visningar och kostnader.

Om du vill använda [!DNL Analytics] som ditt betalda medierapporteringsverktyg behöver din organisation en Experience Cloud-inloggning med tillgång till Analysis Workspace. Advertising Cloud-teamet hjälper dig att kartlägga dina Advertising Cloud-data till enskilda rapporteringsprogram i Analysis Workspace. Du kan skicka Advertising Cloud-data till alla rapporteringsprogram, men du bör vara medveten om vilka rapportsviter som har mappats till Advertising Cloud och vilka som inte har det. Beroende på rapportsviten kan detta ändra rapporterade data.

[Advertising Cloud ID:n  [!DNL Analytics]](ids.md) i fungerar som andra eVars-variabler med en anpassad, permanent förfallotid. Som standard är attributsökningsfönstret inställt på 60 dagar under Advertising Cloud-implementeringen. Om du vill ändra den här inställningen ska du arbeta med din kontoansvarige på Adobe.

Advertising Cloud-dimensioner läggs till med suffixet&quot;(AMO ID)&quot; (t.ex.&quot;Ad Type (AMO ID)&quot;). En lista med tillgängliga dimensioner finns i &quot;[Advertising Cloud Metrics in Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot;.

>[!NOTE]
>
> När du visar Advertising Cloud-data (eller en datauppsättning) i [!DNL Analytics] bör du vara medveten om att mått och rapporter baseras på reglerna som är angivna i [!DNL Analytics]. Informationen kan skilja sig från vad du ser i andra rapporteringssystem, som annonsserverrapporter, [!DNL DSP]-rapporter eller sökmotorrapporter. För att förstå dataskillnaderna i [!DNL Analytics] måste du veta när data upphör att gälla, vad som definierar ett besök, vad som betraktas som senaste beröringsattribuering jämfört med total bestående attribuering och andra faktorer. Mer information finns i [Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud](data-variances.md).

## Använda analyser för att driva Advertising Cloud Campaigns och Portfolio

[!DNL Analytics for Advertising Cloud] möjliggör bättre optimering och enklare målgruppssegmentering genom att skicka två huvudsignaler till Advertising Cloud, utan att ytterligare pixlar krävs:

* Konverteringsmått som ska användas som anbudssignaler:
   * standardvärden, som [!UICONTROL Revenue] och [!UICONTROL Cart Views].
   * mått för webbplatsengagemang, t.ex. sidvisning och besök.
   * anpassade intäktsmått.
   * reserverade intäktsmått.
* Segment skapade i [!DNL Analytics] och publicerade i Experience Cloud.

   Du kan använda [!DNL Analytics]-segment för omdirigering av förstahandswebbplatser i [!DNL DSP] och betalda sökannonser.

   (Endast Advertising Cloud Search) Annonsörer med [!DNL Analytics] men inte Audience Manager kan också skapa Googles taggbaserade målgrupper (ommarknadsföringslistor) och kundmatchande målgrupper (kundlistor) från [!DNL Analytics] segment som delas med Experience Cloud.

### Webbplatskonverteringsmått som budsignaler

Du kan använda standardhändelser och anpassade händelser från [!DNL Analytics] för att skapa viktade mål i Advertising Cloud. Målen ligger till grund för budgivningsbeslut för dina [!DNL DSP]-paket och sökportföljer.

>[!NOTE]
>
> Du kan inte mappa beräknade värden från [!DNL Analytics] till Advertising Cloud.

Advertising Cloud-teamet hjälper dig att identifiera och mappa de händelser som gäller för betalmedieprestanda till Advertising Cloud, där de visas i [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Se &quot;[Analysstatistik i Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; för en lista över tillgängliga mätvärden.

### Analyssegment för återmarknadsföring av webbplatser

Advertising Cloud kan importera [!DNL Analytics]-segment för återmarknadsföring för Advertising Cloud DSP och [!DNL Search] annonser med hjälp av integreringen mellan [!DNL Analytics] och Experience Cloud.

För att få åtkomst till segmenten [!DNL Analytics] måste ett annonserarkonto ha [Experience Cloud ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiverad. När ID-tjänsten är aktiverad blir alla segment i Experience Cloud (inklusive segment som skapats i [!DNL Analytics] och publicerats i Experience Cloud, segment som skapats i Adobe Audience Manager, segment som skapats i Experience Cloud med [!DNL People core service] samt segment som skapats i Adobe Experience Platform och skickats till Advertising Cloud via Audience Manager) tillgängliga i Advertising Cloud så snart de bearbetats.

[!DNL Analytics] segmenten är tillgängliga inom 24 timmar och uppdateras dagligen.

Mer information om tjänsten Experience Cloud Publiker finns i [Experience Cloud Publiker](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exempel på hur du använder integreringen

### Använda Advertising Cloud-data i Analysis Workspace

Om du vill veta hur du kan använda dina Advertising Cloud-data för att skapa visuella rapporter i Analysis Workspace ska du titta i videon &quot;[Introduktion till arbetsyta och rapportering](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Skapa Advertising Cloud Dashboards

Om du vill veta hur du kan spåra dina Advertising Cloud-data mot dina mål i Analysis Workspace kan du titta på videon &quot;[Create Advertising Cloud Dashboards with Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Använda Advertising Cloud-id:t för analys av webbplatsposter

Se videon &quot;[Skapa rapporter för Advertising Cloud Site Entry Reports](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html) om du vill se hur du kan skapa en webbpostrapport från Advertising Cloud för övervakning av veckodag, tid, webbläsare och geografisk påverkan.&quot;

>[!MORELIKETHIS]
>
>* [Video: Introduktion till [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud ID:n som används av Analytics](ids.md)
>* [JavaScript Code for Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Förväntade datavariationer  [!DNL Analytics] mellan och Advertising Cloud](data-variances.md)
>* [Advertising Cloud Metrics in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

