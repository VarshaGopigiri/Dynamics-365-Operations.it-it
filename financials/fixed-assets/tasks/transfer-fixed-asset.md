--- 
title: Trasferire un cespite
description: "Questa guida attività trasferirà le informazioni finanziarie per un libro cespiti da un set di dimensioni finanziarie in un nuovo set di dimensioni finanziarie."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ebde1e8bd8a87b44dd77b9050d05d6c2f4774ef2
ms.contentlocale: it-it
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-a-fixed-asset"></a>Trasferire un cespite

[!include[task guide banner](../../includes/task-guide-banner.md)]

Questa guida attività trasferirà le informazioni finanziarie per un libro cespiti da un set di dimensioni finanziarie in un nuovo set di dimensioni finanziarie.  Utilizza il ruolo Ragioniere e i dati dimostrativi per la persona giuridica USMF.

1. Passare a Cespiti > Cespiti > Cespiti.
2. Nell'elenco, individuare e selezionare il cespite da trasferire.
3. Nel riquadro azioni fare clic su Cespite.
4. Fare clic su Trasferisci cespiti.
5. Nel campo Data di trasferimento immettere una data.
6. Immettere i commenti per descrivere il trasferimento.
    * In questo elenco vengono visualizzati tutti i libri per il cespite.  
7. Contrassegnare i libri da trasferire in un nuovo set di dimensioni finanziarie.
    * In questo elenco vengono visualizzati i valori di dimensione finanziaria esistenti per il libro selezionato.  
    * Selezionare la dimensione finanziaria da aggiornare per il libro cespiti selezionato.  
8. Nel campo Dimensione finanziaria fare clic sul pulsante a discesa per aprire la ricerca.
    * Impostare altri valori di dimensione finanziaria in base alle esigenze.  
    * Tutti i valori di dimensione finanziaria vengono modificati quando avviene un trasferimento, sia che il valore sia stato immesso o lasciato vuoto. Ad esempio, se è stato immesso un valore per il BusinessUnit e sono stati lasciati vuoti dimensioni finanziarie Reparto e CostCenter. Se la struttura dei conti consente valori vuoti per CostCenter e Reparto, il trasferimento determinerà che ciascun modello di valore abbia il nuovo valore per BusinessUnit e un valore vuoto per CostCenter e Reparto.  
9. Fare clic su Aggiorna.
    * Si ha l'opportunità di visualizzare l'anteprima delle modifiche prima di finalizzare il trasferimento.  
    * Esaminare i risultati prima di trasferire i libri cespiti.  
10. Fare clic su Trasferisci.

