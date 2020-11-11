---
description: Algemene vragen en antwoorden over de Adobe Experience Platform Auditor
seo-description: Algemene vragen en antwoorden over de Adobe Experience Platform Auditor
seo-title: Veelgestelde vragen over Adobe Experience Platform Auditor
title: Veelgestelde vragen over Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 3%

---


# Veelgestelde vragen over Adobe Experience Platform Auditor{#auditor-faq}

Dit artikel bevat de antwoorden op veelgestelde vragen over Adobe Experience Platform Auditor.

* [Wat is Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Komt mijn bedrijf in aanmerking om de Auditor van de Platform te gebruiken?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Welke technologieën van Adobe geeft de Auditor van de Platform?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Hoeveel controles kan ik uitvoeren?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Wat is er gekropen voor een controle?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Hoe lang duurt een controle?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Welke informatie wordt in een rapport verstrekt?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Hoe handelbaar is die informatie?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Kan de Platform Auditor de niet-Adobe-technologie controleren?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Kan ik mijn IP-adressen goedkeuren om het scannen van pagina&#39;s toe te staan...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Gebruikt de Auditor van de Platform de zelfde IP waaiers zoals Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Wat is Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

De Auditor van de Platform is een dienst van Adobe Experience Cloud die met ObservePoint, deskundigen in het bevestigen van digitale implementaties werd ontwikkeld.

Met de Auditor van de Platform, kunnen de klanten tot 500 webpagina&#39;s tegelijkertijd aftasten en een rapport ontvangen dat toont hoe te om hun implementaties van Adobe Experience Cloud te verbeteren zodat ontvangen zij de volledige waarde van hun Adobe investering.

## Mag ik de Platform Auditor gebruiken? {#section-f90094050d1e44929066a942833435cf}

Alle Adobe Experience Cloud-klantenorganisaties krijgen gratis toegang tot de accountant van het Platform (vanaf 1 mei 2018). Elke gebruiker moet akkoord gaan met de gebruiksvoorwaarden van Adobe/ObservePoint in de Adobe Experience Cloud-gebruikersinterface voordat hij of zij toegang krijgt tot de functionaliteit. Neem contact op met uw accountmanager als u zich wilt afmelden.

## Hoe heb ik toegang tot de Auditor van het Platform? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. U kunt ook rechtstreeks naar [https://auditor.adobe.com](https://auditor.adobe.com) gaan.

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

## Hoeveel controles kan ik uitvoeren? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Er is geen limiet voor het aantal controles dat u kunt uitvoeren. De gebruikers zijn beperkt tot één controle die tegelijkertijd loopt. Er treedt een fout op als u een controle probeert te starten met dezelfde instellingen als de controle die wordt uitgevoerd.

## Wat is er gekropen voor een controle? {#section-6d068ed69ece4a1bb6d0c34454550c45}

De ObservePoint-technologie doorloopt momenteel URL&#39;s die in documentkoppelingen zijn gevonden. Koppelingen in knoppen, pagineringswidgets en andere dergelijke pagina-elementen lopen niet door.

## Hoe stel ik nieuwe criteria voor om de controleur van de Platform te testen? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Hoe lang duurt een controle? {#section-5086ae27ef1f4671a9d951348654633a}

Er zijn veel factoren die bijdragen tot de tijd die nodig is om een audit te voltooien, zoals:

* Tijdstip van laden pagina

   De ObservePoint-engine laadt elke pagina van de controle in een browser. Hoe sneller een pagina wordt geladen, hoe sneller de controle wordt voltooid.
* Gelijktijdige verbindingen

   De Controleur van het Platform gebruikt één enkele verbinding om elke pagina te bezoeken. Voor accounts met volledig observerpunt worden maar liefst tien engines tegelijk gebruikt.
* Netwerkstilte

   Nadat elke pagina laadt, wacht de controle op een netwerkstilte van zeven seconden alvorens aan de volgende pagina te werk te gaan. Als een pagina veel netwerkverzoeken verzendt die voorkomen nadat de pagina laadt, wacht onderbreking na 60 seconden.
* Pagina opnieuw

   Als er geen pagina of tag kan worden gevonden, wordt die URL opgeslagen en later in de controle geretourneerd. De controle zal een pagina tot drie keer bezoeken om ervoor te zorgen dat de fout niet door een voorbijgaande kwestie werd veroorzaakt.
* Verwerking

   Nadat een controle is gelopen, worden alle gegevens het verzameld verwerkt en door de regels gefiltreerd. Deze verwerkingstijd is belangrijk, maar neemt niet zo veel tijd in beslag als de scan zelf.

>[!NOTE]
>
>De Auditor van het Platform stelt één enkele aftasten tegelijkertijd in werking. De Volledige rekeningen ObservePoint kunnen vele controles achtereenvolgens in werking stellen.

## Welke informatie wordt in een rapport verstrekt? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Elke scan genereert een rapport waarin wordt aangegeven welke URL&#39;s zijn gescand, welke problemen zijn aangetroffen op deze webpagina&#39;s en hoe de gevonden problemen kunnen worden verholpen.

De resultaten van scans worden uitgesplitst in drie categorieën:

* Configuratie
* Codeconsistentie
* Tagaanwezigheid

Naast deze drie categorieën bevat het rapport waarschuwingen die informatie bevatten waarvan u op de hoogte moet zijn, maar waarvoor niet noodzakelijkerwijs onmiddellijk actie nodig is.

De aanbevelingen die binnen deze categorieën vallen, worden vervolgens uitgesplitst in drie extra categorieën:

* Zeer aanbevolen
* Aanbevolen
* Geslaagd

## Hoe handelbaar is die informatie? {#section-9308c1ea882048b781087ae6d2eee9f0}

Alle aanbevelingen die via de Platform Auditor worden gedaan, zijn bedoeld om u te helpen actie te ondernemen om een probleem met de implementatie van Adobe Experience Cloud-oplossingen, zoals DTM of Target, op te lossen. Om dit mogelijk te maken, heeft het team van Platforms Auditor uitgebreid gewerkt aan zeer gedetailleerde instructies over wat moet worden gedaan waar. U kunt een spreadsheet van alle gescande URL&#39;s en alle testresultaten exporteren, zodat u probleemgebieden eenvoudig kunt identificeren. Hier is een voorbeeld van één aanbeveling voor een implementatie DTM:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>Een _satelliet.pageBottom() functie is vereist voor een correcte implementatie DTM. Voeg het inlinescript toe vlak voor de afsluitende &lt;/body&gt;-tag om de juiste DTM-functionaliteit te garanderen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kan de Platform Auditor de niet-Adobe-technologie controleren? {#section-f6e73c56083b4815bbf901296038bcd4}

Nee. Nochtans, laat het volledige aanbod ObservePoint klanten toe om al uw marketing markeringen en technologieën te controleren en te controleren. Als Adobe-klant hebt u toegang tot een gratis proefaccount. Ga naar de pagina Auditor Platform van [ObservePoint voor toegang tot uw proefaccount](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Kan ik mijn IP adressen goedkeuren om het aftasten van pagina&#39;s toe te staan die door login worden beschermd? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Deze functionaliteit wordt momenteel niet ondersteund zonder het volledige ObservePoint-aanbod.

## Gebruikt de Auditor van de Platform de zelfde IP waaiers zoals ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

Het kruipen wordt uitgevoerd door ObservePoint, zodat worden de zelfde IP adressen gebruikt.

Zie de documentatie [van](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ObservePoint voor meer details.
