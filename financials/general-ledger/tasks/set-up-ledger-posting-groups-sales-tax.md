--- 
title: Impostare gruppi di registrazione contabile per l'IVA
description: L'IVA viene calcolata e registrato nei conti principali specificati in Gruppi registrazione contabile.
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0682afed4664e1491ed46e4e40f467015701711
ms.contentlocale: it-it
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Impostare gruppi di registrazione contabile per l'IVA

[!include[task guide banner](../../includes/task-guide-banner.md)]

L'IVA viene calcolata e registrato nei conti principali specificati in Gruppi registrazione contabile. I gruppi di registrazione contabile vengono collegati a ciascun codice IVA. È possibile impostare singoli gruppi di registrazione contabile per ciascun codice IVA, utilizzare un solo gruppo per tutti i codici IVA o assegnare più gruppi ai codici IVA. Questa registrazione utilizza la società dimostrativa DEMF. 

1. Andare a Imposta > Impostazioni > IVA > Gruppi registrazione contabile.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Gruppo registrazione contabile.
4. Nel campo Descrizione digitare un valore.
5. Nel campo IVA a debito selezionare il conto principale per l'IVA in uscita pagabile all'ufficio IVA.
    * L'IVA viene riscossa per conto dell'ufficio IVA quando si vendono beni e servizi soggetti a imposta.  
6. Nel campo IVA a credito selezionare il conto principale per l'IVA in entrata pagabile all'ufficio IVA.
    * I fornitori riscuotono l'IVA per conto dell'ufficio IVA quando si acquistano beni e servizi soggetti a imposta. Questo campo non è disponibile se è selezionata l'opzione Applica regole di tassazione IVA nella pagina Parametri di contabilità generale. L'IVA versata ai fornitori viene invece addebitata nello stesso conto utilizzato per gli acquisti.   
7. Nel campo Importo IVA intracomunitaria, selezionare il conto principale per la registrazione dell'IVA detraibile non richiesta o non dichiarata all'ufficio IVA dai fornitori come parte della GST/HST reverse charge UE.
    * L'opzione IVA intracomunitaria deve essere selezionata per il codice IVA nella fascia IVA utilizzata nella transazione.  Questo campo non è disponibile se è selezionata l'opzione Applica regole di tassazione IVA nella pagina Parametri di contabilità generale.   
8. Nel campo IVA intracomunitaria a debito selezionare il conto principale per la registrazione dell'IVA in entrata pagabile all'ufficio IVA.
    * L'opzione IVA intracomunitaria deve essere selezionata nel Codice IVA nella Fascia IVA per registrare l'IVA intracomunitaria. Se è selezionata l'opzione Applica regole di tassazione IVA in Parametri di contabilità generale, la contropartita viene registrata nel conto spese della transazione.   
9. Nel campo Conto di liquidazione, selezionare il conto principale in cui verrà registrato il saldo netto dei conti CoGe specificato nei campi VAT intracomunitaria a debito e IVA a credito.
    * Il saldo verrà creato dopo che è stato eseguito il processo di liquidazione e registrazione IVA.  Se l'ufficio IVA per il periodo di liquidazione è associato a un conto fornitore, il saldo viene registrato invece nel conto fornitore.   
10. Nel campo Sconto di cassa fornitore, selezionare il conto principale per la registrazione dello sconto di cassa per i codici IVA associati al gruppo di registrazione contabile.
    * È facoltativo e se non viene immesso alcun conto, verrà utilizzato il conto principale in Codici sconto di cassa. Può essere utile utilizzare conti diversi per gruppo di registrazione contabile se si utilizza l'opzione Storna IVA su sconto di cassa in Fasce IVA.  
11. Nel campo Sconto di cassa fornitore, selezionare il conto principale per la registrazione dello sconto di cassa per i codici IVA associati al gruppo di registrazione contabile.
    * È facoltativo e se non viene immesso alcun conto, verrà utilizzato il conto principale in Codici sconto di cassa. Può essere utile utilizzare conti diversi per gruppo di registrazione contabile se si utilizza l'opzione Storna IVA su sconto di cassa in Fasce IVA.  
12. Fare clic su Salva.

