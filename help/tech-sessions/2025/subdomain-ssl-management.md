---
title: Technische sessies - Adobe Campaign-subdomein en SSL-beheer in het Configuratiescherm
description: Leer hoe u subdomeinen binnen het Configuratiescherm van Adobe Campaign kunt delegeren en configureren, SSL-certificaten kunt instellen en de configuratie kunt controleren om te zorgen voor een veilige e-maillevering.
solution: Campaign
feature: Subdomains and Certificates
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3409
last-substantial-update: 2025-09-05T00:00:00Z
jira: KT-18866
source-git-commit: 18ce421793d97372198151afc92b24f3bed053a8
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Technische sessies: Adobe Campaign-subdomein en SSL-beheer in het Configuratiescherm

In deze zitting, onderzoeken wij de concepten subdomain delegatie en configuratie binnen Adobe Campaign, met inbegrip van de installatie van SSL certificaten aan veilige subdomeinen.

Leer wat een subdomein is, zijn doelstellingen, en de delegatiemethodes die Adobe toelaten om het effectief te gebruiken. De sessie heeft ook betrekking op de principes van het beveiligen van een subdomein via SSL-certificaten en op de aanbevolen procedures voor het onderhouden van een veilige omgeving.

Wij verstrekken geleidelijke begeleiding bij het vormen van subdomeinen gebruikend het zelfbedieningspaneel van de Controle, die potentiële obstakels en hoe te om hen te richten benadrukt. Deelnemers krijgen praktische kennis om hun subdomeinen probleemloos in te stellen en te beveiligen.

Of u nu beheerder, ontwikkelaar of eigenaar van het platform bent, deze sessie stelt u in staat om subdomeinen in Adobe Campaign op betrouwbare wijze te configureren en te beveiligen.

>[!VIDEO](https://video.tv.adobe.com/v/3471391/?learn=on&enablevpops)

## Subdomeinbeheer uitvoeren in Adobe Campaign

Ontgrendel de essentiële elementen van subdomein delegatie, configuratie, en veiligheid voor de communicatie van Adobe Campaign e-mail:

* **Subdomain de Delegatie** verkies tussen volledige of delegatie van de NAAM om te controleren hoe Adobe uw DNS en e-mailleverbaarheid beheert.
* **DNS &amp; SSL Opstelling** De Juiste configuratie van MX, SPF, DKIM, DMARC, en SSL certificaten is essentieel voor veilige, betrouwbare e-mail die verzenden.
* **het zelfbedieningshulpmiddel van het Comité van de Controle** van het Gebruik Adobe om subdomain opstelling te stroomlijnen, verslagen te controleren, en SSL certificaten te beheren.
* **Gemeenschappelijke Punten** vermijd vertragingen en fouten door controlechronologie, verslagvereisten, en het oplossen van problemenstappen te begrijpen.

Het beheersen van deze processen zorgt ervoor dat uw campagnes veilig zijn, kunnen worden geleverd, en de reputatie van uw merk handhaven.

## Delegatiemethoden** Volledig vs. CNAME

* **Volledige Delegatie** Adobe beheert alle DNS verslagen voor subdomain, die optimale leverbaarheid en veiligheid verzekeren. Aanbevolen voor de meeste gebruikers.
* **Klant van de Delegatie van de NAAM van 0} en Adobe delen DNS verantwoordelijkheden.** De klant maakt CNAME-records die verwijzen naar door Adobe beheerde bronnen.
* **Belangrijke verschillen:
* **Volledige** Adobe heeft volledig gezag; minder klantenonderhoud.
* **CNAME** Gedeelde verantwoordelijkheid; meer handstappen voor klant.
* **Uiteinde** laat nooit uw worteldomein-slechts subdomain-afvaardigen om het verliezen van controle over uw belangrijkste domein te vermijden.
