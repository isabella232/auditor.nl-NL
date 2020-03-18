---
description: Deze verwijzing verstrekt meer informatie over de tests Auditor voor markeringsaanwezigheid uitvoert.
seo-description: Deze verwijzing verstrekt meer informatie over de tests Auditor voor markeringsaanwezigheid uitvoert.
seo-title: Tagaanwezigheid
title: Tagaanwezigheid
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Tagaanwezigheid

Deze verwijzing verstrekt meer informatie over de tests Auditor voor markeringsaanwezigheid uitvoert.

De controleur evalueert of de markering bestaat, en of het op de juiste plaats in uw paginacode is.

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
   <td colname="col1"> <p><b>Cloud voor advertenties - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> De tag Advertising Cloud is niet beschikbaar in het DOM. </p> </td> 
   <td colname="col3"> <p>Implementeer de Cloud-tag Advertising met de Launch Extension voor Advertising. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Cloud voor adverteren - segmentpixel geïmplementeerd</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> Werk de pixels van het segment Advertising Cloud bij tot de nieuwe afbeeldingstags voor Advertising Cloud. Het gebruik van verouderde AMO-segmenttags kan leiden tot gegevensverlies. </p> </td> 
   <td colname="col3"> <p>Implementeer de pixel van het Advertising Cloud-segment met de Launch Extension voor Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analyse - geladen in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De tag Adobe Analytics is niet gedetecteerd. </p> </td> 
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
   <td colname="col2"> <p> De callback <span class="codeph"> _satelliet.pageBottom()</span> is niet gevonden in de <span class="codeph"> &lt;body&gt;</span> van de pagina, die vereist is voor Dynamic Tag Management. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom- </span>aanroep helemaal niet op de pagina staat of als deze in de <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie) staat. De waarde wordt alleen doorgegeven als pageBottom <span class="codeph"> zich ergens in de tag</span> &lt;body&gt; <span class="codeph"></span> bevindt. Als het helemaal niet op de pagina is, zal het niet functioneren en de andere twee <span class="codeph"> pageBottom</span> tests zullen ook ontbreken. </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom-tag geactiveerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De DTM- <code> pageBottom</code> tag is niet gedetecteerd. </p> <p>Dit zou kunnen voorkomen als de vraag binnen een <code> if</code> verklaring is die in iets gelijkaardig aan <code> if (false) {_satellite.pageBottom()}</code>resulteert. Dus, hoewel het zou kunnen bestaan en correct geplaatst zijn, zou de markering niet kunnen branden. </p> </td> 
   <td colname="col3"> <p>Installeer de DTM- <code> pageBottom</code> aanroep op elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Kan de code voor Experience Cloud ID Service niet vinden. De Experience Cloud ID (MCID) wordt ten zeerste aanbevolen om ervoor te zorgen dat u de meeste waarde haalt uit uw Experience Cloud-oplossingen en is essentieel voor id-beheer in verschillende Experience Cloud-oplossingen. </p> </td> 
   <td colname="col3"> <p> Installeer de meest recente versie van MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - aanwezigheid van cookie</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Het <span class="codeph"> AMCV_</span> cookie is niet gevonden. U moet een bezoekersobject instantiëren met de code <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> Als dit een DTM-implementatie is, controleert u of de AdobeOrg-id correct is ingevoerd in de MCID-tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - MID-waarde aanwezig</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De MID-waarde is niet gevonden in het <span class="codeph"> AMCV_</span> cookie. </p> </td> 
   <td colname="col3"> <p>Test opnieuw om te controleren op een eventuele MCID API-latentie. Neem contact op met de klantenservice van Adobe als de aandoening aanhoudt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Starten - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. Starten is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
   <td colname="col3"> <p>Controleer of de bibliotheek Launch op de pagina is geïmplementeerd en niet wordt geblokkeerd door volgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Starten - Er zijn niet meerdere ingesloten scripts</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Er mogen niet meerdere insluitscripts op de pagina worden geladen. Productieplaatsen mogen slechts één opstartbibliotheek laden. </p> </td> 
   <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Starten - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De callback <span class="codeph"> _satelliet.pageBottom()</span> is niet gevonden binnen de <span class="codeph"> &lt;body&gt;</span> van de pagina, die is vereist voor Starten. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom- </span>aanroep helemaal niet op de pagina staat of als deze in de <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie) staat. De waarde wordt alleen doorgegeven als pageBottom <span class="codeph"> zich ergens in de tag</span> &lt;body&gt; <span class="codeph"></span> bevindt. Als het helemaal niet op de pagina is, zal het niet functioneren en de andere twee <span class="codeph"> pageBottom</span> tests zullen ook ontbreken. </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste opstartfunctionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Starten - pageBottom callback zou niet moeten bestaan wanneer asynchroon opgesteld</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>De callback <span class="codeph"> _satelliet.pageBottom()</span> is gevonden op de pagina. Dit zou niet het geval moeten zijn wanneer Launch asynchroon wordt geïmplementeerd. </p> </td> 
   <td colname="col3"> <p>Verwijder het<span class="codeph"> script _satelliet.pageBottom()</span> om de juiste opstartfunctionaliteit in te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Doel - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Doel moet worden gedefinieerd in het DOM. </p> </td> 
   <td colname="col3"> <p>Installeer de meest recente versie van Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Doel - Bibliotheek geladen in &lt;head&gt;</b> </p> <p>Dikte: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De doelbibliotheek moet in de tag <span class="codeph"> &lt;head&gt;</span> worden geladen. </p> </td> 
   <td colname="col3"> <p> Controleer of de doelbibliotheek in de tag <span class="codeph"> &lt;head&gt;</span> is geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>
