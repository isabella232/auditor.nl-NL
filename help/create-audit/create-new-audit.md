---
description: Nieuwe audit maken met Adobe Experience Platform Auditor
seo-description: Create a new audit in Adobe Experience Platform Auditor
seo-title: Create a new audit in Adobe Experience Platform Auditor
title: Nieuwe audit maken met Adobe Experience Platform Auditor
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
exl-id: 1c4eed8e-4d49-49af-95c5-df13c9f13e4a
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Nieuwe controle maken{#create-a-new-audit}

>[!NOTE]
>
>De gebruikers zijn beperkt tot één controle die tegelijkertijd loopt. Er treedt een fout op als u een controle probeert te starten met dezelfde instellingen als de controle die wordt uitgevoerd. U kunt de koppeling in het foutbericht gebruiken als u de audit die momenteel wordt uitgevoerd wilt annuleren, zodat u een nieuwe kunt maken.

Gebruik desgewenst de koppeling onder aan de pagina om toegang te krijgen tot een gratis, volledig uitgeruste proefaccount met ObservePoint.

1. Klik in de lijst Auditor op **[!UICONTROL New Audit]**.

   De [!DNL New Audit] wordt geopend.

   ![](assets/config.png)

1. (Vereist) Geef de audit een naam.

   De naam mag maximaal 250 tekens lang zijn.
1. (Vereist) Geef de eerste URL op.

   Het protocol wordt vereist wanneer het specificeren van beginnende URL. De beginnende URL is de pagina waar de controle begint kruipend. Als de Adobe Experience Platform Auditor eenmaal is gestart, doorloopt deze tot 500 pagina&#39;s en worden de koppelingen gevolgd die beginnen bij de eerste URL. Zie [Filters opnemen en uitsluiten](../create-audit/filters.md) voor meer informatie . De eerste URL kan maximaal 250 tekens lang zijn.

   >[!NOTE]
   >
   >In sommige gevallen kan het 48 uur duren voordat een scan van 500 pagina&#39;s is voltooid.

1. Geef een of meer e-mailadressen op voor meldingen over deze controle.

   U kunt meerdere e-mails opgeven door elk adres te scheiden met een komma. De aanvrager wordt standaard op de hoogte gesteld. E-mailadressen worden in real-time gevalideerd. Als u een ongeldig adres ingaat, wordt uw op het scherm op de hoogte gebracht.

   Elke e-mail is beperkt tot maximaal 250 tekens, inclusief het einde van het domein (bijvoorbeeld .com).

1. Geef het volgende op [!UICONTROL Include Filters].

   Dit veld kan exacte URL&#39;s, gedeeltelijke URL&#39;s of reguliere expressies bevatten. Gebruik dit veld voor criteria waaraan elke URL moet voldoen. Eventuele gekropen URL&#39;s die niet overeenkomen met de [!UICONTROL Include Filter] criteria zijn niet opgenomen in de auditresultaten.

   U zou folders kunnen ingaan u de controle wilt aftasten. Of, kunt u dwars-domein of zelfverwijzingscontrole uitvoeren, waar u de controle op één domein moet beginnen en op een ander beëindigen. Typ hiertoe de domeinen die u wilt doorlopen. voor complexe URL-patronen gebruikt u een reguliere expressie.

   >[!NOTE]
   >
   >Als u een pagina in uw filters opneemt, maar deze niet is verbonden met de eerste URL, of als de controleur van het Platform 500 pagina&#39;s scant voordat deze pagina wordt bereikt, wordt de pagina niet gescand en wordt deze niet opgenomen in de testresultaten.

   De include-filters zijn beperkt tot 1000 tekens per regel.

   Zie [Inclusief lijst](../create-audit/filters.md) voor meer informatie .
1. Geef filters voor uitsluiten op.

   De [!UICONTROL Exclude List] voorkomt dat URL&#39;s worden gecontroleerd. Gebruik exacte URL&#39;s, gedeeltelijke URL&#39;s of reguliere expressies, net als in de [!UICONTROL Include List].

   Een gebruikelijke manier is om een logout-koppeling uit te sluiten als de audit een gebruikerssessie heeft (bijvoorbeeld: `/logout`, dat wil zeggen elke URL die de tekenreeks bevat `/logout`).

   De uitsluitingsfilters zijn beperkt tot 1.000 tekens per regel.

   Zie [Lijst uitsluiten](../create-audit/filters.md) voor meer informatie .
1. (Optioneel) U kunt desgewenst de include- en uitsluitingsfilters testen en uw URL&#39;s testen.

   Voer de filters en URL&#39;s in en klik vervolgens op **[!UICONTROL Apply]** om de test uit te voeren.

   ![](assets/test-advanced-filters.png)

1. Klik op **[!UICONTROL Run Report]**.
