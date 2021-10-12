---
title: Om [!UICONTROL Deal ID Inbox]
description: Lär dig mer om funktionen [!UICONTROL Deal ID inbox] som gör att du kan acceptera privata avtal som du redan har förhandlat med utgivare den [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (tidigare [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Om [!UICONTROL Deal ID Inbox]

Med DSP [!UICONTROL Deal ID inbox] kan du snabbt skapa avtal som Advertising Cloud DSP har importerat från utgivare via SSP (Supply Side Plattforms) så att du inte behöver konfigurera varje avtal manuellt. Du kan acceptera de garanterade och ej garanterade privata lagererbjudanden som du redan har förhandlat med utgivare på [!DNL FreeWheel], [!DNL Google Authorized Buyers] (tidigare [!DNL AdX]) och [!DNL Magnite DV+] (tidigare [!DNL Rubicon]) från [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP är den första DSP som kan integreras med [!DNL FreeWheel]-API:t.

I [!UICONTROL Deal ID inbox] kan du se detaljerna om erbjudandet så som din utgivare ser dem, snabba upp konfigurationen av erbjudandet och undvika fel vid manuell inmatning.

DSP uppdaterar automatiskt alla avtalsdetaljer varje dag kl. 04.30 EST. Den uppdaterar även alla [!DNL FreeWheel]-avtal och uppdaterar befintliga avtal från [!DNL Google] och [!DNL Magnite DV+] varje timme. Du kan även uppdatera avtalsinformationen manuellt för att fylla i nya avtal när som helst.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>För programmatiska garanterade avtal via [!DNL Google Authorized Buyers] måste du leverera minst 90 % av budgeten, annars förlorar ditt konto åtkomsten till [!DNL Google] avtal i [!UICONTROL Deal ID inbox].

## Implementera [!UICONTROL Deal ID Inbox]

För att få dina erbjudanden i [!UICONTROL Deal ID inbox] måste SSP-kontona mappa din organisations DSP till ditt SSP-konto. DSP delar organisationens kontonamn med de berörda SSP:erna. Kontakta din kontoansvarige på Adobe för instruktioner.

Under avtalsförhandlingar ska du be utgivaren att skicka avtalet till din köpare i stället för till det överordnade DSP kontot. Avtalsidentifieraren kan vara ett namn eller ett ID, beroende på SSP.

## Åtgärder ni kan vidta

* **Granska** återförsäljarna för att verifiera att SSP har skickat rätt utgivare, flygdatum, CPM och annan avtalsinformation. Om utgivaren har gjort ett misstag kontaktar du dem utanför DSP så att de kan korrigera och skicka om avtalet.

* **Godkänn** avtal efter granskning och de visas inte längre i  [!UICONTROL Deal ID inbox]. Godkända erbjudanden listas i [!UICONTROL Inventory] > [!UICONTROL Deals] och är redo att ingå i annonsörernas praktik.

* **Ignorera** transaktioner som inte behövs eller som inte har begärts. Ignorerade erbjudanden flyttas till fliken [!UICONTROL Ignored Deals] i [!UICONTROL Deal ID inbox], som fungerar som ett arkiv. DSP varnar inte SSP:er och utgivare när du ignorerar ett avtal.

* **Ändra detaljer för redan accepterade** avtal från  [!UICONTROL Inventory] >  [!UICONTROL Deals] (inte i  [!UICONTROL Deal ID inbox]). När utgivare skickar ändringar till avtal ansvarar annonsörer på liknande sätt för att implementera dessa ändringar i [!UICONTROL Inventory] > [!UICONTROL Deals] eftersom [!UICONTROL Deal ID inbox] inte synkroniserar ändringar från SSP:er efter att avtal har skapats.

## Vilka typer av avtal kan inte accepteras?

När en avtalslista inte innehåller en ![Acceptera](/help/dsp/assets/accept.png)-ikon eller en [!UICONTROL Accept]-knapp kan du inte acceptera den från [!UICONTROL Deal ID inbox]. I stället kan du [skapa avtals-ID-informationen manuellt](/help/dsp/inventory/deal-id-create.md).

Du kan inte acceptera följande typer av avtal:

* [!DNL Google] erbjudanden som inte är i USD.

* [!DNL Magnite DV+] erbjudanden som inte är i USD

* [!DNL FreeWheel] erbjudanden som inte finns i din kontovaluta.

* Erbjudanden som har ett slutdatum före idag.

* Gamla [!DNL Magnite DV+]-erbjudanden som är märkta som&quot;flera medietyper&quot;.

Avtalsinformationen innehåller anledningen till att erbjudandet inte är tillgängligt att acceptera.

>[!MORELIKETHIS]
>
>* [Acceptera ett avtal i Inkorgen för avtal-ID](deal-id-inbox-accept.md)
>* [Översikt över inventeringsfunktioner](inventory-overview.md)

