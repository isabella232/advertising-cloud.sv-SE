---
title: '"[!DNL Adobe][!DNL Audience Analytics] för Advertising Cloud-kunder"'
description: Lär dig använda [!DNL Adobe][!DNL Audience Analytics] för reklamanvändningsfall
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] för Advertising Cloud-kunder

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) är en integrering mellan Adobe Audience Manager och Adobe Analytics som gör att Audience Manager-kunder kan skicka segment till [!DNL Analytics] för bättre insikter om webbplatsaktiviteter.

Advertising Cloud-kunder kan dra nytta av [!DNL Audience Analytics]. Integreringen gör att du kan:

* Skicka Advertising Cloud exponeringsdata direkt till [!DNL Analytics] fastställa inverkan av den övre trattens aktivitet på nedströmsverksamheten.

* Bestäm marknadsföringskanaler och ingångspunkter för sajter utifrån exponeringsannonser i den övre tratten.

* Layer the integration with [!DNL Analytics for Advertising Cloud] lägga in demografiska segment från tredje part från [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) med [!DNL Analytics for Advertising Cloud] för mer information om användarprofiler.

   [!DNL Audience Marketplace] ger åtkomst till dataflöden från tredje part med prenumerationsmodeller för aktivering som tillåter köpare att skicka data till en destination. Om data används i en [!DNL Analytics] och då tas ingen aktiveringsavgift ut.

* (Annonsörer med Advertising Cloud DSP) Lägg till ytterligare exponeringssegment för att få en helhetsbild av hanteringen.

   Advertising Cloud DSP kan skicka exponeringsdata till Audience Manager som användbara signaler genom att implementera pixlar för antingen Adobe Experience Platform eller Audience Manager. Vidarebefordra samma data till [!DNL Analytics] möjliggör avancerad dataanalys. Se &quot;[Översikt över Advertising Cloud Media Data Integration med Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; för mer information.

Mer information om [!DNL Audience Analytics], inklusive dess förutsättningar och arbetsflöde, se &quot;[Audience Analytics - översikt](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exempel på hur du använder [!DNL Audience Analytics] Data med Advertising Cloud Data

Nedan följer exempel på hur du kan använda kombinerade data i [!DNL Analytics] [!DNL Analysis Workspace].

### Se effekten av Övre trattaktivitet på nedströmsaktivitet

Använd exponeringssegment i Audience Manager för att se hur aktiviteten på den övre delen av arbetsytan påverkar webbplatsaktiviteten nedströms. Inkludera makro-ID:n från Advertising Cloud eller tredje part i spårningspixlarna för att spåra påverkan på en detaljerad nivå, från kampanjnivå till nivån på webbplatsen där användaren exponerades.

Huvudsakliga fördelar:

* Spåra exponering via tratt/annonstyper och användning [!DNL Audience Analytics] för att fastställa ingångshastigheten och överlappa nästa fas av kundresan.

* Fastställ effekten av den övre trattaktiviteten på aktiviteter längre fram i kedjan.

* Anslut [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> och [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> för att fastställa en helhetsresa till webbplatsen.

Nedan följer exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Se effekten av den övre trattaktiviteten på aktiviteter längre fram i kedjan](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Använd [!DNL Audience Analytics] Segmentdata från tredje part för användarprofilanalys

Använd Audience Manager-segment från tredje part för att få en djupare analys av hur användare interagerar med webbplatsen. Ni kan använda informationen för att avgöra vilka nya målgrupper från tredje part som medierna ska aktiveras för, baserat på hur profiler från tredjepartssegmenten interagerar med viktiga resultatindikatorer för mediekampanjernas webbplatser.

>[!TIP]
> Använd Audience Manager `Audiences ID` och `Audiences Name` mått [!DNL Analytics], precis som andra dimensioner som [!DNL Analytics] samlingar.

Nedan följer exempel på rapporter som du kan skapa i [!DNL Analysis Workspace].

![Använda segment från tredje part för att förbättra användarprofilanalysen](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud-integrering med Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

