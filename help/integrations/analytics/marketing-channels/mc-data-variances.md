---
title: Varför olika kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]
description: Lär dig varför kanaldata som spåras av AMO-ID kan variera från kanaldata som spåras av [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Varför olika kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

En vanlig fråga från användare som lär sig om integrationen av Advertising Cloud och [!DNL Marketing Channels] datauppsättningarna är&quot;What orsakar datavariationen mellan AMO-ID:t och [!DNL Marketing Channels]?&quot; Eller ibland: &quot;Varför bryts data? Jag behöver all statistik för att matcha alla rapporter.&quot; Men diskrepanser visar inte att data är &quot;brutna&quot;, och diskrepanser förväntas och kanske önskas. Låt oss se varför integreringen har utformats på det här sättet.

De två datauppsättningarna har olika primära användningsområden:

* [!DNL Marketing Channels]: Det primära användningsexemplet för [!DNL Marketing Channels] är att jämföra data över flera kanaler med en gemensam attribueringsmodell. Analytikerna kan använda [!UICONTROL Marketing Channel] för att få bättre insikter om hur kanalerna interagerar med varandra. Denna insikt kan hjälpa er att fatta beslut på makronivå om hur ni ska investera i varje kanal och kan leda till insikter om hur besökare från varje kanal interagerar med webbplatsen.

   The [!DNL Analytics] [!UICONTROL Marketing Channel] Dimensionen är därför konfigurerad för att hämta och spåra alla kanaler. [!DNL Marketing Channels] kan även konfigureras för att fånga upp Advertising Cloud DSP-visningar och klickningar, och detta i relation till andra marknadsföringskanaler.

* Advertising Cloud AMO ID: Det primära användningsområdet för Advertising Cloud AMO ID-data är att mata in Advertising Cloud avancerade [!DNL Adobe Sensei]-baserade budgivningsalgoritmer. Algoritmerna fattar automatiskt tusentals anbudsbeslut på mikronivå varje dag för att maximera annonsutgifterna och uppnå målen för [!DNL DSP] kampanj eller [!DNL Search] portfolio. Ju mer konverteringsdata algoritmerna kan koppla ihop kampanjer, desto bättre kan algoritmerna fatta dessa beslut.

   Om du vill samla in dessa data ska du [!DNL Analytics for Advertising Cloud] integreringen överför råa AMO-ID:n som kan översättas som klicknings- och genomsiktsspårningskoder i Adobe Analytics AMO ID-dimension - som lagras antingen som en anpassad variabel (eVar) eller en reserverad variabel (rVar). Klickningar för andra kanaler är inte inställda i AMO ID-dimensionen, så AMO ID-dimensionen kan inte spåra inmatning från dessa andra kanaler. Resultatet är att AMO-ID:t kvarstår genom [!DNL Marketing Channes]l ingångspunkter.

Mer information om möjliga dataavvikelser mellan data som spåras av Advertising Cloud och [!DNL Analytics]-spårade data, se &quot;[Förväntade datavariationer mellan [!DNL Analytics] och Advertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Förväntade datavariationer mellan [!DNL Analytics] och Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Advertising Cloud ID för att skapa [!DNL Marketing Channels] Bearbetar regler](mc-ids.md)
>* [Använda [!DNL Analytics Marketing Channels] med Advertising Cloud Data](mc-ac-data.md)
>* [Video: Rapportera med Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

