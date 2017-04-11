---
title: Creare piani di retribuzione fissa
description: La retribuzione fissa fa riferimento allo stipendio lordo regolare o alle retribuzioni del dipendente. Questo articolo descrive i componenti che devono essere impostati per creare un piano di retribuzione fissa e iscrivere i dipendenti.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: bbf08a9620dbc8ad928fe40a3ae5e9b2a2fcb373
ms.lasthandoff: 03/31/2017


---

# <a name="create-fixed-compensation-plans"></a>Creare piani di retribuzione fissa

La retribuzione fissa fa riferimento allo stipendio lordo regolare o alle retribuzioni del dipendente. In questo argomento vengono descritti i componenti che devono essere impostate per poter creare un piano di retribuzione fissa e l'iscrizione dei dipendenti.

Gli importi di retribuzione fissa possono essere calcolati per i dipendenti in base a fattori quali prestazioni, regione e incrementi di budget. Microsoft Dynamics 365 per il supporto delle operazioni Passaggi, classi e tipi di banda.

## <a name="fixed-compensation-components"></a>Componenti di retribuzione fissa
### <a name="compensation-levels"></a>Livelli retributivi

È possibile utilizzare ** livelli retributivi ** per impostare la retribuzione per diversi processi, consentono di assicurarsi che i dipendenti che contengono i processi vengono pagati ragionevolmente. ** Livelli retributivi ** nella pagina, è possibile impostare i livelli retributivi necessari per ciascun passaggio, e sono grado di banda. Utilizzare i pulsanti **Su** e **Giù** per inserire i livelli nell'ordine corretto, in base al relativo tipo. Impostando i livelli retributivi su una mansione, è possibile garantire che tutti i dipendenti che detengono una posizione per tale mansione vengano retribuiti allo stesso livello.

### <a name="reference-points"></a>Punti di riferimento

I **punti di riferimento** sono le colonne nella griglia che definiscono gli intervalli di retribuzione per ciascun livello. Il livello retributivo corrisponde alla riga nella griglia. I punti di riferimento tipici di un piano di tipo al grado è un minimo, un punto intermedio e un valore massimo. I punti di riferimento ** impostazioni di punti di riferimento ** nella pagina.

### <a name="compensation-grids"></a>Griglie retributive

Dopo aver impostato i livelli e i punti di riferimento, è possibile combinarli per creare una **griglia di retribuzione**. Nella pagina **Griglie retributive**, definire le informazioni sulla griglia. Ad esempio, specificare lo scopo per il quale la griglia viene utilizzata, il tipo di piano con cui verrà utilizzata e le colonne o i punti di riferimento necessari nella griglia. Dopo aver completato l'immissione di tali informazioni, fare clic su **Struttura retributiva** per aggiungere livelli e importi alla griglia. 

**Suggerimento:** utilizzare la funzione **Modifiche di massa** sulla struttura retributiva per impostare gli importi iniziali, quindi l'incremento per percentuali o importi tra i livelli o i punti di riferimento.

### <a name="pay-frequencies"></a>Frequenze retribuzione

Le **Frequenze retribuzione** vengono utilizzate per definire la modalità in cui viene specificato lo stipendio o la retribuzione di un dipendente (ad esempio 10 EUR all'ora o 50.000 EUR all'anno) e la conversione tra le tariffe orarie, settimanali, mensili (12 mesi) e annuali. Ad esempio, una società che utilizza una settimana lavorativa di 38 ore per i relativi dipendenti retribuiti all'ora imposta una frequenza di retribuzione pari a una frequenza oraria di 1, settimanale di 38, mensile di 164,6666666667 e annuale di 1.976. Queste conversioni vengono utilizzate per calcolare le diverse tariffe retributive visualizzate nel record di retribuzione fissa del dipendente.

## <a name="fixed-compensation-plans"></a>Piani di retribuzione fissa
È possibile progettare il piano di retribuzione fissa per combinare tutti i componenti configurati. Per creare un piano di retribuzione fissa, aprire la pagina **Piani di retribuzione fissa**. In questa pagina è possibile immettere un nome e una descrizione del piano, selezionare il tipo di piano (scala, fascia o grado), selezionare la frequenza di retribuzione che verrà utilizzata per la tariffa retributiva del dipendente (importo orario, annuale e così via) e impostare alcune opzioni che controllano come viene elaborata l'elaborazione. 

L'impostazione **Tolleranza non compresa nell'intervallo** consente di specificare con quale rigidità si desidera assicurarsi che gli importi di retribuzione siano compresi tra il valore minimo e massimo. Una tolleranza di tipo **Rigido** richiede che la retribuzione rientri nell'intervallo definito per un livello specificato. Una tolleranza **Flessibile** avvisa quando l'importo di retribuzione non rientra nell'intervallo ma consente di continuare. Se la tolleranza è impostata su **Nessuno**, è possibile immettere qualsiasi importo di retribuzione per un dipendente senza ricevere messaggi di errore o di avviso. 

** Regola di assunzione ** l'impostazione consente di specificare se tutti i dipendenti devono ricevere lo stesso aumento, indipendentemente dalla data che sono stati Dipendente (** regola di assunzione ** = ** ** nessuno), ovvero se i dipendenti devono ricevere una percentuale del premio, in base alla durata sono stati assunti durante il ciclo (** regola di assunzione ** = ** la percentuale **). 

Una **matrice di utilizzo del range** è utile se si desidera ridurre il tempo necessario affinché i dipendenti raggiungano il punto intermedio del rispettivo range o aumentare il tempo necessario affinché i dipendenti raggiungano il punto di riferimento massimo nel range. Ad esempio, si desidera assegnare ai dipendenti che si trovano nella fascia del 25 percento di livello inferiore del rispettivo range il 110 percento del loro premio per raggiungimento obiettivi, ma si desidera assegnare ai dipendenti che si trovano nella fascia del 25 percento di livello superiore del rispettivo range solo l'80 percento del loro premio per raggiungimento obiettivi, in modo da impedire loro il raggiungimento del valore massimo altrettanto rapidamente. 

Dopo aver definito gli elementi di base del piano di retribuzione fissa, è possibile impostare la struttura retributiva per il piano. Fare clic su ** compensazione di attrezzaggio **. Un cursore di dialogo verrà aperto che restituisce tre opzioni:

-   Creare una nuova griglia di retribuzione selezionando un'impostazione di punti di riferimento e immettendo un nome per la griglia.
-   Creare una nuova griglia di retribuzione effettuando una copia di una griglia esistente che è possibile utilizzare come punto di partenza.
-   Utilizzare una griglia di retribuzione esistente che è già stata definita. Tutti i piani di retribuzione che utilizzano la stessa griglia ricevono aggiornamenti se la griglia viene modificata.

Una volta selezionata un'opzione, verrà visualizzata la pagina **Struttura retributiva** e sarà possibile apportare modifiche alla griglia di retribuzione nuova o esistente.

## <a name="fixed-compensation-enrollment"></a>Iscrizione a un piano di retribuzione fissa
### <a name="determine-who-is-eligible-for-the-plan"></a>Stabilire chi è idoneo per il piano

Il primo passaggio per l'iscrizione dei dipendenti a un piano di retribuzione fissa consiste nello stabilire chi è idoneo per la retribuzione definita nel piano. Finché non si determina l'idoneità, non sarà possibile assegnare il piano ai dipendenti. Per impostare l'idoneità, aprire ** regole di idoneità ** la pagina. In questo caso, si crea una nuova regola di idoneità per il piano di retribuzione e definire i criteri che un dipendente deve soddisfare per ottenere per un piano. È possibile limitare l'idoneità in base al reparto, al sindacato, al paese di retribuzione (località), alla mansione, alla funzione lavorativa, al tipo di mansione o al livello retributivo. I dipendenti possono essere iscritti a un piano di retribuzione solo se soddisfano tutte le condizioni impostate nella regola di idoneità. 

**Nota:** le regole di idoneità vengono utilizzate per determinare l'idoneità per i piani di retribuzione fissa e variabile. 

La regola di idoneità considera il valore di campi specifici nei record Mansione, Posizione e Dipendente per stabilire se un dipendente è idoneo per un piano di retribuzione.

-   Nella pagina **Mansione**, la regola di idoneità considera i seguenti campi:
    -   Il campo **Mansione**
    -   Nella scheda **Classificazione mansione**, i campi **Funzione** e **Tipo di mansione**
    -   Nella scheda **Retribuzione**, il campo **Livello**
-   Nella pagina **Posizioni**, la regola di idoneità considera i campi **Reparto** e **Paese di retribuzione**.

La regola di idoneità viene inoltre considerato sindacati associati al dipendente (su ** dipendenti ** pagine, ** ** lavoratore nella scheda, quindi ** informazioni personali ** &gt; ** sindacati **).

### <a name="define-fixed-compensation-actions"></a>Definire azioni relative alla retribuzione fissa

Le **Azioni retribuzione fissa** vengono utilizzate quando si impostano o si applicano modifiche alla retribuzione fissa di un dipendente. Le azioni retribuzione fissa consentono di immettere nomi descrittivi per i tipi di azioni che un responsabile retribuzione e benefit può eseguire. Tipi diversi di azioni dispongono di una logica speciale, in modo da poter essere utilizzati in situazioni specifiche. 

Ad esempio, se la retribuzione fissa viene impostata per un dipendente, è possibile utilizzare solo azioni con un tipo di **Assunzione/Riassunzione**. In questo caso, è consigliabile creare tre azioni diverse di tipo **Assunzione/Riassunzione** e nominarle **Assunzione**, **Riassunzione** e **Trasferimento**. Si dispone così di una spiegazione più descrittiva del motivo per cui la retribuzione fissa è stata assegnata a un dipendente o è stata modificata.

### <a name="enroll-the-employee"></a>Iscrivere il dipendente al piano

È ora possibile assegnare un piano di retribuzione fissa a un dipendente. Aprire la pagina **Dipendenti**, quindi selezionare il dipendente per iscriverlo al piano di retribuzione. Nel riquadro azioni, fare clic su retribuzione ** ** &gt; ** piano di retribuzione fissa **. È ora possibile creare una nuova azione di retribuzione fissa per tale dipendente. 

**Nota:** il campo del piano di retribuzione indica solo i piani per i quali un dipendente è idoneo in base alle regole di idoneità impostate per ciascun piano. Se non si specifica alcuna regola di idoneità per un piano, nessun dipendente sarà idoneo per tale piano. 

Il sistema verifica che l'importo di retribuzione specificato per un piano di retribuzione del tipo di grado o fascia rientri nei punti di riferimento minimo e massimo per il livello retributivo specificato sulla mansione del dipendente. Se l'importo di retribuzione non rientra nell'intervallo consentito, viene visualizzato un messaggio di errore o di avviso, a seconda del livello di tolleranza impostato nel piano di retribuzione fissa.

<a name="see-also"></a>Vedere anche
--------

[Piani di retribuzione](compensation-plans.md)

