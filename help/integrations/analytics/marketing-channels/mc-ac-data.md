---
title: Använda [!DNL Marketing Channels] med Advertising Cloud Data
description: Lär dig hur du använder Advertising Cloud-data i [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Använda [!DNL Analytics Marketing Channels] med Advertising Cloud Data

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

Genom att använda både Advertising Cloud- och [!DNL Marketing Channels]-rapporterna kan ni få värdefulla insikter om hur era digitala medier påverkar webbplatsaktiviteten.

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Följande bild visar hur Advertising Cloud och [!DNL Marketing Channels] spårar de enskilda besök som utgör en besökares resa. Advertising Cloud-rapporter i [!DNL Analytics] är begränsade till endast betald displayannonsering och sökannonsering som handlas via Advertising Cloud, med hjälp av AMO-ID:t. [!DNL Marketing Channels] spårar dock alla kanaler som konfigurerats i bearbetningsreglerna för [!DNL Marketing Channels].

![Hur Advertising Cloud och  [!DNL Marketing Channels] spårar de enskilda besöken på en besökares resa](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Vid det första besöket gick användaren in på webbplatsen via en e-postkampanj, genomförde tio sidvisningar och sedan gick han/hon. Vid det andra besöket gick användaren in på webbplatsen via en displayannons, genomförde tio sidvisningar och sedan gick han/hon. Vid det tredje besöket gick användaren in på webbplatsen via naturlig sökning, utförde fem sidvisningar, genomförde en konvertering på 250 dollar och åt vänster. Lägg märke till skillnaden i spårning mellan [!DNL Marketing Channels] och Advertising Cloud. Den enda kanal som Advertising Cloud spårar på den här resan är [!UICONTROL Display]. Advertising Cloud spårar kanalbesöket [!UICONTROL Display] och attribuerar efterföljande engagemangsdata (som sidvisningar) och konverterar tillbaka till den reklamens påverkan. [!DNL Marketing Channels], å andra sidan, ger en fullständig bild av alla kanaler.

Eftersom AMO-ID:t finns kvar under besökarens resa kan du använda AMO-ID-data för att se hur Advertising Cloud påverkar andra marknadsföringskanaler. AMO-ID:t [kvarstår i 60 dagar som standard](/help/integrations/analytics/overview.md), men du kan konfigurera persistensen efter behov.

## Kombinera data från Advertising Cloud och marknadsföringskanaler för att analysera medieprestanda

Inom [!DNL Analytics] kan ni kombinera Advertising Cloud beständiga betalda annonser och de omfattande besöksdata [!DNL Marketing Channels] för att bättre analysera ert medieprestanda så att ni bättre kan påverka kundresan.

I följande analys används Advertising Cloud-data för att visa olika versioner av hur en annonsering påverkar webbplatskonverteringen. Alla tre kolumnerna använder samma konverteringsmått, men varje kolumn ger en egen berättelse:

* I kolumn 1 behandlas AMO ID-data som är permanenta under besökarens resa. Kolumn 1 anger att 641-program som startas vid ett tillfälle var länkade till en Advertising Cloud-annons, antingen via en genomgång eller en klickningshändelse. I den här vyn beaktas ingen annan [!DNL Marketing Channels]-attribuering.

* I [!DNL Marketing Channels]-datauppsättningen tillskrivs dock 641 Applications Starts andra marknadsföringskanaler. De sista två kolumnerna tar 641 Applications Starts och begränsar data till kanalerna [!UICONTROL Display Click-Through] och [!UICONTROL Display View-Through], vilket visar konverteringarna som inträffar i en senaste pekattribueringsmodell.

![exempel på hur en displayannons påverkar webbplatskonverteringen](/help/integrations/assets/a4adc-mc-display-impact.png)

Du kan gå ett steg längre med den här analysen. Du kan dela upp Advertising Cloud-raden ytterligare via en marknadsföringskanal för att se var Advertising Cloud-konverteringarna är kopplade till 641 Applications Starts. Du vet redan att fem av dessa konverteringar är kopplade till en sista pekskärm genom klickning och 19 är kopplade till en sista pekskärm genom. Det betyder fortfarande att 617 Applications Starts kan tillskrivas andra marknadsföringskanaler. Du kan dra och släppa dimensionen Sista beröringskanalen ovanpå Advertising Cloud DSP-radobjektet för att visa kanalattribueringen för resten av programmen Starts och visa visningskanalens påverkan över flera kanaler.

![Så här lägger du till dimensionen Sista beröringskanalen](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Nu kan du se hur de återstående programmen börjar. E-post beviljas för 357 program med senaste beröring som har ett AMO-ID kvar. Med hjälp av den här typen av analyser kan ni se vilken effekt Advertising Cloud webbannonser har på alla kanaler. Med bara en datauppsättning och attribueringsmodell är den här typen av insikter inte tillgängliga.

![exempel på hur olika kanaler påverkas av visningskanalerna](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Du kan förbättra analysen ytterligare genom att använda ett Staplingsdiagram som är inställt på&quot;100 % staplade&quot; för att visa trenddata över tiden. Den här visualiseringen gör det enklare att övervaka vilka sista beröringskanaler som påverkas mest av era displaymarknadsföringskampanjer.

![exempel på hur de olika kanalerna påverkas av visningskanalerna](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Advertising Cloud ID:n för att  [!DNL Marketing Channels] skapa bearbetningsregler](mc-ids.md)
>* [Varför olika kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Rapportera med Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Översikt över [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

