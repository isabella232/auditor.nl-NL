---
description: Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert voor de consistentie van tags.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs for tag consistency.
seo-title: Tag consistency
title: Codeconsistentie
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
exl-id: 681cf2f8-e022-4fb0-a06a-b4986710f501
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# Codeconsistentie

Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert voor de consistentie van tags.

De consistentietests van de controleur van het Platform zoeken naar inconsistenties op alle gescande pagina&#39;s. Dit zijn waarden of configuraties die voor alle pagina&#39;s op de site hetzelfde moeten zijn om nauwkeurige gegevensverzameling te garanderen.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Testen </th> 
   <th colname="col2" class="entry"> Criteria </th> 
   <th colname="col3" class="entry"> Aanbeveling </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analyse - Consistente codeversie </b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Er zijn meerdere versies van de Analytics-code gevonden. </p> </td> 
   <td colname="col3"> <p>Vervang alle instanties van Analytics door de huidige versie. </p> </td> 
  </tr> 
 </tbody> 
</table>
