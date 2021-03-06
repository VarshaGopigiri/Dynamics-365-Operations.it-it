--- 
title: Completare l'impostazione di base di una rappresentazione generale prodotto rilasciata
description: Questa procedura mostra come completare la configurazione minima necessaria prima che la rappresentazione generale prodotto possa essere utilizzata nelle versioni DBA.
author: YuyuScheller
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 35617f5bec877fbe8a89d015eda16a66ee14d335
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Completare l'impostazione di base di una rappresentazione generale prodotto rilasciata

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questa procedura mostra come completare la configurazione minima necessaria prima che la rappresentazione generale prodotto possa essere utilizzata nelle versioni DBA.

Questa è la terza procedura di otto che illustra come sviluppare le combinazioni per la configurazione basata su dimensioni. La società di dati dimostrativi utilizzata per creare questa procedura è USMF.

1. Fare clic su Gestione informazioni sul prodotto > Prodotti > Prodotti rilasciati.
2. Nell'elenco trovare e selezionare il record desiderato.
    * Selezionare la rappresentazione generale prodotto che è stata rilasciata nella seconda procedura. La rappresentazione generale prodotto viene creata con la tecnologia di configurazione basata su dimensioni.  
3. Nel riquadro azioni fare clic su Prodotto.
4. Fare clic su gruppi di dimensioni per aprire la finestra di dialogo a discesa.
5. Nel campo Gruppo di dimensioni di immagazzinamento fare clic sul pulsante a discesa per aprire la ricerca.
6. Nell'elenco trovare e selezionare il record desiderato.
    * Il gruppo dimensione di immagazzinamento determina quali dimensioni di immagazzinamento vengono utilizzate per la transazione del prodotto. Selezionare Sito per questa procedura.  
7. Nell'elenco fare clic sul collegamento nella riga selezionata.
8. Nel campo Gruppo di dimensioni di tracciabilità fare clic sul pulsante a discesa per aprire la ricerca.
9. Nell'elenco trovare e selezionare il record desiderato.
    * Il gruppo dimensione di tracciabilità determina quali dimensioni di tracciabilità vengono utilizzate per la transazione del prodotto. Selezionare Nessuna per questa procedura.  
10. Nell'elenco fare clic sul collegamento nella riga selezionata.
11. Fare clic su OK.
12. Nell'elenco fare clic sul collegamento nella riga selezionata.
13. Fare clic su Modifica.
    * Aprire il modulo Dettagli prodotto rilasciato per continuare l'attività di configurazione.  
14. Nel campo Gruppo di modelli di articoli fare clic sul pulsante a discesa per aprire la ricerca.
15. Nell'elenco trovare e selezionare il record desiderato.
    * I gruppi di modelli di articoli contengono impostazioni che determinano la modalità in cui gli articoli vengono controllati e gestiti all'entrata e all'uscita. Determinano inoltre in che modo viene calcolato il consumo di articoli. Selezionare FIFO per questa procedura.  
16. Nell'elenco fare clic sul collegamento nella riga selezionata.
17. Espandere o comprimere la sezione Gestisci costi.
18. Nel campo Gruppo di articoli fare clic sul pulsante a discesa per aprire la ricerca.
19. Nell'elenco trovare e selezionare il record desiderato.
    * I gruppi di articoli vengono utilizzati per la gestione delle scorte mediante la divisione degli articoli di magazzino in gruppi. Selezionare CarAudio per questa procedura.  
20. Nell'elenco fare clic sul collegamento nella riga selezionata.
21. Nel riquadro azioni fare clic su Piano.
22. Fare clic su Impostazioni ordine predefinite.
23. Nel campo Tipo di ordine predefinito selezionare un'opzione.
    * Selezionare Produzione per specificare che l'opzione di rifornimento predefinita per la rappresentazione generale prodotto è di produrla.  
24. Chiudere la pagina.
25. Chiudere il modulo Dettagli prodotto rilasciato.


