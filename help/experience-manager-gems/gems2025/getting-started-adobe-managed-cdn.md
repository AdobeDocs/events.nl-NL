---
title: AEM GEM's - Aan de slag met door Adobe beheerde CDN
description: Leer hoe u een door Adobe beheerde CDN configureert in AEM Cloud Service om de prestaties en beveiliging te verbeteren met nieuwe CDN-configuratiemogelijkheden.
role: Developer, User
level: Intermediate
feature: Edge Delivery Services
doc-type: Event
duration: 3438
last-substantial-update: 2025-01-30T00:00:00Z
jira: KT-17227
exl-id: 4cd0332f-95bf-45f4-a765-aba020c0d7b0
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# AEM GEM&#39;s - Aan de slag met door Adobe beheerde CDN

Meer informatie over de door Adobe beheerde CDN in AEM Cloud Service en over de manier waarop deze kan worden geconfigureerd. Sluit u aan bij ons om de nieuwe CDN-configuratiemogelijkheden te verkennen die kunnen worden gebruikt om de prestaties en de beveiliging van uw AEM as a Cloud Service-toepassingen te verbeteren. In deze sessie ontdekt u:

* Wat is de Adobe CDN
* Relevante topologieën voor AEMaaCS en Edge Delivery Services
* Typische gebruiksgevallen die met CDN-regels kunnen worden geïmplementeerd
* Hoe te om RDEs te gebruiken om configuraties snel te testen en op te stellen CDN

>[!VIDEO](https://video.tv.adobe.com/v/3443168/?learn=on&enablevpops)

*Opgenomen op 22 Januari, 2025*

Heb je een vraag, misschien een opmerking?  Sluit me aan bij de bespreking in de [&#x200B; Gemeenschappen van Experience League &#x200B;](https://adobe.ly/4haufPK)!

## Toetsen

### Belangrijke functies van door Adobe beheerde CDN

* **de Domeinen en de Certificaten van de Douane** Essentieel voor het ontvangen van douanedomeinen en certificaten om veilige verbindingen te vestigen.
* **Caching** die de reacties van HTTP van geheim voorgeheugen leveren is beduidend sneller (onder 10 milliseconden) vergeleken bij het halen van van de oorsprong (honderden milliseconden).
* **uit-van-de-Doos en Eigen CDN** Adobe verstrekt een uit-van-de-doos beheerde CDN, maar de gebruikers kunnen hun eigen CDN ook brengen.

### Configuratieopties

* **de Transformaties van het Verzoek** wijzigen kopballen, herschrijven wegen, blokverkeer, en richten verzoeken opnieuw.
* **Filters van het Verkeer** Blok of staat verkeer toe dat op specifieke regels wordt gebaseerd.
* **Steun van de Authentificatie** voor randsleutel, ponssleutel, en basisauthentificatie.
* **de verzoeken van de Volmacht van de Selecteurs van de Oorsprong van 0&rbrace; aan verschillende oorsprong die op bepaalde regels wordt gebaseerd.**
* **Transformaties van de Reactie** wijzigt reactiekopballen en status.

### Implementatie en aanpassing

* **de Pijpleiding van de Configuratie** stelt dossiers YAML op om CDN regels te vormen.
* **de regels van de de verkeersfilter van het Verkeer van de Bescherming van het Verkeer** om, verkeer te blokkeren, te registreren en te waarschuwen dat op patronen wordt gebaseerd.
* **het Beperken van het Tarief** beschermt tegen aanvallen DDoS door het aantal verzoeken per IP te beperken.

### Gereedschappen en analyse

* **de Stapel van Elasticsearch Kibana** analyseert gebruik en verkeer met verstrekte dashboards.
* **Logboek dat** door:sturen logboeken aan een instantie van de Splunk voor analyse.

### Hooglichten demo

* **het Opstellen van Configuraties** Demonstreerde het opstellen van de regels en de omleidingen van de verkeersfilter.
* **Authentificatie en de Selectie van de Oorsprong** toonde hoe te opstellings basisauthentificatie en volmachtsverkeer aan verschillende oorsprong.

### Aanbevolen procedures

* **Snelle Reacties** verzekeren snelle reacties van oorsprong om kwetsbaarheid te vermijden.
* **het Goede In cache plaatsen** Hefboomwerking om verkeer efficiënt te behandelen.
* **de Dashboards van het Gebruik** analyseren verkeer en gebruik om aangewezen tariefgrenzen te plaatsen.
* **combineer Strategieën** Gebruik verschillende tarief beperkende strategieën voor betere bescherming.
* **de Reeks Alarm** krijgt bericht wanneer de plaats onder aanval is.
* **Regels van de Test** Begin met het registreren acties alvorens te blokkeren om regels te verzekeren werken zoals verwacht.

### Contact en feedback

* **de Terugkoppeling en Gevallen van het Gebruik** bereiken uit aan het team voor geavanceerde gebruiksgevallen en terugkoppelen.
* **Toekomstige Zittingen** nemen aan opiniepeilingen deel om onderwerpen voor toekomstige zittingen voor te stellen.
