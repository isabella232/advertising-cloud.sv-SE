---
title: Advertising Cloud-integrering med Adobe Audience Manager
description: Läs om de olika sätten Advertising Cloud kan utbyta data med Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: c761c96b32171bcfba12ed4a39235e6e8b6f6d34
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Advertising Cloud-integrering med Adobe Audience Manager

Du kan integrera Advertising Cloud med Audience Manager på följande sätt.

## Synkronisera Audience Manager och andra [!DNL Adobe] Segment för annonsinriktning

Advertising Cloud Search och Advertising Cloud DSP kan hämta in metadata, hierarkidata och unika målgruppsdata för alla annonsörers och reklambyråers Audience Manager och andra [!DNL Adobe] målgrupper. Den här unika anslutningen är bara tillgänglig för marknadsförare som använder Advertising Cloud. Se &quot;[Importera Adobe Audience Manager-segment för annonsinriktning](/help/integrations/audience-manager/import-audiences.md).&quot;

### Använd Audience Manager och annat [!DNL Adobe] Segment att skapa [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Valda annonsörer med [!DNL Advertising Cloud Search] endast*

Inom [!DNL Search]kan du skapa [!DNL Google Ads] Google kund matchar målgrupper från användar-ID:n med era befintliga Audience Manager-segment som har [!UICONTROL Adobe Media Optimizer (HTTP)] och [!UICONTROL Adobe Media Optimizer Batch Destination] som destinationer. ([!DNL Media Optimizer] är ett tidigare namn för Advertising Cloud Search.) Detta omfattar Adobe Analytics-segment som publiceras till Adobe Experience Cloud och segment som skapas i Adobe Experience Cloud med [!DNL People core service]. Mer information finns i hjälpen för produkten i [!DNL Search].

[Kunden matchar målgrupper från användar-ID:n](https://support.google.com/google-ads/answer/9199250) fungerar som webbplatstaggbaserade målgrupper, men ett icke-PII ID tilldelas unika målgruppsmedlemmar för distinkta fördelar jämfört med standardkundmatchning och taggbaserade målgrupper för webbplatser.

Om du vill skapa nödvändiga användar-ID:n måste du använda en Advertising Cloud JavaScript-tagg <!-- with a user ID parameter -->på era webbplatser. Kontakta ditt Advertising Cloud Search-kontoteam om du vill ha mer information.

![process för att skapa segment](/help/integrations/assets/ad_search_user_id_pic.png)

När du har skapat målgrupperna kan du använda dem i [!DNL Google Ads] kampanjer som [mål eller undantag på kampanjnivå eller annonsnivå](#audience-manager-targets).

### Använd Audience Manager och andra [!DNL Adobe] Segment att rikta eller exkludera annonser {#audience-manager-targets}

* (Valda annonsörer med [!DNL Search]) Du kan använda valfritt [!DNL Google Ads] målgrupper som [skapad med [!DNL Adobe] segment](#audience-manager-google-audiences) som kampanjnivå eller annonsnivå som mål eller undantag i er [!DNL Google Ads] kampanjer.

* (Annonsörer med Advertising Cloud DSP) Du kan använda dina befintliga [!DNL Adobe] segment som mål för era annonsplaceringar. Du kan också inkludera segmenten i återanvändbara målgrupper, som du kan använda som mål eller undantag för flera placeringar.

* (Annonsörer med Advertising Cloud Creative) Du kan använda dina befintliga [!DNL Adobe] segment som mål för specifika kreatörer i era annonsupplevelser.

>[!NOTE]
>
>Mer information om hur du skapar målgrupper i Audience Manager och Experience Cloud [!DNL Audience Library] gränssnitt, och vanliga användningsområden för olika typer av målgrupper, se[Alternativ för att skapa målgrupper](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Skicka DSP data för medieexponering till Audience Manager

*Annonsörer med endast DSP*

Advertising Cloud DSP-kunder med Adobe Audience Manager kan hämta in data från annonskampanjer med pixelanrop till Audience Manager. Sedan kan ni använda kampanjdata för att bygga regelbaserade egenskaper, som ni kan använda för att definiera nya segment för att möjliggöra olika DSP, som mer avancerad segmentering, frekvenshantering, marknadsföringsanalyser och rapportinsikter.

Se &quot;[Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; för mer information.

## Få djupare insikter om webbplatsaktivitet med Audience Analytics

Advertising Cloud kunder med [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kan skicka både Advertising Cloud-spårade data och Audience Manager-segment till [!DNL Analytics] för bättre insikter om webbplatsaktiviteter.

Mer information finns i &quot;[[!DNL Adobe][!DNL Audience Analytics] för Advertising Cloud-kunder](/help/integrations/audience-manager/audience-analytics.md).&quot;
