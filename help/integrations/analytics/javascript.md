---
title: JavaScript-kod för [!DNL Analytics for Advertising]
description: JavaScript-kod för [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# JavaScript-kod för [!DNL Analytics for Advertising]

*Annonsörer med endast Adobe Advertising-Adobe Analytics Integration*

*Annonsörer med endast DSP*

För DSP [!DNL Analytics for Advertising] integreringen spårar genomskinlig och klickbar interaktion mellan webbplatser. Klicka-för-klickningsbesök spåras av Adobe Analytics standardkod på dina webbsidor. den [!DNL Analytics] koden hämtar parametrarna AMO ID och EF ID i landningssidans URL och spårar dem i deras respektive reserverade eVars. Du kan spåra visningar genom att distribuera ett JavaScript-kodfragment på dina webbsidor.

På den första sidvyn vid ett besök på webbplatsen kontrollerar JavaScript-koden i Adobe om besökaren tidigare har sett eller klickat på en annons. Om användaren tidigare har kommit in på webbplatsen via en klickning eller inte har sett någon annons, ignoreras besökaren. Om besökaren har sett en annons och inte har gått in på webbplatsen via ett klick under [klicka på uppslagsfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc) som anges i Adobe Advertising, så använder Adobe Advertising JavaScript-koden antingen a) [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html) för att generera ett extra ID (`SDID`) eller b) använder Adobe Experience Platform [!DNL Web SDK] `generateRandomID` metod för att generera en `[!DNL StitchID]`. Båda ID:n används för att knyta ihop data från Adobe Advertising med besökarens Adobe Analytics-träff. Adobe Analytics frågar sedan Adobe Advertising efter det AMO ID och EF ID som är kopplat till annonsplaceringen. AMO-ID:t och EF-ID:n fylls sedan i i deras respektive eVars. Dessa värden gäller under en angiven period (som standard 60 dagar).

[!DNL Analytics] skickar statistik om webbplatstrafiken (t.ex. sidvisningar, besök och hur länge de används) och [!DNL Analytics] Anpassade händelser eller standardhändelser till Adobe Advertising-timme, med EF ID som nyckel. Dessa [!DNL Analytics] mätvärden körs sedan genom Adobe Advertising Attribution System för att koppla konverteringarna till klicknings- och exponeringshistoriken.

>[!NOTE]
>
>JavaScript-spårningslogiken för Adobe-annonsering finns på Adobe sidan och har därför praktiskt taget ingen inverkan på sidinläsningstiden.
>
>Logiken i [!DNL DCM] dataanslutning till [!DNL Analytics] (med [!DNL Google Campaign Manager 360]) för DSP finns på klientsidan. Klientsidans sammanslagning saktar ned sidbelastningen och ökar risken för dataförlust. Detta beror på att [!DNL Analytics] JavaScript måste pinga [!DNL DoubleClick] och vänta [!DNL DoubleClick] för att skicka tillbaka den senaste klicknings-/tryckinformationen till [!DNL Analytics]. När [!DNL DSP] teamet skapar [!DNL DCM] dataanslutning måste du ange hur länge du vill fördröja sidan.

## Distribuera JavaScript-koden

JavaScript-biblioteket består av två rader som tillåter [!DNL Analytics] och Adobe för att kommunicera med varandra. Om [!DNL Analytics for Advertising] integreringen slutfördes under Adobe Advertising-implementeringen, så du borde ha fått den här koden med instruktioner om hur den ska distribueras.

### Koden

#### Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Placera koden där

The [!DNL Analytics for Advertising] JavaScript-funktionen måste komma efter Experience Cloud ID-tjänsten men före Analytics App Measurement-koden så att det kompletterande ID:t (`SDID`) eller `[!DNL StitchID]` kan ingå i ert Analytics-samtal.

![Kodplacering](/help/integrations/assets/a4adc-code-placement.png)

### Verifierar koddistribution

Du kan utföra valideringen med valfritt verktyg för paketkodsnuttar (t.ex. [!DNL Charles], [!DNL Fiddler], eller [!DNL Chrome Developer Tools]) genom att jämföra värdena för de fyra ID:n mellan begäran som går till Adobe Advertising och begäran som kommer att [!DNL Analytics], enligt nedan.

#### Bekräfta koden med [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öppna [!DNL Chrome Developer Tools] och klicka på **Nätverk** -fliken.

1. Läsa in en webbsida som innehåller [!DNL Analytics for Advertising] JavaScript.

1. Filtrera [!UICONTROL Network] tabba efter `last` och granska två rader:

   ![Filtrera vid senaste](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Den första raden är anropet till JavaScript-biblioteket och kallas för `last-event-tag-latest.min.js`.
   * Den andra raden är det samtal som skickar begäran till Adobe Advertising. Den börjar så här: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Om du inte ser samtalet till Adobe Advertising, är det kanske inte den första sidvyn i ditt besök. I testsyfte kan du ta bort cookien så att nästa anrop blir den första sidvyn för motsvarande besök:

      1. På fliken Program hittar du `adcloud` cookie, och verifiera att cookien innehåller `_les_v` (senaste besök) med värdet `y` och en UTC-epok som går ut om 30 minuter.
      1. Ta bort `ad cloud` cookie och uppdatera sidan.

1. (Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod) Filtrera på `/b/ss` för att se Analytics-träffen.

   ![Filtrera på `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod) Filtrera på `/interact` för att verifiera att nyttolasten för begäran till Edge Network innehåller `advertisingStitchID`.

   ![Filtrera på `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Jämför ID-värdena mellan de två träffarna. Alla värden kommer att finnas i frågesträngsparametrar förutom rapportsvitens-ID i Analytics-träffen, som är URL-sökvägen omedelbart efter `/b/ss/`.

   | ID | Analysparameter | Edge Network | Adobe Advertising Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS-organisation | `mcorgid` |  | `_les_imsOrgid` |
   | Kompletterande data-ID | sdid |  | `_les_sdid` |
   | Häftnings-ID | stitchId | `advertisingStitchID` under `_adcloud` property |  |
   | Analytics Report Suite | Värdet efter `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud Visitor-ID | mitten |  | `_les_mid` |

   Om ID-värdena matchar varandra bekräftas JavaScript-implementeringen. Adobe Advertising skickar [!DNL Analytics] om det finns någon klicknings- eller vyspårningsinformation på servern.

#### Bekräfta koden med [!DNL Adobe Experience Cloud Debugger]

1. Öppna [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) på din hemsida.
1. Gå till [!UICONTROL Network] -fliken.
1. I [!UICONTROL Solutions Filter] verktygsfält, klicka [!UICONTROL Adobe Advertising] och [!UICONTROL Analytics].
1. I [!UICONTROL Request URL – Hostname] parameterrad, lokalisera `lasteventf-tm.everesttech.net`.
1. I [!UICONTROL Request – Parameters] rad, granska genererade signaler, liknande steg 3 i &quot;[Bekräfta koden med [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod) Kontrollera att `Sdid` parametern matchar `Supplemental Data ID` i Adobe Analytics-filtret.
   * (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod) Kontrollera värdet på `advertisingStitchID` parametern matchar `Sdid` skickas till Experience Platform Edge-nätverket.
   * Om koden inte genereras kontrollerar du att cookien för Adobe Advertising har tagits bort i [!UICONTROL Application] -fliken. Uppdatera sidan och upprepa processen när den har tagits bort.

   ![Granskning [!DNL Analytics for Advertising] JavaScript-kod i [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising]](overview.md)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising]](prerequisites.md)

