---
title: Adobe Advertising Cloud support for the California Consumer Privacy Act &#58; Stöd för åtkomst och borttagning av konsumentdata
description: Lär dig mer om vilka dataförfrågningstyper som stöds, obligatoriska inställnings- och fältvärden samt exempel på API-åtkomstbegäranden som använder äldre produkt-ID:n och returnerade datafält.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Adobe Advertising Cloud Support for the California Consumer Privacy Act: Stöd för åtkomst och borttagning av konsumentdata

*För Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP och Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om Kaliforniens konsumentsekretesslag.

California Consumer Privacy Act (CCPA) är Kaliforniens nya integritetslag, som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina personuppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Advertising Cloud support så att ditt företag kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av Advertising Cloud produkter och tjänster, inklusive hantering av förfrågningar om åtkomst och radering av personuppgifter och hantering av förfrågningar om att avanmäla försäljning av personuppgifter.

I det här dokumentet beskrivs hur Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) och [!DNL Media Optimizer DCO] - som tjänsteleverantörer - stöder konsumenternas rättigheter att få tillgång till och ta bort personuppgifter med Adobe [!DNL Experience Platform Privacy Service API] och [!DNL Privacy Service UI].

Mer information om hur Advertising Cloud DSP stöder konsumentens rätt att avanmäla sig från försäljning av personuppgifter finns i [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Stöd för avanmälan från konsumenter](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

Mer information om sekretessavtal för CCPA för Adobe finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Dataförfrågningstyper som stöds för Advertising Cloud

Adobe Experience Platform ger företag möjlighet att utföra följande uppgifter:

* Få tillgång till data på cookie-nivå eller data på enhets-ID-nivå (för annonser i mobilappar) i [!DNL Search], [!DNL Creative], [!DNL DSP] eller [!DNL DCO].
* Ta bort data på cookie-nivå som lagras i [!DNL Search], [!DNL Creative], [!DNL DSP] eller [!DNL DCO] för konsumenter med en webbläsare; eller ta bort ID-nivådata som lagras i [!DNL DSP] för konsumenter som använder appar på mobila enheter.
* Kontrollera status för en eller alla befintliga begäranden.

## Nödvändiga inställningar för att skicka begäranden för Advertising Cloud

Om du vill begära åtkomst till och radera konsumentpersonuppgifter från Advertising Cloud måste du:

1. Distribuera ett JavaScript-bibliotek för att hämta och ta bort kundens cookies. Samma bibliotek, `AdobePrivacy.js`, används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Adobe Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Advertising Cloud kräver det.

   Du bör distribuera biblioteket på webbsidan från vilken dina kunder kan skicka in begäran om åtkomst och borttagning, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta Adobe-cookies (namnområdes-ID: `gsurferID`) så att du kan skicka dessa identiteter som en del av begäran om åtkomst och borttagning via [!DNL  Adobe Experience Platform Privacy Service API].

   När kunden begär att få ta bort personuppgifter tar biblioteket också bort kundens cookie från kundens webbläsare.

   >[!NOTE]
   >
   >Att ta bort personuppgifter skiljer sig från att avanmäla sig, vilket förhindrar målgruppsanpassningen för en slutanvändare med målgruppssegment. När en konsument begär att få ta bort personuppgifter från [!DNL Creative], [!DNL DSP] eller [!DNL DCO], skickar biblioteket också en begäran till Advertising Cloud om att kunden ska avanmäla sig från segmentmål. För annonsörer med [!DNL Search] rekommenderar vi att du ger dina kunder en länk till [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), där det förklaras hur du avanmäler dig från målgruppsanpassning för målgruppssegment.

1. Identifiera ditt IMS-organisations-ID och se till att det är länkat till dina Advertising Cloud-konton.

   Ett IMS-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med @AdobeOrg. De flesta Adobe Experience Cloud-kunder har tilldelats ett IMS-organisationsnummer. Om ditt marknadsföringsteam eller den interna systemadministratören i Adobe inte känner till din organisations IMS-organisation eller inte vet om den har etablerats kan du kontakta Adobe kundtjänst på gdprsupport@adobe.com. Du måste ha IMS-organisations-ID för att kunna skicka begäranden till sekretess-API:t.

   >[!IMPORTANT]
   >
   >Kontakta företagets Advertising Cloud-representant för att bekräfta att alla din organisations Advertising Cloud-konton - inklusive [!DNL DSP]-konton eller annonsörer, [!DNL Search]-konton och [!DNL Creative]- eller [!DNL DCO]-konton - är kopplade till ditt IMS Org ID.

1. Använd antingen [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (för automatiska begäranden) eller [Privacy Servicens användargränssnitt](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (för ad hoc-begäranden) för att skicka begäranden om åtkomst och radering av personuppgifter till Advertising Cloud för konsumenternas räkning och för att kontrollera status för befintliga förfrågningar.

   För annonsörer som har en mobilapp för att interagera med kunder och lansera kampanjer med [!DNL DSP] måste du ladda ned de sekretessfärdiga SDK:erna för Experience Cloud. Med Mobile SDK:er kan företag ange statusflaggor för avanmälan, hämta konsumentens enhets-ID (namnområdes-ID: `deviceID`) och skicka begäranden till Privacy Service-API:t. Din mobilapp kräver SDK version 4.15.0 eller senare.

   När du skickar en begäran om konsumentåtkomst returnerar Privacy Service-API:t information om en konsument baserat på den angivna cookien eller enhets-ID:t, som du sedan måste returnera till konsumenten.

   När du skickar en begäran om att ta bort en kund tas cookie-ID:t eller enhets-ID:t och alla kostnads-, klicknings- och intäktsdata som är kopplade till cookien bort från servern.

   >[!NOTE]
   Om ditt företag har flera Adobe Experience Cloud Identity Management Service Organization ID:n (IMS Org ID:n) måste du skicka separata API-begäranden för varje. Du kan dock göra en API-begäran till flera Advertising Cloud-underlösningar ([!DNL Search], [!DNL Creative], [!DNL DSP] och [!DNL DCO]), med ett konto per underlösning.

Alla dessa steg är nödvändiga för att få support från Advertising Cloud. Mer information om dessa och andra relaterade uppgifter som du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar de objekt du behöver, finns i [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Obligatoriska fältvärden i Advertising Cloud JSON-begäranden

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;>ditt IMS-organisations-ID-värde *>*

&quot;användare&quot;:

* `"key":` &lt;>vanligtvis kundens *namn>*

* `"action":` antingen  `**access**` eller  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (vilket anger adcloud cookie space)

   * `"value":` &lt;>den faktiska kundens cookie ID-värde som hämtats från  `AdobePrivacy.js`*>*

* `"include": **adCloud**` (som är den Adobe-produkt som är tillämplig på ansökan)

* `"regulation": **ccpa**` (som är den sekretessregel som gäller för begäran)

## Exempel på begäran som har skickats av en konsument med ett användar-ID från Advertising Cloud som har hämtats från AdobePrivacy.js

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## Datafält som returneras för åtkomstbegäranden

Nedan följer ett exempel på ett personligt informationsåtkomstsvar för Advertising Cloud.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
