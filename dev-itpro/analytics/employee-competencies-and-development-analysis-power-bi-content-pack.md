---
title: Contenuti Power BI sullo sviluppo e le competenze dei dipendenti
description: "In questo argomento vengono fornite i contenuti Power BI sullo sviluppo e le competenze dei dipendenti in Dynamics 365 for Operations. Viene descritto come accedere ai report inclusi nel pacchetto di contenuti e vengono fornite informazioni sul modello dati e sulle entità utilizzati per creare un pacchetto di contenuti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 770a832efe8ee2da44d65670b1818be4fcf4bcc0
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Contenuti Power BI sullo sviluppo e le competenze dei dipendenti

[!include[banner](../includes/banner.md)]


In questo argomento vengono fornite i contenuti Power BI sullo sviluppo e le competenze dei dipendenti in Dynamics 365 for Operations. Viene descritto come accedere ai report inclusi nel pacchetto di contenuti e vengono fornite informazioni sul modello dati e sulle entità utilizzati per creare un pacchetto di contenuti.

<a name="accessing-the-content-pack"></a>Accesso al pacchetto di contenuti
--------------------------

Il pacchetto di contenuti sullo sviluppo e le competenze dei dipendenti è disponibile nella libreria delle risorse condivise in Microsoft Dynamics Lifecycle Services (LCS). Per ulteriori informazioni su come scaricare il pacchetto di contenuti e collegarlo ai dati Microsoft Dynamics 365 for Operations, vedere [Contenuto Power BI in LCS da Microsoft e dai partner](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Report inclusi nel pacchetto di contenuti
Dopo aver collegato il pacchetto di contenuti ai dati di Microsoft Dynamics 365 for Operations, nei report vengono visualizzati i dati dell'organizzazione. Se non è mai stato usato Microsoft Power BI in precedenza, è possibile ottenere informazioni in merito nella [pagina Formazione guidata a Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). I report inclusi nel pacchetto di contenuti dispongono di grafici e tabelle contenenti informazioni aggiuntive. Nella seguente tabella vengono illustrati i report.

| Report                            | Contenuto                                               |
|-----------------------------------|--------------------------------------------------------|
| Analisi di sviluppo e delle competenze | Tipi di competenza dei membri del team e competenze dei membri del team in base al tipo |
| Profilo competenze                     | Profilo competenze del dipendente selezionato                |
| Analisi competenze                    | Competenze per tipo e valutazione                              |

È possibile filtrare i grafici e i riquadri in questi report e aggiungerli al dashboard. Per ulteriori informazioni su come applicare filtri ed eseguire aggiunte in Power BI, vedere [Creare e configurare un dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Informazioni su modelli ed entità di dati
I dati di Dynamics 365 for Operations vengono utilizzati per compilare i report nel pacchetto di contenuti sullo sviluppo e le competenze dei dipendenti. Nella tabella seguente vengono illustrate le entità su cui è stato basato il pacchetto di contenuti.

| Entità                            | Contenuto                                                                                                   | Relazioni con altre entità                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Forzalavoro\_OffsetCalendario         | Offset di calendario su report suddivisi                                                                          |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_Società                | Società in base a cui filtrare i report                                                                             |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_Retribuzione           | Tariffa retributiva e frequenza nel tempo                                                                           |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_RetribuzioneCorrente    | Tariffa retributiva e frequenza a partire dalla data corrente                                                              | Forzalavoro\_Società Forzalavoro\_RetribuzioneCorrente Forzalavoro\_DatiDemografici Forzalavoro\_Mansione Forzalavoro\_Posizione                                                                                                                                                                                            |
| Forzalavoro\_PosizioneCorrente        | Posizione a partire dalla data corrente, equivalente a tempo pieno (FTE), posizioni aperte e posizioni da aperte ad assegnate | Forzalavoro\_Mansione Forzalavoro\_Posizione                                                                                                                                                                                                                                                                      |
| Forzalavoro\_LavoratoreCorrente          | Lavoratori a partire dalla data corrente, età e numero di dipendenti                                                         | Forzalavoro\_Società Forzalavoro\_Retribuzione Forzalavoro\_PosizioneGeografica Forzalavoro\_Prestazioni Forzalavoro\_CompetenzaPersona Forzalavoro\_NomeLavoratore Forzalavoro\_NomeSuperiore Forzalavoro\_TitoloLavoratore Forzalavoro\_DatiDemografici Forzalavoro\_Mansione Forzalavoro\_Impiego Forzalavoro\_Posizione                     |
| Forzalavoro\_Data                   | Giorni, settimane, mesi e anni.                                                                             |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_DatiDemografici           | Data di nascita, sesso, origine etnica e stato civile                                                   |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_Impiego             | Data di inizio, data di fine e data della transizione                                                                  |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_PosizioneGeografica     | Città, provincia, codice postale e stato/regione o provincia                                                           |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_Mansione                    | Funzione, tipo e titolo                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_CompetenzaPreferitaMansione      | Importanza, valutazione, competenza e il livello di competenza                                                                 | Forzalavoro\_Competenza Forzalavoro\_Mansione                                                                                                                                                                                                                                                                         |
| Forzalavoro\_AssegnazionePosizionePrecedente | Motivo dell'assegnazione, data di inizio, data di fine e mansione                                                           | Forzalavoro\_OffsetCalendario Forzalavoro\_Data Forzalavoro\_Mansione Forzalavoro\_Posizione                                                                                                                                                                                                                            |
| Forzalavoro\_Prestazioni            | Valutazione, descrizione e modello di valutazione                                                                      |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_CompetenzaPersona            | Livello, data livello e competenza                                                                               | Forzalavoro\_Competenza                                                                                                                                                                                                                                                                                        |
| Forzalavoro\_AnalisiCompetenzaPersona    | Certificato, livello, data livello e competenza                                                                    | Forzalavoro\_NomeLavoratore Forzalavoro\_Competenza                                                                                                                                                                                                                                                                  |
| Forzalavoro\_Posizione               | Reparto, FTE, posizione, tipo di posizione e titolo                                                        |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_TendenzaPosizione          | Posizioni nel tempo, FTE e mansione                                                                          | Forzalavoro\_OffsetCalendario Forzalavoro\_Data Forzalavoro\_Mansione Forzalavoro\_Posizione                                                                                                                                                                                                                            |
| Forzalavoro\_NomeSuperiore    | Nome, cognome e nome completo                                                                       |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_Competenza                  | Competenza, tipo di competenza e valutazione                                                                              |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_LavoratoreCongedato       | Lavoratori congedati, data del congedo, titolo, posizione e mansione                                             | Forzalavoro\_Società Forzalavoro\_Retribuzione Forzalavoro\_PosizioneGeografica Forzalavoro\_Prestazioni Forzalavoro\_NomeLavoratore Forzalavoro\_NomeSuperiore Forzalavoro\_OffsetCalendario Forzalavoro\_Data Forzalavoro\_TitoloLavoratore Forzalavoro\_DatiDemografici Forzalavoro\_Impiego Forzalavoro\_Mansione Forzalavoro\_Posizione |
| Forzalavoro\_NomeLavoratore             | Nome, cognome e nome completo                                                                       |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_TitoloLavoratore            | Titolo e data di anzianità                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Forzalavoro\_TendenzaLavoratore             | Lavoratori nel tempo, numero di dipendenti, società e posizione                                                        | Forzalavoro\_Società Forzalavoro\_Retribuzione Forzalavoro\_PosizioneGeografica Forzalavoro\_Prestazioni Forzalavoro\_NomeLavoratore Forzalavoro\_NomeSuperiore Forzalavoro\_OffsetCalendario Forzalavoro\_Data Forzalavoro\_TitoloLavoratore Forzalavoro\_DatiDemografici Forzalavoro\_Impiego Forzalavoro\_Mansione                     |

Le entità sono state utilizzate per creare le misure calcolate nel modello dati. Queste misure calcolate vengono quindi utilizzate per calcolare gli indicatori di prestazione chiave (KPI) e i report utilizzati nel pacchetto di contenuti. Se si desidera includere calcoli aggiuntivi nei report e nei dashboard, è possibile scaricare e modificare il file CompetenciesandDevelopment.pbix da LCS. Questo file è il modello dati predefinito utilizzato per creare il pacchetto di contenuti. Una volta apportate le modifiche, è possibile creare un pacchetto di contenuti per l'organizzazione e un dashboard che contengono le informazioni aggiunte.

## <a name="additional-resources"></a>Risorse aggiuntive
Di seguito sono riportati alcuni collegamenti utili correlati alle entità e alla creazione di contenuto per Power BI:

-   [Entità di dati](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Creazione di pacchetti di contenuti per l'organizzazione](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modellazione di dati tramite Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Aggiunta di riquadri Power BI ad aree di lavoro](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)




