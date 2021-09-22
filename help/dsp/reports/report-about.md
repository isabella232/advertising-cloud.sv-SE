---
title: Om anpassade rapporter
description: Lär dig mer om alternativ för att skapa anpassade rapporter manuellt eller med förkonfigurerade rapportmallar.
feature: DSP Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# Om anpassade rapporter

Med anpassade rapporter kan ni anpassa innehållet i och leveransen av rapportdata med kampanjdimensionerna (som annonsören, placeringen, webbplatser eller geos) och de mätvärden som är viktiga för er. Du kan antingen:

* Konfigurera kampanjresultatrapporter helt och hållet på detaljnivå.
* Välj bland förkonfigurerade rapportmallar och anpassa dem ytterligare.

Du kan generera rapporter en gång eller schemalägga att de ska genereras varje dag, vecka eller månad klockan 03:00 i den angivna tidszonen. När en rapport har skapats skickas ett meddelande till varje angiven e-postmottagare med en länk som filen kan hämtas från.

>[!NOTE]
>
>Du kan även visa on demand-data på alla nivåer i en kampanj (kampanj, paket, placering eller annons) [i den relevanta kampanjhanteringsvyn](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tillgängliga rapporttyper

* **[!UICONTROL Custom]:** Den här rapporten är en tom mall som du kan använda för att skapa en egen anpassad rapport med de flesta mått och mätvärden. [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo]och  [!UICONTROL Site] rapporter är variationer av den här mallen med förvalda kolumner och dimensioner för respektive användningsfall.

* Förkonfigurerade rapportmallar

   * **[!UICONTROL Billing]:** Använd den här rapporten för att förstå viktiga faktureringsvärden som utgiftsmått för mediefakturering per kampanj.

      >[!NOTE]
      >
      >Den här rapporten innehåller data om faktureringssegmentet. Om en användare eller enhet får ett intryck som tillhör flera segment, krediteras endast ett fakturerbart segment med intrycket.

   * **[!UICONTROL Conversion]:** Använd den här rapporten för att förstå hur era kampanjer fungerar baserat på konverteringsstatistik som hämtats med hjälp av Advertising Cloud konverteringsspårning. Den här rapporten innehåller multitouch-attribuering.

   * **[!UICONTROL Device]:** Använd den här förifyllda mallen för att se nyckeltal efter enhetsrelaterade dimensioner.

   * **[!UICONTROL Frequency (by Impression)]:** Använd den här rapporten för att förstå hur visningar ska visas för unika tittare (t.ex. hur många unika tittare som såg ett intryck, två visningar, tre exponeringar osv.). Data är tillgängliga via placering eller kampanj.

      >[!NOTE]
      >
      >* Data är tillgängliga efter den 1 mars 2019.
      >* Frekvensen beräknas utifrån ett urval data.
      >* För en del lager skickas ingen enhets-ID, vilket förhindrar frekvensspårning. Den här rapporten innehåller bara avtryck som det fanns en enhetsidentifierare för.


   * **[!UICONTROL Frequency (by App/Site)]:** Använd den här rapporten för att förstå hur många unika användare som nås via app eller per webbplats. Du kan också se hur många unika användare som har nåtts via en viss app eller webbplats (&quot;distinkta unika användare&quot;).

      >[!NOTE]
      >
      >* Data är tillgängliga efter 15 november 2018.
      >* För vissa privata lager skickas ingen enhets-ID, vilket förhindrar frekvensspårning.


   * **[!UICONTROL Geo]**: Använd den här förifyllda mallen för att se nyckeltal efter geografiska dimensioner.

   * **[!UICONTROL Margin]:** Använd den här rapporten för att se nyckeltal som marginal, vinst och andra utgiftsmått per kampanj eller placering.

   * **[!UICONTROL Segment]:** Använd den här förifyllda mallen för att se nyckeltal efter segment.

      >[!NOTE]
      >
      >* Den här rapporten ska visa hur olika målsegment fungerar. Den använder data om segmentmedlemskap. När ett intryck skickas till en person eller enhet som tillhör två eller flera målsegment innehåller rapporten en rad för varje segment. Av den anledningen kanske inte summorna i den här rapporten matchar den faktiska leveransen.
      >* Konverteringsstatistik och anpassade måldata för segment är tillgängliga efter 2 augusti 2019. Alla andra data för segment är tillgängliga från och med den 1 juni 2018.


   * **[!UICONTROL Site]:** Som standard innehåller standardvärden, totala mediekostnader och totala fakturerbara nettoutgifter per webbplats.

## Kontorapportering {#cross-account-reporting}

Alla organisationer som har flera DSP-konton kan välja att aktivera kontoöverskridande data i anpassade rapporter, beroende på organisationens behov. Du kan till exempel ge konto A åtkomst till data för konto B och ge konto B åtkomst till data för konto C (men inte konto A). Kontakta din kontoansvarige om du vill aktivera och konfigurera den här funktionen.

När funktionen har aktiverats för din organisation kan du [filtrera](report-settings.md) någon av följande rapporttyper efter konto:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] och [!UICONTROL Conversion].

Kontoinställningarna på [!UICONTROL Settings] > [!UICONTROL Account] anger a) de andra konton vars data är tillgängliga för ditt konto och b) de andra konton som kan komma åt dina kontodata.

>[!MORELIKETHIS]
>
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)
>* [Om rapporter på plattformen](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)

