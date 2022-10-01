---
title: Syntax för målgruppssegmentslogik
description: Referera till den syntax du kan använda för att definiera logiken för målgruppssegment.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: efd04189de975f8f075dec7851a3a06d2d647ded
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Syntax för målgruppssegmentslogik

När du skapar återanvändbara målgrupper kan du definiera segmentlogik manuellt med hjälp av alfanumeriska segment-ID:n (nycklar) och följande syntax:

* () för att ange en grupp
* `||` for [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; för [!DNL AND]
* ! for [!DNL NOT] (exkludera)

>[!NOTE]
>
>* Alla angivna segmentgrupper inkluderas om de inte föregås av ! (som utesluter dem).
>* Du kan [hitta segment-ID:t för en målgrupp](reusable-audience-clipboard.md) från [!UICONTROL Audiences] > [!UICONTROL All audiences].


Till exempel följande logik:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

betyder (på engelska)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>I placeringsinställningarna kan du använda sparade målgrupper antingen som målgrupper för att explicit målinrikta eller som separata målgrupper för att exkludera från målinriktning. Se till att segmentlogiken återspeglar syftet med målgruppen.

>[!MORELIKETHIS]
>
>* [Kopiera segmentnyckeln för en återanvändbar publik till Urklipp](reusable-audience-clipboard.md)
>* [Om Audience Management](audience-about.md)
>* [Skapa en återanvändbar publik](reusable-audience-create.md)
>* [Målgruppsinställningar](audience-settings.md)
>* [Tillgängliga dataproviders från tredje part](third-party-data-providers.md)

