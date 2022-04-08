---
title: Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]
description: Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: 11a13816ccd2ef0c47efa615c54c0f7ce2f83734
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]

*Annonsörer med Advertising Cloud DSP och Advertising Cloud Search*

Läs följande information innan du integrerar Advertising Cloud med Adobe Analytics.

## Krav för rapportering av Advertising Cloud-data i [!DNL Analytics]

* Något av följande:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.0 eller senare
* Alla versioner av Adobe Analytics (inklusive [!DNL Prime], [!DNL Premium], eller [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` version 2.1 eller senare

>[!TIP]
>
>Använd den senaste versionen av varje bibliotek för att förbättra datakvaliteten.

## Krav för delning av analyssegment med Advertising Cloud

* Identitetstjänst för Experience Cloud: `visitorAPI.js` version 2.1 eller senare
* Adobe Analytics: `!DNL appMeasurement.js` version 1.8 eller senare

## Rapporteringskrav [!DNL Analytics] Data i Advertising Cloud

Ge Advertising Cloud implementeringsteam följande information:

* The [!DNL Analytics] Rapportera det programsvit-ID som ska användas för rapportering av betalmediaaktivitet och för matning av webbplatsaktivitet för optimering och rapportering i Advertising Cloud
* Företagets organisations-ID (Org-ID) för Experience Cloud.

Du hittar båda dessa ID:n på [Fliken Sammanfattning i Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Sammanfattningsskärmen för Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Data i Advertising Cloud {#lookback-a4adc}

För [!DNL Analytics] data skickas till Advertising Cloud för rapportering och optimering. Dessa data omfattas av attribueringsreglerna, inklusive fönster för att visa och klicka, som är konfigurerade för annonsören i Advertising Cloud.

![inställningar för visningsfönster på annonsnivå i Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud attribueringsklickningsfönster: Det antal dagar efter den första klickningen som klickningen kan kopplas till en konvertering. Som standard är det här värdet 60 dagar; det högsta antalet är 90 dagar
* Advertising Cloud attribueringsvisningsfönster: Det antal dagar efter det att ett annonsintryck inträffar där intrycket kan tillskrivas en konvertering. Som standard är det här värdet 14 dagar. max 30 dagar

   >[!NOTE]
   >
   > Fönstret för visningssökning är specifikt för Advertising Cloud, inte [!DNL Analytics for Advertising Cloud], rapporter.

The [!DNL Analytics for Advertising Cloud] JavaScript använder dessa inställningar för att avgöra hur långt tillbaka en genomskinlig post eller klickbar post till webbplatsen ska vara giltig. Mer information om hur du ser genom- och genomklickningar finns i &quot;[Advertising Cloud ID:n som används av Analytics](ids.md).&quot;

## Advertising Cloud Data in [!DNL Analytics]

[!DNL Analytics] ställer in Advertising Cloud ID:n (AMO ID:n) i Analytics-träffen, enligt annonsörens inställning för beständighet i eVar, som gäller både klickningar och genomvisningar. Den beständiga inställningen är konfigurerad på Advertising Cloud baksida och din [!DNL Adobe] kontoteamet kan ändra det.

* [!DNL Analytics for Advertising Cloud] eVar förfallodatum: 60 dagar som standard för AMO ID:n

>[!NOTE]
>
>Om du vill segmentera data för en annan tidsram kan du [skapa anpassade segment](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) med olika uppslagsfönster i Analysis Workspace.

## Annonsmiljöer som stöds

* Sök
* Visa
* Video
* Onlinevideo
* Inbyggt

Kontakta [!DNL Adobe] kontoteam för de senaste annonsmiljöerna som stöds i varje kanal.

## Saker att känna till innan du implementerar

* Advertising Cloud implementeringsteam kommer att konfigurera integreringen.

* Inga extra kostnader debiteras för den här integreringen och serveranrop leder inte heller till ytterligare [!DNL Analytics] eller Advertising Cloud.

* [!DNL Analytics for Advertising Cloud] är annonsserveragnostiker: en genomskinlig eller klickbar bild kan komma från vilken annonsserver som helst, och rätt ID genereras vid webbplatsinmatning.

* Integreringen godkänns endast [!DNL Analytics] standardhändelser och anpassade händelser till Advertising Cloud för att optimera köp av betalmedia och annonsinsatser. Det går inte [!DNL Analytics] segment, beräknade värden och eVars till Advertising Cloud för optimering av anbud.

* Advertising Cloud skapar beständiga ID:n i [!DNL Analytics] baserat på den senaste annonsen som klickades eller visades innan användaren kom in på webbplatsen, baserat på [klicka och visa sökningsfönster](#lookback-a4adc) som konfigurerats i Advertising Cloud. Om en besökare skulle ha båda typerna av webbplatspostinteraktioner i sin profil, och klickningen ligger inom uppslagsperioden, skulle besökarens klicknings-ID åsidosätta det genomsöknings-ID som används för platsrapportering.

* [!DNL Analytics for Advertising Cloud] Vid konverteringsspårning i Adobe Analytics används ett konfigurerbart uppföljningsfönster (60 dagar som standard). Advertising Cloud rapporter återspeglar webbplatskonverteringar och engagemang i slutet av detta uppföljningsfönster.

* Alla annonstyper stöds. Alla annonsmiljöer stöds dock inte.

   Annonser för uppkopplad TV (CTV) spåras till exempel inte eftersom det inte finns några klick i CTV och inga konverteringar kan ske på samma enhet. Men om annonsen visas i en skrivbordsmiljö kan vissa data för genomskinlig webbplatspost spåras.

* [!DNL Analytics] konverteringar spåras för närvarande och tilldelas endast en besökare på samma enhet.

* [!DNL Analytics for Advertising Cloud] saknar stöd för konverteringar i appvyn.

* Direktspårning stöds inte för annonsörer som använder en serversidesimplementering av [!DNL Analytics].

### Kompletterande ID

När identitetstjänsten Experience Cloud har implementerats för en webbplats träffar som innehåller data från [!DNL Analytics] eller Advertising Cloud innehåller ett extra ID.

Exempel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Alla Advertising Cloud-samtal som används av en [!DNL Analytics for Advertising Cloud] aktivitet för att leverera innehåll eller registrera målmåttet måste ha en motsvarande [!DNL Analytics] en träff som delar samma extra ID.

När du felsöker i [!DNL Analytics]måste du bekräfta att det kompletterande ID:t finns för [!DNL Analytics] träffar. I [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)kan du se detta ID på fliken Advertising Cloud som `sdid` parameter.

>[!NOTE]
>
> Den här implementeringen fungerar ungefär som [!DNL Analytics for Target] integrering.

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [JavaScript Code for Analytics for Advertising Cloud](/help/integrations/analytics/javascript.md)

