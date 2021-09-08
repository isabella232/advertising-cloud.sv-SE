---
title: Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud
description: Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# Förväntade datavarianser mellan [!DNL Analytics] och Advertising Cloud

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

Annonsörer med [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) -->-integreringsspåret har betalat annonser via Advertising Cloud och Adobe Analytics. När ni spårar media, kampanjer och kanaler via flera system matchar sällan samma datauppsättningar från olika system helt. I det här dokumentet beskrivs hur du bör förvänta dig att data för medier som har sålts via Advertising Cloud ska jämföras med data i de olika system där mediet spåras i [!DNL Analytics].

>[!NOTE]
>
>Det här dokumentet fokuserar på Advertising Cloud och Analytics, men många av de viktigaste punkterna kan också överföras till andra spårningslösningar.

## Attributionsskillnader i liknande rapporter

### Olika Lookback-fönster och attribueringsmodeller

Integreringen [!DNL Analytics for Advertising Cloud] använder två variabler (eVars eller rVars \[reserverade eVars]\) för att hämta [EF ID och AMO ID](ids.md). Variablerna konfigureras med ett enda uppslagsfönster (den tid som klickningar och genomgångar tilldelas) och en attribueringsmodell. Om inget annat anges konfigureras variablerna så att de matchar standardfönstret för klickning på annonsnivå och attribueringsmodellen i Advertising Cloud.

Uppslagsfönster och attribueringsmodeller kan dock konfigureras i både Analytics (via eVars) och Advertising Cloud. I Advertising Cloud kan attribueringsmodellen dessutom konfigureras inte bara på annonsörsnivå (för anbudsoptimering) utan även inom enskilda datavyer och rapporter (endast för rapportering). En organisation kanske föredrar att använda den jämna distributionsattribueringsmodellen för optimering, men använder den senaste touchattribueringen för rapporter i Advertising Cloud DSP eller [!DNL Search]. Om du ändrar attribueringsmodeller ändras antalet konverteringar.

Om ett rapportsökningsfönster eller en attribueringsmodell ändras i en produkt och inte i en annan, kommer samma rapporter från varje system att visa distinkta data:

* **Exempel på avvikelser orsakade av olika uppslagsfönster:**

   Anta att Advertising Cloud har ett 60-dagars klickfönster och att [!DNL Analytics] har ett 30-dagars uppslagsfönster. Anta också att en användare kommer till webbplatsen via en Advertising Cloud-spårad annons, lämnar och sedan återgår till dag 45 och konverterar. Advertising Cloud kommer att attribuera konverteringen till det ursprungliga besöket eftersom konverteringen gjordes inom 60-dagars uppslagsfönstret. [!DNL Analytics]Men det går inte att attribuera konverteringen till det ursprungliga besöket eftersom konverteringen inträffade efter att 30-dagars uppslagsfönstret hade gått ut. I det här exemplet skulle Advertising Cloud rapportera ett högre antal konverteringar än vad [!DNL Analytics] skulle göra.

   ![Exempel på en konvertering som har tilldelats i Advertising Cloud men inte  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exempel på avvikelser orsakade av olika attribueringsmodeller:**

   Anta att en användare interagerar med tre olika Advertising Cloud-annonser innan de konverterar, med intäkt som konverteringstyp. Om en Advertising Cloud-rapport använder en jämn distributionsmodell för attribuering, fördelas intäkterna jämnt över alla annonser. Om [!DNL Analytics] däremot använder den sista pekattribueringsmodellen, kommer intäkterna att fördelas till den sista annonsen. I följande exempel tilldelar Advertising Cloud 10 US-dollar av de 30 US-dollarintäkterna till var och en av de tre annonserna, medan [!DNL Analytics] tilldelar alla 30 US-dollar i intäkter till den sista annansen som användaren ser. När du jämför rapporter från Advertising Cloud och [!DNL Analytics], kan du förvänta dig att se effekten av skillnaden i attribuering.

   ![Olika intäkter som tillskrivs Advertising Cloud och  [!DNL Analytics] baseras på olika attribueringsmodeller](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Det bästa sättet är att använda samma uppslagsfönster och attribueringsmodell i både Advertising Cloud och [!DNL Analytics]. Samarbeta med din kontoansvarige på Adobe om det behövs för att identifiera de aktuella inställningarna och för att hålla konfigurationerna synkroniserade.

Samma koncept gäller alla andra kanaler som använder olika uppslagsfönster eller attribueringsmodeller.

#### Olika Lookback-fönster för vystyrningsspårning {#impression-lookback}

I Advertising Cloud baseras attribueringen på klick och visningar och du kan konfigurera olika uppslagsfönster för klick och visningar. I [!DNL Analytics] baseras dock attribueringen på klickfrekvens och genomskinlighet, och du har inte möjlighet att ange olika attribueringsfönster för klickfrekvens och genomskinlighet. spårning för varje start vid det första webbplatsbesöket. Ett intryck kan göras samma dag eller flera dagar innan en genomgång sker, vilket kan påverka var attribueringsfönstret börjar i varje system.

Vanligtvis sker de flesta genomskinliga konverteringar tillräckligt snabbt för att båda systemen ska kunna attribuera krediter. Vissa konverteringar kan dock inträffa utanför Advertising Cloud visningsfönster, men i uppslagsfönstret [!DNL Analytics]. sådana konverteringar tillskrivs genomgången i [!DNL Analytics] men inte till intrycket i Advertising Cloud.

Anta att en besökare fick en annons dag 1 i följande exempel, utförde ett besök (dvs. besökte annonsens landningssida utan att tidigare klicka på annonsen) dag 2 och konverterades dag 45. I det här fallet skulle Advertising Cloud spåra användaren från dag 1-14 (med 14-dagars uppslag), [!DNL Analytics] skulle spåra användaren från dag 2-61 (med 60-dagars uppslag) och konverteringen dag 45 skulle tillskrivas annonsen inom [!DNL Analytics] men inte inom Advertising Cloud.

![Exempel på en genomsiktskonvertering som har tilldelats i  [!DNL Analytics] men inte i Advertising Cloud](/help/integrations/assets/a4adc-viewthrough-example.png)

En annan orsak till diskrepanser är att du i Advertising Cloud kan tilldela visningskonverteringar en anpassad *genomsiktsvikt* som är relativ till den vikt som tilldelats en klickbaserad konvertering. Standardbredden för genomvyn är 40 %, vilket innebär att en genomsiktskonvertering räknas som 40 % av värdet för en klickbaserad konvertering. [!DNL Analytics] innehåller ingen sådan viktning av genomskinliga konverteringar. En 100 USD-intäktsorder som hämtas in i [!DNL Analytics] kommer alltså att diskonteras till 40 USD i Advertising Cloud om du använder standardvyns vikt - en skillnad på 60 USD.

Ta hänsyn till dessa skillnader när du jämför vykonverteringar mellan Advertising Cloud- och [!DNL Analytics]-rapporter.

#### Tillgängliga attribueringsmodeller

| Advertising Cloud Attribution | [!DNL Analytics] Attribut | eVar/rVar-allokering |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Använd inte* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>För linjär allokering attribuerar [!DNL Analytics] framgångshändelser lika i alla eVar inom ett enda besök, så använd linjär allokering med en eVar som förfaller till&quot;Besök&quot;. För annonsering leder emellertid användningen av linjär attribuering till en allokering som inte är helt linjär och till mindre än-idealisk rapportering. Om en besökare till exempel interagerar med tre annonser innan de konverterar till tre separata besök, tillskrivs bara den annons som sågs vid det senaste besöket konverteringen, inte alla tre annonserna.
>
>Dessutom förhindrar en växling av konverteringsallokering till eller från &quot;Linjär&quot; att historiska data visas, vilket kan leda till felaktiga data i rapporter. Linjärt allokering kan till exempel dela intäkten över ett antal olika eVar. Om du ändrar allokeringen till&quot;Senaste&quot; kopplas 100 % av denna intäkt till det senaste enskilda värdet. Den här föreningen kan leda till felaktiga slutsatser.
>
>För att undvika förvirring gör [!DNL Analytics] historiska data otillgängliga i rapporteringsgränssnittet. Du kan visa historiska data om du ändrar tillbaka eVar till den ursprungliga allokeringsinställningen, men du bör inte ändra eVar allokeringsinställningar bara för att få tillgång till historiska data. Adobe rekommenderar att du använder en ny eVar när du vill använda en ny allokeringsinställning för data som redan spelas in, i stället för att ändra allokeringsinställningarna för en eVar som redan har en stor mängd historiska data.

Se en lista över [!DNL Analytics]-attribueringsmodeller och deras definitioner på [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Om du är inloggad på Advertising Cloud hittar du en lista över attribueringsmodeller på
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Attribut för händelsedatum i Advertising Cloud

I Advertising Cloud kan du rapportera konverteringsdata antingen efter associerat klickdatum/händelsedatum (datumet för klickhändelsen eller tryckhändelsen) eller efter transaktionsdatumet (konverteringsdatumet). Konceptet för klicknings-/händelsedatumrapportering finns inte i [!DNL Analytics]. alla konverteringar som spåras i [!DNL Analytics] rapporteras per transaktionsdatum. Därför kan samma konvertering rapporteras med olika datum i Advertising Cloud och [!DNL Analytics]. Tänk dig en användare som klickar på en annons den 1 januari och konverterar den 5 januari. Om du visar konverteringsdata per händelsemedatum i Advertising Cloud rapporteras konverteringen den 1 januari när klickningen inträffade. I [!DNL Analytics] skulle samma konvertering rapporteras den 5 januari.

![Exempel på en konvertering som tilldelats olika datum](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribut i [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] Med ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) rapportering kan ni konfigurera regler för att identifiera olika marknadsföringskanaler baserat på distinkta aspekter av träffinformation. Du kan spåra Advertising Cloud-spårade kanaler ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] och [!UICONTROL Paid Search]) som [!DNL Marketing Channels] genom att använda frågesträngsparametern `ef_id` för att identifiera kanalen. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Även om  [!DNL Marketing Channels] rapporterna kan spåra Advertising Cloud-kanaler kanske uppgifterna av flera anledningar inte stämmer överens med Advertising Cloud-rapporterna. Mer information finns i följande avsnitt.

>[!NOTE]
>
> Följande centrala begrepp gäller också för flerkanalsspårning som omfattar kampanjer som inte spåras i Advertising Cloud, till exempel variabeln [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (kallas även Dimensionen Spårningskod eller eVar 0) och anpassad eVar.

### Potentiellt annorlunda attribueringsmodeller i [!DNL Marketing Channels]

De flesta [!DNL Marketing Channels]-rapporter har konfigurerats med [!UICONTROL Last Touch]-attribuering, som den senaste marknadsföringskanalen som identifieras tilldelas 100 % av konverteringsvärdet. Om du använder olika attribueringsmodeller för [!DNL Marketing Channels]-rapporterna och Advertising Cloud-rapporterna kommer det att leda till skillnader i de tilldelade konverteringarna.

### Ett potentiellt annorlunda fönster för att söka efter i [!DNL Marketing Channels]

Uppslagsfönstret för [!DNL Marketing Channels] kan anpassas. I Advertising Cloud går det att konfigurera fönstret för klicksökning, men ett fast 60-dagarsfönster är vanligt. Om de två produkterna använder olika fönster för sökning kan du förvänta dig avvikelser i data.

### Olika kanalattribut i [!DNL Marketing Channels]

Advertising Cloud rapporterar att endast betalda medier som har sålts via Advertising Cloud (betald sökning för Advertising Cloud Search-annonser och visning för Advertising Cloud DSP-annonser) tas emot, medan [!DNL Marketing Channels]-rapporter kan spåra alla digitala kanaler. Detta kan leda till en diskrepans i den kanal för vilken en konvertering görs.

Till exempel har betalsökningar och naturliga sökkanaler ofta en symbiotisk relation, där varje kanal hjälper den andra. [!DNL Marketing Channels]-rapporten kommer att attribuera vissa konverteringar till naturlig sökning som Advertising Cloud inte kommer att göra eftersom den inte spårar naturlig sökning.

Överväg också en kund som visar en displayannons, klickar på en betald sökannons, klickar i ett e-postmeddelande och lägger sedan en 30 USD-order. Även om både Advertising Cloud och [!DNL Marketing Channels] använder den senaste pekattribueringsmodellen skulle konverteringen fortfarande tilldelas olika till var och en. Advertising Cloud har inte åtkomst till [!UICONTROL Email]-kanalen, så den skulle kreditera betald sökning för konverteringen. [!DNL Marketing Channels]har dock tillgång till alla tre kanalerna, vilket innebär att konverteringen får  [!UICONTROL Email] poäng.

![Exempel på olika konverteringsattribuering i Advertising Cloud jämfört med  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Mer information om varför mätvärdena kan variera finns i &quot;[Varför kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;.

## Data Differences in Adobe Analytics [!DNL Paid Search Detection]

Med funktionen [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) i [!DNL Analytics] kan företag [definiera regler för att spåra betald och organisk söktrafik](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) för angivna sökmotorer. Regler för [!DNL Paid Search Detection] använder både en frågesträng och den refererande domänen för att identifiera betald och naturlig söktrafik. [!DNL Paid Search Detection]-rapporterna ingår i den större gruppen med [rapporter om att söka efter metoder](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html), som förfaller antingen när en viss händelse (till exempel en kundvagnsutcheckning) inträffar eller besöket avslutas.

Följande gränssnitt används för att skapa en [!DNL Paid Search Detection]-regeluppsättning:

![Exempel på en regel för identifiering av betald sökning i  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

De resulterande [!DNL Paid Search Detection]-rapporterna innehåller [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] och [!UICONTROL Natural Search Keywords].

Observera följande två begränsningar med data i [!DNL Paid Search Detection]-rapporter:

* Rapporterna [!UICONTROL Paid Search Keywords] och [!UICONTROL Natural Search Keywords] visar sökfrågorna som identifieras av de refererande URL:erna, inte nyckelorden som användarna lägger bud på. Advertising Cloud- och [!DNL Analytics]-rapporter visar de faktiska nyckelorden, så vänta dig inte att de ska stämma överens med [!DNL Paid Search Detection]-nyckelordsrapporterna.

* När funktionen [!DNL Paid Search Detection] ursprungligen skapades var den ursprungliga sökfrågan (teckensträngen som användaren angav i sökfältet i sökmotorn) mer lättillgänglig för annonsörer via den refererande URL:en. Idag är sökmotorer i stort sett otydliga med sökfrågan och nyckelordsrapporterna [!DNL Paid Search Detection] har ett begränsat värde eftersom de flesta frågedata tillhör &quot;unspecified&quot;.

   Med [!DNL Analytics for Advertising Cloud] kan annonsörer fortfarande spåra betalda nyckelord i [!DNL Analytics]. Den refererande domänen informerar motorn om vilken sökmotor som körde trafiken. Eftersom den annonserarspecifika kontoinformationen inte är kopplad till den refererande domänen, listas all trafik under sökmotorn. Annonsörer med flera konton i samma sökmotor bör referera till Advertising Cloud- eller [!DNL Analytics]-rapportering för kontospecifik rapportering.

### Varför ska jag konfigurera [!DNL Paid Search Detection]?

Med [!DNL Paid Search Detection]-rapporterna kan du identifiera naturlig söktrafik i [[!DNL Analytics Marketing Channels] rapporterna](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html). Att separera betald söktrafik och naturlig söktrafik är ett bra sätt att förstå det värde som naturlig sökning tillför hela marknadsföringsekosystemet.

## Klicka igenom dataverifiering för [!DNL Analytics for Advertising Cloud] {#data-validation}

För integreringen bör du validera klickinformationen för att säkerställa att alla sidor på webbplatsen följer klickfrekvensen.

I [!DNL Analytics] är ett av de enklaste sätten att validera [!DNL Analytics for Advertising Cloud]-spårning att jämföra klickningar med instanser genom att använda det beräknade mätvärdet för&quot;Click to AMO ID Instances&quot;, som beräknas enligt följande:

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] representerar det antal gånger som AMO-ID:n (`s_kwcid` parametrar) spåras på webbplatsen. Varje gång en annons klickas läggs en `s_kwcid`-parameter till på landningssidans URL. Antalet [!UICONTROL AMO ID Instances] motsvarar därför antalet klick och kan valideras mot faktiska annonsklickningar. Vi ser vanligtvis en matchningsfrekvens på 80 % för [!DNL Search] och en matchningsfrekvens på 30 % för [!DNL DSP]-trafik (vid filtrering så att endast klickfrekvens [!UICONTROL AMO ID Instances] inkluderas). Skillnaden i förväntningarna mellan sökning och visning kan förklaras av det förväntade trafikbeteendet. Sökfunktionen hämtar avsikten, och som sådan har användarna vanligtvis för avsikt att klicka på sökresultaten från sin fråga. Användare som ser en webbannons eller en videoannons är mer benägna att klicka på annonsen oavsiktligt och sedan antingen hoppa från webbplatsen eller avbryta det nya fönster som läses in innan sidaktiviteten spåras.

I Advertising Cloud-rapporter kan du jämföra klickningar med instanser med hjälp av mätvärdet [!UICONTROL ef_id_instances] i stället för [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Du bör förvänta dig en hög matchningsfrekvens mellan AMO ID och EF ID, men vänta inte med 100 % paritet eftersom AMO ID och EF ID i grunden spårar olika data, och den här skillnaden kan leda till små skillnader i det totala [!UICONTROL AMO ID Instances] och [!UICONTROL EF ID Instances]. Om summan [!UICONTROL AMO ID Instances] i [!DNL Analytics] skiljer sig från [!UICONTROL EF ID Instances] i Advertising Cloud med mer än 1 % kontaktar du din kontoansvarige på Adobe för att få hjälp.

Mer information om AMO ID och EF ID finns i [Advertising Cloud ID:n som används av Analytics](ids.md).

Följande är ett exempel på en arbetsyta som du kan använda för att spåra klickningar på instanser.

![Exempel på en arbetsyta som spårar klickningar till instanser](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Jämföra datauppsättningar i [!DNL Analytics for Advertising Cloud] med i Advertising Cloud

[AMO ID](ids.md) (s_kwcid frågesträngsparameter) används för rapportering i [!DNL Analytics], och [EF ID](ids.md) används för rapportering i Advertising Cloud. Eftersom de är distinkta värden kan ett värde vara skadat eller inte läggas till på landningssidan.

Anta att vi har följande landningssida:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

där EF-ID:t är &quot;`test_ef_id`&quot; och AMO-ID:t är &quot;`test_amo_id`&quot;.

Om en omdirigering sker på en webbplats kan URL:en sluta på följande sätt:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

där EF-ID:t är &quot;`test_ef_id`&quot; och AMO-ID:t är &quot;`test_amo_id#redirectAnchorTag`&quot;.

I det här exemplet lägger tillägget av ankartaggen till oväntade tecken i AMO-ID:t, vilket resulterar i ett värde som inte känns igen i Analytics. Detta AMO-ID skulle inte klassificeras och konverteringar som är kopplade till det skulle hamna under [!UICONTROL unspecified] eller [!UICONTROL none] i [!DNL Analytics]-rapporter.

Men även om sådana här problem är vanliga så brukar de vanligtvis inte resultera i en hög procent skillnader. Men om du upptäcker stora skillnader mellan AMO ID:n i [!DNL Analytics] och EF ID:n i Advertising Cloud kontaktar du kontohanteraren i Adobe för att få hjälp.

## Andra mätvärden

### Skillnaden mellan klick och besök {#clicks-vs-visits}

De verkar analoga, men klick och besök representerar olika data:

* **Klicka:** [!DNL DSP] eller så spelar sökmotorn in ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Besök:** [!DNL Analytics] definierar en  [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) besökssekvens med en serie sidvisningar som användaren utför och som avslutas enligt ett av flera kriterier, till exempel 30 minuters inaktivitet.

En klickning kan per definition leda till flera besök.

Titta på följande exempel: Användare 1 och Användare 2 får båda åtkomst till en webbplats genom att klicka på en Advertising Cloud-annons. Användare 1 visar fyra sidor och går sedan ut för dagen, så det första klicket ger ett besök. Användare 2 visar två sidor, löv för en 45-minuters lunch, återvänder, visar ytterligare två sidor och sedan löv, I det här fallet resulterar den första klickningen i två besök.

![Exempel på skillnaden mellan klick och besök](/help/integrations/assets/a4adc-visits-example.png)

### Skillnaden mellan klick och genomklickningar

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klick och klickningar är två olika mätvärden:

* **Klicka:** [!DNL DSP] eller så spelar sökmotorn in ett klick när en besökare klickar på en annons på en utgivares webbplats.

* **Klickningar:** [!DNL Analytics] registrerar en klickfrekvens när besökaren kommer in på målwebbplatsen, landningssidan läses in och  [!DNL Analytics] begäran längst ned på sidan skickar data till  [!DNL Analytics].

Klickningar och klickningar kan skilja sig avsevärt på grund av oavsiktliga annonsklick. Vi har observerat att de flesta klick på displayannonser är oavsiktliga klick, och dessa oavsiktliga besökare klickar på knappen Bakåt innan landningssidan läses in, så [!DNL Analytics] kan inte spela in en klickning. Detta gäller särskilt annonser där en oavsiktlig klickning är mer sannolik, som mobilannonser, videoannonser och annonser som fyller skärmen och måste stängas innan användaren kan visa sidan.

Webbplatser som är inlästa på mobila enheter är också mindre benägna att resultera i klickningar på grund av lägre bandbredder eller tillgänglig processorkraft, vilket gör att landningssidor tar längre tid att läsa in. Det är inte ovanligt att 50-70 % av klickningarna inte leder till klickningar. I mobilmiljöer kan skillnaden vara så hög som 90 % på grund av kombinationen av en långsammare webbläsare och den större sannolikheten att användaren av misstag klickar på annonsen när han eller hon bläddrar igenom sidan eller försöker stänga annonsen.

Klickdata kan också spelas in i miljöer där klickningar inte kan spelas in med de aktuella spårningsmekanismerna (t.ex. klick som går in i eller från en mobilapp) eller där annonsören endast har använt en spårningsmetod (t.ex. med den genomskinliga JavaScript-metoden, webbläsare som blockerar cookies från tredje part spårar klickningar, men inte klickningar). En viktig orsak till att Adobe rekommenderar att man använder sig av både klicknings-URL:er och JavaScript-spårningsmetoder är att maximera täckningen av spårbara klickningar.

### Använda Advertising Cloud Traffic Metrics för icke-Advertising Cloud-Dimensioner

Advertising Cloud förser Analytics med [reklamspecifika trafikdata och relaterade dimensioner från DSP och Search](advertising-cloud-metrics-in-analytics.md). Mätvärdena som tillhandahålls av Advertising Cloud gäller endast de angivna Advertising Cloud-dimensionerna och data är inte tillgängliga för andra dimensioner i [!DNL Analytics].

Om du till exempel visar måtten [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] per konto, som är en Advertising Cloud-dimension, ser du det totala värdet [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] per konto.

![Exempel på Advertising Cloud-statistik i en rapport som använder en Advertising Cloud-dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Om du däremot visar måtten [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] med en siddimension (till exempel Sida), som Advertising Cloud inte tillhandahåller data för, blir [!UICONTROL AMO Clicks] och [!UICONTROL AMO Cost] för varje sida noll (0).

![Exempel på Advertising Cloud-mått i en rapport som använder en dimension som inte stöds](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Använda [!UICONTROL AMO ID Instances] som ersättning för klickningar med icke-Advertising Cloud-Dimensioner

Eftersom du inte kan använda [!UICONTROL AMO Clicks] med webbplatsdimensioner kan det vara bra att hitta en som motsvarar klick. Det kan vara frestande att använda besök som ersättning, men det är inte det bästa alternativet eftersom varje besökare kan ha flera besök. (Se &quot;[Skillnaden mellan klick och besök](#clicks-vs-visits).&quot; Vi rekommenderar i stället att du använder [!UICONTROL AMO ID Instances], vilket är antalet gånger som AMO-ID:t hämtas. Även om [!UICONTROL AMO ID Instances] inte matchar [!UICONTROL AMO Clicks] exakt är de det bästa alternativet för att mäta klicktrafiken på webbplatsen. Mer information finns i &quot;[Dataverifiering för [!DNL Analytics for Advertising Cloud]](#data-validation).&quot;

![Exempel  [!UICONTROL AMO ID Instances] i stället  [!UICONTROL AMO Clicks] för en dimension som inte stöds](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID:n som används av [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Advertising Cloud Metrics in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Data i Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Varför data kan variera mellan Advertising Cloud och [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

