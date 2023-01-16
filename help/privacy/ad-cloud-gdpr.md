---
title: Stöd för annonsering i Adobe enligt den allmänna dataskyddsförordningen
description: Lär dig mer om vilka dataförfrågningstyper som stöds, obligatoriska inställnings- och fältvärden samt exempel på API-åtkomstbegäranden som använder äldre produkt-ID:n och returnerade datafält
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Stöd för annonsering i Adobe enligt den allmänna dataskyddsförordningen

*För [!DNL Adobe Advertising Search]; Adobe Advertising DSP. Adobe Advertising Creative; och Adobe Advertising DCO*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om den allmänna dataskyddsförordningen.

Den allmänna dataskyddsförordningen (GDPR), som är en lag som gäller den 25 maj 2018, ger alla individer (registrerade) inom EU:s gränser kontroll över sina personuppgifter och förenklar regelmiljön för den internationella verksamheten. Denna lag gäller alla företag (registeransvariga) som erbjuder varor eller tjänster för att övervaka, övervaka eller samla in personuppgifter från enskilda personer inom EU:s gränser vid den tidpunkt då deras personuppgifter behandlas, oavsett var den registeransvarige befinner sig.

Adobe Experience Cloud fungerar som personuppgiftsbiträde för alla personuppgifter som de tar emot och lagrar för sina kunders räkning. Som personuppgiftsansvarig avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Det här dokumentet beskriver hur [!DNL Advertising Search]; Reklamkreatörer; Reklam DSP (Demand Side Platform). och [!DNL Advertising DCO] ge stöd för de registrerade i GDPR för åtkomst och borttagning av data med hjälp av Adobe Experience Platform Privacy Service API och användargränssnittet för Privacy Service.

Mer information om vad GDPR innebär för ditt företag finns i [GDPR och er verksamhet](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Dataförfrågningstyper som stöds för Adobe-annonsering

Adobe Experience Platform ger företag möjlighet att utföra följande uppgifter:

* Åtkomst till data på cookie-nivå eller data på enhets-ID-nivå (för annonser i mobilappar) inom [!DNL Search], [!DNL Creative], [!DNL DSP], eller [!DNL DCO].
* Ta bort data på cookie-nivå som lagras i [!DNL Search], [!DNL Creative], [!DNL DSP], eller [!DNL DCO] för registrerade i en webbläsare, eller ta bort data på ID-nivå som lagras i [!DNL DSP] för registrerade som använder appar på mobila enheter.
* Kontrollera status för en eller alla befintliga begäranden.

## Nödvändig inställning för att skicka begäranden för Adobe-annonsering

Om du vill begära åtkomst till och ta bort data för Adobe-annonsering måste du:

1. Distribuera ett JavaScript-bibliotek för att hämta och ta bort era cookies för registrerade data. Samma bibliotek, `AdobePrivacy.js`, används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Adobe Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Adobe Advertising kräver det.

   Du bör distribuera biblioteket på den webbsida från vilken de registrerade kan skicka in begäran om åtkomst och borttagning, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta Adobe-cookies (namnområdes-ID: `gsurferID`) så att du kan skicka dessa identiteter som en del av begäran om åtkomst och borttagning via Adobe Experience Platform Privacy Service API.

   När den registrerade begär att få ta bort personuppgifter tar biblioteket också bort den registrerades cookie från den registrerades webbläsare.

   >[!NOTE]
   >
   >Att ta bort personuppgifter skiljer sig från avanmäl dig, vilket stoppar målsättningen för en slutanvändare med målgruppssegment. När en registrerade begär att få ta bort personuppgifter från [!DNL Creative], [!DNL DSP], eller [!DNL DCO], skickar biblioteket också en begäran till Adobe om att avanmäla den registrerade från segmentmålinriktning. För annonsörer med [!DNL Search]rekommenderar vi att du ger de registrerade en länk till [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), som förklarar hur man avanmäler sig från målgruppssegmentsmålgruppsanpassning.

1. Identifiera ditt organisations-ID för Experience Cloud och se till att det är länkat till dina Adobe Advertising-konton.

   Ett Experience Cloud-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med &quot;@AdobeOrg&quot;. De flesta Experience Cloud-kunder har tilldelats ett organisations-ID. Om ditt marknadsföringsteam eller den interna systemadministratören i Adobe inte känner till ditt företags-ID eller inte vet om det har etablerats kontaktar du Adobe kundtjänst på gdprsupport@adobe.com. Du behöver organisations-ID:t för att kunna skicka begäranden till sekretess-API:t med hjälp av `imsOrgID` namnutrymme.

   >[!IMPORTANT]
   >
   >Kontakta företagets Adobe Advertising-representant för att bekräfta att alla era Adobe-annonskonton finns - inklusive [!DNL DSP] Konton eller annonsörer. [!DNL Search] konton, och [!DNL Creative] eller [!DNL DCO] konton - är länkade till ditt företags-ID för Experience Cloud.

1. Använd antingen [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (för automatiska förfrågningar) eller [Privacy Servicens användargränssnitt](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (vid ad hoc-begäran) att skicka in begäran om åtkomst och radering till Adobe för de registrerade samt att kontrollera status för befintliga förfrågningar.

   För annonsörer som har en mobilapp för att interagera med registrerade personer och starta kampanjer med DSP måste du ladda ned de sekretessfärdiga SDK:erna för Experience Cloud. Med Mobile SDK:er kan personuppgiftsansvariga ange statusflaggor för avanmälan, hämta den registrerade personens enhets-ID (namnområdes-ID: deviceID) och skicka begäranden till Privacy Services-API. Din mobilapp kräver SDK version 4.15.0 eller senare.

   När du skickar en begäran om åtkomst för en registrerad returnerar Privacy Services-API information som baseras på den angivna cookien eller det angivna enhets-ID:t, som du sedan måste returnera till den registrerade.

   När du skickar en begäran om borttagning av en registrerad tas cookie-ID:t eller enhets-ID:t och alla kostnads-, klicknings- och intäktsdata som är kopplade till cookien bort från servern.

   >[!NOTE]
   Om ditt företag har flera Experience Cloud-organisations-ID:n måste du skicka separata API-förfrågningar för varje. Du kan dock göra en API-begäran till flera Adobe Advertising-underlösningar ([!DNL Search], [!DNL Creative], [!DNL DSP]och [!DNL DCO]), med ett konto per dellösning.

Alla dessa steg är nödvändiga för Adobe Advertising. Mer information om dessa och andra relaterade uppgifter du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar de objekt du behöver finns i [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Obligatoriska fältvärden i JSON-begäranden om Adobe-annonsering

&quot;&quot;företagskontext&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ditt IMS-organisations-ID-värde*>

`"users":`

* `"key":` &lt;*vanligtvis namnet på den registrerade*>

* `"action":` antingen `**access**` eller `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (som anger [!DNL adcloud] cookie space)

   * `"value":` &lt;*den registrerade personens cookie-ID-värde som hämtats från`AdobePrivacy.js`*>

* `"include": **adCloud**` (som är den Adobe-produkt som är tillämplig på ansökan)

* `"regulation": **gdpr**` (som är den sekretessregel som gäller för begäran)

## Exempel på begäran som skickats av den registrerade med ett användar-ID för Adobe-annonsering som hämtats från `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## Datafält som returneras för åtkomstbegäranden

Nedan följer ett exempel på ett åtkomstsvar för Adobe Advertising.

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
