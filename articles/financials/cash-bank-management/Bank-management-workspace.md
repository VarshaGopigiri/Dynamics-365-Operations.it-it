---
title: Area di lavoro gestione banche
description: "Vengono fornite le informazioni sull'area di lavoro gestione banche. In quest'area di lavoro vengono visualizzate le informazioni relative ai conti bancari della società e comprende una visualizzazione di riepilogo e una pagina di analisi. Nella visualizzazione di riepilogo vengono visualizzati i riquadri di riepilogo, le informazioni sul conto bancario, un grafico del saldo e informazioni correlate. La pagina dell'analisi dei dati utilizza le funzionalità di Microsoft Power BI per visualizzare le rappresentazioni correlate ai saldi del conto bancario."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 92a52646063c145d733b9d2960253004e8eab80a
ms.openlocfilehash: 3c38807e9ed3b2ced37ada35b72e388c125bd654
ms.contentlocale: it-it
ms.lasthandoff: 03/05/2018

---
# <a name="bank-management-workspace"></a>Area di lavoro gestione banche

[!include [banner](../includes/banner.md)]

Nell'area di lavoro **Gestione banche** vengono visualizzate le informazioni relative ai conti bancari della società. Questa area di lavoro include una visualizzazione **Riepilogo** e una pagina **Analisi**. Nella visualizzazione **Riepilogo** vengono visualizzati i riquadri di riepilogo, le informazioni sul conto bancario, un grafico del saldo e informazioni correlate. La pagina **Analisi** dei dati utilizza le funzionalità di Microsoft Power BI per visualizzare le rappresentazioni correlate ai saldi del conto bancario.

## <a name="summary-view"></a>Visualizzazione di riepilogo

### <a name="summary"></a>Riepilogo

Nei riquadri della sezione **Riepilogo** viene fornita una panoramica dei conti bancari e l'accesso rapido alle pagine usate più di frequente. Le informazioni di riconciliazione estratti conto sono specifiche della funzionalità avanzata di riconciliazione estratti conto. Vengono incluse solo le informazioni per i conti bancari con l'opzione **Riconciliazione estratti conto avanzata** impostata su **Sì** nella pagina **Conto bancario**. Nella sezione **Riepilogo** è possibile importare i file bancari elettronici per i conti bancari di tutte le persone giuridiche.

### <a name="bank-accounts"></a>Conti bancari

Ciascun conto bancario della persona giuridica è rappresentato da una scheda nella sezione **Conti bancari**. Viene visualizzato il saldo corrente ed è possibile eseguire il drill-down delle transazioni che costituiscono l'importo del saldo riepilogativo. Anche l'importo **Transazioni provvisorie** consente di eseguire il drill-down delle transazioni che costituiscono l'importo riepilogativo. Le transazioni provvisorie sono tutte le transazioni in sospeso che sono state registrate utilizzando la funzionalità di registrazione provvisoria ma che non sono state cancellate. L'importo **Saldo in sospeso** è il saldo corrente meno le transazioni provvisorie o in sospeso.

Nella scheda viene visualizzato anche la data dell'ultima riconciliazione del conto bancario. Queste informazioni vengono visualizzate solo se la riconciliazione degli estratti conto avanzata è attivata per il conto bancario.

### <a name="balance"></a>Stato patrimoniale

Nel grafico **Saldo** vengono visualizzati i dati storici del saldo del conto bancario selezionato nella sezione **Conti bancari** o un riepilogo dei dati storici del saldo per tutti i conti bancari della persona giuridica. Questi dati sono disponibili per diversi periodi: la settimana corrente, il mese corrente, l'anno corrente, gli ultimi cinque anni e tutti i periodi (lo storico completo del conto bancario). 

Se si visualizza il grafico **Saldo** per un singolo conto bancario, i dati storici dei saldi verranno visualizzati nella valuta del conto bancario. Se si visualizza il grafico per tutti i conti bancari della persona giuridica, i dati storici dei saldi verranno visualizzati nella valuta di contabilizzazione.

Le informazioni relative alla data dell'ultimo aggiornamento dei dati sono visualizzate nella parte superiore del grafico. È possibile aggiornare i dati secondo le necessità.

### <a name="related-information"></a>Informazioni correlate

Nella sezione **Informazioni correlate**, è possibile aprire la pagina **Giornale di registrazione generale** per completare i trasferimenti bancari. È inoltre possibile aprire rapidamente le pagine **Transazioni provvisorie** e **Transazioni bancarie**.

## <a name="analytics-view"></a>Visualizzazione Analisi

La pagina **Analisi** mostra le metriche importanti dei conti bancari della società corrente. Le visualizzazioni riportate di seguito sono disponibili nella pagina:

-   Saldo bancario totale nella valuta di sistema
-   Saldo per persona giuridica
-   Saldo effettivo odierno rispetto al saldo previsto nella valuta del conto bancario
-   Saldo per conto bancario
-   Saldo per valuta

È possibile visualizzare l'analisi dei dati bancari per tutte le società dall'area di lavoro **Panoramica situazione di cassa - tutte le società**.

