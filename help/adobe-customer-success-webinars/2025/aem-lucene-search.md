---
title: Essentiële tips en aanbevolen procedures voor AEM Lucene Search
description: Verhoog de digitale betrokkenheid met geavanceerde AEM-zoekgereedschappen, zoals filters, facetten, automatische suggesties, NGram en spellingcontrole. Leer van echte demos.
solution: Experience Manager
feature: Search
role: Admin, Developer
level: Intermediate, Experienced
doc-type: Event
duration: 3630
last-substantial-update: 2025-11-13T00:00:00Z
jira: KT-19550
source-git-commit: 84c9a126769fa94b0197d12ca594137e13edc510
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# Essentiële tips en aanbevolen procedures voor AEM Lucene Search

Ontdek hoe u uw digitale aanwezigheid kunt verbeteren en de betrokkenheid van klanten kunt verbeteren met de meest geavanceerde zoekfuncties, zoals filters, facetten, automatische suggesties, NGram en spellingcontrole. Leer van real-world demos en verbeter inzicht in het optimaliseren van uw onderzoeksmogelijkheden met AEM en Lucene. Dit webinar biedt u de mogelijkheid om uw zoekervaring op te voeren en voorop te blijven in het digitale landschap.

>[!VIDEO](https://video.tv.adobe.com/v/3476410/?learn=on&enablevpops)

## Krachtig zoeken in Adobe Experience Manager ontgrendelen

Adobe Experience Manager (AEM) maakt gebruik van Lucene-zoekopdrachten voor snelle, relevante resultaten in inhoud, elementen en metagegevens. Deze zitting verkent hoe de indexen van Lucene werken, hoe te om hen te vormen, en de beste praktijken voor het maximaliseren van onderzoeksprestaties.

* **het Onderzoek van Lucene is overal** Bevoegdheden onderzoek in de auteur, de uitgever, en portals van AEM, behandelend auto-suggesties, filters, facetten, en paginering.
* **de Prestaties van de Aandrijving van de Definities van de Index** Het aanpassen van de indexdefinities van Oak is essentieel voor efficiënt, gericht onderzoek.
* **Kopieer bestaande indexdefinities van de Aanpak van de Praktijken van 0&rbrace; &lbrace;, grens geïndexeerde eigenschappen, en gebruik de juiste vlaggen voor full-text en bezitsonderzoeken.**
* **de Geavanceerde Eigenschappen verbeteren UX** Gezichten, auto-suggereert, spellingcontrole, het opvoeren, en het stammen kunnen voor rijkere onderzoekservaringen worden toegelaten.

Als u deze beginselen begrijpt, kunt u zorgen voor stabiele zoekmogelijkheden van hoge kwaliteit in AEM, waarmee u zowel technische als zakelijke doelstellingen ondersteunt.

## Bouwblokken voor Lucene Index

AEM Lucene-indexdefinities vormen de basis voor zoekprestaties en nauwkeurigheid. De belangrijkste componenten omvatten:

* **Type** specificeert indexsoort (Luzern, bezit, enz.).
* **de Beperking van het Type van Knoop** richt specifieke inhoudstypes (b.v., dam :Asset, cq :Page).
* **Beperking van de Weg** Beperkt het indexeren aan bepaalde bewaarplaatspaden voor efficiency.
* **controleert de samengevoegde Regels** diepte en werkingsgebied van geïndexeerde inhoud, die relevante eigenschappen verzekeren zijn doorzoekbaar.
* **Regels van de Index** de configuratie van de Kern; reeksen vlaggen zoals nodeScopeIndex (brede full-text onderzoek) en geanalyseerd (tokenization/normalization).

De zorgvuldige configuratie van deze elementen zorgt ervoor dat de onderzoeksvragen snel, relevant, en middel-efficiënt zijn.

## Zoekprestaties optimaliseren

De efficiënte onderzoeksoptimalisering in AEM Lucene impliceert strategische configuratie en naleving van beste praktijken:

* **Begin met Bestaande Indexen** kopieert en wijzigt altijd uit-van-de-doosdefinities, bouwt nooit van kras.
* **Grens Geïndexeerde Eigenschappen** omvat slechts noodzakelijke eigenschappen om indexen te houden len en uitvoerend.
* **Gebruik alleen markeringen:
   * **nodeScopeIndex** waar voor brede full-text onderzoek
   * **geanalyseerd** waar voor bezit-niveau tokenization
   * **evaluatePathRestriction** waar voor op weg-gebaseerde vragen
* **Bezit het Indexeren** verkiest bezitsbeperkingsonderzoeken naar beste prestaties; gebruik full-text slechts wanneer nodig.
* **het Sorteren &amp; Facets** laat propertyIndex en orde voor het sorteren toe; reeks facet** waar voor op telling-gebaseerd filtreren.

Het toepassen van deze strategieën leidt tot snellere vragen, verminderd middelgebruik, en relevantere resultaten.

