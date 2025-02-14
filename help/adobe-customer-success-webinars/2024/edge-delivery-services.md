---
title: De levering van inhoud optimaliseren - De kracht van Edge Services ontgrendelen
description: De sessie over Edge Delivery Services (EDS) ging over de architectuur, integratie met op documenten gebaseerde en op AEM gebaseerde authoring, snel maken van sites, aanpassingsopties en aanbevolen procedures voor het handhaven van hoge prestaties.
solution: Experience Manager, Experience Manager as a Cloud Service
feature: Edge Delivery Services
role: Admin, Developer, Leader, User
level: Intermediate
doc-type: Event
duration: 3589
last-substantial-update: 2024-12-06T00:00:00Z
jira: KT-16631
exl-id: 2057e491-9ec3-4bfe-b85a-6b74d70822bf
source-git-commit: 32060a6a0d2cc24b8dc09c8f5e9f9d9c679e6d3e
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# De levering van inhoud optimaliseren: de kracht van Edge Services vrijmaken

In deze sessie geven we een overzicht van Edge Delivery Services (EDS) en de architectuur ervan. Via de Universal Editor zullen we uitzoeken hoe EDS integreert met op documenten gebaseerde ontwerpen en op AEM gebaseerde ontwerpen. In een live demo wordt EDS in actie gebracht, gevolgd door bronnen voor verdere verkenning en een sessie met vragen en antwoorden.

>[!VIDEO](https://video.tv.adobe.com/v/3440938/?learn=on&enablevpops)

## Toetsen

### Inleiding tot EDS

* EDS is een reeks van composable diensten die worden ontworpen om de mogelijkheden van ATM te verbeteren. &#x200B;
* Het is bedoeld om uitzonderlijke ervaringen te bieden die de betrokkenheid en conversies stimuleren met snelle ontwikkelingscycli en een 100% vuurtorenscore. &#x200B;

### Ontwerpopties

* **op document-Gebaseerde Authoring** gebruikt vertrouwde hulpmiddelen zoals Microsoft Word of Google Docs voor inhoudsverwezenlijking, die snelle inhoudsverwezenlijking zonder uitgebreide opleiding toestaat. &#x200B;
* **Universele Redacteur** verstrekt een interface van WYSIWYG gelijkend op de traditionele plaatsen van ATM, die voor gedetailleerdere en visuele inhoudsverwezenlijking toestaan. &#x200B;

### Architectuur

* EDS integreert binnen het Amazon Cloud Service-kader. &#x200B;
* Deze functie ondersteunt een serverloze implementatie en kan werken zonder een traditionele auteur- of uitgeversinstantie. &#x200B;
* Twee niveaus van caching kunnen worden uitgevoerd: op het niveau van de klanteninfrastructuur en het niveau van EDS. &#x200B;

### Contentmanagement

* Voor op documenten gebaseerde authoring zijn een GitHub-account, Google Drive of Microsoft SharePoint, een secundaire insteekmodule en een codesynchronisatieprogramma vereist. &#x200B;
* EDS met IAM authoring vereist een GitHub-account, een IAM als cloudservice-licentie en een codesynchronisatiehulpmiddel.

### Ontwikkeling en implementatie

* Het maken van een site met EDS gaat snel en duurt vaak minder dan een dag. &#x200B;
* Lokale ontwikkeling kan worden uitgevoerd met de opdracht Omhoog om een lokale versie van de website te maken.
* Wijzigingen kunnen worden doorgevoerd om vertakkingen voor testdoeleinden te voorzien voordat ze worden samengevoegd in de hoofdvertakking. &#x200B;

### Aanpassing en uitbreidbaarheid

* Aangepaste componenten kunnen worden gemaakt met eenvoudige CSS en JavaScript. &#x200B;
* De architectuur staat voor derdeintegratie en douane auteursbronnen toe.

### Aanbevolen procedures

* Het wordt aanbevolen om vanilla JavaScript en CSS te gebruiken voor het bijhouden van hoge vuurtorscores.
* Elke introductie van bibliotheken zoals React moet zorgvuldig worden overwogen en getest om te voorkomen dat de prestaties afnemen.

### Ondersteuning en documentatie

* Er is uitgebreide documentatie beschikbaar om gebruikers door het installatie- en aanpassingsproces te begeleiden. &#x200B;
* Gebruikers worden aangespoord om Adobe-ondersteuning te zoeken voor onopgeloste problemen. &#x200B;
