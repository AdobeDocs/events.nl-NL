---
title: Vraag het de Expert - Meting van snelheid
description: Leer om snelheid te meten en te volgen gebruikend  [!DNL Workfront]  rapporterend. Deze workshop werd op 14 augustus 2019 vastgelegd.
doc-type: feature video
team: Technical Marketing
jira: KT-9912
last-substantial-update: 2023-08-15T00:00:00Z
exl-id: 83053de2-e386-4243-a9c8-a2ad9d51790f
duration: 4630
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '3962'
ht-degree: 0%

---

# Vraag het de Expert - Meting van snelheid

Leer de snelheid te meten en bij te houden met behulp van [!DNL Workfront] reporting. Deze workshop werd op 14 augustus 2019 vastgelegd.

>[!VIDEO](https://video.tv.adobe.com/v/341057/?quality=12)

## Aangepaste velden die worden gebruikt in de presentatie

Bespaar tijd door de berekeningen hieronder te kopiëren en te plakken.

>[!NOTE]
>
>De syntaxis voor aangepaste veldberekeningen is gewijzigd sinds de presentatie in 2019 is gegeven, maar de concepten en andere instructies in de presentatie zijn nog steeds correct.
>&#x200B;>**De berekeningen hieronder zijn bijgewerkt om op de recentste syntaxisregels te wijzen.**

**eerste Vastlegt Datum**

Indeling: Datum

Berekening:

```
IF(ISBLANK({DE:First Commit Date}),{defaultBaseline}.{plannedCompletionDate},{DE:First Commit Date})
```

**Eerste Duur**

Indeling: Tekst

Berekening:

```
IF(ISBLANK({DE:First Duration}),{defaultBaseline}.{durationMinutes},{DE:First Duration})
```

**werk-om verhouding** vast te leggen

Format :Number

Berekening:

```
ROUND(DIV({actualDurationMinutes},{DE:First Duration}),1)
```

**werk-aan-verbind de Status van de Verhouding**

Format :Text

Berekening:

```
IF({DE:Work-to-Commit Ratio}>2,"Terrible",IF({DE:Work-to-Commit Ratio}>1.6,"Poor",IF({DE:Work-to-Commit Ratio}>1.2,"Not Bad","Excellent")))
```

**Aangepaste Snelheid**

Format :Number

Berekening:

```
ROUND(DIV({actualDurationMinutes},{durationMinutes}),1)
```

**Aangepaste Status van de Snelheid**

Format :Text

Berekening:

```
IF({DE:Adjusted Velocity}>2,"Terrible",IF({DE:Adjusted Velocity}>1.6,"Poor",IF({DE:Adjusted Velocity}>1.2,"Not Bad","Excellent")))
```

## Vragen en antwoorden

**Vraag**

Hallo, bedankt voor het organiseren van dit webinar. Ik heb een vraag over Veld in Workfront. In ons systeem, creeerden wij een douanegebied genoemd &quot;Staat&quot;die een combinatie van Status en Voorwaarde is. In dit veld staat een heleboel beelden in duizenden projecten, die zeer belangrijk zijn voor ons gegevensextract van Tableau. Maar nu willen we dit veld verwijderen en in plaats daarvan het veld Voorwaarde gebruiken, het native veld. Hebt u enig idee hoe ik dit veld kan omdraaien zonder gegevens te verliezen? Alles wat ik kan doen zonder gegevens te verliezen, is het handmatig schakelen van project naar project.

**Antwoord**

In een dergelijke situatie kunt u filteren en bulkbewerking gebruiken om de reeks van het vullen van het veld Voorwaarde op basis van uw aangepaste veld Staat semi-automatisch te maken.

Dit zijn de stappen die u moet uitvoeren:

1. Bepaal welke statuswaarden u wilt toewijzen aan Condition-waarden. Stel dat u een statuswaarde hebt van &quot;Late&quot; en &quot;Erg laat&quot; die beide zijn toegewezen aan een Condition-waarde van &quot;In Trouble&quot;
1. Maak een projectrapport met alle projecten met een staatswaarde van &quot;Late&quot; en &quot;Erg laat&quot;
1. Voer het rapport uit. Zorg ervoor u alle projecten toont (zie opties bij lagere recht van het rapport)
1. Klik op checkbox in de hogere linkerzijde van het rapport in de bar met kolomrubrieken. Hiermee worden alle projecten in het rapport geselecteerd
1. Klik op de knop Bewerken boven de rapportlijst
1. Voorwaardetype instellen op Handmatig
1. Stel het veld Voorwaarde in op Problemen
1. Klik op Wijzigingen opslaan


**Vraag**

Hoe wordt Uitstekend, Niet Slecht, enz. gedefinieerd?

**Antwoord**

Dit was slechts een voorbeeld, maar zo heb ik het opgezet. Eerst berekende ik twee indexen:

Aangepaste snelheid

De formule voor dit is Ware Duur/Geplande Duur (die op het gebied van de Duur in een project wordt opgeslagen). Aangezien de Geplande Duur van het project kan veranderen telkens als het project wordt hergepland, vertegenwoordigt de Geplande Duur het definitieve herplan.

Werkelijke verhouding

Deze formule is als Aangepaste Snelheid behalve dat in plaats van het gebruiken van de Geplande waarde van de Duur van het definitieve plan willen wij de Geplande Duur gebruiken die eerst aan de klant werd beloofd. Wij veronderstellen dat de Originele basislijn deze informatie bevat (en wij zijn van nu af aan van plan om onze projectmanagers te vragen om hun projecten op deze manier te plannen zodat wij nauwkeurige gegevens kunnen vangen). We hebben deze waarde voor de duur vastgelegd vanaf de oorspronkelijke basislijn en de waarde First Duration genoemd.

Door de Ware Duur door of Geplande Duur of Eerste Duur te delen, komen wij met een aantal terecht dat ons kan vertellen hoe dicht wij aan op doel kwamen. Als de Geplande Duur of Eerste Duur aan de Ware Duur gelijk zijn zal de index 1 gelijk hebben. Als de werkelijke duur groter is, is het antwoord meer dan 1. Hoe groter het aantal dat we hebben gedaan toen we onze datum ontmoetten.

Dus, gezien alles wat ik besloot om statussen toe te wijzen voor zowel de Aangepaste Snelheid als de Werk-aan-Commit verhouding als volgt:

* 1.1 of lager noemde ik Uitstekend.
* 1.2 tot 1.5 Ik noemde &quot;Niet slecht&quot;.
* 1,6 tot 1,9 heette ik Poor.
* 2 of hoger noemde ik Terrible.

**Vraag**

Wat moet de werknemer doen om de tijd te volgen die nodig is om de projecten uit te voeren?

**Antwoord**

We volgen de werkelijke uren van het werken aan de projecten hier niet. We volgen de duur gewoon en vergelijken deze. Maar als je uren volgt, en werkelijke uren over geplande uren wilt gebruiken om snelheid te berekenen, zou je hetzelfde type rapport kunnen doen door geplande uren te vergelijken met werkelijke uren. U wilt ook geplande uren vastleggen vanaf de oorspronkelijke basislijn.

**Vraag**

Kunt u filters verstrekken die voor Snelheid worden gebruikt?

**Antwoord**

Ik gebruikte twee filterregels voor de rapporten van de Snelheid:

* Categorieën > Id > Gelijk > WPI-projectgegevens (dit is het aangepaste formulier met alle berekende velden). Ik wil alleen projecten zien die dit aangepaste formulier gebruiken)
* Project > Status > > Gelijk > Voltooid (ik wil alleen voltooide projecten zien omdat ze een werkelijke waarde voor Duur hebben die aangeeft hoe lang het duurde om alles af te ronden. De huidige projecten zouden geen nauwkeurige Ware Duur voor het berekenen van snelheid verstrekken)

Ik heb ook andere filters toegevoegd om mijn rapport klein genoeg te houden om voor webinar te beheren, maar in uw productieomgeving zou u waarschijnlijk alle projecten met de WPI douanevorm in een bepaalde tijdspanne willen zien. U zou op de Werkelijke Datum van de Voltooiing van het project voor dat kunnen willen filtreren.

**Vraag**

Als u een project kopieert, draagt het de zelfde basislijnen aan het nieuwe project?

**Antwoord**

Neen, de basislijnen zijn niet inbegrepen in het gekopieerde project

**Vraag**

Voor een proces van de taakgoedkeuring, kunt u me tonen hoe te om een rapport tot stand te brengen dat een controletrail door taak in een project met een tijd/datumstempel voor elke fiatteur verstrekt?

**Antwoord**

Maak een taakrapport. Klik op het tabblad Kolommen (Weergave) op Kolom toevoegen. In het vak &quot;Tonen in deze kolom:&quot; typt u &quot;fiatten&quot;. Hier ziet u de verschillende goedkeuringsvelden waarover u kunt rapporteren. Ik zou u willen voorstellen eerst een kolom voor alles (behalve om het even welke IDs) toe te voegen, dan kunt u zien welke informatie wordt getoond.

Ga nu naar het tabblad Filters en voeg een filterregel toe voor:

Taak >> Is Goedkeuring > Gelijk > Waar. Hiermee worden alleen taken weergegeven waaraan een goedkeuring is gekoppeld.

Voeg zo nodig extra filters toe.

**Vraag**

Ik wil graag een proefverslag opstellen. Een lijst van projecten die aantonen hoeveel proefdrukken zij hebben en hoeveel versies van dat bewijs bestaan.

**Antwoord**

Maak een documentrapport.

In de standaardweergave wordt het versienummer weergegeven. U wilt dat daar laten, maar u kunt andere kolommen wijzigen.

Groepeer het rapport door de Naam van het Project.

Filter het rapport door Huidige Versie :Proof identiteitskaart is niet leeg.

Hiermee geeft u een lijst met alle proefdrukken in elk project. Er wordt een rij weergegeven voor elke proefdruk en het versienummer (dit is hetzelfde als het totale aantal versies).

**Vraag**

Kunt u snelheid gebruiken op taakniveau? In plaats van projectniveau?

**Antwoord**

Ja, maar u moet het aangepaste formulier voor het project kopiëren en er een aangepaste taakvorm van maken. Dan zult u de berekening in het Eerste gebied van de Datum moeten uitgeven Vastleggen en zult de verwijzing in &quot;StandaardBasislijn&quot;in &quot;StandaardTaak van de Basislijn&quot;veranderen. Doe hetzelfde voor Eerste duur. Vervolgens kunt u het aangepaste taakformulier toevoegen aan alle taken die u wilt meten. U zult taakrapporten in plaats van projectrapporten voor deze moeten creëren. Nochtans zult u nog moeten ervoor zorgen dat de Originele projectbasislijn als standaardbasislijn wordt geplaatst. Alle taakgegevens worden gehouden in de zelfde basislijn met de projectgegevens.

**Vraag**

Moet de eerste datum voor vastleggen handmatig worden ingesteld door de eigenaar van het project? Of kan het zich terugtrekken uit bestaande velden?

**Antwoord**

De eerste Vastlegdatum wordt vastgelegd vanaf de standaardbasislijn. Zolang de standaardbasislijn de originele basislijn is zal dit de geplande voltooiingsdatum van het project tonen op het tijdstip dat het eerst aan Huidige status werd geplaatst.

**Vraag**

De berekende gebieden in douaneformulieren moeten nog periodiek correct worden verfrist? Of gebeurt dat nu automatisch van de ene op de andere dag (of bij een andere trigger)?

**Antwoord**

Berekende velden worden opnieuw berekend:

* Wanneer een gebruiker het object bewerkt
* Bij bulkbewerking met geactiveerde aangepaste expressies opnieuw berekenen
* Wijzigingen in het formulier met de optie Vorige berekeningen bijwerken

**Vraag**

Als de snelheid Duur overweegt, zou de Percentage Voltooid in de Voorkeur van het Project op Duur moeten worden gebaseerd?

**Antwoord**

Nr, verwijst de optie van de Voorkeur van het Project slechts naar hoe Percentage wordt berekend Voltooid. Deze instelling heeft geen invloed op de waarde voor de duur zelf.

**Vraag**

Wat is het verschil tussen de eerste en de planningsduur?

**Antwoord**

De eerste Duur is het aantal dagen u oorspronkelijk de klant beloofde het project zou nemen. Wij krijgen dit aantal van de originele basislijn die werd geregistreerd toen het project van Planning in Huidige werd veranderd.

De geplande Duur is het aantal dagen vanaf de aanvang van uw project tot de Geplande Datum van Voltooiing. In eerste instantie zijn deze twee termijnen gelijk, maar als het project ooit opnieuw gepland was en de geplande uitvoeringsdatum gewijzigd was, is de geplande duur ook veranderd.

De waarde van de rapporten van de Snelheid komt uit ons die kunnen zien hoeveel de Geplande Duur van de Eerste Duur is veranderd. We kunnen dit zien net zo lang als toen we voor het eerst basislijnen opnamen als projecten van Planning naar Current veranderden.

**Vraag**

Kunnen de arbeiders door kleur worden geplaatst zodat zijn zij het zelfde over alle rapporten?

**Antwoord**

Als u in een taakrapport de groep Toegewezen aan >> Naam groepeert, kunt u een kleur aan bepaalde arbeiders op het lusje van de Grafiek toewijzen. Kies op het tabblad Diagram de optie Aangepaste kleuren naast het vak Naam toewijzen aan > Naam en voeg een kleur toe voor elke worker.

**Vraag**

Ik probeer te bepalen of het mogelijk is om een dashboard met één gebied tot stand te brengen dat een vorm van het taakniveau kijkt om te zien of is het aanwezig en secundair als bepaalde gebieden niet leeg zijn. Is dit mogelijk?

**Antwoord**

Laten we eens kijken of ik je vraag begrijp. Stel dat ik een aangepaste taakvorm heb met de naam Tammy Form met daarin een veld met de naam Tammy Field.

U wilt een taakrapport waarin alle taken worden weergegeven waaraan Tammy Form is gekoppeld en waarin Tammy Field een bepaalde waarde heeft.

Ja, dat kunt u doen. U zou enkel een filter in uw taakrapport met twee filterregels nodig hebben:

Categorieën > ID Gelijk Formulier

Taak > Tammy-veld is niet leeg

**Vraag**

Is er een manier om een rapport te creëren om naar een specifiek genoemd document in de Bibliotheek van het Document te zoeken? Een deel van het dashboard willen wij meten als bepaalde documenten bestaan.

**Antwoord**

Ja. U moet een documentrapport maken. Het lijkt alsof u een specifieke documentnaam zou kunnen willen verstrekken telkens als u het rapport in werking stelt. Als dat het geval is zou ik adviseren om Opties van het Rapport te gaan en de Prompts van het Rapport te selecteren. Voeg een herinnering voor Document > Naam toe.

**Vraag**

Kunt u een kleur/hexadecimale waarde kiezen die niet in het grafieklusje wordt vermeld maar die een nieuwe kleur is die nieuwe hexadecimale waarde bijvoorbeeld een nieuwe kleur van mijn merkkleuren is om me toe te staan om de rapporten aan te passen?

**Antwoord**

Ja, je kunt alle RGB-code invoeren die je mogelijk hebt gevonden. Dit is een standaardcode die aangeeft hoeveel rood, groen en blauw de kleur bevat. Workfront accepteert een hexadecimale waarde van 000000 tot FFFFFF. Als u dus de code van uw merkkleur kent, kunt u deze gebruiken.

**Vraag**

Kunt u de definitie van de rapporten in het dashboard nogmaals toelichten (geef een overzicht van de maatregelen die elk rapport neemt)?

**Antwoord**

Grafiek Aangepaste snelheidsstatus

> Dit toont aan hoe goed wij bij de voltooiing van projecten op tijd toen het vergelijken van de Ware Duur van het project met de Geplande Duur deden. De geplande duur is aangepast omdat het project tijdens de levenscyclus opnieuw werd gepland.

Statusdiagram verhouding vastleggen

> Dit toont aan hoe goed wij bij de voltooiing van projecten op tijd toen het vergelijken van de Ware Duur van het project met de Eerste Duur deden. De eerste Duur die de originele tijd is die wij de klant beloofden dat het project zou vergen om te voltooien. De eerste Duur werd berekend van de waarde van de Duur van het project toen het eerst van Planning in Huidige status werd veranderd. Dit was de Duur die in de Oorspronkelijke basislijn wordt geregistreerd.

Snelheidsstatuslijstrapport

> Dit verslag bevat alle berekende aangepaste velden en de belangrijke data voor dezelfde projecten in de grafieken. Het doel is om onze berekeningen te kunnen controleren en desgewenst meer informatie te krijgen.

**Vraag**

Hoe hebt u de nieuwe gegevens toegevoegd aan de x-as?

**Antwoord**

Wanneer u door om het even wat in een rapport groepeert zal het u toestaan om een grafiek tot stand te brengen. Vervolgens kunt u de X- of Y-as instellen op het tabblad Diagram.

**Vraag**

Kunt u het verschil tussen de eerste duur en de werkelijke duur overschrijden?

**Antwoord**

De eerste Duur is het aantal dagen u oorspronkelijk de klant beloofde het project zou nemen. Wij krijgen dit aantal van de originele basislijn die werd geregistreerd toen het project van Planning in Huidige werd veranderd.

De werkelijke duur is het aantal dagen vanaf het begin van het project tot de datum waarop het project daadwerkelijk is voltooid.

**Vraag**

Hoe is de basisfactor van het project in dit rapport?

**Antwoord**

De originele basislijn van het project bevat de Geplande Datum van Voltooiing en de Geplande Duur die bestonden toen het project eerst in de status van Huidig werd veranderd. Als uw proces het project moest plannen alvorens het aan Huidig te plaatsen dan zou dit de datum vertegenwoordigen u toegezegde om het project tegen te voltooien.

**Vraag**

Is er een manier om het nieuwe formulier massaal toe te passen op oude projecten?

**Antwoord**

Ja, kunt u veelvoudige projecten van een lijst selecteren. Als u dit doet, wordt de optie Bewerken linksboven in de lijst weergegeven. Als u op Bewerken klikt wanneer er meerdere objecten zijn geselecteerd, plaatst u de zogenaamde &#39;bulkbewerking&#39;. Op deze manier kunt u een aangepast formulier toevoegen aan meerdere projecten.

Een kortere weg voor het toevoegen van douaneformulieren aan een groot aantal projecten moet een rapport tot stand brengen dat u filtert om slechts die projecten te omvatten u wilt. In plaats van projecten afzonderlijk te selecteren, klikt u op het selectievakje boven het eerste selectievakje in de lijst en selecteert u de volledige lijst.

**Vraag**

Is het mogelijk om dubbele ingangen uit binnen de groepering op een taakrapport te verwijderen, maar niet over groepen?

**Antwoord**

De beste manier om over groeperingen in lijstrapporten te denken is dit:

Eerst bepaalt u met het tabblad Filter welke items worden weergegeven in de lijst. Er zijn geen dubbele vermeldingen. Het filter wordt toegepast op elk object. Als het door het filter loopt, wordt het één keer in de lijst weergegeven als het helemaal niet wordt weergegeven.

De volgende groepering wordt toegepast op de gefilterde lijst. Een groepering identificeert één ding over de voorwerpen in de lijst, zoals de naam van de portefeuille het in is (u kunt niet op een lijst van dingen groeperen, slechts op één enkel ding). Vervolgens worden alle objecten met dezelfde waarde in die groep weergegeven, zoals alle projecten in hetzelfde portfolio. Alle projecten waarvoor geen portfolio is geselecteerd, worden in de groep met de naam &quot;Geen waarde&quot; weergegeven.

Het resultaat is dat objecten niet in meerdere groepen kunnen worden weergegeven. En of een object in de lijst wordt weergegeven, wordt volledig door het filter gecontroleerd (en of de persoon die het rapport uitvoert rechten heeft om het te bekijken).

**Vraag**

Zou u om het even welk ander rapport willen adviseren om Snelheid te volgen? Een aanbeveling op hoog niveau is geweldig omdat ik weet dat er niet genoeg tijd is om de details te bespreken.

**Antwoord**

Net als bij elk verslag is het eerste wat u moet doen, het bepalen wat u wilt weten. De volgende stap is toegang tot die informatie, die in sommige gevallen u betekent moet beginnen het te volgen.

Een van de redenen waarom ik besloot om Actual Duration te vergelijken met twee soorten Geplande Duur was omdat ik vond dat het interessante inzichten over snelheid bood. De gegevens waren ook al beschikbaar, dus ik hoefde ze niet te volgen. Met een paar berekeningen kon ik de gegevens extraheren in een formulier waarover ik kon rapporteren.

Maar u zou net zo goed kunnen beslissen om andere informatie over taken of projecten te volgen om over te rapporteren.

Workfront heeft geen ingebouwde snelheidsrapporten, zodat zou ik u en uw teambrainstorm op wat u wilt weten om snelheid te bepalen en dan te zien wat u moet volgen adviseren.

**Vraag**

Kunt u iets berekenen op KOLOM-niveau? In plaats van een berekend VELD vanuit een aangepast formulier aan te roepen?

**Antwoord**

Voor deze berekeningen zou een expressie value in tekstmodus kunnen worden gebruikt. We hadden Eerste Duur of Eerste Vastlegdatum echter niet kunnen doen, we moesten die vastleggen op een plaats waar ze niet zouden veranderen.

Wat betreft het werk-aan-Commit de Status van de Verhouding en de Aangepaste Status van de Snelheid, moesten deze douanegebieden zijn zodat wij hen in het lusje van de Grafiek konden gebruiken. Het tabblad Diagram herkent tekstmodusgroepen niet, maar moet aangepaste velden zijn. En omdat we werkgebonden ratio en aangepaste snelheid nodig hadden om die statussen te berekenen, moesten ze ook aangepaste velden zijn. In dit geval moesten ze allemaal aangepaste velden zijn, maar het is altijd goed om beide manieren te overwegen en te kiezen wat het beste werkt. Bedankt voor de vraag.

**Vraag**

Onze projecten veranderen vaak als gevolg van vertragingen of veranderingen door de klant. Ons verslag zou allemaal &quot;verschrikkelijk&quot; kunnen zijn. Wat is een aanbeveling voor het volgen van redenen voor verandering? Wij dachten om een douaneformulier op documentniveau toe te voegen dat reden voor verandering (of interne of cliëntverandering) meldt, maar zich afvraagt wat beste praktijken zijn.

**Antwoord**

De beste praktijken moeten een dropdown gebruiken om dit te volgen. Plaats zoveel &quot;redenen&quot; als u daar kunt bedenken om mee te beginnen en voeg vervolgens een &quot;andere&quot; optie toe om een reden vast te leggen die niet op de lijst staat. Als die nieuwe reden kijkt of gemeenschappelijk wordt voeg het aan uw dropdown toe. U kunt gemakkelijk over dingen in een drop-down lijst rapporteren, en u kunt op dit gebied groeperen (u kunt niet op checkboxes of een multi-select drop-down groeperen).

Nog een opmerking hierover. U kunt niet alle projecten in uw rapporten van de Snelheid willen omvatten. Als je insecten corrigeert of &quot;gaat waar niemand eerder heen is gegaan&quot; dan maak je waarschijnlijk niet dezelfde betrokkenheid bij een einddatum als wanneer je een huis bouwt dat je al vele malen eerder hebt gebouwd.

Zorg er dus voor dat u zich op de snelheid van uw rapportage richt op plaatsen waar dit u kan helpen uw doelen te bereiken.

**Vraag**

Als ik de standaardbasislijn op een project aan &quot;Origineel&quot;plaats en dan het project uit huidig neem en het in huidig terugzet, zal het mijn standaardbasislijn veranderen?

**Antwoord**

Ja. Elke keer dat u de status wijzigt in Huidig, krijgt u een nieuwe basislijn en wordt dit de nieuwe standaardbasislijn. Maar alle vorige basislijnen zullen nog bestaan en u kunt de originele basislijn manueel plaatsen om de standaardbasislijn opnieuw te zijn.

**Vraag**

Is er een manier om in een rapport op te nemen welke gebieden bewerkbaar zijn? Kan ik beperkingen instellen voor bepaalde velden?

**Antwoord**

U kunt de weergave- en bewerkingsrechten voor velden in een aangepast formulier beperken. U moet de velden in een sectie opnemen en in de sectie-instellingen kunt u de rechten kiezen die gebruikers nodig hebben om velden in de sectie te kunnen weergeven of bewerken.

**Vraag**

Kunt u een rapport maken waarin wordt gezocht naar een specifiek benoemd document in de documentbibliotheek?

**Antwoord**

Ja. U moet een documentrapport maken. Het lijkt alsof u een specifieke documentnaam zou kunnen willen verstrekken telkens als u het rapport in werking stelt. Als dat het geval is zou ik adviseren om Opties van het Rapport te gaan en de Prompts van het Rapport te selecteren. Voeg een herinnering voor Document > Naam toe.

**Vraag**

Waarom zijn in rapporten waarden beschikbaar als kolom maar niet als selectie of groepering? Bijvoorbeeld: Issue Source.

**Antwoord**

De belangrijkste reden dat een kolom misschien wel kan worden weergegeven, maar niet kan worden gegroepeerd, is dat deze een lijst kan bevatten, zoals aangepaste velden of taaktoewijzingen voor selectievakjes. Groeperen in een lijst is niet toegestaan.

**Vraag**

Hoe kan ik in een rapport (op welke gebieden) scheiden wanneer de ingang van haar en wanneer de uren daadwerkelijk werden uitgevoerd?

**Antwoord**

Het veld Datum van item voor het object Uur verwijst naar de datum waarop de uren zijn gewerkt. Hierdoor verschilt Invoerdatum van andere objecten, waarbij dit de datum is waarop het object is gemaakt. Hoewel er geen aanmaakdatum voor uren is, is er een &quot;Laatst bijgewerkte datum&quot;, die eerst de aanmaakdatum is en vervolgens een datum waarop het uur is bewerkt.

**Vraag**

Vanuit een rapporteringsstandpunt hoe kunnen wij tot de gegevens van de Basislijn toegang hebben? Ik heb een project met meerdere basislijnen. Ik wil zien hoe individuele taken in elke basislijn werden gepland. Is er een manier om een rapport te schrijven dat het projectplan voor elke basislijn zal tonen?

**Antwoord**

Een rapport zal u tonen welke gebieden u voor de basislijn wilt zien die momenteel als gebrek wordt geplaatst, zodat kon u de basislijn veranderen en uw rapport verfrissen om gebieden met de nieuwe basislijn te zien.

Maar als u grafisch informatie over uw taken wilt zien kunt u dat doen gebruikend de de grafiekeigenschap van Gantt. Schakel Gantt in in een takenlijst (met het pictogram Gantt in de rechterbovenhoek naast Automatisch opslaan) en ga vervolgens naar het pictogram Instellingen net onder en rechts en klik erop. Schakel het vakje Basislijn in en geeft alle basislijnen weer. U kunt deze één voor één selecteren en de veranderingen in uw taken in de mening van Gantt zien.

**Vraag**

Hoe te om een rapport tot stand te brengen om de veranderingen in zijn status voor een bepaalde periode, bijvoorbeeld vorige maand te vinden.

**Antwoord**

Met de functie Analytics in Workfront kunt u historische gegevens, waaronder statuswijzigingen, bekijken.

Maar u kunt de informatie van de statusverandering ook krijgen gebruikend een rapport van de Nota. U kunt filteren om statusveranderingen op projecten te zien als u het gebied van de Status van het Project volgt.

Zo eerst, ga naar Opstelling>Interface>de Doelen van de Update en zorg ervoor de Status van het Project één van de Ingebouwde Gebieden is die wordt gevolgd. Als het niet is moet u het toevoegen.

Maak nu een notitierapport en voer de volgende handelingen uit:

Op het tabblad Kolommen (Weergave):

* Vervang de kolom &quot;Notititietekst&quot; in &quot;Tekst controleren&quot;. Hiermee wordt informatie weergegeven over de gewijzigde status van en naar
* Laat de kolommen &quot;Project: Name&quot; en &quot;Entry Date&quot; staan
* Klik op de kolom Datum van item en schakel Sorteren op deze kolom in het deelvenster Kolominstellingen in. Als u wilt dat de meest recente statuswijzigingen bovenaan worden weergegeven, wordt de sortering aflopend.

Op het tabblad Groepen:

* Groep voor project: Naam

Maak op het tabblad Filters de volgende filterregels:

* Opmerking > Audittype > Gelijk > Status wijzigen
* Voeg extra regels toe om door de Datum van de Ingang van de Nota te filtreren. U kunt dit liever buiten Filters laten en een rapportprompt gebruiken
* Filter naar wens op project, portfolio of andere gegevens.

**Vraag**

Als Planner kunt u rapporten voor andere gebruikers trekken?

**Antwoord**

Een Planner kan rapporten maken en deze delen met alle gebruikers, zelfs met personen die geen gebruikers zijn. Wanneer het bekijken van het rapport, ga naar de Acties van het Rapport>delend, dan klik op het tandwielpictogram in de hogere recht van het vakje van de Toegang van het Rapport. Kies &quot;Maak dit openbaar aan externe gebruikers.&quot; -optie. U kunt de geleverde koppeling kopiëren en naar iedereen verzenden. Ze zullen het rapport in real time in hun browser zien.
