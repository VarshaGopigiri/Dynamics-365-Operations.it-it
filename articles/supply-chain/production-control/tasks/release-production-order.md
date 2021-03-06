---
title: Rilasciare un ordine di produzione
description: Questa procedura indica come rilasciare un ordine di produzione.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 6e628d8564c093c5d75fffe268b2107262d508c3
ms.contentlocale: it-it
ms.lasthandoff: 02/06/2018

---
# <a name="release-a-production-order"></a>Rilasciare un ordine di produzione

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questa procedura indica come rilasciare un ordine di produzione. La società di dati dimostrativi utilizzata per creare questa procedura è USMF. Si tratta della quarta procedura su sette che spiega il ciclo di vita dell'ordine di produzione.

1. Andare a Controllo produzione > Ordini di produzione > Tutti gli ordini di produzione.
    * Nella griglia selezionare un ordine di produzione con lo stato Programmato.  
2. Nel riquadro azioni fare clic su Ordine di produzione.
3. Fare clic su Rilascia.
    * In questa pagina, è possibile confermare il rilascio dell'intervallo selezionato di ordini di produzione. Fare clic su Seleziona se si desidera aggiungere ordini.  
    * Il passaggio di rilascio indica quando l'ordine di produzione viene rilasciato allo shop floor di produzione in modo che gli operatori dello shop floor possano indicare lo stato di avanzamento nei processi di produzione. I documenti di produzione che contengono le informazioni rilevanti sull'elaborazione dei processi possono essere emessi. Il lavoro del magazzino per il prelievo delle materie prime viene generato per gli articoli impostati per il processo di magazzino.  
4. Fare clic sulla scheda Generale.
    * Selezionare i report di produzione da stampare. Il report della scheda processi stampa una pagina per ciascun processo programmato e richiede che l'ordine di produzione venga programmato a livello di processo. Il report contiene informazioni sull'ora di inizio e di fine programmata, la quantità da produrre e la risorsa che elabora il processo. Il report del processo del ciclo di lavorazione raccoglie le stesse informazioni nella stessa pagina, ma non stampa una pagina per ciascun processo. Nel report Scheda del ciclo di lavorazione vengono visualizzate solo le operazioni ma non i processi. Di conseguenza, il report non richiede la programmazione dei processi, ma può essere utilizzato quando gli ordini di produzione vengono programmati a livello di operazione.  
5. Fare clic sulla casella di controllo Stampa scheda ciclo di lav.
6. Fare clic su OK.
7. Chiudere la pagina.

