---
description: Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert voor de aanwezigheid van tags.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs for tag presence.
seo-title: Tag presence
title: Tagaanwezigheid
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
exl-id: a6ac4d95-2f96-4abb-b39b-4dd0d8df5fe8
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 5%

---

# Tagaanwezigheid

Deze naslaggids bevat meer informatie over de tests die Adobe Experience Platform Auditor uitvoert voor de aanwezigheid van tags.

De Auditor van het Platform evalueert of de markering bestaat, en of het op de juiste plaats in uw paginacode is.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Testen </th> 
   <th colname="col2" class="entry"> Criteria </th> 
   <th colname="col3" class="entry"> Aanbeveling </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> De Advertising Cloud-tag is niet beschikbaar in het DOM. </p> </td> 
   <td colname="col3"> <p>Implementeer de Advertising Cloud-tag met de Advertising Cloud-extensie voor Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Geïmplementeerde segmentpixel</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> Upgrade de Advertising Cloud-segmentpixels naar de nieuwe Advertising Cloud-tags voor alleen afbeeldingen. Het gebruik van verouderde AMO-segmenttags kan leiden tot gegevensverlies. </p> </td> 
   <td colname="col3"> <p>Implementeer het Advertising Cloud-segmentpixel met de Advertising Cloud-extensie voor Platform launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analyse - geladen in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De Adobe Analytics-tag is niet gedetecteerd. </p> </td> 
   <td colname="col3"> <p>Installeer de nieuwste versie van Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p>Aanvullende informatie: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-probleemoplossing</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Code voor kop- en voetteksten toevoegen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. Dynamic Tag Management is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
   <td colname="col3"> <p>Controleer of de DTM-bibliotheek op de pagina is geïmplementeerd en niet wordt geblokkeerd door daaropvolgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Eén insluitcode</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Productieplaatsen mogen slechts één DTM-bibliotheek laden. </p> </td> 
   <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De <span class="codeph"> _satelliet.pageBottom()</span> callback is niet gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> van de pagina, vereist door Dynamic Tag Management. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom </span>de vraag wordt niet gevonden bij allen op de pagina, of als het in <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie). Het gaat alleen door als <span class="codeph"> pageBottom</span> bevindt zich ergens in de <span class="codeph"> &lt;body&gt;</span> tag. Als het helemaal niet op de pagina staat, werkt het niet en de andere twee <span class="codeph"> pageBottom</span> de tests zullen ook mislukken . </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tag voor een correcte DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom-tag geactiveerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De DTM <code> pageBottom</code> tag is niet gedetecteerd. </p> <p>Dit zou kunnen voorkomen als de vraag binnen een <code> if</code> verklaring die in iets gelijkaardig aan resulteert <code> if (false) {_satellite.pageBottom()}</code>. Dus, hoewel het zou kunnen bestaan en correct geplaatst zijn, zou de markering niet kunnen branden. </p> </td> 
   <td colname="col3"> <p>De DTM installeren <code> pageBottom</code> roep op elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-service - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>De Experience Cloud ID-servicecode is niet gevonden. De Experience Cloud-id (MCID) wordt ten zeerste aanbevolen om ervoor te zorgen dat u de meeste waarde uit uw Experience Cloud-oplossingen haalt en is van essentieel belang voor het beheer van id's voor alle Experience Cloud-oplossingen. </p> </td> 
   <td colname="col3"> <p> Installeer de meest recente versie van MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-service - aanwezigheid cookie</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De <span class="codeph"> AMCV_</span> cookie niet gevonden. U moet een bezoekersobject instantiëren vanuit het dialoogvenster <span class="codeph"> VisitorAPI.js</span> code. </p> </td> 
   <td colname="col3"> <p> Als dit een DTM-implementatie is, controleert u of de AdobeOrg-id correct is ingevoerd in de MCID-tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-service - MID-waarde aanwezig</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/nl-NL/id-service/using/intro/cookies.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De MID-waarde is niet gevonden in het dialoogvenster <span class="codeph"> AMCV_</span> cookie. </p> </td> 
   <td colname="col3"> <p>Test opnieuw om te controleren op een eventuele MCID API-latentie. Neem contact op met de klantenservice van Adobe als de aandoening aanhoudt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b> Starten - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. platform launch is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
   <td colname="col3"> <p>Controleer of de Platform launch-bibliotheek op de pagina is geïmplementeerd en niet wordt geblokkeerd door volgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Starten - Er zijn niet meerdere ingesloten scripts</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Er mogen niet meerdere insluitscripts op de pagina worden geladen. Productieplaatsen mogen slechts één Platform launch-bibliotheek laden. </p> </td> 
   <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Starten - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De <span class="codeph"> _satelliet.pageBottom()</span> callback is niet gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> van de pagina, die door Platform launch wordt vereist. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom </span>de vraag wordt niet gevonden bij allen op de pagina, of als het in <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie). Het gaat alleen door als <span class="codeph"> pageBottom</span> bevindt zich ergens in de <span class="codeph"> &lt;body&gt;</span> tag. Als het helemaal niet op de pagina staat, werkt het niet en de andere twee <span class="codeph"> pageBottom</span> de tests zullen ook mislukken . </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tags gebruiken om de juiste functionaliteit voor Platform launches te garanderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Starten - pageBottom callback zou niet moeten bestaan wanneer asynchroon opgesteld</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> _satelliet.pageBottom()</span> callback werd gevonden op de pagina, die niet het geval zou moeten zijn wanneer de Platform launch asynchroon wordt opgesteld. </p> </td> 
   <td colname="col3"> <p>Verwijder de<span class="codeph"> _satelliet.pageBottom()</span> script om de juiste functionaliteit voor Platform launches in te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Doel - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Doel moet worden gedefinieerd in het DOM. </p> </td> 
   <td colname="col3"> <p>Installeer de meest recente versie van Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Doel - Bibliotheek geladen in &lt;head&gt;</b> </p> <p>Dikte: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De doelbibliotheek moet in het dialoogvenster <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
   <td colname="col3"> <p> Controleer of de doelbibliotheek is geladen in het dialoogvenster <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
  </tr> 
 </tbody> 
</table>
