---
title: Vraag het de Expert - het Begrijpen van mix en capaciteit
description: Leer om mix en capaciteit binnen uw onderneming te meten. Dit webinar werd geregistreerd op 2 oktober 2019.
doc-type: feature video
team: Technical Marketing
kt: 9913
exl-id: 49cce53f-457b-4973-a0d9-1b5ce2272884
duration: 4239
source-git-commit: 91f20c3e9ee5ae5b259d5cb3da476974acdc6585
workflow-type: tm+mt
source-wordcount: '2229'
ht-degree: 0%

---

# Vraag het de Expert - het Begrijpen van mix en capaciteit

Leer om mix en capaciteit binnen uw onderneming te meten. Dit webinar werd geregistreerd op 2 oktober 2019.

>[!VIDEO](https://video.tv.adobe.com/v/341119/?quality=12)

## Vragen en antwoorden

**Vraag**

Hoe plaatst u %s op een kolomdiagram?

**Antwoord**

De %-waarden die in het Mix-rapport worden vermeld, staan daar omdat op het tabblad Diagram de optie &#39;Kolommen groeperen&#39; en de optie Gestapeld op 100% is gekozen. Als we &#39;Gestapeld&#39; zouden kiezen, zou dat de geplande uurtotalen weergeven en niet het percentage.

**Vraag**

Als uw afdeling/organisatiewerklast een mengeling van projecten/taken, en kwesties/verzoeken is, hoe adviseert u het krijgen van een overzicht op hoog niveau (in een rapport van Workfront) van WPI.

**Antwoord**

Projecten, taken en kwesties moeten elk hun eigen verslagen met hun eigen douaneformulieren hebben. Ze kunnen echter elk hetzelfde veld Werktype gebruiken. U kunt de drie rapporten in één dashboard willen tonen.

**Vraag**

Moeten we de bewerkingstaken bulksgewijs uitvoeren om ze operationeel of strategisch te maken?

**Antwoord**

De techniek die we voorstellen is een rapport te maken waarmee u een lijst met taken krijgt die operationeel zijn. Zodra u hebt dat u alle taken kunt selecteren in één keer, geeft bulkbewerking hen, dan voegt het douaneformulier met het Type van Werk toe en plaatst het het werktype aan Operationeel voor alle taken in één keer. U volgt dezelfde procedure om een lijst met strategische taken te verzamelen, deze bulksgewijs te bewerken en het aangepaste formulier toe te voegen, enzovoort.

Een paar ideeën worden vermeld in Webinar voor douaneherinneringen die u zouden kunnen helpen een lijst krijgen, zoals het controleren op bepaalde woorden in de taaknaam, de projecteigenaar, de portefeuille, of toegewezen gebruikers. Dit zijn gewoon ideeën. U moet een verslag opstellen dat het beste werkt in uw situatie.

**Vraag**

Als ik vier categorieën in mijn mix heb, kan ik dan een doel voor elk creëren en dan over delta tussen voorspelling versus plan vs werkelijk rapporteren? (4 categorieën Campagne, BedrijfsEenheid, Web, en Product). We hebben de categorieën op projectniveau in aangepaste vorm/velden. Het doel zou zijn om een driemaandelijkse prognose (begroting/prognose) op te stellen, waarna de geplande uren naar die en uiteindelijk naar de werkelijkheid worden bijgehouden.

**Antwoord**

Als u alle categorieën op één douaneveld hebt (laten wij het Type van Werk voor nu roepen), enkel een projectrapport groeperen zich op Geplande Uren eerst en het Type van het Werk tweede. Filter uw projectrapport om projecten in Planning binnen gewenste datumwaaiers te tonen. Gebruik een grafiek met gegroepeerde kolommen of staven die op 100% zijn gestapeld als u percentages wilt zien. Dit zou uw Voorspeld rapport kunnen zijn.

U kon het rapport kopiëren en het uitgeven om een rapport tot stand te brengen dat op Huidige projecten wordt gebaseerd, nog het tonen van de mengeling die op Geplande Uren wordt gebaseerd.

U kunt het rapport opnieuw kopiëren, het veranderen in groep door Werkelijke Uren in plaats van Geplande Uren tonen slechts voltooide projecten binnen gewenste datumwaaier. Dit zou de procentuele mix laten zien op basis van de werkelijke uren.

**Vraag**

Werkt dit als u meerdere categorie-id&#39;s hebt voor een project of taak?

**Antwoord**

Ja, als u meerdere id&#39;s hebt, moeten deze als volgt worden gescheiden door een tab:

```
EXISTS:1:$$EXISTSMOD=NOTEXISTS
EXISTS:1:$$OBJCODE=OBJCAT
EXISTS:1:categoryID=5d76d82600e7926bb51eeb1e0886810e 5d54288d01034619f2eb2c74f6472f18
EXISTS:1:objID=FIELD:ID
```

De beste manier om ze te scheiden met een tab-teken is om eerst uw lijst met categorieën in de builder te maken. Als u meerdere aangepaste formuliernamen plaatst en overschakelt naar de tekstmodus, worden deze weergegeven als id&#39;s gescheiden door tabs.

De veelvoudige IDs wordt behandeld als OFs, zodat als om het even welk van hen aan de taak in bijlage is zal het niet op het rapport verschijnen.

**Vraag**

Wordt in het verslag &quot;ANDed&quot; of &quot;ORed&quot; genoemd?

**Antwoord**

De individuele douaneherinneringen zijn &quot;ANDed&quot;. Zo als u Pam als projecteigenaar en Rekening zoals die aan de taak wordt toegewezen zult u slechts taken zien die aan Rekening worden toegewezen die in projecten zijn waar Pam de projecteigenaar is.

**Vraag**

Waarom kunt u alleen op bepaalde kolommen sorteren? U kunt dus niet sorteren op toewijzingen.

**Antwoord**

&quot;Toewijzingen&quot; is een lijst en u kunt niet sorteren of groeperen in een lijst met items. U kunt alleen op een afzonderlijk item sorteren of groeperen.

U kunt dit illustreren door een lijst met taken als deze in één taak op te nemen:

```
Jane
Bill
Dan
```

En een lijst van taken als dit op een andere taak:

```
Bill
Jane
Helen
```

Welke taak zou eerst in een soort moeten verschijnen? U kunt &#39;&#39;sorteren op de voornaam in de lijst&#39;&#39; zeggen, maar dit is niet noodzakelijk nuttig, omdat u de volgorde niet kunt bepalen. Workfront voorkomt het probleem door het helemaal niet toe te staan om op lijsten te sorteren.

En groeperen op lijst? Als we door een lijst namen konden groeperen, dan zouden alle taken die aan Jane, Bill, Dan waren toegewezen, samen zijn gegroepeerd en alle taken die aan Jane, Dan, Bill (zelfde lijst, maar in een verschillende orde) werden toegewezen in een verschillende groepering. Workfront voorkomt het probleem door groeperen op lijsten niet toe te staan.

**Vraag**

Worden de geplande uren gebruikt voor strategische taken en de werkelijke werktijden?

**Antwoord**

Nee. In ons voorbeeld gebruiken wij Geplande Uren om het niveau van inspanning te tonen die voor zowel strategische als operationele taken wordt gepland. Op die manier kunnen we ze gemakkelijk met elkaar vergelijken, of het nu of in de toekomst was. U kunt de werkelijke uren ook gebruiken om strategische en operationele taken te vergelijken, maar alleen voor taken in het verleden, aangezien de uren die mensen hebben gerapporteerd als de tijd die ze daadwerkelijk aan de taken hebben besteed.

**Vraag**

Hoe verantwoorden we in de bronnenplanner taken die in het verleden waren gepland, maar nog niet zijn voltooid? De geplande uren lijken niet vooruit te lopen en tonen daarom in de komende weken geen taken/uren die middelen nodig hebben.

**Antwoord**

Er is geen &quot;automatisch&quot; vooruitschuiven van onvoltooid werk. U moet uw project opnieuw plannen wanneer dit gebeurt. Misschien zijn de middelen die u oorspronkelijk aan een bepaalde taak had toegewezen niet beschikbaar in het nieuwe tijdkader, zodat moet de projectmanager dit bekijken en de beste manier beslissen om te herplannen. Dit zou kunnen betekenen dat belanghebbenden worden betrokken en dat goedkeuring wordt verkregen voor de wijzigingen in het plan.

**Vraag**

Zou u het aanraden om de VTE aan te passen in plaats van 2 uur per dag voor het controleren van e-mail, onderbrekingen?

**Antwoord**

Ja, als u FTE aan .75 plaatst die een gebruiker zoals beschikbaar 6 uren per dag in de Planner van het Middel zal tonen. Dit zal hun beschikbaarheid elke dag zijn. Als u hen voor verschillende periodes afhankelijk van de datum wilt tonen niet beschikbaar, zoals niet de laatste dag van elk kwartaal, dan is een overheadproject de manier om dit te doen.

Sommige mensen geven de voorkeur aan overheadprojecten omdat ze ze voor zichzelf kunnen bouwen en ze desgewenst kunnen wijzigen, terwijl ze misschien geen rechten hebben om hun eigen VTE te bewerken.

**Vraag**

Zijn de gegevens voor het dashboard van de teamcapaciteit beschikbaar aan iedereen u het rapport met ongeacht deelt welke toestemmingen zij op het werk hebben?

**Antwoord**

Als een gebruiker geen toestemming heeft om het voorwerp te bekijken, zal het niet binnen het rapport/dashboard zichtbaar zijn. Als u echter wilt dat iedereen dezelfde resultaten ziet, gaat u naar Rapporthandelingen > Bewerken > Rapportinstellingen en voert u in het veld &quot;Dit rapport uitvoeren met de toegangsrechten van&quot; uw naam in. Hierdoor kunnen de gebruikers die op dit rapport worden gedeeld, de exacte resultaten zien die u ziet. Het zal hen geen extra toegang tot het resultaat zelf verlenen, zodat kunnen sommige resultaten of niet klikbaar zijn.

**Vraag**

Hoe kunnen wij een rapport creëren dat al personeel toont dat aan een project algemeen (niet op taakniveau) wordt toegewezen?

**Antwoord**

U kunt een kolom binnen een Rapport van het Project tot stand brengen die alle gebruikers toont die als deel van het het Staven lusje (het Team van het Project) worden vermeld. U wilt de volgende tekstmodus gebruiken:

```
displayname=Project Team
listdelimiter=<p>
listmethod=nested(projectUsers).lists
textmode=true
type=iterate
valuefield=user:name
valueformat=HTML
```

**Vraag**

Ik zou graag een rapport/dashboard hebben waarin wordt opgenomen hoe mijn team werkt. In het bijzonder de volgende scenario&#39;s: - Projecten die ik bezit / Voor mij gemaakte projecten / Taken die ik toewees aan anderen / Taken die aan mij zijn toegewezen

**Antwoord**

Projecten die ik heb

Er is een ingebouwd rapport met de naam &quot;Huidige projecten&quot;, waarin alle huidige projecten worden weergegeven. U kunt dit project uitgeven en een filterregel :Project toevoegen > identiteitskaart van de Eigenaar > Gelijk > $$USER.IDThen sparen en het rapport anders noemen aan &quot;Projecten I Bezit&quot;.

Voor mij gemaakte projecten

Er is een ingebouwd rapport met de naam &quot;Mijn projecten&quot; waarin alle huidige projecten worden weergegeven waar u zich in het projectteam bevindt (u bent dus de eigenaar, sponsor of toegewezen aan een taak). Niet zeker of dit is wat u vraagt maar er zijn geen andere manieren om te weten of creeerde iemand een project voor u buiten het maken van u de eigenaar van het project, sponsor of het toewijzen van u aan een taak.

Taken die ik aan anderen heb toegewezen

Maak een taakrapport met de gewenste filters en ga vervolgens naar het tabblad Filter en klik op Overschakelen naar tekstmodus. Voeg deze code toe aan wat er al is:

```
EXISTS:1:$$OBJCODE=ASSGN
EXISTS:1:taskID=FIELD:ID
EXISTS:1:assignedByID=$$USER.ID
```

Dit zal u alle taken tonen waar de het programma geopende gebruiker minstens één van de huidige toegewezen. Als de toegewezen personen door meerdere personen zijn toegewezen, wordt alleen de naam van de eerste persoon die iemand heeft toegewezen, weergegeven als &quot;Gevraagd door&quot; op de bestemmingspagina. Als u alle toegewezen mensen wilt zien en wie elk toegewezen u een kolom aan uw mening kunt toevoegen, overschakelen op tekstwijze, en wat daar met dit is vervangen:

```
displayname=All Assignees and Requesters
listdelimiter=<p>
listmethod=nested(assignments).lists
textmode=true
type=iterate
valueexpression=CONCAT("Assigned To: ",{assignedTo}.{name},"; Requested By: ",{assignedBy}.{name})
valueformat=HTML
```

Taken die aan mij zijn toegewezen

Er is een Ingebouwd rapport genoemd &quot;Mijn Taken&quot;die u alle onvolledige taken op Huidige projecten zullen tonen waar u de taakeigenaar bent. Ik zou u willen voorstellen de filter verandert om u alle taken te tonen waar u één van de potentieel vele toegewezen gebruikers, niet alleen de taakeigenaar bent. U doet dit door de filterregel te verwijderen

```
Task > Assigned To ID > Equal > $$USER.ID 
```

en vervangen door

```
Assignment Users > ID > Equal > $$USER.ID
```

**Vraag**

Is er een manier om etiketten op grafieken aan te passen? Ik heb ontdekt dat wanneer ik een grafiek creeer om projectstatussen te weerspiegelen - de naam van de huisgroep uiteindelijk in het etiket wordt opgenomen.

**Antwoord**

De etiketten op grafieken gebruiken de gebiedsnaam van wat u op groepeert. U kunt de labels dus alleen wijzigen door een berekend aangepast veld met de gewenste naam te gebruiken. Plaats in de sectie Berekening van het veld de veldnaam van het native veld waarop u wilt groeperen.

**Vraag**

Hoe kleurt u de rapportbalken op Chuck&#39;s Team Assignements alstublieft? Dus amber voor achter, rood voor laat en groen voor op tijd? Kan de volgorde ook worden gewijzigd in logischer, bijvoorbeeld rood/oranje/groen of omgekeerd?

**Antwoord**

Als u de kleuren wilt wijzigen die in het rapport worden gebruikt voor de opties voor de status van de voortgang, bewerkt u het rapport en klikt u op het tabblad Diagram. Ga naar de vervolgkeuzelijst Aangepaste kleuren >. Het wordt naast het vak &#39;Linkeras (Y)&#39; of &#39;Gegevens groeperen op&#39; weergegeven, afhankelijk van het feit of u kolommen of staven wilt groeperen. In die vervolgkeuzelijst kunt u kleuren selecteren. Als u klikt op de nummers rechtsonder in de kleuropties, kunt u de kleur selecteren in een groter palet.

Jammer genoeg kunt u niet de orde van deze veranderen.

**Vraag**

Kunt u een grafiek tot stand brengen waar het aan de Aantal projecten richt dat een arbeider een taak binnen wordt toegewezen?

**Antwoord**

Ja, dit is hoe:

* Een projectrapport maken
* Als de gebruiker in kwestie de het programma geopende gebruiker is, zou de filter deze lijn moeten omvatten:

```
   Project Users > ID > Equal >$$USER.ID 
```

* Als dat niet het geval is, plaatst u de gebruikersnaam in plaats van [!DNL $$USER.ID] . Hierin worden alle projecten weergegeven waarin deze persoon een taak krijgt toegewezen of de eigenaar of sponsor is. Als u slechts projecten wilt zien waar zij taken worden toegewezen zou u deze twee extra filterregels moeten toevoegen:

```
   Project > Owner ID > Not Equal > $$USERID
   Project > Sponsor ID > Not Equal > $$USERID
```

* Maak ten minste één groepering, zodat u een diagram kunt maken. Groeperen op alles, zoals bedrijf. Klik vervolgens op het tabblad Diagram en kies een diagram. Het &quot;Aantal van het Verslag&quot;zal het gebrek voor één as zijn. Dit is het aantal projecten waarin de gebruiker een toewijzing heeft.

Wanneer een gebruiker een taak op een project (die aan een taak of een projecteigenaar of een projectsponsor wordt toegewezen) wordt gegeven die persoon wordt toegevoegd aan het projectteam en kan in het het Personeelsstatuut onder het sublusje van Mensen worden gezien. Als een gebruiker wordt verwijderd uit de eigenaar van het project, de sponsor of het hebben van om het even welke taaktaken zijn hun naam nog op het projectteam. U moet de afbeelding handmatig verwijderen als u deze wilt verwijderen. Houd er rekening mee dat dit van invloed kan zijn op de nauwkeurigheid van de rapportresultaten. Als u iemand uit het projectteam wilt verwijderen, gaat u naar Staven > Personen en selecteert u de persoon of personen. Klik vervolgens op de knop Verwijderen boven de lijst.

**Vraag**

Hoe kunt u de aflopende volgorde van een kolom wijzigen in de tekstmodus (in een groep)?

**Antwoord**

U kunt verkiezen om de meeste kolommen in het lusje van Kolommen (Mening) te sorteren wanneer het bouwen van een rapport. Als u geen groepen hebt, wordt het volledige lijstrapport gesorteerd. Als u groepen hebt, wordt de volgorde in elke groep op basis van die keuze gesorteerd.

**Vraag**

Hoe kan ik kolom creëren die de Leden van het Team zal identificeren die aan een goedkeuringsstadium worden toegewezen?

**Antwoord**

Als u een Taak of Uitgave/Verzoek rapport in werking stelt, is er een kolom beschikbaar binnen Report Builder genoemd &quot;Approvers en Status&quot; die in deze informatie zal trekken.
