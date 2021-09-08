---
title: JavaScript-kod för [!DNL Analytics for Advertising Cloud]
description: JavaScript-kod för [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# JavaScript-kod för [!DNL Analytics for Advertising Cloud]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

*Annonsörer endast med Advertising Cloud DSP*

För Advertising Cloud DSP spårar [!DNL Analytics for Advertising Cloud]-integreringen genomskärnings- och klickningsinteraktioner mellan webbplatser. Klicka-för-klickningsbesök spåras av Adobe Analytics standardkod på dina webbsidor. koden [!DNL Analytics] hämtar parametrarna för AMO ID och EF ID i landningssidans URL och spårar dem i deras respektive reserverade eVars. Du kan spåra visningar genom att distribuera två rader JavaScript-kod på dina webbsidor.

På den första sidvyn vid ett besök på webbplatsen kontrollerar Advertising Cloud JavaScript-koden om besökaren tidigare har sett eller klickat på en annons. Om användaren tidigare har kommit in på webbplatsen via en klickning eller inte har sett någon annons, ignoreras besökaren. Om besökaren har sett en annons och inte har öppnat webbplatsen via ett klick i [klickfönstret](/help/integrations/analytics/prerequisites.md#lookback-a4adc) i Advertising Cloud, använder Advertising Cloud JavaScript-koden [Experience Cloud ID-tjänsten](https://experienceleague.adobe.com/docs/id-service/using/home.html) för att generera ett extra ID (`SDID`), som används för att sammanfoga data från Advertising Cloud till besökarens Adobe Analytics-träff. Adobe Analytics frågar sedan Advertising Cloud efter det AMO-ID och EF-ID som är kopplat till annonsplaceringen. AMO-ID:t och EF-ID:n fylls sedan i i deras respektive eVars. Dessa värden gäller under en angiven period (som standard 60 dagar).

[!DNL Analytics] skickar uppgifter om webbplatstrafiken (t.ex. sidvisningar, besök och hur lång tid som tillbringats) och  [!DNL Analytics]  anpassade händelser eller standardhändelser till Advertising Cloud per timme, med EF-ID som nyckel. Dessa [!DNL Analytics]-mått körs sedan genom Advertising Cloud attribueringssystem för att koppla konverteringarna till klicknings- och exponeringshistoriken.

>[!NOTE]
>
>Spårningslogiken i Advertising Cloud JavaScript finns på Adobe och påverkar därmed inte sidans inläsningstid.
>
>Logiken för dataanslutningen [!DNL DCM] till [!DNL Analytics] (med [!DNL Google Campaign Manager 360]) för Advertising Cloud DSP finns däremot på klientsidan. Klientsidans sammanslagning saktar ned sidbelastningen och ökar risken för dataförlust. Detta inträffar eftersom JavaScript-koden [!DNL Analytics] måste pinga [!DNL DoubleClick] och vänta på att [!DNL DoubleClick] ska skicka tillbaka de senaste klicknings-/visningsdata till [!DNL Analytics]. När ditt [!DNL DSP]-team konfigurerar dataanslutningen [!DNL DCM] måste du ange hur länge du vill fördröja sidan.

## Distribuera JavaScript-koden

JavaScript-biblioteket består av två rader som gör att [!DNL Analytics] och Advertising Cloud kan kommunicera med varandra. Om [!DNL Analytics for Advertising Cloud]-integreringen slutfördes under Advertising Cloud-implementeringen bör du ha fått den här koden med instruktioner om hur den ska distribueras.

Om du inte redan har koden kontaktar du Advertising Cloud supportteam.

### Placera koden där

JavaScript-funktionen [!DNL Analytics for Advertising Cloud] måste komma efter Experience Cloud ID-tjänsten men före Analytics App Measurement-koden så att det kompletterande ID:t (`SDID`) kan inkluderas i Analytics-anropet.

![Kodplacering](/help/integrations/assets/a4adc-code-placement.png)

### Verifierar koddistribution

Du kan utföra valideringen med vilken paketsniffer som helst av verktygstyperna (till exempel [!DNL Charles], [!DNL Fiddler] eller [!DNL Chrome Developer Tools]) genom att jämföra värdena för de fyra ID:n mellan begäran som går till Advertising Cloud och begäran som går till [!DNL Analytics] enligt instruktionerna nedan.

#### Bekräfta koden med [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öppna [!DNL Chrome Developer Tools] och klicka på fliken **Nätverk**.
1. Läs in en webbsida som innehåller JavaScript-koden [!DNL Analytics for Advertising Cloud].
1. Filtrera fliken [!UICONTROL Network] med `last` och granska två rader:

   ![Filtrera vid senaste](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Den första raden är anropet till JavaScript-biblioteket och heter `last-event-tag-latest.min.js`.
   * Den andra raden är det samtal som skickar begäran till Advertising Cloud. Den börjar så här: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Om du inte ser samtalet till Advertising Cloud är det inte säkert att det är första sidan av besöket. I testsyfte kan du ta bort cookien så att nästa anrop blir den första sidvyn för motsvarande besök:

      1. På fliken Program letar du reda på cookien `adcloud` och kontrollerar att cookien innehåller `_les_v` (senaste besök) med värdet `y` och en UTC-epoch-tidsstämpel som går ut om 30 minuter.
      1. Ta bort cookien `ad cloud` och uppdatera sidan.
1. Filtrera på `/b/ss` för att se Analytics-träffen.

   ![Filtrera på  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. Jämför ID-värdena mellan de två träffarna. Alla värden kommer att finnas i frågesträngsparametrar förutom rapportsvitens-ID i Analytics-träffen, som är URL-sökvägen omedelbart efter `/b/ss/`.

   | ID | Analysparameter | Advertising Cloud-parameter |
   |--- |--- |--- |
   | Experience Cloud IMS-organisation | `mcorgid` | `_les_imsOrgid` |
   | Kompletterande data-ID | sdid | `_les_sdid` |
   | Analytics Report Suite | Värdet efter `/b/ss/` | `_les_rsid` |
   | Experience Cloud Visitor-ID | mitten | `_les_mid` |

   Om ID-värdena matchar varandra bekräftas JavaScript-implementeringen. Advertising Cloud skickar eventuella klicknings- eller genomskinlighetsspårningsdetaljer till [!DNL Analytics]-servern om sådana finns.

#### Bekräfta koden med [!DNL Adobe Experience Cloud Debugger]

1. Öppna [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) på din hemsida.
1. Gå till fliken [!UICONTROL Network].
1. Klicka på [!UICONTROL Advertising Cloud] och [!UICONTROL Analytics] i verktygsfältet [!UICONTROL Solutions Filter].
1. Leta reda på `lasteventf-tm.everesttech.net` i parameterraden [!UICONTROL Request URL – Hostname].
1. Granska de genererade signalerna på raden [!UICONTROL Request – Parameters*], liknande steg 3 i &quot;[Bekräfta koden med [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * Kontrollera att parametern `SDID` matchar `Supplemental Data ID` i Adobe Analytics-filtret.
   * Om koden inte genereras kontrollerar du att Advertising Cloud-cookien har tagits bort på fliken [!UICONTROL Application]. Uppdatera sidan och upprepa processen när den har tagits bort.

   ![Granska  [!DNL Analytics for Advertising Cloud] JavaScript-kod i  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Översikt över [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Krav och viktig information för implementering [!DNL Analytics for Advertising Cloud]](prerequisites.md)

