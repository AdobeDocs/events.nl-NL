---
title: Aanbevolen procedures voor de ontwikkeling en implementatie van componentscripts in as a Cloud Service Experience Manager
description: In deze sessie worden de nieuwste best practices beschreven die Adobe Experience Manager-ontwikkelaars kunnen volgen voor een meer voorspelbare implementatie van toepassingen. Vooraf gecompileerde, gebundelde scripts zijn geïntroduceerd als een Apache Sling-functie in 2019 en worden sinds 2020 in AEMaaCS gebruikt en bieden ontwikkelaars twee belangrijke verbeteringen ten opzichte van de klassieke manier waarop Adobe Experience Manager-componenten worden geïmplementeerd - 1. de scripts kunnen een versienummer hebben en expliciete afhankelijkheidsketens, zoals elke Java API 2. de scriptcompilatie kan nu worden uitgevoerd tijdens het ontwikkelproces van de toepassing, zodat potentiële fouten snel kunnen worden opgespoord (bijvoorbeeld ontbrekende afhankelijkheden, onjuist API-gebruik, enz.) We zullen ons richten op de manier waarop ontwikkelaars hun projecten kunnen instellen om hun scripts als vooraf gecompileerde bundels te leveren en lokale Adobe Experience Manager Sling Feature-analyseprogramma's te gebruiken om te controleren of aan de API-vereisten wordt voldaan, zodat ze eventuele fouten vroegtijdig kunnen afvangen.
solution: Experience Manager
feature: Developer Tools
topic: Development
role: Developer, Architect
level: Beginner, Intermediate, Experienced
version: Cloud Service
kt: 9177
type: Event
exl-id: ba85855c-2624-486d-a754-370fb1308c5a
source-git-commit: ca06e5a8b1602a7bcfb83a43f529680a5a96bacf
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 6%

---

# Aanbevolen procedures voor de ontwikkeling en implementatie van componentscripts in as a Cloud Service Experience Manager

In deze sessie worden de nieuwste best practices beschreven die Adobe Experience Manager-ontwikkelaars kunnen volgen voor een meer voorspelbare implementatie van toepassingen. Vooraf gecompileerde, gebundelde scripts zijn geïntroduceerd als een Apache Sling-functie in 2019 en worden sinds 2020 in AEMaaCS gebruikt en bieden ontwikkelaars twee belangrijke verbeteringen ten opzichte van de klassieke manier waarop Adobe Experience Manager-componenten worden geïmplementeerd: 1. de scripts kunnen een versienummer hebben en expliciete afhankelijkheidsketens, zoals elke Java API 2. de scriptcompilatie kan nu worden uitgevoerd tijdens het ontwikkelproces van de toepassing, zodat potentiële fouten snel kunnen worden opgespoord (bijvoorbeeld ontbrekende afhankelijkheden, onjuist API-gebruik, enz.) We zullen ons richten op de manier waarop ontwikkelaars hun projecten kunnen instellen om hun scripts als vooraf gecompileerde bundels te leveren en lokale Adobe Experience Manager Sling Feature-analyseprogramma&#39;s te gebruiken om te controleren of aan de API-vereisten wordt voldaan, zodat ze eventuele fouten vroegtijdig kunnen afvangen.

Doorgaan met gesprek in **[Experiencen League](https://adobe.ly/3zJrS0f)**.

>[!VIDEO](https://video.tv.adobe.com/v/337851/?quality=12&learn=on&hidetitle=true)

## Aanvullende bronnen

- [Documentatie voor Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html)
- [Overzicht van Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html)
- [Adobe Experience Platform-tutorials](https://experienceleague.adobe.com/docs/platform-learn/tutorials/overview.html?lang=nl)
