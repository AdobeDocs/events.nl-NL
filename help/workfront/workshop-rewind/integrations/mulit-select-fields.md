---
title: Navigeren door de Workfront API- en Fusion-wijzigingen voor Multi-Select-velden met versnelling
description: Meer informatie over aanstaande Adobe Workfront API- en Fusion-wijzigingen, waaronder updates voor meerdere velden, versiebeheer van abonnementen voor gebeurtenissen en strategieën om onderbrekingswijzigingen te voorkomen.
feature: Workfront API, Workfront Fusion, Workfront Integrations and Apps
topic: Integrations
role: Admin, Developer, Leader, User
level: Beginner, Intermediate, Experienced
doc-type: Event
duration: 3172
last-substantial-update: 2025-08-08T00:00:00Z
jira: KT-18631
source-git-commit: 6225f36c5d26ecca5ebc2aca24a2d592a3279570
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Navigeren door de Workfront API- en Fusion-wijzigingen voor Multi-Select-velden met versnelling

Deze workshop werd op 25 juni 2025 opgenomen en bevatte Andy Hess, die de komende wijzigingen in de Workfront API en Fusion deelde.

>[!VIDEO](https://video.tv.adobe.com/v/3469978/?learn=on&enablevpops)

## Bronnen

Samen met de opnamen op aanvraag hebben we de diapresentatie en aanvullende bronnen opgenomen:
* [ het dek PDF van de Schuifregelaar ](https://workfront-experience.s3.us-west-2.amazonaws.com/Training/Guides/Customer+Success+at+Scale/Navigating+the+API+and+Fusion+Changes+for+Multi-Select+Fields+with+Ease+062425.pdf)
* Een gebeurtenis die in samenwerking met het team van de Ontwikkeling van de Software van Adobe werd ontvangen werd geleverd begin Mei op de veranderingen in de Abonnementen van de Gebeurtenis als u meer op dat specifieke gebied wilt leren, [ [de Follow-up van de Gebeurtenis] Behoud Uw Scenario&#39;s van de Fusie tijdens de Bijvoeging van de Abonnementen V2 ](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/m-p/754182#M4041)

## Belangrijkste Takeaways en Middelen

* Wijzigingen in de multiselect-velden van de Workfront API vinden plaats in versie 21 (oktober 2025) om een consistente JSON-arrayindeling te garanderen in plaats van een combinatie van een tekenreeks/arrayrespons
* Er wordt nu een versie van een abonnement voor gebeurtenissen geïntroduceerd. Versie 2 retourneert meerkeuzevelden altijd als arrays, terwijl versie 1 de huidige inconsistente werking behoudt
* Abonnementen voor nieuwe gebeurtenissen worden automatisch standaard ingesteld op versie 2. Medio januari 2026 worden alle abonnementen automatisch bijgewerkt naar versie 2
* Later dit jaar wordt een nieuwe Workfront-connectorversie uitgebracht met een handmatig upgradeproces om de moduletoewijzing te behouden en onderbrekingswijzigingen te voorkomen
* Fusion AI-assistent is momenteel beschikbaar, maar vereist een ondertekende AI-overeenkomst en een juiste instelling voor licenties. Neem contact op met uw accountmanager als u vragen hebt of meer wilt leren. [ Meer informatie bij het gebruiken van AI binnen Fusie ](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/manage-scenarios/fusion-ai-assistant)
* [ momenteel beschikbare malplaatjes van de Fusie van Workfront ](https://experienceleague.adobe.com/en/docs/workfront-fusion/using/create-and-manage-templates/currently-available-fusion-templates)
* [ Vraag voor de malplaatjes van de Fusie ](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/call-for-fusion-template-ideas/m-p/732085#M3686) - als u suggesties voor nieuwe malplaatjes van de Fusie hebt, voeg die hier toe! Dit is waar het team ideeën van trekt  

Als u om het even welke vervolgvragen hebt, gelieve te antwoorden aan deze [ Communautaire Post van Experience League ](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-navigating-the-workfront-api-and-fusion-changes/td-p/761253)! 

We hopen u te zien in toekomstige workshops over succes bij de klant!  Ben zeker om de [ Gebeurtenissen van Workfront ](https://experienceleague.adobe.com/events/?filters=Workfront) op Experience League voor de volledige lijst te controleren en te registreren.