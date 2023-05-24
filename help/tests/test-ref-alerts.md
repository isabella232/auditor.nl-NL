---
description: Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.
seo-description: This reference provides more information about the alerts Adobe Experience Platform Auditor displays for tests.
seo-title: Alerts
title: Waarschuwingen
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
exl-id: 9e7ade9b-6f3c-4f1f-87b1-5dbaed63ae36
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 1%

---

# Waarschuwingen{#alerts}

Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.

Waarschuwingen tonen problemen waarvan je op de hoogte moet zijn, maar die geen invloed hebben op je score. Dit zijn aanbevelingen voor best practices die in sommige gevallen niet van toepassing zijn op uw implementatie.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
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
    --> <p><b>Advertising Cloud - Correct geïmplementeerde omzettingstag</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de juiste conversietag wordt gebruikt. </p> <p> <p>Waarschuwing: Het gebruik van verouderde conversietags voor TubeMogul kan gegevensverlies tot gevolg hebben. </p> </p> </td> 
   <td colname="col3"> <p>Voer een upgrade uit op de conversiepixels naar de nieuwe Advertising Cloud-tags voor conversie van alleen afbeeldingen. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Adobe Experience Platform Launch worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - JS-tag corrigeren gebruikt</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud moet de nieuwste JavaScript-tags gebruiken. </p> </td> 
   <td colname="col3"> <p>Upgrade uw Advertising Cloud JavaScript naar de nieuwste versie. Als u de verouderde JavaScript-versies gebruikt, kan de functionaliteit verloren gaan. </p> <p>Dit kan gemakkelijker door het gebruik van de uitbreiding van Advertising Cloud voor Platform launch worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Tag met alleen afbeelding</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>De Advertising Cloud-indeling voor afbeeldingspixels moet overeenkomen met een van de volgende aanbevolen indelingen: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;hash_value&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;hash_value&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;numeric_id&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Upgrade uw Advertising Cloud-pixels naar de nieuwe Advertising Cloud-tags voor alleen afbeeldingen, zodat u de volledige Advertising Cloud-functionaliteit kunt benutten. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Platform launch worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Segmentpixels DSP synchroniseren ingeschakeld</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de TubeMogul-segmentpixel een DSP-instelling bevat en adviseer dat de instelling aan de pixel wordt toegevoegd. </p> <p>De instelling DSP synchroniseren wordt bepaald door het gebruik van een parameter voor een queryreeks, dus </p> <p>ALS de tag wordt geactiveerd naar<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;hash_value&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;hash_value&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;numeric_id&gt;?"</span> </p> <p>EN de tag bevat de URL-parameter <span class="codeph"> "sid=")</span> </p> <p>Controleer VERVOLGENS of de URL-parameter <span class="codeph"> "cs=0"</span> of<span class="codeph"> "cs=1"</span> bestaat, en als niet adviseert dat <span class="codeph"> "cs=1"</span> worden toegevoegd aan deze pixels, zodat de overeenkomende populatiegraad kan worden verbeterd. </p> </td> 
   <td colname="col3"> <p> De URL-parameter toevoegen <span class="codeph"> "cs=1"</span> op uw Advertising Cloud-pixels zodat DSP synchroniseren kan plaatsvinden. Hierdoor nemen de overeenkomende populaties toe. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Platform launch worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamische Tag Management vereist <span class="codeph"> _satelliet.pageBottom()</span> functie. Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tag voor een correcte DTM-functionaliteit. </p> <p> <p>Opmerking: Het wordt aanbevolen de tag als <i>last</i> in de <span class="codeph"> &lt;body&gt;</span>. Als deze is gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> -tag, heeft de kans om te werken, maar omdat dit niet de beste praktijk is, kan deze onjuist functioneren of onverwachte of ongewenste resultaten opleveren. </p> </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tag voor een correcte DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - zelfgehoste</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De DTM-bibliotheek Akamai wordt gehost op Adobe-instantie op <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Zelf hosten is de geadviseerde benadering voor het laden van DTM omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, vermindert derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De DTM-bibliotheken kunnen worden gehost en beheerd via uw eigen webhosting of CDN. </p> </td> 
   <td colname="col3"> <p>Zelfhosting is de aanbevolen methode voor het laden van DTM op een pagina. Hoewel DTM-hosting via de Akamai CDN in de meeste gevallen werkt, verbetert zelforhosting de paginaprestaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Experience Cloud ID-service - Gebruik slechts één AdobeOrg</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>In een normale MCID-implementatie moet één AdobeOrg worden gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of er meerdere AdobeOrg-id's bestaan voor deze implementatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Aanvullende informatie</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>platform launch moet een <span class="codeph"> pageBottom </span>callback-functie die als laatste in de hoofdtekst van de pagina is gedefinieerd, indien synchroon geïmplementeerd. </p> <p> <p>Opmerking: Het wordt aanbevolen de tag als <i>last</i> in de <span class="codeph"> &lt;body&gt;</span>. Als deze is gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> -tag, heeft de kans om te werken, maar omdat dit niet de beste praktijk is, kan deze onjuist functioneren of onverwachte of ongewenste resultaten opleveren. </p> </p> </td> 
   <td colname="col3"> <p>platform launch vereist <span class="codeph"> _satelliet.pageBottom()</span> functie voor synchrone plaatsingen. Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tags gebruiken om de juiste functionaliteit voor Platform launches te garanderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Starten - Zelfgehost</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Aan de slag met Adobe Experience Platform Launch</a> </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> asynchrone implementatie van platform launch</a> </p> </td> 
   <td colname="col2"> <p>De Platform launch wordt gehost op de Akamai-instantie van de Adobe op <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Zelf-ontvangen is de geadviseerde benadering voor het laden van Platform launch omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, verminderend derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De bibliotheken van de Platform launch kunnen door uw eigen Web worden ontvangen en worden beheerd die of CDN. </p> </td> 
   <td colname="col3"> <p>Hoewel het ontvangen van Platform launches via Akamai CDN in de meeste gevallen werkt, wordt geadviseerd dat zelf-ontvangen als eerste stap in het verbeteren van paginaprestaties wordt uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Starten - moet asynchroon worden geïmplementeerd</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>platform launch moet asynchroon worden geïmplementeerd voor optimale prestaties. </p> </td> 
   <td colname="col3"> <p>De asynchrone parameter opnemen in het inlinescript voor een correcte functionaliteit van de asynchrone Platform launch </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Doel - Inhoud in mboxDefault</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De inhoud moet in mboxDefault bestaan wanneer u at.js gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of de inhoud beschikbaar is. </p> </td> 
  </tr> 
 </tbody> 
</table>
