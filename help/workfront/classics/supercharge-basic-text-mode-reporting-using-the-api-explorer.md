---
title: Vraag het de Expert - de Rapportering van de Wijze van de Tekst van de Opstuwing Basis gebruikend de Ontdekkingsreiziger API
description: Leer meer over de API-verkenner, hoe u deze gebruikt en hoe u uw rapporten kunt verbeteren met behulp van de standaardtekstmodus. Dit webinar werd geregistreerd op 22 januari 2020.
doc-type: feature video
team: Technical Marketing
kt: 9918
exl-id: f859c4eb-8b3c-4d91-9765-9957dc4678f5
duration: 4068
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '1656'
ht-degree: 0%

---

# Vraag het de Expert - de Rapportering van de Wijze van de Tekst van de Opstuwing Basis gebruikend de Ontdekkingsreiziger API

Leer over [[!UICONTROL API Explorer] &#x200B;](https://developer.adobe.com/workfront/api-explorer/), hoe te om het te gebruiken, en hoe te om uw rapporten te verbeteren leveraging basistekstwijze. Dit webinar werd geregistreerd op 22 januari 2020.

>[!VIDEO](https://video.tv.adobe.com/v/341124/?quality=12)

## Aanvullende bronnen

![&#x200B; een grafiek die voorbeelden van de regels van de tekstwijze toont &#x200B;](assets/text-mode-chart.png)


**Definitieve &quot;Alle Rollen van de Baan&quot;kolom**

```
description="Primary =" indicates the user's primary job role
displayname=All Job Roles
listdelimiter=<p>
listmethod=nested(userRoles).lists
textmode=true
type=iterate
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("Primary = ",{role}.{name}),{role}.{name})
valueformat=HTML
```

**Wijze van de Tekst voor &quot;Alle Teams&quot;kolom**

```
displayname=All Teams
listdelimiter=<p>
listmethod=nested(teams).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

**Wijze van de Tekst voor &quot;Alle Groepen&quot;kolom**

```
displayname=All Groups
listdelimiter=<p>
listmethod=nested(userGroups).lists
textmode=true
type=iterate
valuefield=group:name
valueformat=HTML
```

**Wijze van de Tekst voor &quot;Directe Rapporten&quot;kolom**

```
displayname=Direct Reports
listdelimiter=<p>
listmethod=nested(directReports).lists
textmode=true
type=iterate
valueexpression={name}
valueformat=HTML
```

## Vragen en antwoorden

**Vraag**

Is het mogelijk om om het even welke inzameling in een rapport te gebruiken, gebruikend tekstwijze?

**Antwoord**

Ja, u kunt elk gewenst object in het gebied met verzamelingen gebruiken. Je zult willen verkennen en zien waartoe je toegang hebt. Niet alles heeft toegang tot zowel het gebruikersobject als het taakrolobject, zoals we hebben gezien met het object Gebruikersrollen in de API-verkenner.

**Vraag**

Kunt u &quot;voorwaardelijk gebruik van verschillende inzamelingen in de zelfde kolom (projectupdates vs taakupdates)&quot;bespreken

**Antwoord**

Wanneer u in het herhalingsgebied bent en u het waardegebied of de waardeuitdrukking daar ziet, heeft dat toegang tot één van de punten in uw inzamelingslijst. Met behulp van het waardeveld krijgen we bijvoorbeeld de naam van die taakrol of iets anders dat zich in dat item in de lijst bevindt. Als u in een taak bent, kan een taakvoorwerp het project van verwijzingen voorzien dat het binnen is.

**Vraag**

Kunt u bespreken of de &quot;taak de inzameling van updates slechts mogelijk in een taakrapport is?&quot;

**Antwoord**

Wanneer u een uitgiftenrapport maakt, kunt u taakinformatie zien als de kwestie tegen de taak is gemeld en u die informatie ook vanuit de verzameling kunt zien. Behalve die situaties zou u in een taakrapport moeten zijn om de gegevens van de taakinzameling te zien.

**Vraag**

Kunt u de formaatvoorbeelden van de Tekst ([!DNL CSS]) delen?

**Antwoord**

Workfront ondersteunt [!DNL CSS] niet in de tekstmodus.

**Vraag**

Wat is de beste en/of snelste manier om een aangepaste veldnaam te zoeken - voor rapportage in de tekstmodus? Ik heb de bewerkingsoptie HTML in browser OF gebruikt door een gebied in een rapport toe te voegen en op tekstwijze over te schakelen om het te pakken MAAR.. nieuwsgierig hoe anderen dit uitvoeren.

**Antwoord**

Ik vind het snelst om het gebied in UI dan schakelaar aan de Wijze van de Tekst te selecteren en de gebiedsnaam te kopiëren. Dit zorgt ervoor dat ik de correcte spelling voor het gebied krijg.

**Vraag**

Hoe kan ik tekstwijze gebruiken om leden van een team in een rapport te identificeren? Wij gebruiken momenteel teamtaken in de werkschema&#39;s van de taakgoedkeuring en zouden van de teamleden in het huidige goedkeuringsstadium in een kolom gelijkend op willen een lijst maken hoe de Approvers en het gebied van de Status werken.

**Antwoord**

Als u wilt verwijzen naar de teamleden die zijn gekoppeld aan de huidige goedkeuringsfase, moet u verwijzen naar een verzameling waarnaar wordt verwezen, wat momenteel niet mogelijk is via de mogelijkheden van de Workfront-tekstmodus. De kolom die uw organisatie momenteel gebruikt die het Team verbonden aan de goedkeuring toont is uw beste optie.

**Vraag**

Moet het veld en de naam van het object in het juiste geval staan (bijv. rol vs. rol)?

**Antwoord**

Wanneer u in de tekstmodus naar objecten verwijst, wilt u deze precies zo schrijven als de rechterkolom van de API Explorer. Bijvoorbeeld, als u een naam van het Project van een rapport van de Taak wilt van verwijzingen voorzien, zou uw waardegebied als het volgende kijken:

```
valuefield=project:name
```

Nochtans, in het geval van Kwesties, worden die genoemd opTasks in de Ontdekkingsreiziger van API. Als u dus een rapport van het Uur in werking zou stellen en een kolom voor de naam van de Uitgave wilt toevoegen, zou het waardegebied
ziet er als volgt uit:

```
valuefield=opTask:name
```

**Vraag**

Ik wil een rapport maken waarin voor elk project de huidige actieve taak(en) wordt (worden) weergegeven. Hoe kan ik dat het beste doen? Ik denk dat het een taakrapport zou zijn dat ook kolommen met projectinfo heeft toegevoegd?

**Antwoord**

Dat klopt. Een taakverslag is hiervoor het beste. U zou &quot;Actieve Taken&quot;moeten bepalen. Als u predecessors gebruikt dan zou dit taken zijn die Klaar zijn. Zo kunt u door Klaar filteren = Waar. Dit zou om het even welke taken brengen die klaar zijn om te beginnen. Dan zou ik willen adviseren dat u door de Naam van het Project groepeert, deze manier uw taken allen worden gegroepeerd en u kunt in een blik zien welke taken tot welk Project behoren.

**Vraag**

Bestaat er een manier om rapporten op te stellen die gegevens berekenen - bijvoorbeeld het percentage projecten dat aan bepaalde criteria voldoet?

**Antwoord**

De beste manier om een rapport te creëren om gegevens (% bijvoorbeeld) te presenteren of te berekenen zou zijn groeperingen op uw rapport toe te passen en dan een grafiek toe te passen. Als u een cirkeldiagram aan uw rapport moest toevoegen, hebt u de optie voor de schijfsegmenten om in waarden of percentages te zijn.

**Vraag**

Kunt u tekstwijze gebruiken om de leden van een team te identificeren die aan het huidige stadium van de taakgoedkeuring gelijkend op Approvers en de kolom van de Status worden toegewezen?

**Antwoord**

U zou een inzamelingskolom op tekstwijze aan uw rapport van de Taak met het volgende moeten toevoegen:

```
displayname=Current Approval Stage Approvers 
listdelimiter=<p> 
listmethod=nested(currentApprovalStep.stepApprovers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

**Vraag**

Kunt u filteren waar alle groepen een bepaalde groep bevatten?

**Antwoord**

Als u de punten in uw rapport wilt filtreren, zou u het onder het filterlusje van uw rapport doen. Dus als u alleen gebruikers wilde zien waar een van hun groepen Boekhouding was, voegt u een filterregel toe die als volgt luidt:

```
Other Groups>ID>Equal>Accounting
```

**Vraag**

Is er een manier om een rapport tot stand te brengen dat de daadwerkelijke duur van een combinatie taken bepaalt?

**Antwoord**

U zou uw rapport moeten filtreren om slechts de combinatie taken te omvatten u wilt. Dan zou u een Ware kolom van de Duur in uw mening moeten zetten en het samenvatten door Som in de Montages van de Kolom, en tot slot zou u uw rapport op één of andere manier moeten groeperen. Wanneer u het rapport in werking stelt zal de groeperingsbar het totaal van de daadwerkelijke duur tonen in de rijen die worden gegroepeerd.

**Vraag**

Is er een manier om taken af te trekken die onder een ouder vallen om de duur voor de rest taken onder een ouder te bepalen?

**Antwoord**

De duur van een oudertaak wordt berekend door de begindatum van de vroegste beginnende taak van de einddatum van de recentste beëindigende taak onder die ouder af te trekken. In een rapport weet u slechts over elke individuele taak die in overweging wordt genomen of om te tonen of niet. De rapportmotor heeft geen manier om aan informatie van één taak te hangen en het te gebruiken wanneer het bekijken van een andere taak. Zo de enige manier om te verwezenlijken wat u vraagt is een taak te verwijderen uit het zijn onder een bepaalde ouder terwijl in de lijst van de projecttaak en waar te nemen hoe de duur van de oudertaak herberekent.

**Vraag**

Voor voorwaardelijke groeperingen, is een douaneformulier (denk &quot;Westerse Staten&quot;, &quot;Centrale Staten&quot;, &quot;Oostelijke Staten&quot;) om de individuele groepen te decoderen een gemeenschappelijke techniek die goed aan die nota werkt, wanneer u het gebruiken van berekende groeperingen versus berekende parameters adviseert?

**Antwoord**

Berekende groepen (ook wel een expressie met een waarde in een groep genoemd) zijn handig om een resultaat weer te geven op de groeperingsbalk. Dit kan ook worden gedaan gebruikend een berekend douanegebied. Voor elke aanpak zijn de voor- en nadelen:

* Waardeexpressies worden telkens berekend wanneer de browserpagina wordt vernieuwd. Dit kan beter zijn dan berekende aangepaste velden die opnieuw worden berekend wanneer het object waaraan ze zijn gekoppeld, wordt bewerkt of wanneer de berekende velden in een bulkbewerking opnieuw worden berekend, of wanneer het aangepaste formulier wordt bewerkt en de optie Vorige berekeningen bijwerken is geselecteerd.
* Waardeexpressies kunnen echter niet worden gebruikt in grafieken, voorwaardelijke opmaak of filter. U moet hiervoor berekende aangepaste velden gebruiken.

**Vraag**

Is er geen manier om de groeperende vertoningsnaam van &quot;Geen Waarde&quot;in om het even wat te veranderen wij verkiezen om het voor rapporteringsdoeleinden te roepen? Met andere woorden, het zal ALTIJD &quot;Geen Waarde&quot; zijn?

**Antwoord**

Er is een manier om &quot;Geen Waarde&quot; te vervangen door iets anders. Stel dat u een projectrapport hebt gegroepeerd op Portfolio Name. Alle projecten die niet aan een portfolio zijn toegewezen, worden gegroepeerd met de titel:

```
Portfolio: Name: No Value
```

Als u dit wilt wijzigen, bewerkt u de groepering in de tekstmodus en vervangt u deze regel:

```
group.0.valuefield=portfolio:name
```

met deze regel:

```
group.0.valueexpression=IF(ISBLANK({portfolio}.{name}),"Not in any Portfolio",{portfolio}.{name})
```

De groep heeft nu de volgende titel:

```
Portfolio: Name: Not in any Portfolio
```

**Vraag**

Is er een parameter om onvolledige toewijzingen te volgen, d.w.z.:

1. Taken met één toewijzing waaraan geen persoon is toegewezen of
1. Taken met veelvoudige taken die minstens één unassigned individueel voor de gevraagde rollen hebben

**Antwoord**

Dit zou kunnen worden verwezenlijkt door een Rapport van de Toewijzing en het filtreren voor te gebruiken

```
Assigned To ID > Is Blank and Role ID > Is Not Blank
```

Dit zal zich in alle taken of kwesties trekken die aan een rol, maar niet noodzakelijk een specifieke gebruiker zijn toegewezen. U zult de kolommen voor de naam van de Taak en van de Uitgave moeten toevoegen om te zien tot welk voorwerp de taak behoort, en als gegroepeerd door de naam van het Project het zou moeten helpen om het georganiseerd te houden.

**Vraag**

Chuck, ik vergeet het, maar herinner je je de eigenschap in de tekstmodus die dan zal renderen als knopinfo, bij aanwijzen?

**Antwoord**

description= staat u toe om tooltip te tonen wanneer het hangen over de kolomkopbal.

**Vraag**

Kan ik rapporteren over een veld voor selectievakjes waarin meerdere selecties zijn toegestaan, maar alleen de eerste selectie in het rapport opnemen?

**Antwoord**

Ja. De geselecteerde keuzen in het veld Selectievakje bevinden zich in één tekenreeks, waarbij elke selectie door een komma wordt gescheiden. U gebruikt de expressie SEARCH om de positie van de eerste komma in het veld Selectievakje te bepalen en gebruikt vervolgens die index met de expressie LEFT om zoveel tekens vanaf het begin van de lijst weer te geven. Hier is de code:

```
valueexpression=IF(SEARCH(",",{DE:Checkbox Field},0)>0,LEFT({DE:Checkbox Field},SEARCH(",",{DE:Checkbox Field},0)),{DE:Checkbox Field})
```

Als u een komma in een selectienaam in het selectievakje gebruikt, wordt alleen het gedeelte van die selectie weergegeven tot aan de eerste komma.
