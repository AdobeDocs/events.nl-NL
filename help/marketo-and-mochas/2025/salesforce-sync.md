---
title: Marketo & Mochas - Salesforce Sync
description: U kunt de synchronisatie tussen Marketo en Salesforce besturen met de hulp van experts op het gebied van machtigingen, zichtbaarheid in het veld, samenwerking met beheerders en aanbevolen procedures voor een vloeiende, geoptimaliseerde integratie.
feature: Salesforce Integration
topic: Integrations
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3547
last-substantial-update: 2025-08-07T00:00:00Z
jira: KT-18706
source-git-commit: bc5752512fb1bc50cefe0180c308574e821888a2
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---


# Marketo &amp; Mochas: Salesforce Sync

Marketo kent maar weinig geïntegreerde oplossingen, maar Salesforce is de krachtigste van allen. Met ongeveer 90% van de Marketo-klanten die ook Salesforce gebruiken, heeft Adobe zich ertoe verbonden klanten te adviseren over het theorize, diagnosticeren en optimaliseren van de synchronisatie tussen beide. De Marketo-synchronisatie met SFDC is grotendeels gebaseerd op de machtigingen in SFDC die aan de Marketo Sync User zijn verleend. Dit kan voor klanten wegens veelvoudige beheerders of verschillende teams moeilijk zijn die silo&#39;s in communicatie rond updates in het systeem creëren.

Dit webinar gaat als volgt te werk omdat het betrekking heeft op de Marketo &lt;-> SFDC sync:

・ Uitleg van de vogels-oog-mening van hoe de synchronisatie werkt
・ Velden en objecten verbergen via Marketo Sync User in SFDC
・ Communiceren met de SFDC-beheerder
・ Efficiënt werken met Marketo Support
・ Te vermijden dingen bij het synchroniseren van Marketo naar SFDC

>[!VIDEO](https://video.tv.adobe.com/v/3470624/?learn=on&enablevpops)

## Aanbevolen procedures voor het gebruik van Salesforce Sync

Als u Salesforce Sync met Marketo effectief wilt gebruiken, volgt u deze best practices, die stap voor stap worden uitgelegd in eenvoudige termen:

1. **Begrijp het Proces van de Synchronisatie**

   De synchronisatie maakt verbinding met Marketo en Salesforce, waardoor gegevens tussen de twee systemen kunnen stromen. Beschouw de &quot;Marketo Sync User&quot; als een brug tussen de twee platforms. Deze gebruiker heeft machtigingen om bepaalde gegevens te lezen en te schrijven:

   * **schrijft Toegang** Leads en contacten (Marketo kan deze in Salesforce bijwerken).
   * **leest de Rekeningen van de Toegang**, kansen, douanevoorwerpen, en activiteiten (Marketo kan deze bekijken maar hen niet veranderen).

   Wanneer gegevens veranderen in Salesforce of Marketo, werkt de synchronisatie het andere systeem om de vijf minuten bij. Nochtans, kunt u urgente updates voorrang geven gebruikend stroomstappen zoals &quot;Synchroniseren aan SFDC.&quot;

1. **Schoon Velden** op

   Alleen velden synchroniseren die actief worden gebruikt. Bijvoorbeeld:

   * Als u oude velden hebt, zoals &quot;COVID-19-notities&quot; die niet meer relevant zijn, verwijdert u deze uit de synchronisatie. Hierdoor wordt het proces minder rommelig en sneller.
   * Gebruik geen formuleringsvelden (bijv. &#39;doorvoerleeftijd in dagen&#39;) omdat deze geen tijdstempels bijwerken, wat problemen kan veroorzaken.

1. **verhinderen Achterlogboeken**

   Er treedt een achterstand op wanneer te veel gegevens wachten op synchronisatie. Om dit te voorkomen:

   * Beperk onnodige updates: als een accountscore iets verandert (bijvoorbeeld van 60 naar 61), kan deze updates voor alle gerelateerde contactpersonen activeren. In plaats daarvan kunt u scores groeperen in bereiken (bijvoorbeeld 0-25, 26-50) om updates te reduceren.
   * Batchcampagnes: gebruik batchcampagnes in plaats van triggercampagnes om gegevens efficiënter te verwerken.

1. **beheert Fouten**

   Er kunnen fouten optreden wanneer Marketo een veld probeert bij te werken in Salesforce, maar geen machtigingen heeft. Om problemen op te lossen:

   * Meld u aan bij Salesforce als Marketo Sync-gebruiker en voer dezelfde handeling uit. Zo kunt u problemen met machtigingen of ongeldige gegevens opsporen.
   * Herhalingscampagnes opzetten in Marketo om veelvoorkomende fouten op te lossen, zoals het standaardiseren van land-/staatswaarden (bijvoorbeeld &quot;CA&quot; naar &quot;Californië&quot;).

1. **Filters van de Synchronisatie van het Gebruik de Douane**

   Met aangepaste filters kunt u bepalen welke records synchroniseren tussen Salesforce en Marketo. Maak bijvoorbeeld het veld &#39;Niet synchroniseren met Marketo&#39;. Als dit veld is gemarkeerd als &quot;true&quot; voor een record, wordt het niet gesynchroniseerd met Marketo. Dit is handig als u ongeldige e-mailadressen of verouderde contactpersonen wilt uitsluiten.

1. **Taakverwezenlijking van de Beperking**

   elm Salesforce. Focus op betekenisvolle activiteiten zoals &quot;ingevuld formulier&quot; of &quot;geklikte koppeling in e-mail&quot;.

1. **samenwerken met Uw Admin van Salesforce**

   Aangezien beide systemen bij de synchronisatie betrokken zijn, kunt u nauw samenwerken met uw Salesforce-beheerder om:

   * Rechten voor Marketo Sync User beheren.
   * Verwijder overbodige velden in Salesforce.
   * Synchronisatieproblemen tegelijk oplossen.

1. **Prestaties van de Synchronisatie van de Monitor**

   Controleer regelmatig de synchronisatiestatus in de beheersectie van Marketo:

   Zoek naar spikes in de &quot;Synchronisatie de Trend van de Achtergrond van de Synchronisatie&quot;dashboards of &quot;van de Output van de Synchronisatie&quot;. Deze wijzen op vertragingen of bovenmatige updates.
Als u problemen opmerkt, onderzoekt u welke velden of records het probleem veroorzaken.

1. **Wisely van de Douane van het Gebruik Voorwerpen**

   Aangepaste objecten zijn speciale gegevensstructuren waarin aanvullende informatie kan worden opgeslagen (bijvoorbeeld productdetails). Synchroniseer alleen de aangepaste objecten die nodig zijn voor uw campagnes, zodat de database niet opgeblazen wordt.

1. **Plan voor Scalability**

   Houd bij het instellen van de synchronisatie rekening met de lange termijn:

   * Handhaaf een gegevenswoordenboek om te volgen welke gebieden worden gesynchroniseerd en waarom.
   * Synchroniseer overbodige velden of records om het systeem efficiënt te houden.

Als u deze stappen uitvoert, kunt u zorgen voor een vloeiende en efficiënte integratie tussen Marketo en Salesforce, waarbij fouten worden geminimaliseerd en de waarde van uw gegevens wordt gemaximaliseerd.
