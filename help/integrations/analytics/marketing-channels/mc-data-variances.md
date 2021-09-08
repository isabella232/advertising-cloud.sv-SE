---
title: Varför kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]
description: Lär dig varför kanaldata som spåras av AMO-ID kan variera från kanaldata som spåras av [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Varför kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

En vanlig fråga från användare som lär sig om integrationen av Advertising Cloud- och [!DNL Marketing Channels]-datauppsättningar är&quot;Vad orsakar datavariationen mellan AMO-ID:t och [!DNL Marketing Channels]?&quot; Eller ibland: &quot;Varför bryts data? Jag behöver all statistik för att matcha alla rapporter.&quot; Men diskrepanser visar inte att data är &quot;brutna&quot;, och diskrepanser förväntas och kanske önskas. Låt oss se varför integreringen har utformats på det här sättet.

De två datauppsättningarna har olika primära användningsområden:

* [!DNL Marketing Channels]: Det främsta användningsexemplet för  [!DNL Marketing Channels] är att jämföra data över flera kanaler med en gemensam attribueringsmodell. Analytikerna kan använda dimensionen [!UICONTROL Marketing Channel] för att få bättre insikter om hur kanalerna interagerar med varandra. Denna insikt kan hjälpa er att fatta beslut på makronivå om hur ni ska investera i varje kanal och kan leda till insikter om hur besökare från varje kanal interagerar med webbplatsen.

   Dimensionen [!DNL Analytics] [!UICONTROL Marketing Channel] är därför konfigurerad för att hämta och spåra alla kanaler. [!DNL Marketing Channels] kan även konfigureras för att fånga upp Advertising Cloud DSP-visningar och klickningar, och detta i relation till andra marknadsföringskanaler.

* Advertising Cloud AMO ID: Det primära användningsområdet för Advertising Cloud AMO ID-data är att mata in Advertising Cloud avancerade [!DNL Adobe Sensei]-baserade budgivningsalgoritmer. Algoritmerna fattar automatiskt tusentals anbudsbeslut på mikronivå varje dag för att maximera annonsutgifterna och uppnå målen för [!DNL DSP]-kampanjen eller [!DNL Search]-portföljen. Ju mer konverteringsdata algoritmerna kan koppla samman kampanjer, desto bättre kan algoritmerna fatta dessa beslut.

   För att samla in dessa data skickar [!DNL Analytics for Advertising Cloud]-integreringen råa AMO-ID:n som kan översättas som click-through- och view-through-koder i Adobe Analytics-dimensionens AMO-ID - som lagras antingen som en anpassad variabel (eVar) eller en reserverad variabel (rVar). Klickningar för andra kanaler är inte inställda i AMO ID-dimensionen, så AMO ID-dimensionen kan inte spåra inmatning från dessa andra kanaler. Resultatet är att AMO-ID:t kvarstår genom [!DNL Marketing Channes]l-startpunkter.

Mer information om möjliga dataavvikelser mellan Advertising Cloud-spårade data och [!DNL Analytics]-spårade data finns i &quot;[Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Förväntade datavariationer  [!DNL Analytics] mellan och Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [Grundläggande om [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Använda Advertising Cloud ID:n för att  [!DNL Marketing Channels] skapa bearbetningsregler](mc-ids.md)
>* [Använda  [!DNL Analytics Marketing Channels] med Advertising Cloud Data](mc-ac-data.md)
>* [Video: Rapportera med Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

