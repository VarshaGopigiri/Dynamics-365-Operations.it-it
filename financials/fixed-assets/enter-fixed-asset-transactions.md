---
title: Opzioni di transazione cespiti
description: Questo articolo descrive i metodi diversi disponibili per creare le transazioni cespiti.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 16e501f5f49f75b643685059a093d5c538e1f55d
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-transaction-options"></a>Opzioni di transazione cespiti

Questo articolo descrive i metodi diversi disponibili per creare le transazioni cespiti.

È possibile impostare i cespiti in modo da integrarli con la contabilità fornitori, la contabilità clienti, l'approvvigionamento e la contabilità generale. È inoltre possibile trasferire gli articoli in Gestione articoli ai cespiti se si desidera utilizzare gli articoli internamente.

## <a name="accounts-payable"></a>Contabilità fornitori
È possibile immettere le transazioni cespiti nella pagina Giustificativo giornale di registrazione. È possibile aprire questa pagina dalla pagina Giornale di registrazione fatture. È inoltre possibile aprire la pagina Giornale di registrazione fatture dalla pagina Giornale di approvazione fatture. Nel campo Tipo di conto di contropartita selezionare Cespiti. Quindi, nel campo Conto di contropartita selezionare un numero cespiti. Nella scheda Cespiti immettere i valori nei campi Tipo di transazione e Libro.

## <a name="accounts-receivable"></a>Contabilità clienti
È possibile immettere le transazioni cespiti nella pagina della fattura a testo libero.  Nella pagina della fattura a testo libero, nella griglia delle righe fattura, selezionare una voce. Fare clic sulla scheda dettaglio Dettagli riga. Immettere il numero cespite e il libro per la transazione di dismissione. Nelle fatture a testo libero il tipo di transazione cespiti è sempre Vendita di dismissione.

## <a name="procurement-and-sourcing"></a>Approvvigionamento
È possibile immettere le transazioni cespiti nella pagina Ordine acquisto. Immettere le informazioni necessarie per creare un ordine fornitore, quindi fare clic su OK. Nella pagina Ordine fornitore, fare clic sulla Scheda dettaglio Dettagli riga. Quindi, nella scheda Cespiti, immettere le informazioni sui cespiti. 

Per registrare una transazione di acquisizione di un cespite esistente, specificare il numero cespite, il libro e il tipo di transazione. Il cespite non può essere registrato se una di queste informazioni manca. Per registrare una transazione di acquisizione per un nuovo cespite, selezionare l'opzione Nuovo cespite?, quindi selezionare il gruppo di cespiti a cui assegnare il nuovo cespite. Se tuttavia l'articolo appartiene a un gruppo di modelli inventariali in cui viene utilizzato un modello inventariale Costo standard, non sarà disponibile alcun campo relativo a cespiti per una riga. Inoltre, le opzioni definite nella pagina Parametri cespiti determinano se è possibile registrare transazioni di acquisizione dai moduli di acquisto. 

L'utilizzo del giornale di registrazione Ordine fornitore o Scorte a cespiti per l'acquisizione dei cespiti influisce sul valore di magazzino..

## <a name="general-ledger"></a>Contabilità generale
Nella pagina Giornale di registrazione generale può essere registrato qualsiasi tipo di transazione cespiti. È inoltre possibile utilizzare i giornali di registrazione in Cespiti per registrare le transazioni cespiti.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Opzioni per l'immissione di tipi di transazioni cespiti


| Tipo di transazione                    | Modulo                   | Opzioni                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Acquisizione, Rettifica acquisizione | Cespiti             | Cespiti, Scorte a cespiti   |
|                                     | Contabilità generale           | Giornale di registrazione generale                           |
|                                     | Contabilità fornitori         | Giornale di registrazione fatture, Giornale di approvazione fatture |
|                                     | Approvvigionamento | Ordine acquisto                            |
| Ammortamento                        | Cespiti             | Cespiti                              |
|                                     | Contabilità generale           | Giornale di registrazione generale                           |
| Gestione dismissione                            | Cespiti             | Cespiti                              |
| ** **                               | Contabilità generale           | Giornale di registrazione generale                           |
| ** **                               | Contabilità clienti      | Fattura a testo libero                         |



Per ulteriori informazioni, vedere [] integrazione cespiti (fixed-asset-integration.md).

