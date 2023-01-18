---
title: Översikt över [!DNL Analytics for Advertising]
description: Översikt över [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Översikt över [!DNL Analytics for Advertising]

*Annonsörer med DSP och[!DNL Advertising Search]*

[!DNL Analytics for Advertising] integrerar Adobe Analytics och Adobe Advertising för att utöka och förbättra funktionerna i varje enskild produkt.

Tack vare integreringen kan annonsörer spåra klicknings- och genomskinlighetsinteraktioner på webbplatser i sina [!DNL Analytics] instanser, som gör det möjligt för varumärken att se hur deras annonskostnader leder till webbplatsengagemang och viktiga affärsmål.

Dessutom kan Adobe Advertising få tillgång till de omfattande förstahandsdata som [!DNL Analytics] samlingar med [!DNL Analytics] -taggar finns redan på platsen. Detta ger en mer robust hantering av resor, återmarknadsföring från första part och rapportering av betalda webbplatser. Adobe Advertising kan använda [!DNL Analytics] data för optimering av utgifter och bud.

När de är korrekt anställda, [!DNL Analytics for Advertising] oskarpa linjer mellan två traditionella roller: hantering av annonseringsresan (genom att skicka användare till webbplatsen via annonser) och förstå webbplatsengagemanget med hjälp av webbanalys.

Fördelar:

* Skicka [!DNL Analytics] segment direkt till Adobe Advertising for first-party site remarketing.
* Använd [!DNL Analytics] anpassade händelser och standardhändelser som konverteringssignaler för optimering av betalmediereklam.
* Utnyttja [!DNL Analytics] Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden.
* Bättre samarbete mellan webbanalytiker och betalteam.
* Använd permanenta Adobe Advertising-vy- och click-through-ID:n i [!DNL Analytics] för att förstå webbplatsengagemang.
* Förbättra traditionella betalda medierapporter i Analysis Workspace med anpassade mätvärden, anpassade dimensioner och webbplatsaktivitet som inte är möjliga när du exporterar data eller pixlar till annonsservrar eller andra DSP.
* Utnyttja [!DNL Analytics] finns redan på er webbplats för att spåra och optimera annonser i Adobe.

>[!TIP]
>
> Se en [videointroduktion till [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Använda analyser för betald medierapportering

[!DNL Analytics for Advertising] ger bättre rapporter och insikt i hur annonserna påverkar webbplatsens beteende genom att göra det möjligt för er att:

* Använd permanenta Adobe Advertising-vy- och click-through-ID:n i [!DNL Analytics] för att förstå webbplatsengagemang.
* Utnyttja Analysis Workspace för att bättre förstå webbplatsens startpunkter och besöksbeteenden. Ni har tillgång till dimensionella data och händelsedata för betalda media, som omfattar enhetsnamn för annonskampanjer i Adobe (ned till utplaceringar och annonser) och tillhörande värden, som klick, visningar och kostnader.

Används [!DNL Analytics] som ert betalda medierapporteringsverktyg behöver din organisation logga in på Experience Cloud med tillgång till Analysis Workspace. Adobe Advertising-teamet hjälper er att kartlägga era Adobe Advertising-data till enskilda rapporteringsprogram i Analysis Workspace. Du kan skicka Adobe Advertising-data till alla rapporteringsprogram, men du bör vara medveten om de rapportsviter som har mappats till Adobe Advertising och de som inte har det. Beroende på rapportsviten kan detta ändra rapporterade data.

[Adobe Advertising IDs within [!DNL Analytics]](ids.md) fungerar som andra eVars-variabler med en anpassad, permanent förfallotid. Som standard är attributsökningsfönstret inställt på 60 dagar under Adobe Advertising-implementeringen. Om du vill ändra den här inställningen arbetar du med [!DNL Adobe] kontoteam.

Reklamdimensioner för Adobe läggs till med suffixet&quot;(AMO ID)&quot; (t.ex.&quot;Ad Type (AMO ID)&quot;). Se &quot;[Adobe Advertising Metrics in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; för en lista över tillgängliga dimensioner.

>[!NOTE]
>
> När du visar Adobe Advertising-data (eller en datauppsättning) i [!DNL Analytics]ska du vara medveten om att mätvärden och rapporter baseras på de regler som anges i [!DNL Analytics]. Informationen kan skilja sig från vad du ser i andra rapporteringssystem, t.ex. annonsserverrapporter, [!DNL DSP] rapporter eller sökmotorrapporter. För att förstå datamatchskillnader i [!DNL Analytics]behöver ni veta när eVar upphör, vad som definierar ett besök, vad som betraktas som sista beröringsattribuering jämfört med total bestående attribuering och andra faktorer. Mer information finns i [Förväntade datavariationer mellan [!DNL Analytics] och Adobe](data-variances.md).

## Använd Analytics för att driva annonskampanjer för Adobe och Portfolio

Utan behov av ytterligare pixlar [!DNL Analytics for Advertising] möjliggör bättre optimering och enklare målgruppssegmentering genom att skicka två huvudsignaler till Adobe Advertising:

* Konverteringsmått som ska användas som anbudssignaler:
   * standardvärden, som [!UICONTROL Revenue] och [!UICONTROL Cart Views].
   * mått för webbplatsengagemang, t.ex. sidvisning och besök.
   * anpassade intäktsmått.
   * reserverade intäktsmått.
* Segment skapade i [!DNL Analytics] och publiceras i Experience Cloud.

   Du kan använda [!DNL Analytics] segment för återmarknadsföring av förstahandswebbplatser i [!DNL DSP] och betalda sökannonser.

   ([!DNL Search] endast) Annonsörer med [!DNL Analytics] men inte Audience Manager kan också skapa taggbaserade målgrupper (ommarknadsföringslistor) för Google webbplatser och kundmatchande målgrupper (kundlistor) från [!DNL Analytics] segment som delas med Experience Cloud.

### Webbplatskonverteringsmått som budsignaler

Du kan använda standardhändelser och anpassade händelser från [!DNL Analytics] bygga upp viktade mål i Adobe Advertising. Målen ligger till grund för era anbudsbeslut [!DNL DSP] paket och sökportfolior.

>[!NOTE]
>
> Du kan inte mappa beräknade värden från [!DNL Analytics] till Adobe Advertising.

Adobe Advertising-teamet hjälper er att identifiera och kartlägga de händelser som gäller för betalmedieprestanda i Adobe Advertising, där de kommer att visas i [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Se &quot;[Analytics Metrics in Adobe Advertising](analytics-data-in-advertising.md)&quot; om du vill se en lista över tillgängliga mätvärden.

### Analyssegment för återmarknadsföring av webbplatser

Adobe Advertising can ingest [!DNL Analytics] segment för återmarknadsföring för DSP och [!DNL Search] annonser som använder Experience Cloud-målgruppsintegreringen mellan [!DNL Analytics] och Experience Cloud.

Så här öppnar du [!DNL Analytics] segment, ett annonserarkonto måste ha [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiverat. När ID-tjänsten är aktiverad, alla segment i Experience Cloud (inklusive segment skapade i [!DNL Analytics] och publiceras i Experience Cloud, segment skapade i Adobe Audience Manager, segment skapade i Experience Cloud med [!DNL People core service]och segment som skapats i Adobe Experience Platform och skickats till Adobe Advertising via Audience Manager) blir tillgängliga i Adobe Advertising så snart de bearbetas.

[!DNL Analytics] segmenten är tillgängliga inom 24 timmar och uppdateras dagligen.

Mer information om Publiktjänsten Experience Cloud finns i [Experience Cloud målgrupper](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exempel på hur du använder integreringen

### Använda annonseringsdata från Adobe i Analysis Workspace

Om du vill veta hur du kan använda dina Adobe-annonsdata för att skapa visuella rapporter i Analysis Workspace kan du titta på videon &quot;[Introduktion till arbetsyta och rapportering](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Skapa Adobe Advertising Dashboards

Om du vill veta hur du kan spåra dina Adobe-annonsdata mot dina mål i Analysis Workspace kan du titta på videon &quot;[Skapa Adobe Advertising Dashboards med Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Använda Adobe Advertising ID för webbplatsanalys

Se videon &quot; om du vill se hur du kan skapa en webbannonsrapport i Adobe för övervakning av veckodag, tid på dygnet, webbläsare och geografisk påverkan[Skapa rapporter om webbplatsposter för annonsering i Adobe](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Introduktion till [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising IDs Used by Analytics](ids.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Förväntade datavariationer mellan [!DNL Analytics] och Adobe](data-variances.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Adobe-reklam](/help/integrations/analytics/analytics-data-in-advertising.md)

