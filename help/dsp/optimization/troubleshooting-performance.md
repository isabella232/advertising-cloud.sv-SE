---
title: Felsökningsprestanda
description: Se vanliga prestandaproblem och hur du felsöker dem.
feature: Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Felsökningsprestanda

| Problem | Möjlig orsak | Åtgärder att vidta |
| --- | --- | --- |
| Inga utgifter för placering | Monteringen innehåller inte annonser och/eller annonserna är inte aktiva. | Verifiera att alla förväntade annonser är kopplade till placeringen och att de är godkända och aktiva.<br><br>Se även om placeringen innehåller ett anpassat annonseringsschema som kan begränsa flygperioden för varje annons. Om du vill visa annonseringsschemat för en placering från placeringsvyn klickar du på **[!UICONTROL ...]>[!UICONTROL Ad schedule]** bredvid placeringsnamnet. |
|  | De berörda datumen ligger inte inom de konfigurerade flygdatumen. | Kontrollera att flygdatumen är giltiga på kampanj-, paket- och &#x200B;. |
|  | Budgetmålet har uppnåtts och/eller är inte tillräckligt högt. | Kontrollera budgetinställningarna på kampanj-, paket- och placeringsnivåer. |
|  | Kontot har inte tillräckligt med finansiering. | Om du vill se om ditt konto är tillräckligt finansierat går du till **[!UICONTROL Settings]>[!UICONTROL Account]** och tittar på mängden [!UICONTROL Usable Funds]. Kontakta din kontoansvarige på Adobe om du behöver lägga till mer medel. |
|  | Det finns inget lager tillgängligt. | Kontrollera om de angivna lagerkällorna ([!UICONTROL Public], [!UICONTROL Private] eller [!UICONTROL On Demand]) är:<ul><li>Konfigurera korrekt.</li><li>Aktiv och skickad genom auktioner.</li><li>Kompatibel med tillämplig annons- och placeringstyp.</li></ul><br>Om alla lagerkällor är giltiga och aktiva, ska du rikta in ytterligare eller alla lagerkällor när det är möjligt. |
|  | Det finns inga tillgängliga användare. | Kontrollera att de angivna målgruppsmålen innehåller tillräckligt många aktiva användare. Om de inte gör det kan du utöka målgrupperna genom att lägga till fler målgrupper. |
| Låga utgifter för placering | Avsnittet [!UICONTROL Non Bids] i placeringsdiagnostikrapporten visar möjliga orsaker till varför placeringen inte lade något bud. | [Granska  [!UICONTROL Non Bids] ](/help/dsp/campaign-management/reports/placement-diagnostics.md) rapporten för att förstå varför placeringen inte lade något bud.   <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | Placeringen använder [föranbudsfilter](/help/dsp/campaign-management/placements/placement-settings.md) som begränsar budgivning. | Sänk tröskelvärdena för filter före bud med 5 % för att utvärdera balansen mellan utgifter och resultat. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Tänk på att användning av flera placeringsmål, t.ex. förköpsfilter, geos, lager och målgrupper, kan begränsa budgivning och utgifter kumulativt. |
|  | Praktiktjänstgöring har en låg vinstnivå. | Öka [!UICONTROL Max Bid] för att förbättra vinstfrekvensen.<br><br><b>Obs! </b> Lagerpriserna kan variera beroende på placeringens inriktning.<br><br>En 10-procentig vinst-frekvens anses vara hälsosam. |
|  | Ett lågt antal lager är tillgängligt. | Ange ytterligare eller alla lagerkällor om det är möjligt.<br><br>Tänk på att användning av flera placeringsmål, t.ex. förköpsfilter, geos, lager och målgrupper, kan begränsa budgivning och utgifter kumulativt. |
|  | Ett lågt antal användare är tillgängliga. | Kontrollera att de angivna målgruppsmålen innehåller tillräckligt många aktiva användare. Om de inte gör det kan du utöka målgrupperna genom att lägga till fler målgrupper.<br><br>Tänk på att användning av flera placeringsmål, t.ex. förköpsfilter, geos, lager och målgrupper, kan begränsa budgivning och utgifter kumulativt. |
|  | Paketet innehåller ett stort antal aktiva placeringar. | Minska antalet aktiva placeringar i paketet eller öka den totala paketbudgeten.<br><br>Om paketet har många placeringar men inte tillräckligt med budget, kanske DSP inte kan allokera tillräckligt med budget till varje placering. Varje placering bör ha möjlighet att tillbringa minst 2 USD/dag. Om ditt paket till exempel har en budget på 10 USD/dag är det bäst att ta med fem eller färre platser. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md)

