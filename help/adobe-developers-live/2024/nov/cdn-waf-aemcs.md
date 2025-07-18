---
title: CDN- en WAF-configuratie in Adobe Experience Manager as a Cloud Service
description: Verbeter de prestaties en de veiligheid van de toepassingen van Adobe Experience Manager as a Cloud Service met klantgerichte CDN regels, de bescherming van WAF, en de Pijpleiding Config, zoals die door de deskundigen van Adobe wordt gedeeld.
solution: Experience Manager as a Cloud Service
feature: Security
topic: Performance, Security
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 2211
last-substantial-update: 2024-11-26T00:00:00Z
jira: KT-16574
exl-id: a9f38e79-c707-443d-8b2f-e534ce4dd43d
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CDN- en WAF-configuratie in Adobe Experience Manager as a Cloud Service

Ontgrendel het volledige potentieel van Adobe Beheerde CDN met klantgerichte Regels CDN, de bescherming van WAF, en de Pijpleiding Config. Marius Petria, Sr. Computer Scientist bij Adobe, Quentin Vecchio, Software Development Engineer bij Adobe, en Florian Froese, Software Development Engineer bij Adobe, delen strategieën om de prestaties en beveiliging van Adobe Experience Manager as a Cloud Service applicaties te verbeteren.

>[!VIDEO](https://video.tv.adobe.com/v/3440608/?learn=on&enablevpops&captions=dut)

## Communautaire discussie

Ga verder het gesprek in de Gemeenschap van Adobe Developers Live [ bespreking ](https://adobe.ly/3O0TyYa).

## Belangrijkste punten

* **Inleiding van Nieuwe Mogelijkheden van de Configuratie** De presentatie introduceert nieuwe configuratiemogelijkheden voor CDN in een wolkendienst, die op de capaciteit zich richt om CDN voor diverse gebruiksgevallen te vormen.
* **CDN de Opties van de Configuratie** de nieuwe opties staan voor interactie met HTTP- verzoeken en reacties toe, zoals het toevoegen/verwijderen van kopballen, het herschrijven van verzoekwegen, het blokkeren van verkeer, het opnieuw richten van cliënten, en het proxying aan verschillende oorsprong.
* **de Verbeteringen van de Veiligheid** de nieuwe mogelijkheden omvatten de regels van de verkeersfilter om verkeer te blokkeren of te registreren dat op verzoekpatronen wordt gebaseerd, en de introductie van M WAF voor geavanceerde bescherming tegen Webaanvallen zoals SQL injectie en XSS.
* **Verklarende Configuratie** de configuratie wordt gedaan gebruikend dossiers YAML en door een configuratiepijpleiding in Cloud Manager opgesteld, makend het een snel en ongecompliceerd proces.
* **Transformaties van het Verzoek en van de Reactie** De nieuwe eigenschappen staan voor verzoektransformaties toe om URLs te normaliseren en onnodige vraagparameters te verwijderen, en reactietransformaties om kopballen te plaatsen alvorens reacties naar cliënten te verzenden.
* **Filters van het Verkeer en het Beperken van het Tarief** de filters van het Verkeer kunnen specifieke IPs of landen blokkeren en tarief uitvoeren beperkt om tegen aanvallen te beschermen DDoS. Het beperken van het tarief kan op diverse criteria zoals cliëntIP, gebruikersagent, en verzoekweg worden gevormd.
* **de Controle en Hulpmiddelen van de Analyse** Adobe verstrekt hulpmiddelen zoals Elasticsearch/Kibana en de dashboards van het Splunk om verkeer en gebruik te analyseren, die helpen potentiële veiligheidsbedreigingen identificeren en te verlichten.
* **Praktische Demo** de presentatie omvat een demo die toont hoe te om configuraties op te stellen CDN gebruikend Cloud Manager en hoe te om fouten te behandelen en configuraties plaatselijk te bevestigen gebruikend AEM.
