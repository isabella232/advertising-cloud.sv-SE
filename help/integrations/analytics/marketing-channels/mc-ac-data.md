---
title: Använda [!DNL Marketing Channels] med Adobe Advertising Data
description: Lär dig använda Adobe-reklamdata i [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Använda [!DNL Analytics Marketing Channels] med Adobe Advertising Data

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

Genom att använda både Adobe Advertising och [!DNL Analytics Marketing Channels] kan ni få värdefulla insikter om hur era digitala medier påverkar webbplatsaktiviteten.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Följande bild visar hur Adobe Advertising och [!DNL Marketing Channels] spåra de enskilda besök som utgör en besökares resa. Adobe Advertising reports in [!DNL Analytics] begränsas till enbart betalannonsering, sökannonsering, social annonsering och e-handelskanal som handlas via Adobe Advertising, med AMO-ID:t. Men [!DNL Marketing Channels] spårar alla kanaler som konfigurerats i [!DNL Marketing Channels] Bearbetar regler.

![How Adobe Advertising and [!DNL Marketing Channels] spåra de enskilda besöken på en besökares resa,](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Vid det första besöket gick användaren in på webbplatsen via en e-postkampanj, genomförde tio sidvisningar och sedan gick han/hon. Vid det andra besöket gick användaren in på webbplatsen via en displayannons, genomförde tio sidvisningar och sedan gick han/hon. Vid det tredje besöket gick användaren in på webbplatsen via naturlig sökning, utförde fem sidvisningar, genomförde en konvertering på 250 dollar och åt vänster. Lägg märke till skillnaden i spårning mellan [!DNL Marketing Channels] och Adobe Advertising. Den enda kanal som Adobe Advertising spårar på den här resan är [!UICONTROL Display]. Adobe Advertising spårar [!UICONTROL Display] kanalbesök och attribuerar efterföljande engagemangsdata (t.ex. sidvisningar) och konverteringar tillbaka till reklamens påverkan. [!DNL Marketing Channels], å andra sidan, ger en fullständig bild av alla kanaler.

Eftersom AMO-ID:t finns kvar under besökarens resa kan ni använda AMO-ID-data för att se hur Adobe Advertising påverkar andra marknadsföringskanaler. AMO-ID [kvarstår i 60 dagar som standard](/help/integrations/analytics/overview.md), men du kan konfigurera beständigheten efter behov.

## Hur man kombinerar data från annonser och marknadsföringskanaler i Adobe för att analysera medieprestanda

Inom [!DNL Analytics]kan ni kombinera betalannonsuppgifterna för Adobe-annonsering och [!DNL Marketing Channels] omfattande besöksdata för att bättre analysera hur ert material fungerar så att ni bättre kan påverka kundresan.

I följande analys används data från annonseringen i Adobe för att visa olika versioner av hur en annonsering påverkar webbplatskonverteringen. Alla tre kolumnerna använder samma konverteringsmått, men varje kolumn ger en egen berättelse:

* I kolumn 1 behandlas AMO ID-data som är permanenta under besökarens resa. Kolumn 1 anger att 641-program som börjar var länkade till en annonsering i Adobe, antingen via en genomgång eller en klickningshändelse. Den här vyn kan inte visas på något annat sätt [!DNL Marketing Channels] attribuering i beaktande.

* I [!DNL Marketing Channels] Men de 641 Applications Starts kan tillskrivas andra marknadsföringskanaler. De sista två kolumnerna tar 641 Applications Starts och begränsar data till [!UICONTROL Display Click-Through] och [!UICONTROL Display View-Through] kanaler, visa konverteringar som inträffar i en senaste pekattribueringsmodell.

![exempel på hur en displayannons påverkar webbplatskonverteringen](/help/integrations/assets/a4adc-mc-display-impact.png)

Du kan gå ett steg längre med den här analysen. Du kan dela upp raden för annonsering i Adobe ytterligare via marknadsföringskanal för att se var konverteringarna för annonsering i Adobe är kopplade till 641-programmen börjar. Du vet redan att fem av dessa konverteringar är kopplade till en sista pekskärm genom klickning och 19 är kopplade till en sista pekskärm genom. Det betyder fortfarande att 617 Applications Starts kan tillskrivas andra marknadsföringskanaler. Du kan dra och släppa dimensionen Sista beröringskanalen ovanpå raden DSP annonsering för att visa kanalattribueringen för resten av programmen startar och visa effekten av Display channel i flera kanaler.

![Så här lägger du till dimensionen Sista beröringskanalen](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Nu kan du se hur de återstående programmen börjar. E-post beviljas för 357 program med senaste beröring som har ett AMO-ID kvar. Med hjälp av den här typen av analyser kan ni se vilken effekt Adobe Advertising har haft på alla kanaler. Med bara en datauppsättning och attribueringsmodell är den här typen av insikter inte tillgängliga.

![exempel på hur olika kanaler påverkas av visningskanalerna](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Du kan förbättra analysen ytterligare genom att använda ett Staplingsdiagram som är inställt på&quot;100 % staplade&quot; för att visa trenddata över tiden. Den här visualiseringen gör det enklare att övervaka vilka sista beröringskanaler som påverkas mest av era displaymarknadsföringskampanjer.

![exempel på hur de olika kanalerna påverkas av visningskanalerna](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] Bearbetar regler](mc-ids.md)
>* [Varför kanaldata kan variera mellan Adobe och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Använda [!DNL Marketing Channels] för Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Översikt över [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

