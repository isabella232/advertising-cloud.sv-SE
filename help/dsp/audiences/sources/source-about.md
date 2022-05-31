---
title: Om aktivering av autentiserade segment från målgruppskällor
description: Lär dig mer om hur man hämtar in förstahandssegment från en kunddataplattform.
feature: DSP Audiences
source-git-commit: aac60e8fddce1db3d0101a617fca3af970043648
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Om aktivering av autentiserade segment från målgruppskällor

<!-- Doesn't specifically explain what you can do in our UI -->
*Betafunktion*

Advertising Cloud DSP kan importera förstahandssegment som består av autentiserade signaler som skapats inom en kunddataplattform (CDP). Du kan använda de kapslade segmenten som mål för dina placeringar.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP är integrerat med [den [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), som ingår i Adobe Experience Platform.

I [!DNL Real-time CDP], *mål* är anslutningar till externa dataplattformar som möjliggör smidig dataaktivering. Du kan till exempel använda destinationer för att aktivera dina kända kundrelationer (till exempel hash-kodade e-postadresser) för riktad reklam i olika digitala format som stöds av DSP.

Mer information om destinationer finns i Experience Platform [Destinationshandbok](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), inklusive en översikt över produkten, instruktioner för [skapa målarbetsytor](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) och [skapa målanslutningar](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)och [aktivera data till mål](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Arbetsflöde för att använda DSP integrering med [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Tillåt DSP att översätta kunddatasegment till [!DNL LiveRamp RampIDs]](source-durable-id.md) som är igenkännbara i en anbudsbar miljö.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Skapa en målgruppskälla](source-create.md) för att importera målgrupper till ditt DSP eller ett annonserarkonto.

1. [Konfigurera en [!DNL Real-Time CDP] målanslutning i Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).<!-- Verify URL once it's published. -->

Kontakta din [!DNL Adobe] kontoteam eller `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Aktivera autentiserade segment från varaktiga ID-partners](source-durable-id.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målgruppskälla](source-settings.md)
>* [Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Översikt över destinationskatalogen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)

