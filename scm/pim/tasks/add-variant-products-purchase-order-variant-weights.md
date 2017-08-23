--- 
title: Aggiungere prodotti varianti agli ordini fornitore tramite pesi varianti
description: In questa procedura vengono descritti i passaggi per utilizzare i pesi varianti per popolare automaticamente le righe ordine fornitore per ogni variante di un prodotto.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 410b3a88b3decb31ed6ce9373f14a11bf354acce
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Aggiungere prodotti varianti agli ordini fornitore tramite pesi varianti

[!include[task guide banner](../../includes/task-guide-banner.md)]

In questa procedura vengono descritti i passaggi per utilizzare i pesi varianti per popolare automaticamente le righe ordine fornitore per ogni variante di un prodotto. Quando si seleziona la quantità del prodotto che si desidera acquistare, le righe ordine fornitore vengono create per tutte le varianti del prodotto con le quantità suggerite in base ai pesi configurati nelle varianti prodotto. Questa procedura non include i passaggi per configurare i valori di peso nelle dimensioni prodotto e nelle varianti prodotto. Questa procedura utilizza i dati dimostrativi della società USRT.

1. Fare clic su Contabilità fornitori > Ordini fornitore > Tutti gli ordini fornitore.
2. Fare clic su Nuovo.
3. Nel campo Conto fornitore fare clic sul pulsante a discesa per aprire la ricerca.
4. Nell'elenco fare clic sul collegamento nella riga selezionata.
5. Attivare/disattivare l'espansione della sezione Generale.
6. Nel campo Sito fare clic sul pulsante a discesa per aprire la ricerca.
7. Nell'elenco fare clic sul collegamento nella riga selezionata.
8. Nel campo Magazzino fare clic sul pulsante a discesa per aprire la ricerca.
9. Nell'elenco trovare e selezionare il record desiderato.
10. Nell'elenco fare clic sul collegamento nella riga selezionata.
11. Fare clic su OK.
12. Attivare/disattivare l'espansione della sezione Dettagli riga.
13. Fare clic sulla scheda Varianti.
14. Fare clic su Aggiungi riga.
15. Nell'elenco contrassegnare la riga selezionata.
16. Nel campo Numero articolo digitare '0140'.
17. Impostare la quantità su "1000".
18. Fare clic su Salva.

