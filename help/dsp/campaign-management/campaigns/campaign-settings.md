---
title: Kampanjinställningar
description: Se beskrivningar av tillgängliga kampanjinställningar.
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# Kampanjinställningar

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Kampanjnamnet.

**[!UICONTROL Advertiser]:** (Skrivskyddat för befintliga kampanjer) Den tillämpliga annonseraren (varumärke). Välj en befintlig annonsör eller skapa en ny.

**[!UICONTROL Advertiser URL]:** Annonsörens officiella sida. Det här fältet snabbar upp er process för godkännande av annonser med lagerpartners.

**[!UICONTROL Timezone]:** (Skrivskyddat för befintliga kampanjer) Tidszonen för rapportering och budgivning.

**[!UICONTROL Customer PO]:** (Valfritt) En kundinköpsorder för infogningsordern/inköpsordern.

**[Kampanjdatum]:** Kampanjens start- och slutdatum.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Om marginaler ska hanteras för kampanjen:  *[!UICONTROL Yes]* eller  *[!UICONTROL No]* (standardvärdet).

När du väljer *[!UICONTROL Yes],* anger du marginaltyp och belopp:

* **[!UICONTROL Margin Type]:** Marginaltypen. Du kan inte ändra marginaltypen när du har aktiverat marginalhantering och sparat kampanjen.

   * *[!UICONTROL Fixed]:* (standardvärdet) Tillåter att Advertising Cloud DSP beräknar automatiskt och sätter ändar baserat på en fast marginalprocent av  [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Låter dig hantera marginaler ända ned till placeringsnivån genom att ange ett separat  [!UICONTROL Budget Reserve %] och  [!UICONTROL Gross Budget] för varje paket och placering i kampanjen. Advertising Cloud DSP optimerar utifrån den ekonomiska effektiviteten för varje placering, utan att garantera en viss marginal. Använd detta för infogningsorder som består av flera radobjekt för vilka du har godkänt att leverera ett fast antal enheter eller enhetstyper till en fast ränta.

* **[!UICONTROL Fixed Margin %]:** (Endast kampanjer med fasta marginaler) Standardkoden för varje infogningsorder  <!-- impression? -->, i procent. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

* **[!UICONTROL Budget Reserve %]:** (Endast kampanjer med fasta marginaler; (valfritt) Reserverar en angiven procentandel av  [!UICONTROL Gross Budget] behållaren som en skyddsåtgärd. Detta belopp dras av från [!UICONTROL Gross Budget] för att definiera nettokampanjbudgeten.

**[!UICONTROL Gross Budget]:** (Kampanjer med endast marginalhantering) Bruttokampanjbudgeten, innan de angivna marginaljusteringarna tillämpas.

Du kan lägga till ytterligare en daglig, vecko- eller månadsbudget (brutto):

1. Klicka på **[!UICONTROL Add an additional Gross Budget]**.

1. Ange **[!UICONTROL Gross Budget]** och välj budgetintervallet: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* eller *[!UICONTROL Monthly]*.

Den totala nettobudgeten, som är utgiftstaket för kampanjen, beräknas automatiskt baserat på marginalinställningarna och anges under det här värdet.

**[!UICONTROL Budget]:** (Kampanjer utan marginalhantering) Den övergripande kampanjbudgeten.

**[!UICONTROL Estimated Tax Withholding]:** Innehåller en procentandel av de totala utgifterna över annonsavgifter, annonsavgifter och/eller datarvoden på kontonivån för nationella eller lokala skatter. Kurser är uppskattningar av budgeterings- och kostnadsredovisningsändamål, så de fakturerade skattesatserna kan variera.

Så här beräknar du källskatt:

1. Klicka på **[!UICONTROL Update rates here]**.

1. Ange **[!UICONTROL Estimated tax rate]** som en procentandel.

1. Markera kryssrutan bredvid varje avgiftstyp för vilken du vill hålla inne skatt. Avgiftstyperna är:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gäller alla utgifter för Advertising Cloud DSP-media, inklusive skatter på kampanjhanteringsavgifter.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gäller för alla utgifter på Advertising Cloud DSP utom för media och data. exklusive moms för kampanjhanteringsavgifter

   * *[!UICONTROL Include estimated tax - data fee]:* Gäller alla datatillgångar på Advertising Cloud DSP.

1. Klicka på **[!UICONTROL Submit]**.

>[!NOTE]
>
>* I USA kan olika länder ta med skatteavgifter i annonser, annonsservrar och data. För organisationer i andra länder ska alla tre kategorier av avgifter tas med i beräkningen av momsen.
>
>* Du kan även konfigurera dessa värden i kontots avgiftsinställningar.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (Skrivskyddat för befintliga kampanjer som skapats sedan den 22 juni 2020; inte tillgängligt för kampanjer som skapats före den 22 juni 2020) Den nivå på vilken Advertising Cloud ska rikta annonser och tillämpa frekvensbegränsningar:  *Samma* enhet om du vill rikta en enhet eller  ** Peopol mot en person på alla deras kända enheter.

**[!UICONTROL Device Graph]:** (Skrivskyddat för befintliga kampanjer; kampanjer med personbaserad målinriktning på olika enheter) Enhetsgrafen som ska användas för målinriktning på olika enheter och frekvenshantering:

* *[!UICONTROL LiveRamp - U.S. only]:* Tillgängligt för alla annonsörer för målgruppsanpassning på 0,35 CPM för visningar som levereras med hjälp av  [!DNL LiveRamp] enhetsdiagrammet (d.v.s. för enheter som inte hittas i målgruppssegmenten). Ni kan ange målinriktning mellan olika enheter på placeringsnivå.

   Det här alternativet är även tillgängligt för alla annonsörer, utan avgifter, för frekvenshantering och attribueringsmätning.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Endast tillgängligt för Adobe Experience Cloud- [!DNL Device Co-op] deltagare utan extra kostnad.

>[!TIP]
>
>Om annonsören även använder enhetsövergripande attribuering är det bästa sättet att använda samma inställningar för enhetsgrafer för målinriktning och frekvenshantering som de som anges i annonsörens inställningar för enhetsövergripande attribuering. Om du väljer ett annat enhetsdiagram för kampanjen kan det uppstå rapporteringsavvikelser.

**[!UICONTROL Frequency Cap]:** (Valfritt) Det antal gånger som en unik enhet eller person (beroende på angivet  [!UICONTROL Cross Device Level]värde) kommer att få annonser från kampanjen. Alternativen är *[!UICONTROL Unlimited]* eller ett specifikt belopp per dag, vecka eller månad.

>[!NOTE]
>
> Du kan ange frekvensgränser på kampanj-, paket- och placeringsnivåer. DSP respekterar det striktaste frekvenstaket i kampanjhierarkin.

**[!UICONTROL Packages]:** De  [](/help/dsp/campaign-management/packages/package-about.md) paket som ska inkluderas i kampanjen. Välj befintliga paket och/eller skapa paket som ska inkluderas. Om du skapar paket kan du läsa beskrivningar om [paketinställningarna](/help/dsp/campaign-management/packages/package-settings.md) för mer information.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Följande inställningar aktiverar endast mät- och rapporteringsfunktioner. Prestandaoptimering utförs endast på paket- och placeringsnivå.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Valfritt) Möjliggör  [!DNL IAS] mätning och rapportering av visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Measure On]:** Det lager som ska mätas:  *[!UICONTROL Display and VPAID video inventory]* (standard) eller  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >Videosynlighet kan endast mätas i VPAID-lager.

* **[!UICONTROL IAS Account ID (AnID)]:** (Advertisers with their own  [!DNL IAS] accounts; valfritt) Organisationens  [!DNL IAS] konto-ID, som  [!DNL IAS] faktureras direkt för användning.

* **[!UICONTROL IAS Team ID]:** (Advertisers with their own  [!DNL IAS] accounts; (valfritt) ID:t för organisationens  [!DNL IAS] konto, som  [!DNL IAS] faktureras direkt för användning.  <!-- verify -->

**[!UICONTROL MOAT]:** (Valfritt) Möjliggör  [!DNL MOAT] mätning och rapportering av visningsbarhet, bedrägeri, varumärkessäkerhet och målgruppsverifiering. Ytterligare avgifter tillkommer.

#### Målgruppsverifiering

**[!UICONTROL Nielsen]:** (Valfritt) Gör det möjligt att  [!DNL Nielsen] mäta och rapportera målgruppsverifiering med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Target Gender]:** Det kön som målet ska vara:  *[!UICONTROL Both]* (standard),  *[!UICONTROL Male]* eller  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Det åldersintervall som ska anges som mål. Använd vänster och höger skjutreglage för att minska intervallet efter behov.

* **[!UICONTROL Target Country]:** (Valfritt) Ett land att rikta sig till. [!DNL Nielsen] kommer endast att mäta visningar i de länder som stöds.

**[!UICONTROL comScore vCE]:** (Valfritt) Gör det möjligt att  [!DNL Comscore validated Campaign Essentials (vCE)] mäta och rapportera målgruppsverifiering med de angivna inställningarna. Ytterligare avgifter tillkommer.

* **[!UICONTROL Target Gender]:** Det kön som målet ska vara:  *[!UICONTROL Both]* (standard),  *[!UICONTROL Male]* eller  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Det åldersintervall som ska anges som mål. Använd vänster och höger skjutreglage för att minska intervallet efter behov.

* **[!UICONTROL Target Country]:** (Valfritt) Ett land att rikta sig till. [!DNL Comscore] kommer endast att mäta visningar i de länder som stöds.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Aktiverar förstahandsmätning och rapportering av visningsbarhet med hjälp av  [!DNL IAB Open Video Viewability (OpenVV)] tekniken, baserat på den angivna känslighetsnivån:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Om kampanjhantering](campaign-about.md)
>* [Skapa en kampanj](campaign-create.md)
>* [Redigera en kampanj](campaign-edit.md)

