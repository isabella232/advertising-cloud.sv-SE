---
title: Om [!UICONTROL Simple Ad Serving]
description: Läs mer om [!UICONTROL Simple Ad Serving] hanterar med händelsespårande pixlar.
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Om [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] ger garanterad, obeslutad annonsleverans och rapportering för en viss utgivare och en viss annonstyp med en enda dedikerad placering. Använd [!DNL Simple Ad Serving] när utgivaren inte kan genomföra ditt avtal via ett erbjudande-ID. All målgruppsanpassning, budgetering och begränsning samt frekvensbegränsning hanteras av utgivaren. Utför dessa erbjudanden via pixlar för händelsespårning.

Med [!UICONTROL Simple Ad Serving], hanteras varje annons direkt av utgivaren (webbplatsservern) och DSP tillhandahåller en pixel för händelsespårning som skickas till utgivaren, som måste implementera pixeln och trafikera DSP annonser. Beroende på lagertypen mäter händelsepixlarna intryckta händelser, klickfrekvens och videouppspelningshändelser.

Följande annonstyper är tillgängliga:

* förrullning av datorstandard
* surfplatta och mobilstandard för pre-roll
* ansluten TV-standard för förrullning
* visa
* ljud

Du kan skapa en [!UICONTROL Simple Ad Serving] i [!UICONTROL Inventory] > [!UICONTROL Deals] vy. DSP skapar automatiskt en placering med undertypen[!DNL Simple ad serving]&quot; för annonsen. Placeringen har som mål avtalet men tillåter inte ytterligare målgruppsanpassning, budget eller frekvensbegränsning. Du kan bara redigera vissa av avtalsinställningarna, till exempel avtalsnamn, CPM, avtryck och flygdatum.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] placeringar uppfyller inte kontots användbara medel eller kampanjens och paketets budgetar. Utgifterna spåras dock och räknas in i dessa budgetar. Även när CPM:en är $0 spåras alltid händelsedata.

>[!MORELIKETHIS]
>
>* [Skapa en [!UICONTROL Simple Ad Serving] Erbjudande](simple-deal-create.md)
>* [Redigera [!UICONTROL Simple Ad Serving] Avtalsinställningar](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Inställningar](simple-deal-settings.md)
>* [Visa en detaljerad rapport för ett avtal](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
