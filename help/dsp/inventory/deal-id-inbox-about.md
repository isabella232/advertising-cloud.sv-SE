---
title: Om [!UICONTROL Deal ID Inbox]
description: Läs mer om [!UICONTROL Deal ID inbox] som gör att du kan acceptera privata avtal som du redan har förhandlat med utgivare om [!DNL FreeWheel], [!DNL Google Authorized Buyers] (tidigare känt som [!DNL AdX]), and [!DNL Magnite DV+] (tidigare [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Om [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] Med kan ni snabbt skapa avtal som DSP har importerat från utgivare via plattformar på utbudssidan (SSP) så att ni inte behöver konfigurera varje avtal manuellt. Du kan acceptera de garanterade och ej garanterade privata lagererbjudanden som du redan har förhandlat med utgivare om [!DNL FreeWheel], [!DNL Google Authorized Buyers] (tidigare känt som [!DNL AdX]), och [!DNL Magnite DV+] (tidigare [!DNL Rubicon]) från [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>DSP är den första DSP som kan integreras med [!DNL FreeWheel] API.

I [!UICONTROL Deal ID inbox], kan du se detaljerna om erbjudandet så som utgivaren ser dem, snabba upp avtalsinställningarna och undvika fel vid manuell inmatning.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP uppdaterar automatiskt alla avtalsdetaljer varje dag kl. 04.30 EST. Den uppdaterar även alla [!DNL FreeWheel] Erbjudanden och uppdateringar av befintliga avtal från [!DNL Google] och [!DNL Magnite DV+] varje timme. Du kan även uppdatera avtalsinformationen manuellt för att fylla i nya avtal när som helst.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>För programmatiska annonsköp [!DNL Google Authorized Buyers]måste du leverera minst 90 % av din budget, annars förlorar ditt konto åtkomsten till [!DNL Google] erbjudanden i [!UICONTROL Deal ID inbox].

## Implementera [!UICONTROL Deal ID Inbox]

För att få dina erbjudanden i [!UICONTROL Deal ID inbox]måste dina SSP-konton mappa din organisations DSP till ditt SSP-konto. DSP delar organisationens kontonamn med de berörda SSP:erna. Kontakta [!DNL Adobe] kontoteam för instruktioner.

Under avtalsförhandlingar ska du be utgivaren att skicka avtalet till din köpare i stället för till det överordnade DSP kontot. Avtalsidentifieraren kan vara ett namn eller ett ID, beroende på SSP.

## Åtgärder ni kan vidta

* **Granska erbjudanden** för att verifiera att SSP har skickat rätt utgivare, flygdatum, CPM och annan avtalsinformation. Om utgivaren har gjort ett misstag kontaktar du dem utanför DSP så att de kan korrigera och skicka om avtalet.

* **Acceptera erbjudanden** efter granskning och de visas inte längre i [!UICONTROL Deal ID inbox]. Godkända erbjudanden listas i [!UICONTROL Inventory] > [!UICONTROL Deals] och är redo att inrikta sig på annonsörernas praktik.

* **Ignorera erbjudanden** som inte behövs eller som inte efterfrågas. Ignorerade erbjudanden flyttas till [!UICONTROL Ignored Deals] -fliken i [!UICONTROL Deal ID inbox], som fungerar som arkiv. DSP varnar inte SSP:er och utgivare när du ignorerar ett avtal.

* **Ändra information om redan accepterade erbjudanden** från [!UICONTROL Inventory] > [!UICONTROL Deals] (inte i [!UICONTROL Deal ID inbox]). På samma sätt ansvarar annonsörer för att implementera ändringarna i [!UICONTROL Inventory] > [!UICONTROL Deals] därför att [!UICONTROL Deal ID inbox] synkroniserar inte ändringar från SSP:er efter att avtal har ställts in.

## Vilka typer av avtal kan inte accepteras?

När en avtalslista inte innehåller en ![Acceptera](/help/dsp/assets/accept.png) ikon eller en [!UICONTROL Accept] kan du inte acceptera det från [!UICONTROL Deal ID inbox]. I stället kan du [skapa information om kontrakt-ID manuellt](/help/dsp/inventory/deal-id-create.md).

Du kan inte acceptera följande typer av avtal:

* [!DNL Google] erbjudanden som inte är i USD.

* [!DNL Magnite DV+] erbjudanden som inte är i USD

* [!DNL FreeWheel] erbjudanden som inte finns i din kontovaluta.

* Erbjudanden som har ett slutdatum före idag.

* Gammal [!DNL Magnite DV+] Erbjudanden som är märkta som&quot;flera medietyper&quot;.

Avtalsdetaljerna innehåller anledningen till att erbjudandet inte är tillgängligt att acceptera.

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Översikt över inventeringsfunktioner](inventory-overview.md)

