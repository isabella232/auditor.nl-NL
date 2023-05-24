---
description: Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs.
seo-title: Test reference
title: Testverwijzing
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
exl-id: b368bf43-2007-4f98-a965-ed8fc07c0fdf
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 12%

---

# Testverwijzing{#test-reference}

Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert.

**Huidige versie van testrubriek:** 1.0.5.

Elke test is gewogen. Uw testscore is gelijk aan het toegewezen gewicht. Als u een test met een gewicht van vijf punten doorstaat, krijgt u vijf punten.

* 0: Hiermee wordt u gewaarschuwd voor problemen waarvan u op de hoogte moet zijn, maar die geen invloed hebben op uw score.
* 1: adviseert een optimalisering. Geen invloed op de gegevensnauwkeurigheid.
* 2: Als u deze test niet uitvoert, hebt u geen toegang tot de nieuwste functies en oplossingen in de Experience Cloud.
* 3: Test op efficiëntie en of de implementatie de beste praktijken volgt.
* 4: Als dit mislukt, worden mogelijk onbetrouwbare gegevens verzameld.
* 5: Als dit mislukt, ziet u mogelijk gegevensverlies.

Tests zijn geslaagd/gezakt. Zij testen of aan de testvoorwaarden wordt voldaan of niet aan de testvoorwaarden wordt voldaan, zodat er geen gedeeltelijke scores voor gedeeltelijke naleving zijn. Bijvoorbeeld, als de test op de recentste versie van een oplossing van de Adobe controleert en u slechts één versie achter bent, krijgt u de zelfde score alsof u vijf versies terug bent. De meest recente versies bevatten prestatieverbeteringen en foutoplossingen. Daarom is het raadzaam de meest recente versie te gebruiken.

Het wordt **ten zeerste aanbevolen** om resultaten van niveau 4 of 5 te corrigeren.

Het wordt **aanbevolen** om resultaten van niveau 1 tot 3 te corrigeren.

## Welke technologieën van Adobe geeft de Auditor van de Platform? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID Service (voorheen Marketing Cloud ID Service)
* Target

De volgende oplossingen van Adobe zijn momenteel niet inbegrepen in de testrubriek. Ondersteuning voor deze oplossingen is gepland voor toekomstige updates.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch
