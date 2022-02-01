---
title: Manuella inställningar för avtal-ID
description: Se beskrivningar av inställningarna för manuellt angivna avtal-ID:n.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: cf08c97a6a9fecd637f1776b186a18a5c5cc6435
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Manuella inställningar för avtal-ID

| Avsnitt | Parameter | Beskrivning | Obligatoriskt | Redigerbar |
|---------|-----------|-------------|----------|----------|
| [Avtalsinformation] | [!UICONTROL Deal name] | Namnet som identifierar [!UICONTROL Deal ID] i Advertising Cloud DSP. Ange ett namn eller välj **[!UICONTROL Auto-name]** för att låta Advertising Cloud generera ett namn baserat på avtalsinformationen.<br><br>Exempel på ett namn som genererats automatiskt: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
|  | [!UICONTROL External deal ID] | Det ID som din utgivare och SSP använder för att identifiera erbjudandet. | Ja | Nej |
|  | [!UICONTROL Publisher] | Namnet på utgivaren som säljer det här lagret. | Ja | Nej |
|  | [!UICONTROL SSP] | Den SSP-plattform som avtalet ska köras genom. | Ja | Nej |
|  | [!UICONTROL Media type] | Den typ av media som kommer att köpas genom detta avtal: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, eller *[!UICONTROL Audio]*. Alternativen varierar beroende på SSP.<br><br> Om avtalet tillåter flera medietyper väljer du medietypen för standardplaceringen när du skapar erbjudandet. Senare kan du ändra värdet eller bara [bifoga en ny placering med ytterligare medietyp](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nej |
|  | [!UICONTROL Deal type] | Avtalsåtagande och prisstruktur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Du och utgivaren har inte åtagit sig ett fast antal tryckleveranser. I avtalet anges minimipriset för lagret, men CPM kan variera och öka beroende på marknadsvillkoren.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Du och utgivaren har inte åtagit sig ett fast antal tryckleveranser. Priserna sätts till en förhandlad fast ränta.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Du och utgivaren har kommit överens om ett fördefinierat antal visningar, målinriktning, flygdatum och fast pris.<br><br><b>Obs!</b> Garanterade erbjudanden kräver flygdatum och ett visst antal visningar i [!UICONTROL Tracking] -avsnitt. Du måste också skapa en standardplacering av en programmatisk garanterad (PG) för erbjudandet, och du kan välja att använda erbjudandet för andra placeringar i stället.</li></ul> | Ja | Nej |
|  | [!UICONTROL CPM] | Den framförhandlade kostnaden per tusen visningar (CPM). | Ja | Ja |
|  | [Valuta] | Valutan för erbjudandet.<br><br>Alla SSP accepterar erbjudanden i USD. När SSP godkänner valutan för ditt DSP är även den valutan tillgänglig. | Ja | Nej |
|  | [!UICONTROL Billing method] | Alla erbjudande-ID:n är [!DNL Adobe]-finansierad och -fakturerad. Advertising Cloud betalar alla tillgängliga medieleverantörer baserat på användning, hanterar avvikelser med leverantörerna och skickar en konsoliderad faktura till kontot. Det här alternativet medför ytterligare avgifter enligt kontots rabattkort. | Ja | Nej |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | E-postadressen till det användarkonto som har åtkomst till avtalet. | Nej | Ja |
|  | [!UICONTROL Advertisers that can access this deal] | De specifika annonsörer på kontot som har tillgång till erbjudandet.<br><br><b>Obs!</b> Du kan dela avtalet med annonsörer i ytterligare konton från [!UICONTROL Deals] vy. Klicka på **[!UICONTROL #]**, klicka **[!UICONTROL share]** och dela sedan avtalet med en e-postadress. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Start- och slutdatum för trafik som använder det här avtalet. Datumet är endast avsett för spårningsändamål och påverkar inte annonsleveransen.<br><br><b>Tips:</b> I [!UICONTROL Inventory] > [!UICONTROL Deals] visa [!UICONTROL Pacing & Budget] -kolumnen visar hur avtalet matchar det angivna flygdatumet och det angivna visningsmålet. Om leveransen är under- eller överbelagd kontaktar du utgivaren för att justera hur mycket av volymen den skickar genom erbjudandet. | Garanterade erbjudanden: Ja<br>Erbjudanden utan garanti: Nej | Ja |
|  | [!UICONTROL Impressions] | (Valfritt för erbjudanden utan garanti) Det uppskattade antalet visningar som du förväntar dig att göra med det här erbjudandet. Detta värde är endast avsett för spårning. utgivaren kontrollerar och levererar. | Garanterade erbjudanden: Ja<br>Erbjudanden utan garanti: Nej | Ja |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Skapa information om avtal-ID manuellt](deal-id-create.md)
>* [SSP-partners](ssp-partners.md)
>* [Om privat lager](private-inventory-about.md)

