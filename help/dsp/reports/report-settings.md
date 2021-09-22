---
title: Anpassade rapportinställningar
description: Se beskrivningar av anpassade rapportinställningar.
feature: DSP Custom Reports
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---


# Anpassade rapportinställningar

**[!UICONTROL Name]** Rapportnamnet. Maximala längden är 180 tecken.

**[!UICONTROL Report Type]** Typ av rapport:  *[!UICONTROL Custom]* (som innehåller de mest tillgängliga alternativen),  *[!UICONTROL Billing]*,  *[!UICONTROL Conversion]*,  *[!UICONTROL Device]*,  *[!UICONTROL Frequency (by Impression)]*,   *[!UICONTROL Frequency (by App/Site)]*,  *[!UICONTROL Geo]*,  *[!UICONTROL Margin]*,  *[!UICONTROL Media Performance]*,   *[!UICONTROL Segment]* eller  *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] Avsnitt

**[!UICONTROL Timezone]:** Tidszonen för rapportering.

**[!UICONTROL Observe Daylight Savings Time]:** Beräknar sommartid i de rapporterade tiderna.

**\[Datumintervall\]:** Datumintervallet som data ska genereras för. Antalet tillgängliga dagar varierar beroende på rapport och valda dimensioner. Välj ett alternativ:

* **[!UICONTROL Previous N days]:** Inkluderar data för ett visst antal dagar före idag.

* **[!UICONTROL Custom]:** Inkluderar data mellan specifika start- och slutdatum. Om du vill rapportera data genom föregående dag väljer du **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Inkluderar data för föregående kalendermånad.

**[!UICONTROL Add Filters]:** (Valfritt) Ytterligare dimensioner som data kan filtreras med, oavsett om dimensionerna inkluderas som kolumner i rapporten eller inte:  *[!UICONTROL Account]*,\*  *[!UICONTROL Advertiser]*,  *[!UICONTROL Campaign]*,  *[!UICONTROL Placement]*,  *[!UICONTROL Ad]*,  *[!UICONTROL Ad Type]*,  *[!UICONTROL Video]*,  *[!UICONTROL Video Duration]*,  *[!UICONTROL Country]* och  *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* är endast tillgängligt för följande rapporttyper när din organisation har konfigurerats för [korskontorapportering](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] och [!UICONTROL Conversion]. Kontakta din kontoansvarige på Adobe om du vill ha mer information om kontorapportering.

Så här använder du ett eller flera filter:

* Välj en dimension, markera operatorn (*är lika med* eller *inte är lika med*) och välj sedan önskat värde. Om du till exempel bara vill returnera data för förhandsgranskningsannonser anger du &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Valfritt) Lägg till ytterligare villkor till filtret.
* (Valfritt) Lägg till ytterligare filter, där vart och ett har ett eller flera villkor.

## [!UICONTROL Build Your Report] Avsnitt

**[!UICONTROL Select To Add As Report Headers]:**  De datakolumner, eller rubriker, som ska inkluderas i rapporten. Om du vill lägga till en kolumn expanderar du kategorin och markerar kryssrutan bredvid kolumnnamnet. Alla otillgängliga mått är inaktiverade. De tillgängliga datakategorierna är:

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (sorterat efter annonsörer)
* [!UICONTROL Custom Goals] (sorterat efter annonsörer)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Kolumnrubrikernas ordning. Du kan dra och släppa en kolumn för att anpassa ordningen.

## [!UICONTROL Multi-Touch Conversion Options] Avsnitt

**[!UICONTROL Format]:** Om en rapport ska genereras i  *[!UICONTROL CSV]* (kommaseparerade värden) eller  *[!UICONTROL Tab]* (tabbseparerade värden) format.

**[!UICONTROL Report Headers]:** Om  *[!UICONTROL Include]* eller  *[!UICONTROL Do Not Include]* kolumnrubriker ska användas.

**[!UICONTROL Attribution Rule Settings]:** (Alla  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo]och  [!UICONTROL Segment]rapporter med  [!UICONTROL Site] eller  [!UICONTROL Conversion Metrics]   [!UICONTROL Custom Goals] kolumner; annonsörer med endast Advertising Cloud konverteringsspårning) I rapporten, hur man attribuerar konverteringsdata i en serie händelser som leder till konvertering. Du kan välja mer än en regel om du vill jämföra skillnader mellan reglerna.

>[!NOTE]
>
>Konverteringssökvägarna innehåller alla visningar och klickningar i annonsörens intryckt eller klickbara fönster som är konfigurerade i Advertising Cloud Search. Klick ges företräde framför visningar under konverteringsattribuering. Alla klick i en konverteringsväg får full kredit baserat på attribueringsregeln. Impressions får bara kredit när inga klick spåras i konverteringssökvägen.

* *[!UICONTROL Last Event]:* Attribut konverterar till det sista klicket eller det sista intrycket i konverteringssökvägen.

* *[!UICONTROL Weight Last More]:* Attribut konverterar till alla händelser i konverteringsbanan, men ger den mest viktiga vikten till den senaste händelsen och har i sin tur mindre vikt än föregående händelser.

* *[!UICONTROL Even Distribution]:* Attribut konverteras lika till varje händelse i konverteringssökvägen.

* *[!UICONTROL Weight First More]:* Attribut konverterar till alla händelser i konverteringsbanan, men ger den största vikten till den första händelsen och minskar successivt vikten till följande händelser.

* *[!UICONTROL First Event]:* Attribut konverterar till det första klicket eller intrycket i konverteringssökvägen.

* *[!UICONTROL U-shaped]:* Attribut konverteringen till alla händelser i konverteringsbanan, men ger den största vikten till den första och den sista händelsen, med successivt mindre vikt till händelserna mitt i konverteringsbanan.

* *[!UICONTROL Display Only]:*  Attribut konverterar till den sista DSP klickningen eller intrycket i konverteringssökvägen. Detta inkluderar videoklipp och uppkopplade TV-annonser och utesluter klickningar på Advertising Cloud Search-annonser.

* *[!UICONTROL Social Only]:* Föråldrad

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  (Alla  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo]och  [!UICONTROL Segment]rapporter med  [!UICONTROL Site] eller  [!UICONTROL Conversion Metrics]   [!UICONTROL Custom Goals] kolumner) Vilka typer av konverteringar som ska rapporteras när tidigare händelser inträffar på samma enhet. Du kan inkludera upp till tre typer. För varje vald typ inkluderas en separat kolumn för varje konverteringsmått och den läggs till med det angivna suffixet ([!UICONTROL (tl)], [!UICONTROL (ct)] eller [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inkluderar konverteringar som härrör från klick (CT för genomklickning) och tryck (VT för genomskinlighet). Konverteringar som kan härledas till visningar multipliceras med den angivna genomsiktsvikten. Standardbredden är 100 %, vilket innebär att konverteringar som kan tillskrivas visningar räknas som 100 % av värdet på konverteringar som kan tillskrivas klickningar.

* *[!UICONTROL With Clicks (CT)]:* Inkluderar endast konverteringar som härrör från klickningar.

* *[!UICONTROL Impressions Only (VT)]:* Inkluderar endast konverteringar som härrör från avbildningar eftersom inga klick spårades i konverteringssökvägen.

**[!UICONTROL Cross Device Level]:**  (Alla  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo]och  [!UICONTROL Segment]rapporter med  [!UICONTROL Site] eller  [!UICONTROL Conversion Metrics]   [!UICONTROL Custom Goals] kolumner; Gäller endast annonsörer med enhetsövergripande attribuering) Nivån som konverteringen ska spåras på:  *[!UICONTROL People]* eller  *[!UICONTROL Household]*.

Läs mer om [lösningar för olika enheter](/help/dsp/introduction/features/cross-device-solutions.md).

**[!UICONTROL Cross-Device Breakout]:** (Alla  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo]och  [!UICONTROL Segment]rapporter med  [!UICONTROL Site] eller  [!UICONTROL Conversion Metrics]   [!UICONTROL Custom Goals] kolumner; Gäller endast annonsörer med enhetsövergripande attribuering) Detaljnivån för information om enhetskonverteringar som ska ingå i rapporten. Du kan välja upp till tre nivåer, som vart och ett ska inkluderas i en separat kolumn, om du vill ha en detaljerad fördelning.

* *[!UICONTROL Total People (TP)]:* Innehåller det totala antalet konverteringar, som omfattar både konverteringar mellan enheter och konverteringar mellan enheter (om tillämpligt). I rapporten har &quot;[!UICONTROL (tp)]&quot; lagts till i konverteringsmåttets namn och regeltyp.

* *[!UICONTROL Same Device (SD)]:* Inkluderar endast konverteringar för vilka endast en enhet spårades i konverteringssökvägen. I rapporten har &quot;[!UICONTROL (sd)]&quot; lagts till i konverteringsmåttets namn och regeltyp.

* *[!UICONTROL Cross Device (XD)]:* Inkluderar endast konverteringar för vilka mer än en enhet spårades i konverteringssökvägen. I rapporten har &quot;[!UICONTROL (xd)]&quot; lagts till i konverteringsmåttets namn och regeltyp.

**[!UICONTROL Conversion Reporting Based On]:**  Rapportera konverteringsdata:

* *[!UICONTROL Conversion Timestamp]:* (Standardvärdet) Konverteringar kopplas till konverteringsdatumet.

* *[!UICONTROL Event Timestamp]:* Konverteringar rapporteras baserat på datumet för det intryck eller klick som orsakade konverteringen, enligt vad som anges  [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Email Recipients] Avsnitt

**[!UICONTROL Email]:** E-postadress(er) dit slutförda rapporter eller meddelanden ska skickas om rapporten avbryts på grund av fel. Om du vill ange flera adresser avgränsar du dem med kommatecken eller mellanslag.

**[!UICONTROL Frequency]:** Hur ofta ska rapporten skickas:  *[!UICONTROL Once]*,  *[!UICONTROL Daily]*,  *[!UICONTROL Weekly]* eller  *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Avsnitt

**[!UICONTROL Send & Save]:** När rapporten ska skickas:  *[!UICONTROL On Schedule]* eller  *[!UICONTROL Run Now]*. Schemalagda rapporter levereras senast 09:00 i kontots tidszon.

>[!NOTE]
>
>Du kan [köra en anpassad rapport när som helst](report-run-now.md) från vyn [!UICONTROL Reports].

>[!MORELIKETHIS]
>
>* [Om anpassade rapporter](/help/dsp/reports/report-about.md)
>* [Skapa en anpassad rapport](/help/dsp/reports/report-create.md)
>* [Duplicera en anpassad rapport](/help/dsp/reports/report-copy.md)
>* [Redigera en anpassad rapport](/help/dsp/reports/report-edit.md)
>* [Kör en anpassad rapport](/help/dsp/reports/report-run-now.md)
>* [Anpassade rapportinställningar](/help/dsp/reports/report-settings.md)

* [Tillgängliga rapportkolumner](/help/dsp/reports/report-columns.md)
