---
title: Adobe reklamintegrering med Adobe Audience Manager
description: Lär dig mer om de olika sätt på vilka Adobe Advertising kan utbyta data med Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe reklamintegrering med Adobe Audience Manager

Ni kan integrera Adobe Advertising med Audience Manager på följande sätt.

## Synkronisera Audience Manager och andra [!DNL Adobe] Segment för annonsinriktning

[!DNL Search] och DSP kan hämta in metadata, hierarkidata och unika målgruppsdata för alla annonsörers eller reklambyråers Audience Manager och andra [!DNL Adobe] målgrupper. Den här unika anslutningen är bara tillgänglig för marknadsförare som använder Adobe Advertising. Se &quot;[Importera Adobe Audience Manager-segment för annonsinriktning](/help/integrations/audience-manager/import-audiences.md).&quot;

### Använd Audience Manager och annat [!DNL Adobe] Segment att skapa [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Search] endast*

Inom [!DNL [!DNL Search]], du kan skapa [!DNL Google Ads] Google kund matchar målgrupper från användar-ID:n med era befintliga Audience Manager-segment som har [!UICONTROL Adobe Media Optimizer (HTTP)] och [!UICONTROL Adobe Media Optimizer Batch Destination] som destinationer. ([!DNL Media Optimizer] är ett tidigare namn för [!DNL [!DNL Search]].) Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas i Adobe Experience Cloud med [!DNL People core service]. Mer information finns i produkthjälpen i [!DNL] [!DNL Search]].

[Kunden matchar målgrupper från användar-ID:n](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchning och taggbaserade målgrupper för webbplatser.

Om du vill skapa nödvändiga användar-ID:n måste du använda en JavaScript-tagg för Adobe Advertising <!-- with a user ID parameter -->på era webbplatser. Kontakta din [!DNL [!DNL Search]] kontoteam för mer information.

![process för att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads] kampanjer som [mål eller undantag på kampanjnivå eller annonsnivå](#audience-manager-targets).

### Använd Audience Manager och andra [!DNL Adobe] Segment att rikta eller exkludera annonser {#audience-manager-targets}

* (Valda annonsörer med [!DNL] [!DNL Search]]) Du kan använda valfritt [!DNL Google Ads] målgrupper som [skapad med [!DNL Adobe] segment](#audience-manager-google-audiences) som kampanjnivå eller annonsnivå som mål eller undantag i er [!DNL Google Ads] kampanjer.

* (Annonsörer med DSP) Du kan använda dina befintliga [!DNL Adobe] segment som mål för era annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Advertisers with Advertising Creative) Du kan använda dina befintliga [!DNL Adobe] segment som mål för specifika kreatörer i era annonsupplevelser.

>[!NOTE]
>
>Mer information om hur du skapar målgrupper i Audience Manager och Experience Cloud [!DNL Audience Library] gränssnitt, och vanliga användningsområden för olika typer av målgrupper, se[Alternativ för att skapa målgrupper](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Skicka DSP data för medieexponering till Audience Manager

*Annonsörer med endast DSP*

DSP kunder med Adobe Audience Manager kan hämta in data från annonskampanjer med pixelanrop till Audience Manager. Sedan kan ni använda kampanjdata för att bygga regelbaserade egenskaper, som ni kan använda för att definiera nya segment för att möjliggöra olika DSP, som mer avancerad segmentering, frekvenshantering, marknadsföringsanalyser och rapportinsikter.

Se &quot;[Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; för mer information.

## Få djupare insikter om webbplatsaktivitet med Audience Analytics

Adobe Advertising customers with [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kan skicka både Adobe-annonsdata och Audience Manager-segment till [!DNL Analytics] för bättre insikter om webbplatsaktiviteter.

Mer information finns i &quot;[[!DNL Adobe][!DNL Audience Analytics] för Adobe-reklamkunder](/help/integrations/audience-manager/audience-analytics.md).&quot;
