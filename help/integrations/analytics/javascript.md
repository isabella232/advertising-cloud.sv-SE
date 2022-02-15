---
title: JavaScript-kod för [!DNL Analytics for Advertising Cloud]
description: JavaScript-kod för [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 7bf8f3524954b17d9da336a2210a098bf571399e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# JavaScript-kod för [!DNL Analytics for Advertising Cloud]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

*Annonsörer endast med Advertising Cloud DSP*

För Advertising Cloud DSP [!DNL Analytics for Advertising Cloud] integreringen spårar genomskinlig och klickbar interaktion mellan webbplatser. Klicka-för-klickningsbesök spåras av Adobe Analytics standardkod på dina webbsidor. den [!DNL Analytics] koden hämtar parametrarna AMO ID och EF ID i landningssidans URL och spårar dem i deras respektive reserverade eVars. Du kan spåra visningar genom att distribuera ett JavaScript-kodfragment på dina webbsidor.

På den första sidvyn vid ett besök på webbplatsen kontrollerar Advertising Cloud JavaScript-koden om besökaren tidigare har sett eller klickat på en annons. Om användaren tidigare har kommit in på webbplatsen via en klickning eller inte har sett någon annons, ignoreras besökaren. Om besökaren har sett en annons och inte har gått in på webbplatsen via ett klick under [klicka på uppslagsfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc) i Advertising Cloud, använder Advertising Cloud JavaScript-koden antingen a) [Experience Cloud ID-tjänst](https://experienceleague.adobe.com/docs/id-service/using/home.html) för att generera ett extra ID (`SDID`) eller b) använder Adobe Experience Platform [!DNL Web SDK] `generateRandomID` metod för att generera en `[!DNL StitchID]`. Båda ID:n används för att knyta ihop data från Advertising Cloud med besökarens Adobe Analytics-träff. Adobe Analytics frågar sedan Advertising Cloud efter det AMO-ID och EF-ID som är kopplat till annonsplaceringen. AMO-ID:t och EF-ID:n fylls sedan i i deras respektive eVars. Dessa värden gäller under en angiven period (som standard 60 dagar).

[!DNL Analytics] skickar statistik om webbplatstrafiken (t.ex. sidvisningar, besök och hur länge de används) och [!DNL Analytics] anpassade händelser eller standardhändelser till Advertising Cloud varje timme, med EF ID som nyckel. Dessa [!DNL Analytics] mätvärden körs sedan genom Advertising Cloud attribueringssystem för att koppla konverteringarna till klicknings- och exponeringshistoriken.

>[!NOTE]
>
>Spårningslogiken i Advertising Cloud JavaScript finns på Adobe och påverkar därmed inte sidans inläsningstid.
>
>Logiken i [!DNL DCM] dataanslutning till [!DNL Analytics] (med [!DNL Google Campaign Manager 360]) för Advertising Cloud DSP finns på klientsidan. Klientsidans sammanslagning saktar ned sidbelastningen och ökar risken för dataförlust. Detta beror på att [!DNL Analytics] JavaScript måste pinga [!DNL DoubleClick] och vänta [!DNL DoubleClick] för att skicka tillbaka den senaste klicknings-/tryckinformationen till [!DNL Analytics]. När [!DNL DSP] teamet skapar [!DNL DCM] dataanslutning måste du ange hur länge du vill fördröja sidan.

## Distribuera JavaScript-koden

JavaScript-biblioteket består av två rader som tillåter [!DNL Analytics] och Advertising Cloud för att kommunicera med varandra. Om [!DNL Analytics for Advertising Cloud] integreringen slutfördes under Advertising Cloud-implementeringen, och du bör ha fått den här koden med instruktioner om hur den ska distribueras.

**(Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**(Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Placera koden där

The [!DNL Analytics for Advertising Cloud] JavaScript-funktionen måste komma efter Experience Cloud ID-tjänsten men före Analytics App Measurement-koden så att det kompletterande ID:t (`SDID`) eller `[!DNL StitchID]` kan ingå i ert Analytics-samtal.

![Kodplacering](/help/integrations/assets/a4adc-code-placement.png)

### Verifierar koddistribution

Du kan utföra valideringen med valfritt verktyg för paketkodsnuttar (t.ex. [!DNL Charles], [!DNL Fiddler], eller [!DNL Chrome Developer Tools]) genom att jämföra värdena för de fyra ID:n mellan begäran som skickas till Advertising Cloud och begäran som skickas till [!DNL Analytics], enligt nedan.

#### Bekräfta koden med [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öppna [!DNL Chrome Developer Tools] och klicka på **Nätverk** -fliken.

1. Läsa in en webbsida som innehåller [!DNL Analytics for Advertising Cloud] JavaScript.

1. Filtrera [!UICONTROL Network] tabba efter `last` och granska två rader:

   ![Filtrera vid senaste](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Den första raden är anropet till JavaScript-biblioteket och kallas för `last-event-tag-latest.min.js`.
   * Den andra raden är det samtal som skickar begäran till Advertising Cloud. Den börjar så här: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Om du inte ser samtalet till Advertising Cloud är det inte säkert att det är första sidan av besöket. I testsyfte kan du ta bort cookien så att nästa anrop blir den första sidvyn för motsvarande besök:

      1. På fliken Program hittar du `adcloud` cookie, och verifiera att cookien innehåller `_les_v` (senaste besök) med värdet `y` och en UTC-epok som går ut om 30 minuter.
      1. Ta bort `ad cloud` cookie och uppdatera sidan.

1. (Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod) Filtrera på `/b/ss` för att se Analytics-träffen.

   ![Filtrera på `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod) Filtrera på `/interact` för att verifiera att nyttolasten för begäran till Edge Network innehåller `advertisingStitchID`.

   ![Filtrera på `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Jämför ID-värdena mellan de två träffarna. Alla värden kommer att finnas i frågesträngsparametrar förutom rapportsvitens-ID i Analytics-träffen, som är URL-sökvägen omedelbart efter `/b/ss/`.

   | ID | Analysparameter | Edge Network | Advertising Cloud-parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS-organisation | `mcorgid` |  | `_les_imsOrgid` |
   | Kompletterande data-ID | sdid |  | `_les_sdid` |
   | Häftnings-ID | stitchId | `advertisingStitchID` under `_adcloud` property |  |
   | Analytics Report Suite | Värdet efter `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud Visitor-ID | mitten |  | `_les_mid` |

   Om ID-värdena matchar varandra bekräftas JavaScript-implementeringen. Advertising Cloud skickar [!DNL Analytics] om det finns någon klicknings- eller vyspårningsinformation på servern.

#### Bekräfta koden med [!DNL Adobe Experience Cloud Debugger]

1. Öppna [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) på din hemsida.
1. Gå till [!UICONTROL Network] -fliken.
1. I [!UICONTROL Solutions Filter] verktygsfält, klicka [!UICONTROL Advertising Cloud] och [!UICONTROL Analytics].
1. I [!UICONTROL Request URL – Hostname] parameterrad, lokalisera `lasteventf-tm.everesttech.net`.
1. I [!UICONTROL Request – Parameters] rad, granska genererade signaler, liknande steg 3 i &quot;[Bekräfta koden med [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementeringar som använder Experience Cloud Identity Service `visitorAPI.js` kod) Kontrollera att `Sdid` parametern matchar `Supplemental Data ID` i Adobe Analytics-filtret.
   * (Implementeringar som använder Experience Platform [!DNL Web SDK] `alloy.js`kod) Kontrollera värdet på `advertisingStitchID` parametern matchar `Sdid` skickas till Experience Platform Edge-nätverket.
   * Om koden inte genereras kontrollerar du att Advertising Cloud-cookien har tagits bort i [!UICONTROL Application] -fliken. Uppdatera sidan och upprepa processen när den har tagits bort.

   ![Granskning [!DNL Analytics for Advertising Cloud] JavaScript-kod i [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]](prerequisites.md)

