---
title: Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager
description: Lär dig hur du använder händelsepixlar från Audience Manager för att hämta in data på visningsnivå och klicknivå från Advertising Cloud DSP-kampanjer
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Översikt över att skicka DSP exponeringsdata till Adobe Audience Manager

*Annonsörer endast med Advertising Cloud DSP*

*Annonsörer med endast Advertising Cloud-Adobe Audience Manager-integrering*

Advertising Cloud DSP-kunder med Adobe Audience Manager kan använda Audience Manager händelsepixlar för att hämta in data på visningsnivå och klicknivådata från DSP kampanjer. Händelsepixlarna skickar data som åtgärdbara signaler till Audience Manager. Dessa signaler möjliggör olika DSP, t.ex. mer avancerad segmentering, frekvenshantering, marknadsanalyser och rapportinsikter.

DSP debiterar dig inte att skicka dessa signaler till Audience Manager. Men du betalar standardkostnaden för att ta emot Audience Manager baserat på serversamtal enligt Audience Manager-avtalet. Audience Manager tar bort dubbletthändelser som spåras på två olika sätt, så att varje händelse bara debiteras en gång.

>[!NOTE]
>
> Audience Manager har också stöd för att hämta in data från annonsserverns loggfiler, vilket ger mindre flexibilitet. Den processen beskrivs inte i den här dokumentationen.

## Fördelar

* DSP kampanjdata flödar in i Audience Manager i realtid och ni kan använda det för att skapa regelbaserade egenskaper som ni använder för att definiera segment.

* Segmenten är tillgängliga för målgruppsanpassning direkt efter användar- och segmentkvalificering, vilket ger bättre målinriktning i realtid.

* Ni kan utnyttja kampanjdata för exempelvis frekvensbegränsning för alla kreatörer, återmarknadsföring av användare som exponerats för tidigare kampanjer samt analysera beteenden och startpunkter för webbplatser längre fram i kedjan.

* De samlade data ger en enhetlig bild av kampanjens resultat, hjälper till att identifiera anpassade konverteringsvägar och kan användas för att förbättra händelseföljden som leder till konverteringar via Audience Manager [!DNL Audience Optimization Reports] eller genom [[!DNL Audience Analytics] integrering med Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Hur data spåras

Pixlarna för Audience Manager-intrycket och klickhändelsen är cookie-baserade. Pixlarna fångar inte in händelser som inträffar i cookie-fria miljöer, som mobilappar och ansluten TV (CTV).

### Impression-Tracking Pixels

Audience Manager spårar visningsdata för en annons när du kopplar en 1 xl-pixel genomskinlig händelsespårningspixel till annonsen. Händelsepixeln läses in varje gång annonsen skickas till en användare och läses in av webbläsaren. Pixeln läses in från en klientspecifik underdomän till [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), som är en äldre domän för Audience Manager och innehåller parametrar som nyckelvärdepar. Händelseanropet samlar in bild- och konverteringsdata och skickar dem till Audience Manager datainsamlingsservrar.

### Click-Tracking Pixels

Audience Manager spårar klickningar på liknande sätt som visningar, förutom att den inte läser in den genomskinliga händelsepixeln varje gång annonsen visas. Klickdata spåras i stället i annonsens klicknings-URL. Annonsen pekar på en klientspecifik underdomän till [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), som är en äldre domän för Audience Manager, för bearbetning av datainsamlingsservrarna i Audience Manager. Servern dirigerar sedan om användaren till den avsedda landningssidan. URL:en innehåller parametrar som nyckelvärdepar.

>[!NOTE]
>
>Om din organisation använder [!DNL Analytics] spårning behöver du kanske inte spåra Audience Manager-klickningar. Adobe Analytics tar klicksignaler och kan skicka dem till Audience Manager via [vidarebefordran på serversidan](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Samla in klicknings- och imponeringsdata från Advertising Cloud DSP Campaigns](collect.md)
>* [Användningsexempel](use-cases.md)

