---
title: Stampa nelle applicazioni Finance and Operations
description: "In Microsoft Dynamics 365 for Finance and Operations, è possibile stampare i documenti mediante una stampante locale o un dispositivo connesso alla rete. L'articolo fornisce una panoramica su come i documenti vengono stampati."
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 30a418e6c49849369f0a0e3ffa28f31b9b88b7e7
ms.contentlocale: it-it
ms.lasthandoff: 04/13/2018

---

# <a name="printing-in-finance-and-operations-applications"></a>Stampa nelle applicazioni Finance and Operations

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 for Finance and Operations, è possibile stampare i documenti mediante una stampante locale o un dispositivo connesso alla rete. L'articolo fornisce una panoramica su come i documenti vengono stampati.

<a name="printing-overview"></a>Panoramica di stampa
-----------------

Microsoft Dynamics 365 for Finance and Operations fornisce servizi e applicazioni client integrati che rendono più semplice generare, memorizzare e distribuire i documenti di supporto all'attività aziendale. In Finance and Operations, è possibile stampare i documenti mediante una stampante locale o un dispositivo connesso alla rete. Inoltre, è possibile esportare le pagine e i report di Finance and Operations direttamente dal client, come file PDF o documenti di Microsoft Office. Infine, il carico di lavoro distribuito consente di stampare i documenti aziendali direttamente da un dispositivo mobile utilizzando le risorse di rete. Sebbene i requisiti di stampa possano variare, tutti i settori in genere devono creare copie cartacee dei documenti aziendali utilizzando Finance and Operations. La stampa di documenti su dispositivi di rete da applicazioni ospitate presenta una serie unica di sfide. Di seguito sono riportati alcuni esempi.

-   I driver di stampa potrebbero non essere disponibili sul dispositivo dell'utente.
-   Il dispositivo dell'utente potrebbe non essere connesso alla rete aziendale.

Utilizzando un host dedicato e seguendo alcuni semplici passaggi, gli amministratori di sistema possono configurare le distribuzioni in modo che gli utenti possano stampare direttamente da applicazioni aziendali su dispositivi di rete.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Stampa in scenari con applicazioni Finance and Operations

Nella tabella seguente vengono descritti i tre scenari di stampa principali nelle applicazioni di Finance and Operations.

| Scenario                        | Obiettivo                                                      | Soluzione                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 1. Stampa di elementi visualizzati        | Stampa quanto è attualmente visualizzato nel browser.             | Una versione "stampabile" della pagina Web viene generata per il browser.                                             |
| 2. Stampa interattiva         | Stampa un documento di precisione su un dispositivo connesso in locale. | È possibile esportare una versione PDF del report e scaricarlo nel browser.                                          |
| 3. Stampa su un dispositivo di rete | Invia un documento di precisione a una stampante del dominio.     | Un documento di precisione viene inviato a un'applicazione client che viene eseguita su un server ospitato nel dominio del cliente. |

Poiché la soluzione varia a seconda dello scenario, le applicazioni di Finance and Operations forniscono servizi e strumenti integrati per aiutare gli utenti a raggiungere i propri obiettivi:

-   **Scenario 1**: è supportato dal rendering del browser del client HTML5.
-   **Scenario 2**: utilizza le applicazioni client e i servizi Microsoft Office 365.
-   **Scenario 3**: richiede il supporto delle applicazioni client e dei servizi ospitati in Microsoft Azure.

Oltre alla piattaforma distribuita nella sottoscrizione di Azure, le applicazioni di Finance and Operations forniscono ai clienti un'applicazione integrata di Azure che consente di utilizzare più facilmente dispositivi ospitati nel dominio per stampare documenti.

## <a name="service-overview"></a>Panoramica del servizio
Mentre i documenti prodotti dalle applicazioni ospitate sono in attesa di essere stampati su un dispositivo connesso in rete, vengono memorizzati nell'archiviazione BLOB di Azure. L'[agente di distribuzione documenti](install-document-routing-agent.md) utilizza l'autenticazione Azure per stabilire un canale sicuro per i servizi Azure. **Sequenza esecuzione**

1.  Il report viene generato da Microsoft SQL Server Reporting Services (SSRS) e archiviato nell'archiviazione BLOB di Azure. Le impostazioni della stampante collegata vengono memorizzate insieme al documento.
2.  L'agente di distribuzione documenti esegue una query sulla coda del bus di servizio di Azure per individuare i lavori attivi.
3.  Il documento viene scaricato dall'agente di distribuzione documenti e inviato alla stampante di rete.

La soluzione basata su client consente ai clienti di gestire la scalabilità delle esigenze di stampa aziendali. I clienti con carichi di lavoro di stampa di volumi elevati possono installare molti agenti di distribuzione documenti per aumentare il numero di operazioni di stampa simultanee. Alcuni clienti invece richiedono pochissime installazioni dell'Agente di distribuzione documenti per gestire le esigenze di stampa previste.

### <a name="service-components-for-network-printing"></a>Componenti del servizio per la stampa in rete

Il seguente diagramma mostra i componenti di base che consentono di supportare le operazioni di stampa in rete. [![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Si noti che una singola stampante può essere registrata con più agenti di distribuzione documenti. Per risolvere le preferenze della stampante, il servizio in hosting utilizza il percorso di rete che identifica in modo univoco ogni stampante di rete. Di conseguenza, anche quando una stampante è registrata da più client, appare come una singola selezione nell'elenco delle stampanti disponibili nelle applicazioni di Finance and Operations.




