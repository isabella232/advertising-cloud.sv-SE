---
title: Pre-Bid-filter på placeringsnivå och Så här använder du dem
description: Referera till tillgängliga filter på placeringsnivå före köp och se hur du använder dem.
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: d17adc94a211992899e9f2eec6f9e13c16aa02c0
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Pre-Bid-filter på placeringsnivå och Så här använder du dem

| Förköpsfilter | Beskrivning | När ska det här filtret användas |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Ställer in ett minsta förutsägelsetröskelvärde för sannolikheten för att en auktion kommer att resultera i en klickfrekvens. Om du till exempel anger tröskelvärdet till 0,1 % så kommer du inte att lägga något bud på en auktion såvida inte den förväntade sannolikheten för ett klick är större än eller lika med 0,1 %.<br><br><b>Obs!</b> Filter tillämpas före optimeringsmål. Därför kan mycket strikta filter förhindra utgifter. | Använd när du har ett KPI-mål för klickfrekvens (CTR) och inte vill spendera budgeten när CTR ligger under tröskelvärdet. Det här filtret kan vara ganska restriktivt, så det är viktigt att ställa in realistiska mål. Beroende på andra placeringsbegränsningar är målet 0,03-,07 % vanligtvis en bra startpunkt. Ni kan optimera detta på webbplatsnivå efter behov för att förbättra mätvärdena.<br><br>Om målet är att uppnå en lägsta CTR och bästa möjliga CPM är den rekommenderade konfigurationen att kombinera en [!UICONTROL Click Through Rate] filter med optimeringsmålet &quot;[!UICONTROL Lowest CPM].&quot; Om ditt mål är en maximal CPM utan någon verklig fördel när det gäller att överträffa, och en minsta CTR, parar du en [!UICONTROL Click Through Rate] filter med optimeringsmålet &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; kan vara lämpligare. |
| [!UICONTROL 100% Completion Rate] | Anger en obligatorisk minsta slutförandehastighet som måste uppfyllas innan du lägger ett bud på ett intryck. | Använd det här filtret när kampanjens huvudmål är antalet slutförda aktiviteter. Faktor för andra målinriktningsparametrar, men 65 % är den rekommenderade startprocenten. |
| [!UICONTROL Player Size - Adobe] | Anger en nödvändig minsta spelarstorlek med data från Advertising Cloud DSP. Du får köpa en bild när [!UICONTROL Player Size] tröskelvärdet har uppnåtts. | Används för att säkerställa att ni levererar ett komplett spelarlager med data från DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Anger en obligatorisk minsta spelarstorlek, med data från [!DNL Moat] eller [!DNL Integral Ad Science] ([!DNL IAS]). Du får köpa en bild när [!UICONTROL Player Size] tröskelvärdet har uppnåtts. | Används för att säkerställa att ni levererar på hela spelarlistan med plattformstäckande [!DNL Moat] eller [!DNL IAS] data.<br><br><b>Obs!</b> Använd bara det här filtret när kampanjen är konfigurerad att använda [!DNL Moat] eller [!DNL IAS] data. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Anger en obligatorisk minsta visningsprocent, med Advertising Cloud DSP visningsvärden och mått. Du lägger bud på ett intryck när det angivna tröskelvärdet uppnås.<br><br><b>Anteckningar:</b><ul><li>Om kampanjen [!UICONTROL Viewability Sensitivity] inställningen är &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)],&quot; [!DNL Media Rating Council] (MRC) visningsstandarden används för kampanjen. Om [!UICONTROL Viewability Sensitivity] inställningen är &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)],&quot; [!DNL GroupM] visningsmåttstandarden används för kampanjen.</li><li>Måttdefinitioner för Adobe skiljer sig från definitioner från andra tillverkare, så det kan finnas små skillnader med data från tredje part.</li></ul> | Det bästa sättet är att matcha optimeringsmålet och eventuella filterinställningar före bud med kampanjens [!UICONTROL Viewability Sensitivity] inställning. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Hur DSP optimerar era kampanjer](optimization-how-dsp-optimizes-campaigns.md)
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Kampanjinställningar](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Optimeringsmål och Så här använder du dem](optimization-goals.md)

