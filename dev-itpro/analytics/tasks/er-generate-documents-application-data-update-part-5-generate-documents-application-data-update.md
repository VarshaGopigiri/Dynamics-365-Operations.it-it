--- 
title: Generare i documenti con l'aggiornamento dei dati dell'applicazione per la creazione di report elettronici (ER)
description: "Per completare i passaggi di questa procedura, è necessario completare la procedura \"ER Generare documenti con l'aggiornamento dei dati dell'applicazione (Parte 4: Modificare il formato)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 2c562c397ad93b1bbb919b69439f8eea1a9d2644
ms.contentlocale: it-it
ms.lasthandoff: 07/27/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Generare i documenti con l'aggiornamento dei dati dell'applicazione per la creazione di report elettronici (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Per completare i passaggi di questa procedura, è necessario completare la procedura "ER Generare documenti con l'aggiornamento dei dati dell'applicazione (Parte 4: Modificare il formato)".



I passaggi di questa procedura descrivono come progettare le configurazioni ER per generare un documento elettronico e aggiornare i dati dell'applicazione. In questa procedura si esegue la configurazione dei formati ER per generare la dichiarazione Intrastat e aggiornare i dati dell'applicazione per archiviare i dettagli del processo di dichiarazione.



Questa procedura viene creata per utenti con il ruolo di amministratore di sistema o di sviluppatore di report elettronici. Tali passaggi possono essere completati mediante il set di dati DEMF. Prima di iniziare, assicurarsi che il contesto del paese per la società DEMF sia BEL (Belgio).


## <a name="set-up-foreign-trade-parameters"></a>Imposta parametri per il commercio estero
1. Passare a Imposta > Impostazione > Commercio estero > Parametri per il commercio estero.
2. Fare clic sulla scheda Sequenze numeriche.
    * Archiviando i dettagli del processo di dichiarazione Intrastat, dobbiamo identificare i record di ogni archivio creato. A tale scopo è necessario configurare una sequenza numerica speciale.  
3. Selezionare il riferimento 'ID archivio Intrastat'.
4. Nel campo Codice sequenza numerica selezionare un valore.
    * Nel campo 'Codice sequenza numerica' immettere o selezionare il valore 'Fore_2'.  
5. Risolvere le modifiche al codice della sequenza numerica.
6. Fare clic su Salva.
7. Chiudere la pagina.

## <a name="run-modified-er-format"></a>Eseguire il formato ER modificato
1. Passare a Amministrazione organizzazione > Reporting elettronico > Configurazioni.
2. Nella struttura espandere "Intrastat (model)".
3. Nella struttura selezionare "Intrastat (model)\Intrastat (format)".
4. Fare clic su Esegui.
5. Nel campo per immettere il nome del file digitare "intrastat2.xml".
    * intrastat2.xml  
6. Fare clic su OK.

## <a name="review-er-format-executions-results"></a>Esaminare i risultati dell'esecuzione del formato ER
    * Esaminare il file XML generato.  
1. Chiudere la pagina.
2. Passare a Imposta > Dichiarazioni > Commercio estero > Intrastat.
    * Aprire il modulo contenente le transazioni Intrastat incluse nel documento elettronico generato.  
3. Fare clic su archivio Intrastat.
    * Poiché il formato ER eseguito contiene ora impostazioni per l'aggiornamento dei dati dell'applicazione, i dettagli della dichiarazione Intrastat completata sono stati archiviati. In questo modulo, è possibile visualizzare il record di intestazione dell'archivio creato.  
4. Fare clic su Dettagli.
    * In questo modulo, è possibile visualizzare i dettagli dell'archivio creato.  
5. Chiudere la pagina.
6. Chiudere la pagina.
7. Chiudere la pagina.

