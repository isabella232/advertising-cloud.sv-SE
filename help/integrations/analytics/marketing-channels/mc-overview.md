---
title: Grundläggande om [!DNL Marketing Channels]
description: Läs viktig information om [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] bör förstå.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Grundläggande om [!DNL Analytics Marketing Channels]

*Annonsörer med endast Advertising Cloud-Adobe Analytics-integrering*

Den här sidan förklarar viktig information om [!DNL Analytics Marketing Channels] att [!DNL Analytics for Advertising Cloud] måste förstå.

Fullständig dokumentation om [!DNL Marketing Channels], se &quot;[Kom igång med [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Översikt över [!DNL Marketing Channels]

[!DNL Marketing Channels] är en nyckelfunktion i Adobe Analytics. [!DNL Marketing Channels] rapporter visar hur kunderna kommer till er webbplats via rapportfönstret och hur varje kanal påverkar intäkter eller beteenden på plats.

Titta på följande exempel på en korsbesöksresa. Varje besök på er webbplats indikeras av den marknadsföringskanal som besökaren kom in från. Det första besöket, som även kallas First Touch Channel, är e-post. Visning på besök två är en deltagande kanal, och Natural Search betraktas som sista beröringskanalen. Om du använder [!UICONTROL Last Touch Attribution] inom [!UICONTROL Attribution IQ], skulle Natural Search få full konverteringskurs på 250 dollar. Med Experience Cloud ID-tjänsten kan du knyta samman dessa enskilda besök för att visa en resa för en enskild besökare.

![Exempel på konverteringsresa mellan besök i marknadsföringskanaler](/help/integrations/assets/a4adc-mc-sample-journey.png)

Genom att använda [!UICONTROL Marketing Channels] Med Bearbetningsregler kan du skapa uppsättningar av logik för att avgöra vilka kanaler som driver trafiken och för att spåra varje kanal när användarna kommer till webbplatsen. Till exempel [!UICONTROL Email] kanalen anges med en unik spårningskod som genereras när man klickar på den. När den loggas av Adobe Analytics kategoriseras besöket som om det kom från en e-postmarknadsföringskampanj.

## Bearbetningsregler och hur marknadsföringskanaler ställs in

Varje gång en användare kommer till en webbplats gör de det via en URL som de antingen klickade på eller skrev direkt i adressfältet. När användaren kommer till webbplatsen [!DNL Analytics] spårar information som kan användas för att avgöra vilken kanal som körde besöket.

Marknadsförarna lägger ofta till spårningskoder för frågesträngsparametrar i kanal-URL:er för att hjälpa till att spåra kanalens påverkan på deras webbplats. Du kan konfigurera [!DNL Marketing Channels] bearbetningsregler för att avlyssna specifika spårningsparametrar och -värden för att avgöra kanalen utan ytterligare spårning. Om till exempel alla URL:er för e-postkampanjer följer formatet `www.adobe.com?cid=email…` (där URL:en innehåller frågesträngsparametern och -värdet `cid=email`) kan du skapa en regel som lyssnar efter den här spårningskoden och bucket besöket i [!UICONTROL Email] kanal.

Andra kanaler saknar spårbara URL-sökvägar och behöver ytterligare logik för identifiering. Till exempel: [!UICONTROL Earned Social], där en användare klickar på en länk som en annan användare har delat organiskt i ett socialt nätverk, är en viktig kanal att spåra. Marknadsföraren kan dock inte lägga till en spårningskod för frågesträngsparametrar i den delade URL:en. I det här fallet kan du skapa en bearbetningsregel som lyssnar efter den refererande domänen för sociala nätverk av intresse och frånvaron av betalda spårningskoder för att avgöra kanalen. Besöken som uppfyller dessa krav spåras sedan som Earned Social i rapporten Marketing Channels.

Adobe rekommenderar att ni samarbetar med ert analysteam för att ta fram en omfattande uppsättning [!DNL Marketing Channels] bearbetningsregler för att spåra alla kanaler som är relevanta för din verksamhet. På så sätt kan ni skapa kraftfulla attribueringsrapporter.

För att förstå hur Advertising Cloud kan bidra till de signaler som behövs för att skapa anpassade marknadsföringskanaler, se &quot;[Använda reklam-ID:n för att skapa [!DNL Marketing Channels] Regler](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Använda Advertising Cloud ID för att skapa [!DNL Marketing Channels] Bearbetar regler](mc-ids.md)
>* [Varför olika kanaldata kan variera mellan Advertising Cloud och [!DNL Marketing Channels]](mc-data-variances.md)
>* [Använda [!DNL Analytics Marketing Channels] med Advertising Cloud Data](mc-ac-data.md)
>* [Video: Rapportera med Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Översikt över [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

