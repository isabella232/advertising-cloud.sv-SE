---
title: 'Aktivera autentiserade segment från varaktiga ID-partners '
description: Lär dig hur du aktiverar autentiserade målgrupper med en hållbar ID-lösning.
feature: DSP Audiences
source-git-commit: 155ab740084bebfba5fd992a23706129668fcc90
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aktivera autentiserade segment från varaktiga ID-partners

*Betafunktion*

Om du vill aktivera autentiserade målgrupper via en hållbar ID-lösning i Advertising Cloud DSP måste dina segment översättas till [!DNL RampIDs], som kan kännas igen i en anbudsbar miljö. Du kan uppnå detta genom att antingen:

* Utnyttja DSP integrering med [!DNL Adobe Real-Time Customer Data Profile (CDP)] och [!DNL Adobe-LiveRamp Retrieval API].

* Skicka autentiserade segment manuellt till DSP från [!DNL LiveRamp] [!DNL Connect] kontrollpanel.

## Uppgifter

1. För båda alternativen kontaktar du `adcloud-support@adobe.com` för att aktivera följande inställningar i DSP, vilket gör att ni kan inrikta er på autentiserade segment i DSP kampanjer en gång [alla steg i aktiveringsarbetsflödet är slutförda](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] kampanjkonfiguration före segmentdelning från [!DNL Real-Time CDP].

   1. Kontonivån &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Användare delar autentiserade segment manuellt från [!DNL LiveRamp]) Utför följande steg i [!DNL LiveRamp] [!DNL Connect] kontrollpanel:

   1. Aktivera målrutan **[!DNL AAC API 1P Onboarding]**.

   1. Ange [!DNL Identifier Settings] till **[!DNL Ramp ID]** endast.

      ![Identifieringsinställningar](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Valfritt) Om du fortfarande vill få cookie-baserade identifierare skapar du en andra [!DNL AAC API 1P Onboarding] målplatta med &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; och &quot;[!DNL AAID]&quot;.

## Bästa metoder för testning och dataverifiering

* **Mål [!DNL RampID]-baserade segment och cookie-baserade segment i separata kampanjer.**

   * I kampanjinställningarna kan bara en identifierare prioriteras.

   * För närvarande [!DNL RampIDs] går inte att hämta under webbplatshändelser. Det innebär att vissa anpassade mål, som lägsta CPA och ROAS, inte är tillgängliga med autentiserade segment. Använd bara cookie-baserade segment om du har en begränsande KPI för prestanda.

* **Skapa en placering i båda [!DNL RampID] och cookie-baserade kampanjer.**

   * Ange segment som delas från [!DNL LiveRamp] med standardprocessen för aktivering av segment.

   * Samarbeta med Advertising Cloud supportteam för att validera datadistributionen.

Läs mer om DSP integration med [!DNL LiveRamp], kontakt `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Om aktivering av autentiserade segment från målgruppskällor](source-about.md)
>* [Skapa en målgruppskälla för att aktivera förstahandspubliker](source-create.md)
>* [Inställningar för målgruppskälla](source-settings.md)
>* [Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Om Audience Management](/help/dsp/audiences/audience-about.md)

