---
title: Impostare l'analisi RFM
description: In questo argomento viene illustrato come impostare un'analisi Recency, Frequency and Monetary (RFM) dei clienti.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1d5deb781d938dd31326826049372f705bdf6938
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2017



---

# <a name="set-up-rfm-analysis"></a>Impostare l'analisi RFM

[!include[banner](includes/banner.md)]


In questo argomento viene illustrato come impostare un'analisi Recency, Frequency and Monetary (RFM) dei clienti.

L'analisi di recency, di frequenza e monetaria (RFM) è uno strumento di marketing che l'organizzazione può utilizzare per valutare i dati generati dagli acquisti dei clienti. Dopo aver impostato l'analisi RFM, ai clienti viene assegnato un punteggio calcolato RFM mentre eseguono gli acquisti. Il punteggio RFM può essere una valutazione a tre cifre o un numero di aggregazione a seconda del modo in cui l'organizzazione ha configurato l'analisi RFM. Se l'organizzazione utilizza una valutazione a tre cifre per il punteggio, la prima cifra corrisponde alla valutazione di recency del cliente (quando il cliente ha effettuato l'ultimo acquisto presso l'organizzazione). La seconda cifra è la valutazione della frequenza del cliente (con quale frequenza il cliente effettua gli acquisti presso l'organizzazione). La terza cifra indica la valutazione monetaria del cliente (quanto spende il cliente quando effettua acquisti presso l'organizzazione). Si supponga, ad esempio, che l'organizzazione abbia impostato le valutazioni su una scala da 1 a 5, dove 5 è la valutazione più alta. In questo caso, la valutazione di 535 di un cliente fornisce le seguenti informazioni sul cliente:

-   **Valutazione di recency di 5**: il cliente ha effettuato un acquisto recentemente.
-   **Valutazione di frequenza di 3**: il cliente acquista prodotti dall'organizzazione abbastanza spesso.
-   **Valutazione monetaria di 5**: quando il cliente effettua un acquisto, spende una cifra significativa.

Se l'organizzazione utilizza un numero di aggregazione per il punteggio, le singole valutazioni vengono sommate insieme. Se consideriamo lo stesso esempio, il cliente ha una valutazione pari a 13 (5 + 3 + 5).



