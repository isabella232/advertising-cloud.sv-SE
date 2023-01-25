---
title: 'Adobe Advertising support for the California Consumer Privacy Act : Konsumentsupport'
description: Läs mer om stöd för att hämta in förfrågningar om att avanmäla sig från försäljning.
feature: CCPA
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Konsumentens avanmälan från försäljningssupport

*För Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Innehållet i detta dokument är inte juridisk rådgivning och är inte avsett att ersätta juridisk rådgivning. Kontakta ditt juridiska ombud för råd om Kaliforniens konsumentsekretesslag.

California Consumer Privacy Act (CCPA) är Kaliforniens nya integritetslag, som träder i kraft den 1 januari 2020. CCPA ger invånare i Kalifornien nya rättigheter när det gäller personuppgifter och ålägger dataskyddsansvar för vissa enheter som bedriver verksamhet i Kalifornien. CCPA ger konsumenterna rätt att få tillgång till och radera sina uppgifter samt rätt att avanmäla vissa aktiviteter som kvalificerar som &quot;sälja&quot; personuppgifter till tredje part.

Som företag avgör du vilka personuppgifter Adobe Experience Cloud behandlar och lagrar å dina vägnar.

Som tjänsteleverantör tillhandahåller Adobe Advertising stöd till ert företag så att det kan uppfylla sina skyldigheter enligt CCPA som är tillämpliga på användningen av marknadsföringsprodukter och -tjänster från Adobe, inklusive hantering av konsumentförfrågningar om tillgång till och radering av personuppgifter och hantering av konsumentförfrågningar om att avanmäla försäljning av personuppgifter.

I det här dokumentet beskrivs hur Adobe Advertising Demand Side Platform (DSP), som tjänsteleverantör, stöder konsumentens rätt att välja bort&quot;försäljning&quot; av&quot;personuppgifter&quot;, eftersom varje term definieras av CCPA. Det innehåller information om hur du kan förmedla begäran om att avanmäla dig från försäljning till Adobe Advertising och hur du hämtar rapporter om din organisations begäran om att avanmäla dig från försäljning.

Mer information om hur [!DNL Advertising Search]; Reklamkreatörer; och [!DNL Advertising DCO] ge stöd för åtkomst till och radering av personuppgifter för konsumenter, se [Adobe Advertising Support for the California Consumer Privacy Act: Stöd för åtkomst och borttagning av konsumentdata](/help/privacy/ccpa/ccpa-access-delete.md).

Mer information om Adobe sekretessavtal för CCPA finns i [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Kommunicera konsumentförfrågningar om avanmälan vid försäljning till Adobe

Du kan förmedla önskemål om avanmälan från försäljning till konsumenter genom att antingen:

* ett avanmälningssegment för CCPA som skapats i DSP
* Adobe Experience Platform Privacy Service API

### Metod 1: Kommunicera CCPA-begäran om avanmälan vid försäljning med en [!UICONTROL CCPA Opt-Out-of-Sale] Segment i DSP

>[!NOTE]
>
>Användarna stannar kvar i segmenten för avanmälan av CCPA på obestämd tid.

1. Logga in på annonsörens konto i DSP [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Skapa ett CCPA-segment för avanmälan och implementera segmentpixeln för att hämta avanmälningsbegäranden](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Metod 2: Kommunicera CCPA-förfrågningar om avanmälan vid försäljning med Adobe Experience Platform Privacy Service API

*Annonsörer tilldelade endast ett Adobe Experience Cloud-organisations-ID*

1. Distribuera ett JavaScript-bibliotek för att hämta kundens cookies. Samma bibliotek, `AdobePrivacy.js`, används för alla Adobe Experience Cloud-lösningar.

   >[!IMPORTANT]
   >
   >Begäranden till vissa Adobe Experience Cloud-lösningar kräver inte JavaScript-biblioteket, men förfrågningar till Adobe Advertising kräver det.

   Du bör distribuera biblioteket på webbsidan där dina kunder kan skicka in begäran om att avanmäla dig, till exempel företagets integritetsportal. Biblioteket hjälper dig att hämta Adobe-cookies (namnområdes-ID: `gsurferID`) så att du kan skicka in dessa identiteter som en del av begäran om att avanmäla dig via Adobe Experience Platform Privacy Service API.

1. Identifiera ditt organisations-ID för Experience Cloud och se till att det är länkat till dina Adobe Advertising-konton.

   Ett Experience Cloud-organisations-ID är en 24 tecken lång alfanumerisk sträng som läggs till med &quot;@AdobeOrg&quot;. De flesta Experience Cloud-kunder har tilldelats ett organisations-ID. Om ditt marknadsföringsteam eller den interna systemadministratören i Adobe inte känner till ditt företags-ID eller inte vet om det har etablerats kontaktar du Adobe kundtjänst på gdprsupport@adobe.com. Du behöver organisations-ID:t för att kunna skicka begäranden till sekretess-API:t med hjälp av `imsOrgID` namnutrymme.

   >[!IMPORTANT]
   >
   >Kontakta företagets Adobe Advertising-representant för att bekräfta att alla era Adobe-annonskonton finns - inklusive [!DNL DSP] Konton eller annonsörer. [!DNL Search] konton, och [!DNL Creative] eller [!DNL DCO] konton - är länkade till ditt företags-ID för Experience Cloud.

1. Använd Adobe Experience Platform Privacy Service API för att [skicka begäran om avanmälan](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) till Adobe Advertising för konsumenternas räkning och för att kontrollera status för befintliga förfrågningar.

   Se bilagan nedan för ett exempel på en begäran om avanmälan från försäljning.

   >[!NOTE]
   Om ditt företag har flera Experience Cloud-organisations-ID:n måste du skicka separata API-förfrågningar för varje. Du kan dock göra en API-begäran till flera Adobe Advertising-underlösningar ([!DNL Search], [!DNL Creative], [!DNL DSP]och [!DNL DCO]), med ett konto per dellösning.

Alla dessa steg är nödvändiga för att få stöd från Adobe Advertising. Mer information om dessa och andra relaterade uppgifter du behöver utföra med Adobe Experience Platform Privacy Service, och var du hittar de objekt du behöver finns i [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Hämtar rapporter om konsumenter som har lämnat in begäran om avanmälan vid försäljning

Adobe Advertising genererar månatliga rapporter om ID:n som kunder har skickat in för att avanmäla sig från försäljning för kontot. Varje rapport är tillgänglig som en tabbseparerad textfil komprimerad till GZIP-format. Data konsoliderar begäranden som samlats in med CCPA-segment för avanmälan från försäljning som skapats i DSP och alla inskickade data via Privacy Services-API. Användar-ID:n som används i CCPA-segment för avanmälan identifieras av segment och annonsörer. Rapporterna skapas den första i varje månad för föregående månad. Till exempel är användarlistan för juni tillgänglig den 1 juli.

Du kan hämta länkar till de månadsrapporter som har skapats under de senaste tre månaderna, antingen från DSP eller genom att använda DSP Advertising [!DNL Trafficking API]. Varje länk gäller i sju dagar, men uppdateras varje gång en kund försöker hämta en länk.

### Metod 1: Få rapporter om kundernas avanmälan till utförsäljning inom DSP

1. Logga in på annonsörens konto i DSP [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Hämta rapporterna](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Metod 2: Hämta rapporter om konsumentens avanmälan vid försäljning med hjälp av DSP [!DNL Trafficking API]

Den här funktionen är tillgänglig för organisationer som använder [!DNL Trafficking API]. Dokumentationen för [!DNL Trafficking API] för mer information.

Om din organisation inte använder [!DNL Trafficking API] men är intresserad av mer information kan du kontakta [!DNL Adobe] kontoteam.

## Bilaga: Exempel [!UICONTROL CCPA Opt-Out-of-Sale] Begär Privacy Service-API-användare

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

där:

* `"namespace": "AdCloud"` anger `AdCloud` cookie space, och motsvarande värde är kundens cookie-ID som hämtats från `AdobePrivacy.js`
* `"include": ["AdCloud"]` anger att begäran gäller Adobe-reklam
