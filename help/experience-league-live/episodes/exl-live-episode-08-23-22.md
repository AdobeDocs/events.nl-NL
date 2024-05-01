---
title: Vraag de experts - Nuttige extensies in tags (Launch) om extra kosten in rekening te brengen voor de Web SDK
description: Overweegt u het migreren van uw implementatie aan de nieuwe SDK van het Web van de Adobe?  Wij zullen door sommige van onze favoriete uitbreidingen in de bibliotheek van de Markeringen van de Adobe lopen die u zult helpen aangezien u uw gegevensinzameling aan het volgende niveau neemt.
solution: Data Collection, Experience Platform
feature: Tags
kt: 10528
event-start-time: 2022-08-23 09:00-7
event-guests: Rudi Shumpert,Jeff Chasin,Eric Matisoff
exl-id: 5ef987f4-37f5-473f-b9f2-1598b7e655ba
duration: 3833
source-git-commit: 0b2f63198af8767f24783dbafd244c9398c24f33
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Vraag het de deskundigen: Nuttige uitbreidingen in Markeringen (Lancering) helpen superladen de SDK van het Web

Overweegt u het migreren van uw implementatie aan de nieuwe SDK van het Web van de Adobe?  Wij zullen door sommige van onze favoriete uitbreidingen in de bibliotheek van de Markeringen van de Adobe lopen die u zult helpen aangezien u uw gegevensinzameling aan het volgende niveau neemt.

>[!VIDEO](https://video.tv.adobe.com/v/346610/?quality=12&learn=on)

## Vragen en opmerkingen van de show

### Data Element Assistant-extensie van Evolytics

<br> 
**Vraag:** Vanuit het oogpunt van gegevensveiligheid, is Evolytics veilig om te gebruiken, aangezien dit derdeuitbreiding is?

**Antwoord:** Ja. U kunt de extensiecode desgewenst controleren, maar slaat ook geen van de datum op. Er wordt alleen een transformatie uitgevoerd.

<br> 

**Vraag:** Wordt hiermee ook Adobe ECID vastgelegd?

**Antwoord:** De Adobe-ECID wordt niet vastgelegd binnen die extensie. Deze extensie is bedoeld voor het maken van aanvullende, anonieme id&#39;s (onder andere).

**Antwoord:** De Adobe-ECID kan echter op andere manieren worden vastgelegd. We delen dat via de exL-notities en -Twitter, omdat we hier geen links in de chat kunnen delen.

<br>:

**Vraag:** De hash-functionaliteit biedt verschillende hashingtechnieken, zoals SHA-256, en biedt openbare en persoonlijke sleutels?

**Antwoord:** Ja! SHA-256 is de standaardwaarde

<br>:

### Algemene vragen en opmerkingen:

<br>:

**Vraag:** Waar klikken we om de bronbestanden voor extensies te downloaden? Is dat in het menu met drie punten?

**Antwoord:** Ja! De drie punten en vervolgens de bron downloaden (vanuit de catalogusweergave)

<br>:

**Opmerking:** Een van de dingen die ik echt met extensies beschouw, is het tijdbesparende aspect ervan. Veel van hen doen dingen die je doet *kon* doe met sommige douanecode maar met een uitbreiding u te hoeven niet om die code te schrijven.

**Antwoord:** Rechts. Het is herhaalbaar zonder dat het wiel telkens opnieuw moet worden gemaakt.

<br>:

**Vraag:** Hoe zullen de analytische stop-ins met de implementaties van SDK van het Web worden gesteund of worden vervangen?

**Antwoord:** Veel analytische plug-ins zijn tegenwoordig eigenlijk overbodig dankzij de extra flexibiliteit van Workspace en Adobe Tags. Nochtans, die niet zijn, actief voor gebruik door het Web SDK gemigreerd.

<br>:

**Vraag:** Om het even welke ontwikkeling op het volgen van de kaart van de Activiteit gebruikend Web SDK?

**Antwoord:** Ik ben blij om te melden dat de Activity Map actief aan voor steun in Web SDK wordt gewerkt

<br>:

**Vraag:** Zouden wij toegang tot het netwerk van Adobe Edge kunnen hebben om gebeurtenissen te beheren alvorens hen over te brengen naar de eindbestemmingen? Ik begrijp dat we het ook in Launch kunnen doen, maar zou het in de toekomst ook op de server kunnen?

**Antwoord:** Ja! Dit is mogelijk via onze functie voor het doorsturen van gebeurtenissen, die klanten kunnen aanschaffen via al onze Real-Time CDP-producten (Real-Time CDP Connections, Prime of Ultimate).

**Antwoord:** RTCDP-verbindingen (Event Forwarding) biedt de mogelijkheid om meer controle te hebben voordat u het naar niet-adobe doelen verzendt.

**Antwoord:** Bekijk onze andere ExL Live-video&#39;s om er nog meer over te leren (zoals [deze](exl-live-episode-06-23-22.md)).

<br>:

**Opmerking:** Snelle vraag uit voor één van mijn favoriete uitbreidingen: Er is een uitbreiding van de toewijzingstabel waar u een lijst voor een gegevenselement kunt lezen dat &quot;als deze waarde dan dit is plaats het zoals dat.&quot;

**Antwoord:** De flexibiliteit die zij bieden is zeer indrukwekkend. Bedrijven kunnen desgewenst ook hun eigen particuliere extensies maken.

<br>:

**Vraag:** Je liet de individuele gegevens van CRM zien zoals stad en weer, dus waar slaan we de individuele respons op?

**Antwoord:** Reacties worden opgeslagen in elke unieke gebeurtenis die een regel binnen een eigenschap van het doorsturen van gebeurtenissen activeert, en worden alleen in die specifieke gebeurtenis gebruikt.

<br>:

De discussie over dit onderwerp voortzetten in het [Communautaire discussie over Experience League](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform/experience-league-live-post-session-discussion-useful-extensions/m-p/542620#M240).
<br> 

## Extra LIVE-sessies van Experience League uit deze gegevensverzamelingsreeks

* [Vraag het de experts - De grondbeginselen van Web SDK](exl-live-episode-05-26-22.md)
* [Vraag het de experts - RTCDP-verbindingen](exl-live-episode-06-23-22.md)
* [Vraag het de experts - Gegevensstromen en gegevens prep](exl-live-episode-07-21-22.md)

