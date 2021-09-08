---
title: Vanliga frågor om kampanjhantering
description: Lär dig mer om kampanjhantering, inklusive latensperioden för ändringar och vad som händer när du gör budgetändringar under en flygning.
feature: Packages, Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Vanliga frågor om kampanjhantering

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Fördröjning för inställningsändringar

* När du ändrar en placering eller paketinställning, när kommer ändringen att gälla?

   Inställningarna börjar oftast gälla omedelbart, men kan ta upp till 12 timmar.

   Om det är sista leveransdagen kan du göra ändringar tidigt på dagen så att DSP hinner kalibrera om paketet baserat på ändringarna. Om du till exempel ändrar från jämna mellanrum till förhandslastpacing, måste DSP omvärdera hur de kommer att fördela utgifterna under resten av flygningen. Gör inte den sortens förändring om du bara har en timma kvar att leverera på flygningens sista dag.

## Budgetuppdateringar efter halva flygresan

* Hur lång tid tar det att omfördela paketbudgeten när du ändrar en placering?

   Budgettilldelningen baseras på placeringsprestanda, som utvärderas med ett 14-dagars genomsnitt. Ändringar av en placering resulterar endast i ändringar i budgettilldelningen när de orsakar prestandaförändringar under 14-dagarsgenomsnittet.

   När prestandaförändringar inträffar omfördelar DSP paketbudgeten bland enheterna i enlighet med detta under nästa budgetoptimeringscykel, som inträffar vid ungefär midnatt (00:00) i kampanjens tidszon.

* Hur omfördelas budgeten när en placering tas bort från ett paket och läggs till i ett annat paket?

   En placerings hela utgiftshistorik bifogas till placeringen och följer med från paket till paket.

   När du tar bort en placering från ett paket har paketet inte längre någon historik över placeringens utgifter. Paketbudgeten blir (paketbudget - borttagen placeringsbudget) / återstående tidsintervall. Paketbudgeten tilldelas sedan de återstående placeringarna i paketet.

   På samma sätt gäller att om du lägger till samma placering i ett annat paket, kommer placeringens utgiftshistorik att hanteras i DSP när den allokerar budget för alla placeringar i det nya paketet.

* Hur förändras paketeringen på den sista dagen av en flygning?

   På flygningens sista dag förkortas dagen från 24 till 23 timmar så att paketbudgeten inte överskrids. Paketets paketeringsfyllningsstrategi ändras automatiskt till [!UICONTROL Frontload], även om den är inställd på [!UICONTROL even]. Det innebär att 65 % av den dagliga budgeten ska ha nått klockan 11.30 EST.

>[!MORELIKETHIS]
>
>* [Paketinställningar](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placeringsinställningar](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Bästa metoder för att konfigurera resultatkampanjer](/help/dsp/optimization/campaign-best-practices-performance.md)

