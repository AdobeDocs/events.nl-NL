---
title: Aanbevolen procedures voor de ontwikkeling en implementatie van componentscripts in Experience Manager as a Cloud Service
description: In deze sessie worden de nieuwste best practices beschreven die Adobe Experience Manager-ontwikkelaars kunnen volgen voor een meer voorspelbare implementatie van toepassingen. Vooraf gecompileerde, gebundelde scripts zijn geïntroduceerd als een Apache Sling-functie in 2019 en worden sinds 2020 in AEMaaCS gebruikt en bieden ontwikkelaars twee belangrijke verbeteringen ten opzichte van de klassieke manier waarop Adobe Experience Manager-componenten worden geïmplementeerd - 1. de scripts kunnen een versienummer hebben en expliciete afhankelijkheidsketens, zoals elke Java API 2. de scriptcompilatie kan nu worden uitgevoerd tijdens het ontwikkelproces van de toepassing, zodat potentiële fouten snel kunnen worden ontdekt (bijvoorbeeld ontbrekende afhankelijkheden, onjuist API-gebruik, enz.) We zullen ons richten op de manier waarop ontwikkelaars hun projecten kunnen instellen om hun scripts als vooraf gecompileerde bundels te leveren en lokale Adobe Experience Manager Sling Feature-analyseprogramma's te gebruiken om te controleren of aan de API-vereisten wordt voldaan, zodat ze eventuele fouten vroegtijdig kunnen afvangen.
solution: Experience Manager
feature: Developer Tools
topic: Development
role: Developer, Architect
level: Beginner, Intermediate, Experienced
version: Experience Manager as a Cloud Service
kt: 9177
type: Event
exl-id: 71fa0d10-cea5-416e-a6e5-2c729c7793a6
duration: 1899
source-git-commit: 5c946ab73e78d4243ca310032a10bb8e82228c3d
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# Aanbevolen procedures voor de ontwikkeling en implementatie van componentscripts in Experience Manager as a Cloud Service

In deze sessie worden de nieuwste best practices beschreven die Adobe Experience Manager-ontwikkelaars kunnen volgen voor een meer voorspelbare implementatie van toepassingen. Vooraf gecompileerde, gebundelde scripts zijn geïntroduceerd als een Apache Sling-functie in 2019 en worden sinds 2020 in AEMaaCS gebruikt en bieden ontwikkelaars twee belangrijke verbeteringen ten opzichte van de klassieke manier waarop Adobe Experience Manager-componenten worden geïmplementeerd: 1. de scripts kunnen een versienummer hebben en expliciete afhankelijkheidsketens, zoals elke Java API 2. de scriptcompilatie kan nu worden uitgevoerd tijdens het ontwikkelproces van de toepassing, zodat potentiële fouten snel kunnen worden ontdekt (bijvoorbeeld ontbrekende afhankelijkheden, onjuist API-gebruik, enz.) We zullen ons richten op de manier waarop ontwikkelaars hun projecten kunnen instellen om hun scripts als vooraf gecompileerde bundels te leveren en lokale Adobe Experience Manager Sling Feature-analyseprogramma&#39;s te gebruiken om te controleren of aan de API-vereisten wordt voldaan, zodat ze eventuele fouten vroegtijdig kunnen afvangen.

Ga het gesprek in **[Gemeenschappen van Experience League &#x200B;](https://adobe.ly/3zJrS0f)** voort.

>[!VIDEO](https://video.tv.adobe.com/v/337851/?quality=12&learn=on&hidetitle=true)

## Aanvullende bronnen

- [&#x200B; Documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform.html?lang=nl-NL)
- [&#x200B; het Overzicht van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=nl-NL)
- [Tutorials voor Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/overview.html?lang=nl)
