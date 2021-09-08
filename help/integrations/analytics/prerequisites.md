---
title: Krav och viktig information för implementering av [!DNL Analytics for Advertising Cloud]
description: Krav och viktig information för implementering av [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Krav och viktig information för implementering av [!DNL Analytics for Advertising Cloud]

*Annonsörer med Advertising Cloud DSP och Advertising Cloud Search*

Läs följande information innan du integrerar Advertising Cloud med Adobe Analytics.

## Krav för att rapportera Advertising Cloud-data i [!DNL Analytics]

* Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.0 eller senare
* Alla versioner av Adobe Analytics (inklusive [!DNL Prime], [!DNL Premium] eller [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` version 2.1 eller senare

>[!TIP]
>
>Använd den senaste versionen av Experience Cloud Identity Service med CNAME-stöd samt den senaste versionen av Analytics AppMeasurement for JavaScript för att förbättra datakvaliteten.

## Krav för delning av analyssegment med Advertising Cloud

* Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.1 eller senare
* Adobe Analytics: `!DNL appMeasurement.js` version 1.8 eller senare

## Krav för rapportering av [!DNL Analytics]-data i Advertising Cloud

Ge Advertising Cloud implementeringsteam följande information:

* [!DNL Analytics]-rapportsvitens-ID som ska användas för att rapportera betald mediaaktivitet och mata webbplatsaktiviteter för optimering och rapportering i Advertising Cloud
* Företagets organisations-ID (Org-ID) för Experience Cloud.

Du hittar båda dessa ID:n på skärmen [Sammanfattning i Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Sammanfattningsskärmen för Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Data i Advertising Cloud {#lookback-a4adc}

Eftersom [!DNL Analytics]-data skickas till Advertising Cloud för rapportering och optimering omfattas data av attribueringsreglerna, inklusive vilka fönster som har konfigurerats för annonsören i Advertising Cloud som ska visas och klickas.

![inställningar för visningsfönster på annonsnivå i Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud attribueringsklickningsfönster: Det antal dagar efter den första klickningen som klickningen kan kopplas till en konvertering. Som standard är det här värdet 60 dagar; det högsta antalet är 90 dagar
* Advertising Cloud attribueringsvisningsfönster: Det antal dagar efter det att ett annonsintryck inträffar där intrycket kan tillskrivas en konvertering. Som standard är det här värdet 14 dagar. max 30 dagar

   >[!NOTE]
   >
   > Fönstret för visningssökning är specifikt för Advertising Cloud, inte [!DNL Analytics for Advertising Cloud], och rapporterar.

JavaScript-koden [!DNL Analytics for Advertising Cloud] använder dessa inställningar för att avgöra hur långt tillbaka en genomskinlig post eller klickbar post till webbplatsen ska anses vara giltig. Mer information om hur genomskinlighet och klickningar bestäms finns i &quot;[Advertising Cloud ID:n som används av Analytics](ids.md).&quot;

## Advertising Cloud Data in [!DNL Analytics]

[!DNL Analytics] ställer in Advertising Cloud ID:n (AMO ID:n) i Analytics-träffen, enligt annonsörens inställning för beständighet i eVar, som gäller både klickningar och genomvisningar. Inställningen för beständighet har konfigurerats på Advertising Cloud baksida och din kontohanterare på Adobe kan ändra den.

* [!DNL Analytics for Advertising Cloud] eVar förfallodatum: 60 dagar som standard för AMO ID:n

>[!NOTE]
>
>Om du vill segmentera data för en annan tidsram kan du [konfigurera anpassade segment](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) med olika uppslagsfönster i Analysis Workspace.

## Annonsmiljöer som stöds

* Sök
* Visa
* Video
* Onlinevideo
* Inbyggt

Kontakta din kontoansvarige på Adobe för att få de senaste annonsmiljöerna som stöds i varje kanal.

## Saker att känna till innan du implementerar

* Inga extra kostnader debiteras för den här integreringen och serveranrop leder inte heller till ytterligare [!DNL Analytics]- eller Advertising Cloud-avgifter.

* [!DNL Analytics for Advertising Cloud] är annonsserveragnostiker: en genomskinlig eller klickbar bild kan komma från vilken annonsserver som helst, och rätt ID genereras vid webbplatsinmatning.

* Integreringen skickar endast [!DNL Analytics] standard- och anpassade händelser till Advertising Cloud för att optimera köp av betalmedia och annonsinsatser. Det skickar inte [!DNL Analytics] segment, beräknade värden och eVars till Advertising Cloud för anbudsoptimering.

* Advertising Cloud skapar beständiga ID:n inom [!DNL Analytics] baserat på den senaste annonsen som klickades eller visades innan användaren kom in på webbplatsen, baserat på de [click- och view-through-fönster](#lookback-a4adc) som konfigurerats i Advertising Cloud. Om en besökare skulle ha båda typerna av webbplatspostinteraktioner i sin profil, och klickningen ligger inom uppslagsperioden, skulle besökarens klicknings-ID åsidosätta det genomsöknings-ID som används för platsrapportering.

* [!DNL Analytics for Advertising Cloud] Vid konverteringsspårning i Adobe Analytics används ett konfigurerbart uppföljningsfönster (60 dagar som standard). Advertising Cloud rapporter återspeglar webbplatskonverteringar och engagemang i slutet av detta uppföljningsfönster.

* Alla annonstyper stöds. Alla annonsmiljöer stöds dock inte.

   Annonser för uppkopplad TV (CTV) spåras till exempel inte eftersom det inte finns några klick i CTV och inga konverteringar kan ske på samma enhet. Men om annonsen visas i en skrivbordsmiljö kan vissa data för genomskinlig webbplatspost spåras.

* [!DNL Analytics] konverteringar spåras för närvarande och tilldelas endast en besökare på samma enhet.

* [!DNL Analytics for Advertising Cloud] saknar stöd för konverteringar i appvyn.

* Genomvisningsspårning stöds inte för annonsörer som använder en serversidesimplementering av [!DNL Analytics].

### Kompletterande ID

När identitetstjänsten Experience Cloud har implementerats för en webbplats innehåller träffar som innehåller data från [!DNL Analytics] eller Advertising Cloud ett extra ID.

Exempel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

För korrekt dataintegrering måste alla Advertising Cloud-anrop som används av en [!DNL Analytics for Advertising Cloud]-aktivitet för att leverera innehåll eller registrera målmåttet ha en motsvarande [!DNL Analytics]-träff som delar samma extra ID.

När du felsöker i [!DNL Analytics] måste du kontrollera att det kompletterande ID:t finns för [!DNL Analytics] träffar. I [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) kan du se detta ID på fliken Advertising Cloud som `sdid`-parameter.

>[!NOTE]
>
> Den här implementeringen fungerar på liknande sätt som [!DNL Analytics for Target]-integreringen.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [JavaScript Code for Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)

