---
title: Aanbevolen procedures voor migreren van Adobe Analytics naar Adobe Customer Journey Analytics
description: Leer de essentiële stappen en de beste praktijken voor het migreren van Adobe Analytics aan Customer Journey Analytics (CJA), met inbegrip van het schemaontwerp XDM, gegevenstoewijzing, en de opstelling van de gegevensmening.
solution: Analytics, Customer Journey Analytics
topic: Migration
role: Developer
level: Beginner, Intermediate
doc-type: Event
duration: 3654
last-substantial-update: 2025-07-16T00:00:00Z
jira: KT-18535
source-git-commit: 90eb4a9d2cf445c58fde776092fb047f820fa207
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# Aanbevolen procedures voor migreren van Adobe Analytics naar Adobe Customer Journey Analytics

Meer informatie over de migratie van Adobe Analytics naar Customer Journey Analytics (CJA). De sessie wordt georganiseerd door Nicolina Picone en Maurizio Corò van het team van Adobe Ultimate Success en biedt een diepgaand overzicht van CJA, zijn mogelijkheden en beste praktijken voor migratie.

## Belangrijke besproken onderwerpen

* verschillen tussen Analytics en CJA
* het belang van sterke identiteits herkenningstekens, het richten van gegevensstructuren, en het creëren van klantgerichte gegevensmeningen
* omvat strategieën voor het importeren van historische gegevens, het beheren van de toewijzing van marketingkanalen en het benutten van de flexibiliteit van CJA voor op maat gemaakte rapporten

>[!VIDEO](https://video.tv.adobe.com/v/3464911/?learn=on&enablevpops)

## Key Takeways

* **Customer Journey Analytics (CJA) het Overzicht** CJA is een evolutie van Adobe Analytics, die op de volledige klantenreis over veelvoudige touchpoints (b.v., mobiel, Web, CRM, vraagcentra) eerder dan single-track gebeurtenissen concentreert. Het staat voor gegevensverwerking in real time en manipulatie toe.

* **Belangrijke stappen van de Bereidheid van de Migratie** voor het migreren van Adobe Analytics aan CJA omvatten het verzekeren van een sterk identiteitsidentificatiecode (b.v., persoon identiteitskaart), het richten van variabelen en dimensies, en het in kaart brengen van gegevens aan het XDM schema. Historische gegevens kunnen worden geïmporteerd met validatiestappen.

* {de Weergaven van 0} Gegevens en Flexibiliteit **CJA laat de verwezenlijking van klantgerichte gegevensmeningen met aanpasbare zittingsduur, segmenteringsfilters, en attributie montages toe.** Deze flexibiliteit maakt een op maat gesneden rapportage en analyse mogelijk.

* **Beste praktijken voor Historische Gegevens Migratie** bevestigen de gegevens van CJA door het met de gegevens van Adobe Analytics binnen een aanvaardbare waaier (b.v., verschil 10%) te vergelijken. Begin met een kort backfill venster (bijvoorbeeld een maand) en vergroot de schaal geleidelijk.

* **CJA van de Attributie van het Kanaal van de marketing** biedt verbeterde mogelijkheden voor marketing kanaalattributie, die beperkingen zoals de &quot;eerste pagina van bezoek&quot;functie elimineren en meer dynamische zittingsconfiguraties toelaten.
