---
title: De architectuur van Analyse - hoe te om uw gegevensmodel van Customer Journey Analytics te benaderen
description: Leer hoe te om CJA gegevensmodellen met gebeurtenishiërarchieën, attributie, en KPIs te structureren om diepere inzichten van de klantenreis te ontsluiten.
feature: Attribution
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 0
last-substantial-update: 2025-09-04T00:00:00Z
jira: KT-18813
source-git-commit: 124b52203b98a80dd9202dab1b0dbe575475a52b
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# The Architecture of Analysis: How to Approach Your Customer Journey Analytics Data Model

Een cruciaal aspect van het bouwen van een CJA-gegevensmodel is het begrijpen van de hiërarchische relatie tussen verschillende aanraakpunten en interacties. Dit vormt de basis voor zinvolle analyse en inzichten.

Voornaamste overwegingen zijn:

* Het identificeren van en het in kaart brengen van de punten van de klanteninteractie over alle kanalen
* Duidelijke hiërarchieën en relaties tussen gebeurtenissen instellen
* Consistente toewijzingsmodellen definiëren
* Gestandaardiseerde metriek en KPIs creëren

Door deze elementen goed te structureren, kunnen organisaties de volledige klantenreis beter volgen en analyseren, die tot actievere inzichten en betere besluitvormingsmogelijkheden leidt.

>[!VIDEO](https://video.tv.adobe.com/v/3471111/?learn=on&enablevpops)

## Gegevensmodellering ontgrendelen voor krachtige analyse

Ontdek hoe effectieve gegevensarchitectuur in Adobe Experience Platform (AEP) en Customer Journey Analytics (CJA) actioneerbare inzichten en rapportering aanstuurt.

* **het Ontwerp van het Schema van Kant** de keus tussen vlakke schema&#39;s, series, en series van voorwerpen beïnvloedt rechtstreeks analysemogelijkheden en het melden van flexibiliteit.
* **Gegevens die van het Proces van de Transformatie** in AEP worden opgenomen moeten zorgvuldig gestructureerd zijn om naadloze transformatie en bruikbaarheid in CJA te verzekeren.
* **Begrijpend gebeurtenis, zitting, en persoonniveaus van de Hiërarchie van 0} Container is cruciaal voor multi-level analyse en nauwkeurige rapportering.**
* **Praktische Strategieën** Voorste planning, schemabeheer, en het leveraging platformeigenschappen zijn zeer belangrijk aan scalable, toekomstbestendige implementaties.

Het beheersen van deze concepten machtigt teams om hun analytische werkschema&#39;s te optimaliseren en diepere bedrijfsinzichten te ontsluiten.

## Typen schema&#39;s en het gebruik ervan

* **Vlakke Schema&#39;s** het best voor duidelijke, één-aan-één gegevensverhoudingen. Ideaal voor het bijhouden van basisgebeurtenissen en eenvoudige meetwaarden/dimensies.
* **Arrays** nuttig voor lijsten van verwante punten (b.v., productcategorieën, inhoudmarkeringen). Elk arrayelement wordt een afzonderlijke dimensie voor analyse.
* **Arrays van Objecten** Ontworpen voor complexe gebruiksgevallen zoals productaankopen, waar elk voorwerp zijn eigen eigenschappen en verhoudingen handhaaft. Hiermee wordt gedetailleerde analyse op objectniveau ingeschakeld.
* **het kiezen van Wisely** selecteert het eenvoudigste schema dat aan uw behoeften voldoet, maar hefboomwerkings series en voorwerpen voor geavanceerde scenario&#39;s die relatiebehoud vereisen.