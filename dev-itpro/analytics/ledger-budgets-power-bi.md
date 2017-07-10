---
title: Contenuto Power BI Effettivi rispetto al budget
description: "Questo argomento descrive il contenuto Power BI Effettivi rispetto al budget. Viene descritto come accedere ai report inclusi nel contenuto e vengono fornite informazioni sul modello dati e sulle entità utilizzati per creare il contenuto."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: it-it
ms.lasthandoff: 06/13/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Contenuto Power BI Effettivi rispetto al budget

[!include[banner](../includes/banner.md)]


Questo argomento descrive il contenuto Microsoft Power BI **Effettivi rispetto al budget**. Descrive come accedere ai report di Power BI e fornisce informazioni sul modello dati e sulle entità utilizzati per costruire il contenuto. 

# <a name="overview"></a>Panoramica

Il contenuto di Power BI **Effettivi rispetto al budget** è stato creato per i singoli responsabili per il monitoraggio delle prestazioni degli effettivi rispetto al budget nella loro organizzazione. Il contenuto di Power BI **Effettivi rispetto al budget** fornisce visibilità negli scostamenti di budget. È possibile analizzare il budget per l'anno corrente in base a categoria di conti, codice budget, conto principale, descrizioni del conto principale o periodo fiscale per ottenere una migliore comprensione della causa di tutti gli scostamenti. 

# <a name="accessing-the-power-bi-content"></a>Accesso al contenuto Power BI
Se si utilizza l'aggiornamento 2017 di Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, i report del contenuto di Power BI **Effettivi rispetto al budget** vengono visualizzati nelle aree di lavoro **Budget contabili e previsioni** e **CFO**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Report inclusi nel contenuto Power BI
Nella seguente tabella sono descritti i dettagli sulle metriche disponibili in ogni pagina del report nel contenuto di Power BI **Effettivi rispetto al budget**.

| Report                      | Metriche |
|-----------------------------|---------|
| Spese - Effettivi rispetto al budget | <ul><li>Spese totali anno in corso</li><li>Spese totali budget anno in corso</li></ul> |
| Ricavi - Effettivi rispetto al budget  | <ul><li>Ricavi totali anno in corso</li><li>Ricavi totali budget anno in corso</li><ul> |
| Gestione spese                     | <ul><li>Spese totali anno in corso</li><li>Obiettivo per le spese in base al budget </li><ul> |
| Ricavi                     | <ul><li>Ricavi totali anno in corso</li><li>Obiettivo per ricavi in base al budget </li><ul> |
| Reddito netto                  | <ul><li>Reddito netto anno in corso</li><li>Obiettivo per reddito netto in base al budget </li><ul> |

## <a name="extending-the-power-bi-content"></a>Estensione del contenuto Power BI
Utilizzando i pacchetti di contenuti disponibili in Microsoft Dynamics Lifecycle Services (LCS), è possibile fornire eccezionali analisi alle persone che non accedono a Microsoft Dynamics 365. È possibile modificare i pacchetti di contenuti affinché siano inclusi altri report o rappresentazioni e quindi pubblicate i pacchetti contenuti nel tenant Power BI.com per l'analisi. 

Puoi trovare il contenuto di Power BI **Effettivi rispetto al budget** della raccolta delle risorse condivise in LCS. Per ulteriori informazioni su come scaricare il contenuto e implementarlo nell'organizzazione, vedere [Contenuto Power BI in LCS da Microsoft e dai partner](power-bi-content-microsoft-partners.md). Per guardare una demo che mostra come implementare il contenuto di Power BI, vedere [Contenuto di Power BI da Microsoft e partner in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

# <a name="understanding-the-data-model-and-entities"></a>Informazioni su modelli ed entità di dati

| Entità                    | Contenuto |
|---------------------------|----------|
| Attività di contabilità generale | Importo transazione per contabilità generale |
| Attività di budget         | Importi di transazione per il registro di budget |
| Conti principali             | Conti principali per filtrare i report per |
| Calendari fiscali          | Calendari fiscali per filtrare i report per |
| Contabilità generali                   | Contabilità generale utilizzabile per filtrare il report nella contabilità generale corrente |
| Codici budget              | Codici budget per filtrare i report per |
| Persone giuridiche            | Persone giuridiche utilizzabili per filtrare il report nella persona giuridica corrente |
