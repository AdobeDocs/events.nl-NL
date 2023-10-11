---
title: Vraag het de expert - De kwaliteit en betrokkenheid van gaging
description: Leer rapporten te maken die antwoord bieden op vragen over kwaliteit en betrokkenheid. Dit webinar werd geregistreerd op 13 november 2019.
activity: use
doc-type: feature video
team: Technical Marketing
kt: 9914
exl-id: 76a8e418-71c7-414a-9938-e64e4e73c184
source-git-commit: 1792dc318643aec2c12613f621361d72a7a918b1
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 1%

---

# Vraag het de expert - De kwaliteit en betrokkenheid van gaging

Leer rapporten te maken die antwoord bieden op vragen over kwaliteit en betrokkenheid. Dit webinar werd geregistreerd op 13 november 2019.

>[!VIDEO](https://video.tv.adobe.com/v/341120/?quality=12)

## Vragen en antwoorden

**Vraag**

Er zijn velden waarop u kunt filteren, maar die niet beschikbaar zijn wanneer u door deze velden probeert te groeperen. Werkt u om deze consistente opties te maken?

**Antwoord**

Met de rapportagegereedschappen kunt u niet groeperen met een dynamisch veld of een veld waarin meerdere keuzes tegelijk kunnen worden geselecteerd, zoals een selectievakje. U kunt alleen groeperen in velden met één waarde, ook al hebben deze velden veel mogelijkheden.

U kunt filteren op selectievakjes en deze weergeven, u kunt er gewoon niet op groeperen.

**Vraag**

In de iteratie over baan-rollen voorbeeld, kan ik primaire één vette tonen?

**Antwoord**

In de herhaling kunnen we de primaire rol van de baan identificeren. We moeten dit doen in een waardeexpressie, maar HTML-codes worden niet in een waardeexpressie herkend. We moeten dus een andere manier bedenken om de rol als primair te identificeren. Ik plaats &quot;**&quot; voor en na de primaire rolnaam in deze code. Geef het een poging om te zien hoe je het leuk vindt:

```
displayname=All Job Roles 
listdelimiter=<p> 
listmethod=nested(userRoles).lists 
textmode=true
type=iterate 
valueexpression=IF({user}.{roleID}={role}.{ID},CONCAT("**",{role}.{name},"**"),{role}. {name})
valueformat=HTML
```

Hiermee krijgt u een lijst zoals deze:

```
Support Engineer 
QA Engineer 
**Designer**
```

Waar Designer de primaire rol voor deze gebruiker is.

**Vraag**

Hoi! Ik werk een workflow samen voor ons redactieteam, die bijhoudt waar een artikel zich in de levenscyclus bevindt (oorspronkelijk schrijven —> afdelingsrevisies —> eindbewerkingen —> publiceren). Ze willen gemakkelijk zien bij welke mijlpaal of taak het zich momenteel bevindt. De feedback die ik krijg is de standaard Mijlsteenweergave (met rood of groen gearceerd) is te &quot;bezig en complex.&quot; Is er een manier om de &quot;Naam van het Project&quot;en &quot;Huidige Mijlpaal&quot;in een lijst of een net te tonen?

**Antwoord**

Ja. U kunt een taakrapport maken waarin de mijlpalettaken worden weergegeven waaraan momenteel wordt gewerkt en welke taak eraan is gekoppeld. Dat kunt u doen in een tabel of in een lijstrapport.

**Vraag**

Kunnen we in een verslag bewijzen hebben die gecombineerd worden met projectinformatie?

**Antwoord**

Als u een rapport van de Goedkeuring van het Bewijs hebt gecreeerd, kan de projectinformatie in kolommen worden getrokken gebruikend tekstwijze. Bijvoorbeeld, als u de projectnaam in een kolom wilde van verwijzingen voorzien, kon u het volgende gebruiken:

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name 
valueformat=HTML
```

**Vraag**

Ik zou ook meer informatie willen over de rapportage over bewijsgegevens, aangezien deze betrekking hebben op het project. Bijvoorbeeld een projectrapport met een bewijskrachtige beslissing en opmerkingen.

**Antwoord**

Als u in één rapport wilt verwijzen naar projectinformatie en proefdrukinformatie, wilt u een proefdrukrapport maken. Op dit moment kunnen opmerkingen uit een bewijs niet in dit verslag worden opgenomen, maar elk bewijsverkrijgingsbesluit kan op zijn eigen post in de kolom Goedkeuringsbesluit worden gevonden.

**Vraag**

Ik gebruik sharecol vaak om de status van één pagina te creëren (vele kolommen). Nochtans, vind ik dat als nadat ik een rapport creeer ik een kolom bij de bovenkant van de pagina wil toevoegen het zeer tijdrovend is terug te gaan en te wijzigen. Hebt u tips of trucs om dit type wijziging aan te brengen?

**Antwoord**

Als u over het zetten van een kolom bij de bovenkant van een lijst van de kolommen van de tekstwijze spreekt, zult u enkel uw kolommen manueel moeten opnieuw nummeren.

Maar als u reeds het rapport met de eerste kolom hebt gecreeerd die sommige gedeelde kolommen zijn en u een andere gedeelde kolom bovenop de lijst wilt zetten, is dit gemakkelijker.

In de redacteur van het Rapport enkel voeg een paar nieuwe kolommen toe en sleep hen aan het verre linkervan uw scherm van Kolommen (Mening). nadat u dit doet neemt een blik bij wat vroeger de linkerkolom was en u zult merken de aantallen van de tekstwijze kolomaantallen allen hebben verhoogd. Sleep zoveel lege kolommen daar als u nodig hebt. Zorg ervoor dat u iets in die lege kolommen plaatst voordat u het opslaat, anders worden deze verwijderd.

**Vraag**

Hoi - wat het laatste foutopsporingsverslag betreft - hoe kunnen de rapporten voor meerdere projecten worden opgesteld - als er insecten binnenkomen voor meerdere projecten?

**Antwoord**

U kunt filteren op portfolio of project, afhankelijk van de manier waarop u uw werk hebt georganiseerd.

U kunt ook filteren op aanvraagrijen. U zou aan de rijen van het opstellingsverzoek voor elk project kunnen willen waar u klantengebruikers als Revisoren kunt tot stand brengen die login en kaartjes direct aan de verzoekrijen kunnen voorleggen u met hen hebt gedeeld.

**Vraag**

De eerste verslagen waren gebaseerd op projecten/projectnaam, kan dit ook op taken worden gedaan en zo ja wat de beste manier om hen te groeperen, aangezien mogelijk de taaknaam vaker dan niet zou verschillen... dank!

**Antwoord**

Al deze rapporten kunnen als of taak, kwestie of projectrapporten worden gedaan, afhankelijk van hoe u beslist om dingen te volgen.

Een gemeenschappelijke manier om taken te groeperen zou hen eerst door hun projectnaam en dan door de taaknaam binnen elk project moeten groeperen. Als je twee taken met dezelfde naam hebt, is het gemakkelijk om te zien in welk project ze zich bevinden.

**Vraag**

Ik wil weten aan welke proefdrukken ze moeten voldoen, aan welke taak en welk project ze gebonden zijn, wanneer ze zijn gerouteerd, wanneer ze moeten worden uitgevoerd en wie moderator en fiatteur is.

**Antwoord**

Uitstaande proefdrukken kunnen worden gefilterd door Afwachten van besluit > Gelijk > Waar in een proefgoedkeuringsrapport. Er is een kolom voor Fiatteur, die u zal vertellen wie nog geen besluit heeft genomen.

U kunt verwijzen naar de taak of het project waaraan de proefdruk is gekoppeld in de tekstmodus (zie de voorbeelden hieronder).

```
displayname=Task Name
textmode=true 
valuefield=documentVersion:document:task:name 
valueformat=HTML
```

```
displayname=Project Name
textmode=true 
valuefield=documentVersion:document:project:name
valueformat=HTML
```

Wat de verpletterende datum, de vervaldatum en de moderator betreft, kunnen die gebieden momenteel niet in om het even welk van de rapporten van Workfront worden getrokken, zodat zou u in het Bewijs moeten klikken direct om die informatie te bekijken.

**Vraag**

Kunt u een aangepast formulier instellen om automatisch naar een aanvrager te verzenden wanneer zijn aanvraag is voltooid? Als als &quot;klantentevredenheid&quot;onderzoek?

**Antwoord**

Hier is één ding dat u kunt doen dat aan uw behoefte zou kunnen voldoen. U kunt een melding van een herinnering toevoegen aan een uitgave die een e-mail zal verzenden naar &quot;Ingegaan door&quot; nadat er een werkelijk ingevoerde Voltooiingsdatum was ingegaan. De persoon die is ingevoerd door is de persoon die de uitgave heeft gemaakt.

U zou de Herinneringsmelding maken zoals we dat deden in het webinar voor &quot;Herinnering om de After Action Review (AAR) in te vullen&quot;, behalve dit zou een Issue Herinnering zijn. U wilt waarschijnlijk ook een e-mailsjabloon voor de enquête maken. U moet de herinneringsmelding handmatig toepassen op elke uitgave (of bulkbewerking gebruiken).

Een integratie zou beter zijn omdat het de handstappen zou kunnen automatiseren, maar de herinnering bericht kan onmiddellijk worden gedaan.

**Vraag**

Ik creeerde een rapport dat projecten door malplaatjetype toont. Ik kan een lijst maken van de eigenaar van het project, maar niet van de personen die aan een project zijn toegewezen.

**Antwoord**

Als u in het Team van het Project (het Stafelen lusje) aan een kolom binnen uw projectrapport wilt trekken, zult u dit via tekstwijze willen tot stand brengen. De tekstmodus is als volgt:

```
displayname=Staffing 
listdelimiter=<p> 
listmethod=nested(projectUsers).lists 
textmode=true
type=iterate 
valuefield=user:name 
valueformat=HTML
```

## Tekstmoduscode voor het AAR Engagement Report

```
column.0.displayname=Task Details
column.0.value=<b>Project Name:</b>&nbsp;
column.0.valueformat=HTML
column.0.sharecol=true
column.1.valuefield=project:name
column.1.valueformat=HTML
column.1.sharecol=true
column.2.value=<br>
column.2.valueformat=HTML
column.2.sharecol=true
column.3.value=<b>Task Name:</b>&nbsp;
column.3.valueformat=HTML
column.3.sharecol=true
column.4.valuefield=name
column.4.valueformat=HTML
column.4.sharecol=true
column.5.value=<br>
column.5.valueformat=HTML
column.5.sharecol=true
column.6.value=<b>Task Owner:</b>&nbsp;
column.6.valueformat=HTML
column.6.sharecol=true
column.7.valuefield=assignedTo:name
column.7.valueformat=HTML
column.7.sharecol=true
column.8.value=<br>
column.8.valueformat=HTML
column.8.sharecol=true
column.9.value=<b>Actual Completion Date:</b>&nbsp;
column.9.valueformat=HTML
column.9.sharecol=true
column.10.valuefield=actualCompletionDate
column.10.valueformat=HTML
column.11.displayname=Name of Reviewer
column.11.linkedname=Name of Reviewer
column.11.namekey=view.relatedcolumn
column.11.namekeyargkey.0=Name of Reviewer
column.11.namekeyargkey.1=name
column.11.querysort=DE:Name of Reviewer:name
column.11.valuefield=Name of Reviewer:name
column.11.valueformat=customReferenceObjectAsString
column.12.displayname=AAR 1
column.12.description=In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.12.value=<b>AAR 1 Score:</b>&nbsp;
column.12.valueformat=HTML
column.12.sharecol=true
column.13.valuefield=AAR 1 - In your view, does the work match stakeholders’ expectations? Did we achieve the intended results?
column.13.valueformat=customDataLabelsAsString
column.13.sharecol=true
column.14.value=<br>
column.14.valueformat=HTML
column.14.sharecol=true
column.15.value=<br><b>AAR 1 User Comment:</b>&nbsp;
column.15.valueformat=HTML
column.15.sharecol=true
column.16.valuefield=AAR 1 User Comment
column.16.valueformat=customDataLabelsAsString
column.17.linkedname=direct
column.17.namekey=AAR 1 Reviewer Comment
column.17.querysort=DE:AAR 1 Reviewer Comment
column.17.valuefield=AAR 1 Reviewer Comment
column.17.valueformat=customDataLabelsAsString
column.18.linkedname=direct
column.18.displayname=AAR 1 Needs Attn
column.18.querysort=DE:AAR 1 Needs Attention
column.18.valuefield=AAR 1 Needs Attention
column.18.valueformat=customDataLabelsAsString
column.19.linkedname=direct
column.19.displayname=AAR 1 Needs Attn Notes
column.19.querysort=DE:AAR 1 Needs Attention Notes
column.19.valuefield=AAR 1 Needs Attention Notes
column.19.valueformat=customDataLabelsAsString
column.20.displayname=AAR 2
column.20.description=Do You Believe This Work Will Make an Impact?
column.20.value=<b>AAR 2 Score:</b>&nbsp;
column.20.valueformat=HTML
column.20.sharecol=true
column.21.valuefield=AAR 2 - Do You Believe This Work Will Make an Impact?
column.21.valueformat=customDataLabelsAsString
column.21.sharecol=true
column.22.value=<br>
column.22.valueformat=HTML
column.22.sharecol=true
column.23.value=<br><b>AAR 2 User Comment:</b>&nbsp;
column.23.valueformat=HTML
column.23.sharecol=true
column.24.valuefield=AAR 2 User Comment
column.24.valueformat=customDataLabelsAsString
column.25.linkedname=direct
column.25.namekey=AAR 2 Reviewer Comment
column.25.querysort=DE:AAR 2 Reviewer Comment
column.25.valuefield=AAR 2 Reviewer Comment
column.25.valueformat=customDataLabelsAsString
column.26.linkedname=direct
column.26.displayname=AAR 2 Needs Attn
column.26.querysort=DE:AAR 2 Needs Attention
column.26.valuefield=AAR 2 Needs Attention
column.26.valueformat=customDataLabelsAsString
column.27.linkedname=direct
column.27.displayname=AAR 2 Needs Attn Notes
column.27.querysort=DE:AAR 2 Needs Attention Notes
column.27.valuefield=AAR 2 Needs Attention Notes
column.27.valueformat=customDataLabelsAsString
column.28.displayname=AAR 3
column.28.description=Are you proud of the work you did on this?
column.28.value=<b>AAR 3 Score:</b>&nbsp;
column.28.valueformat=HTML
column.28.sharecol=true
column.29.valuefield=AAR 3 - Are you proud of the work you did on this?
column.29.valueformat=customDataLabelsAsString
column.29.sharecol=true
column.30.value=<br>
column.30.valueformat=HTML
column.30.sharecol=true
column.31.value=<br><b>AAR 3 User Comment:</b>&nbsp;
column.31.valueformat=HTML
column.31.sharecol=true
column.32.valuefield=AAR 3 User Comment
column.32.valueformat=customDataLabelsAsString
column.33.linkedname=direct
column.33.namekey=AAR 3 Reviewer Comment
column.33.querysort=DE:AAR 3 Reviewer Comment
column.33.valuefield=AAR 3 Reviewer Comment
column.33.valueformat=customDataLabelsAsString
column.34.linkedname=direct
column.34.displayname=AAR 3 Needs Attn
column.34.querysort=DE:AAR 3 Needs Attention
column.34.valuefield=AAR 3 Needs Attention
column.34.valueformat=customDataLabelsAsString
column.35.linkedname=direct
column.35.displayname=AAR 3 Needs Attn Notes
column.35.querysort=DE:AAR 3 Needs Attention Notes
column.35.valuefield=AAR 3 Needs Attention Notes
column.35.valueformat=customDataLabelsAsString
column.36.displayname=Done
column.36.valuefield=Review Complete
column.36.valueformat=customDataLabelsAsString
```
