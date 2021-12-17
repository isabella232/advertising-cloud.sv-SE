---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: Om blockerade webbplatser på kontonivå och annonsnivå
description: Om blockerade webbplatser på kontonivå och annonsnivå
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Om blockerade webbplatser på kontonivå och annonsnivå

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
Du kan redigera listan över blockerade webbplatser som används för hela Advertising Cloud-kontot och ytterligare listor för enskilda annonsörer i kontot.

Blockerade platser listar definierar uppsättningar av mål som ska uteslutas för dina placeringar. Varje lista kan bestå av webbplatsdomäner på den översta nivån och alla nivåer <!--- verify --> underdomäner (till exempel example.com, my.example.com eller my.new.example.com) och mobilappsnamn (till exempel ??)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

Annonsnivålistor åsidosätter kontonivålistor.

>[!NOTE]
>
>* Listor över blockerade webbplatser på kontonivå och annonsörnivå används utöver Advertising Cloud DSP [globalt blockerad webbplatslista](/help/dsp/introduction/features/brand-safety-media-quality.md), som innehåller webbplatser som inte anses säkra för annonser.
>* Användarna kan också lägga till riktade webbplatser på alla platser.
>* Listor med blockerade webbplatser åsidosätter alltid målwebbplatslistor. Om en placering båda utesluter och innehåller samma mål för en annons, utesluts målet. <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
