---
title: Sequentiële logica volgen in Adobe Analytics en Customer Journey Analytics - Begint en stopt
description: Hoofd opeenvolgende logica in Adobe Analytics met geavanceerde segmentatie, werkingsgebiedcontroles, en afgeleide gebieden om klantengedragspatronen te ontdekken en gegevensnauwkeurigheid te verbeteren.
solution: Analytics, Customer Journey Analytics
role: Developer
level: Intermediate
doc-type: Event
duration: 3370
last-substantial-update: 2025-05-08T00:00:00Z
jira: KT-18017
source-git-commit: cfc7b54ae4360779ca2c41f88fc08089bae99165
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---


# Mastering Sequential Logic in Adobe Analytics en Customer Journey Analytics: start en stop

In deze sessie gaan we onderzoeken hoe u reeksen kunt configureren met de THEN-operator in Adobe Analytics (AA) en Customer Journey Analytics (CJA). Leer om nauwkeurige ondergroepen van activiteit terug te winnen door SLECHTS NA/ALLEEN VOOR REEKS MET UITSLUITENDE controlepunten te combineren.

## Discussiepunten

* Snelle beoordeling van standalone opeenvolgende logische operatoren en visueel framework.
* Beschrijf hoe UITSLUITEN de resultaten van opeenvolgingen beïnvloedt gebruikend SLECHTS NA/VOOR REEKS.
* De huidige gebruiksgevallen en demo&#39;s die tonen hoe u de methodes voor uw zaken kunt goedkeuren.

>[!VIDEO](https://video.tv.adobe.com/v/3458040/?learn=on&enablevpops)

## Hooglichten


1. Opeenvolgende logica en segmentering in Analytics

   * De zitting concentreerde zich op geavanceerde technieken voor het toepassen van opeenvolgende logica in analyses, die het belang benadrukken van het begrip van begin en het tegenhouden van punten in gegevensopeenvolgingen om klantengedrag effectief te analyseren.
   * Sequentiële operatoren werden besproken als hulpmiddelen voor het identificeren van patronen, zoals &#39;webhit gevolgd door een hit via e-mail&#39; of &#39;indiening van toepassingen gevolgd door volgende sessies&#39;.
   * De greedy aard van segmentlogica werd benadrukt, verklarend hoe het de grootste mogelijke gegevensreeks tenzij beperkt door extra voorwaarden terugkeert.
   * Technieken voor het bepalen van werkingsgebied, zoals &quot;slechts vóór&quot;en &quot;slechts na&quot;opeenvolgingen, werden geïntroduceerd om ondergroepen van gegevens te bestuderen die op specifieke bedrijfsvragen worden gebaseerd.
   * Het gebruik van controlepunten, nabijheidsvoorwaarden, en uitsluitingscriteria werd verklaard om gegevensanalyse te verfijnen en complexe bedrijfsvragen te beantwoorden.

2. Meerdere interessepunten afhandelen in gegevensanalyse

   * Andy besprak scenario&#39;s waar de klanten veelvoudige toepassings voorlegging en de behoefte hebben om gedrag na elke voorlegging te analyseren eerder dan enkel eerste.
   * Uitdagingen zoals overlappende aanvragen en het bepalen of oorspronkelijke punten van belang moeten worden opgenomen of uitgesloten, werden behandeld.
   * Er werd gewezen op het belang van het verduidelijken van veronderstellingen en het verfijnen van logica om meerdere voorvallen van een reeks aan te pakken, zodat een nauwkeurige analyse van het gedrag van klanten gedurende hun hele levenscyclus wordt gewaarborgd.

3. Geavanceerde technieken voor het stoppen van gegevensafstemming

   * De sessie introduceerde methoden om te stoppen met het afstemmen van gegevens op specifieke controlepunten aan de hand van uitsluitingscriteria, zodat analisten gegevens kunnen bestuderen tussen gedefinieerde start- en stoppunten.
   * Voorbeelden hiervan waren het analyseren van gedragingen tussen &#39;webresultaten gevolgd door interactie met mobiele apps&#39; en het stoppen bij &#39;e-mailinteractie&#39;.
   * Het gebruik van &quot;binnen&quot;- en &quot;na&quot;-voorwaarden werd uitgelegd om strengere nabijheidsregels te handhaven en ongewenste resultaten van hebzuchtige logica te vermijden.
   * Andy heeft laten zien hoe deze technieken kunnen worden toegepast om het gedrag van klanten te bestuderen ten opzichte van specifieke gebeurtenissen, zoals het indienen van toepassingen.

4. Validatie en verfijning van Data Analysis Logic

   * Andy benadrukte het belang van het bevestigen van veronderstellingen en het testen van logica om nauwkeurige resultaten te verzekeren, aangezien de fouten in segmentbouw of gegevensveronderstellingen gemeenschappelijk zijn.
   * Voorbeelden van onverwachte resultaten als gevolg van hebzuchtige logica werden gedeeld, wat de behoefte aan strikte voorwaarden zoals &quot;binnen één gebeurtenis&quot; of &quot;binnen één sessie&quot; benadrukt.
   * Aanbevolen werd om valideringsbenchmarks, zoals kleine gegevenssets met bekende kenmerken, te testen en de analysemethoden te verfijnen.

5. Toepassing van Opeenvolgende logica op situaties van werkelijk gebruik

   * Andy gaf voorbeelden van praktijkvoorbeelden, zoals het analyseren van klantengedrag na toepassingspogingen of het identificeren van gemeenschappelijke acties na aankopen of negatieve recensies.
   * De sessie toonde aan hoe sequentiële logica kan worden toegepast op studiepatronen zoals &#39;eerste sessie na toepassing&#39; of &#39;tweede sessie na toepassing&#39; voor meerdere instanties.
   * Het belang van het schrapen van analyse aan bredere gegevensreeksen terwijl het handhaven van nauwkeurigheid werd besproken, met voorbeelden van trapsgewijze gevolgen in zitting-vlakke gegevens.

6. Het gebruiken van Afgeleide Gebieden voor Flexibele Analyse

   * Andy introduceerde het concept van het gebruiken van afgeleide gebieden in Adobe Customer Journey Analytics (CJA) om momenten van belang dynamisch te bepalen, die de behoefte verminderen om veelvoudige filters voor elke analyse uit te geven.
   * Met afgeleide velden kunnen analisten filters maken ten opzichte van één veld, zodat ze snel verschillende aandachtspunten kunnen bestuderen, zoals productspecifieke toepassingen of andere klantgebeurtenissen.

7. Praktische toepassingen en toekomstige plannen

   * Andy deelde plannen voor de volgende webinar zitting, die zich op malplaatjes, bedrieglijke bladen, en praktische toepassingen van de behandelde concepten zal concentreren, die zich van opleiding aan actionable gebruiksgevallen bewegen.
   * De sessie werd afgesloten met een oproep tot het indienen van feedback via een opiniepeiling om de interesse in toekomstige onderwerpen te bepalen en ervoor te zorgen dat deze worden afgestemd op de doelstellingen van de deelnemers.
   * Andy benadrukte de micro-overeenkomsten van het Ultimate Success-team en bood gerichte coachingssessies om bedrijven te helpen deze concepten toe te passen op hun specifieke gebruiksgevallen.

8. Materialen delen en follow-upacties

   * Andy bevestigde dat webinar materiaal, inclusief opnamen en blogberichten, met deelnemers zal worden gedeeld en een gedocumenteerde vorm van de inhoud van de sessie zal geven.
   * Aanwezigen werden aangemoedigd om hun TAM&#39;s of CSM&#39;s te bereiken voor verdere hulp en om Ultimate Success-licenties voor persoonlijke coachingssessies te verkennen.
