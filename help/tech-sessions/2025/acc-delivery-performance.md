---
title: Adobe Campaign Classic-leveringsprestaties - Problemen oplossen
description: Deze sessie betrof belangrijke strategieën om de prestaties van e-mail en SMS-berichten met Adobe Campaign te verbeteren. Het behandelde gemeenschappelijke uitdagingen zoals leveringsvertragingen, lage productie, en transactiesolerantie, het aanbieden van oplossingen zoals batchoptimalisering, SQL registreren, en de controle van serverprestaties. De beste praktijken van de leveringsbaarheid omvatten juiste e-mailauthentificatie (SPF, DKIM, DMARC), zwarte lijst controle, en spamcontroles. Voor betere prestaties adviseerden de deskundigen schone werkschema's, het vertragen regels, en het vermijden van gedeelde containers. Tips voor het leveren van SMS-berichten zijn gericht op de juiste installatie van externe accounts en de analyse van logbestanden. De sessie benadrukte ook het bijhouden van validatie, databaseonderhoud met behulp van blotrapporten en het toepassen van druk- en vermoeidheidsregels om de betrokkenheid te vergroten. Een opname van een sessie wordt via e-mail gedeeld en op de website van Adobe Experience geplaatst.
solution: Campaign Classic v7
product: Adobe Campaign
feature: SMS, Deliverability, Troubleshooting
role: User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 2257
last-substantial-update: 2025-04-25T00:00:00Z
jira: KT-17869
exl-id: a7e1e198-b63b-4a2a-9ffc-7f72bf4c61c1
source-git-commit: 3b54c46988da18248024d115997704d9881f5e68
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# Technische sessies: Adobe Campaign Classic-prestaties voor levering - Problemen oplossen

In deze sessie zullen we veelvoorkomende problemen verkennen waarmee we worden geconfronteerd wanneer we optimale prestaties leveren met Adobe Campaign Classic (ACC) en activeerbare strategieën bieden voor het oplossen van problemen en het oplossen van problemen. De deelnemers zullen leren hoe te om prestatiesknelpunten te identificeren, leveringsvoorbereiding/configuratieinconsistenties te behandelen en beste praktijken uit te voeren om vlotte communicatie te verzekeren. Van het optimaliseren van leveringen tot het oplossen van technische problemen, zal dit webinar aanwezigen van de kennis en de hulpmiddelen voorzien die nodig zijn om de efficiency van hun ACC campagnes te verbeteren, betere resultaten te drijven, en kwalitatief hoogwaardige klantenervaringen te leveren.

>[!VIDEO](https://video.tv.adobe.com/v/3457826/?learn=on&enablevpops)

## Toetsen

**Uitdagingen en Oplossingen van de Levering**

* Veelvoorkomende problemen zijn vertragingen bij de levering, mislukte voorbereiding, vastgelopen leveringen, lage succespercentages, lage doorvoer, lage betrokkenheid en trage levering van transacties.
* De oplossingen omvatten het optimaliseren van levering het in batches plaatsen, het controleren van serverprestaties, het toelaten van SQL vraagregistreren, het herzien van controlelogboeken, en het verzekeren van juiste configuratie van eigenschappen MTA en IP.

**Beste praktijken van de Levering**

* Ervoor zorgen dat e-mailverificatie correct is (SPF, DKIM, DMARC).
* De status van een zwarte lijst controleren en spam-triggerende inhoud vermijden.
* Gebruik spamcontroles om spamscores te beoordelen voordat u e-mails verzendt.

**optimaliserend de Prestaties van de Levering**

* Gebruik zuiver het richten werkschema&#39;s en beperk verpersoonlijkingsgebieden.
* Voer throttling regels, partijverwerking, en topologieregels voor uitsluitingen en het filtreren uit.
* Vermijd het delen van containers over meerdere kanalen om knelpunten te voorkomen.

**de Leveringskwesties van SMS van het Oplossen van problemen**

* Zorg ervoor dat externe accounts op unieke wijze zijn geconfigureerd en dat SMS-processen worden uitgevoerd.
* Controleer SMS-logboeken op fouten en verifieer reguliere expressies in SMP-instellingen.
* Neem contact op met de serviceprovider voor problemen met verkeerde configuratie.

**de Traagheid van de Transactionele Levering**

* Interne en totale verwerkingstijden bewaken.
* Zorg ervoor dat de grootte van de levering binnen de limieten ligt (60 GB voor batch, 30 GB voor gebeurtenis).
* Controleer de typologische regels en personalisatie-instellingen.

**het Volgen en Betrokkenheid**

* Workflows voor bijhouden en serverlogbestanden valideren.
* Test aangepaste volgformules in lagere omgevingen voordat u gaat produceren.
* Zorg ervoor dat de trackingservers actief zijn.

**Onderhoud van het Gegevensbestand**

* Gebruik opbladerrapporten om tabellen met een hoge opbloei te identificeren en een DB-vacuüm te rechtvaardigen.

**Algemene Aanbevelingen**

* Gebruik druk- en vermoeidheidsregels om onnodige e-mails te beperken.
* Segmenteer grote leveringen in kleinere batches om de prestaties te optimaliseren.
