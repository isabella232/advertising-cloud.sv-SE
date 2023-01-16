---
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Samarbetsdokumentation för Adobe Advertising

Det här är dokumentationsarkivet för Adobe Advertising, inklusive korsproduktsdokument och DSP. (Senare kommer det att innehålla dokument för sökning och eventuellt (?) för Creative.)

**Obs! Den här sidan publiceras inte i kunddokumentationen.**

## Innehåll

+ `TOC.md` i roten av en användarhandbok, där du kan ordna de ämnen som finns i handboken.
+ Varje användarhandbok har en unik `TOC.md`, där du kan ordna alla sidor/ämnen efter behov.


## Användarhandbok

+ Introduktionen till användarhandboken kallas `overview.md`
+ Varje avsnitt i användarhandboken har en egen katalog.
   + Om det finns ett ämne i guiden som heter *Implementering*, är motsvarande katalog `/implementation`
+ Alla bildresurser lagras i `/assets` i roten av användarhandboken.
   + Alla bilder i `/assets` kommer att lokaliseras.
   + Alla bilder i `/no-localize` kommer inte att lokaliseras (det kommer en överraskning!). Detta kan användas för att i lokala versioner säkerställa att specifika resurser inte reproduceras i onödan.

## Metadata för användarhandboksnivå

+ Metadata som beskriver användarhandboken lagras i `TOC.md`. Detta omfattar följande:
   + product - product/capabilities.
   + cloud - molnet som den här produkten tillhör.
   + målgrupp - målgrupp eller arketyp som guiden riktar sig till.
   + användarhandbok - namn på användarhandboken.

## Metadata för sidnivå

+ Metadata som krävs för att beskriva ett dokument lagras som en del av varje enskild sida. Detta omfattar följande:
   + rubrik - sidans rubrik
   + description - description of page
   + seo-title - seo alternativ titel
   + seo-description - alternativ titel för SEO-ändamål
   + short title - (valfritt fält)
   + index - ja/nej - kommer sidan att indexeras av Adobe sökplattform
   + translate - yes / no - will this page localized
   + beta - är den här produkten i betaversion?
   + omdirigering - kan användas för att skapa en referens till en ny sida om det skulle behövas
   + doc-type: referens (standard) / felsökning / utvecklare / självstudiekurs / kb / whitepaper

## Mer information

Mer publiceringsanvisningar, stilguider, exempel och andra resurser finns i:

+ [Riktlinjer för författare **specifikt för Adobe Advertising**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [Samarbete för alla Adobe-skribenter](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

Se även:

+ contribute.md En översikt över hur du kan bidra till dokumentationen.

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-behavior.md För en översikt över de beteendestandarder vi förväntar oss när ni bidrar till detta dokumentationsprojekt.
