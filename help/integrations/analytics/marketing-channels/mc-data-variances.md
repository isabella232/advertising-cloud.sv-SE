---
title: Varför kanaldata kan variera mellan Adobe och [!DNL Marketing Channels]
description: Lär dig varför kanaldata som spåras av AMO-ID kan variera från kanaldata som spåras av [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Varför kanaldata kan variera mellan Adobe och [!DNL Marketing Channels]

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

En vanlig fråga från användare som lär sig om integrationen av Adobe-annonseringen och [!DNL Marketing Channels] datauppsättningarna är&quot;What orsakar datavariationen mellan AMO-ID:t och [!DNL Marketing Channels]?&quot; Eller ibland: &quot;Varför bryts data? Jag behöver all statistik för att matcha alla rapporter.&quot; Men diskrepanser visar inte att data är &quot;brutna&quot;, och diskrepanser förväntas och kanske önskas. Låt oss se varför integreringen har utformats på det här sättet.

De två datauppsättningarna har olika primära användningsområden:

* [!DNL Marketing Channels]: Det primära användningsexemplet för [!DNL Marketing Channels] är att jämföra data över flera kanaler med en gemensam attribueringsmodell. Analytikerna kan använda [!UICONTROL Marketing Channel] för att få bättre insikter om hur kanalerna interagerar med varandra. Denna insikt kan hjälpa er att fatta beslut på makronivå om hur ni ska investera i varje kanal och kan leda till insikter om hur besökare från varje kanal interagerar med webbplatsen.

   The [!DNL Analytics] [!UICONTROL Marketing Channel] Dimensionen är därför konfigurerad för att hämta och spåra alla kanaler. [!DNL Marketing Channels] kan även konfigureras för att fånga upp annonsens DSP-visningar och klickningar, och det gör det i relation till andra marknadsföringskanaler.

* Adobe Advertising AMO ID: Det primära användningsområdet för data från Adobe Advertising AMO ID är att mata in den avancerade [!DNL Adobe Sensei]-baserade budgivningsalgoritmer. Algoritmerna fattar automatiskt tusentals anbudsbeslut på mikronivå varje dag för att maximera annonsutgifterna och uppnå målen för [!DNL DSP] kampanj eller [!DNL Search] portfolio. Ju mer konverteringsdata algoritmerna kan koppla ihop kampanjer, desto bättre kan algoritmerna fatta dessa beslut.

   Om du vill samla in dessa data ska du [!DNL Analytics for Advertising] integreringen överför råa AMO-ID:n som kan översättas som klicknings- och genomsiktsspårningskoder i Adobe Analytics AMO ID-dimension - som lagras antingen som en anpassad variabel (eVar) eller en reserverad variabel (rVar). Klickningar för andra kanaler är inte inställda i AMO ID-dimensionen, så AMO ID-dimensionen kan inte spåra inmatning från dessa andra kanaler. Resultatet är att AMO-ID:t kvarstår genom [!DNL Marketing Channels] startpunkter.

Mer information om möjliga datavariationer mellan data som spåras i Adobe och [!DNL Analytics]-spårade data, se &quot;[Förväntade datavariationer mellan [!DNL Analytics] och Adobe](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Förväntade datavariationer mellan [!DNL Analytics] och Adobe](/help/integrations/analytics/data-variances.md)
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Adobe Advertising ID:n för att skapa [!DNL Marketing Channels] Bearbetar regler](mc-ids.md)
>* [Använda [!DNL Analytics Marketing Channels] med Adobe Advertising Data](mc-ac-data.md)
>* [Video: Använda [!DNL Marketing Channels] för Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

