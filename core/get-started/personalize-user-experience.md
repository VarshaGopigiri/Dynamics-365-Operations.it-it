---
title: Personalizzare l&quot;esperienza utente
description: In questo articolo viene illustrato come personalizzare Microsoft Dynamics 365 for Operations.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 689efef6ffa10bbee30cd734f3f09ba20957834d
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2017


---

# <a name="personalize-the-user-experience"></a>Personalizzare l'esperienza utente

[!include[banner](../includes/banner.md)]


In questo articolo viene illustrato come personalizzare Microsoft Dynamics 365 for Operations.

Sono disponibili numerosi tipi di personalizzazioni in Microsoft Dynamics 365 for Operations. Alcune personalizzazioni vengono effettuate tramite la selezione da un elenco di opzioni in una pagina di configurazione. Alcune personalizzazioni sono implicite, ad esempio, Dynamics 365 for Operations tiene traccia della larghezza delle colonne delle griglie se modificate e dello stato espanso/compresso delle schede dettaglio. Altre personalizzazioni sono esplicite. Per le personalizzazioni esplicite, l'utente utilizza una modalità interattiva di personalizzazione e può modificare l'aspetto di una pagina direttamente gestendo il modo in cui gli elementi vengono visualizzati o si comportano nella pagina. 

Tutte le personalizzazioni, di qualsiasi tipo, che un utente applica in Dynamics 365 for Operations sono valide solo per tale utente, indipendentemente dalla società con cui l'utente interagisce. Le modifiche che un utente apporta a una pagina non influiscono su altri utenti nel sistema.

## <a name="systemwide-options-for-the-current-user"></a>Opzioni a livello di sistema per l'utente corrente
Nella barra di spostamento individuare l'icona dell'ingranaggio che corrisponde al pulsante di menu **Impostazioni**. Aprendo il menu **Impostazioni** si ha a disposizione una serie di opzioni. Selezionare **Opzioni** per visualizzare la pagina **Opzioni** dell'utente. In questa pagina solo disponibili quattro schede di opzione: **Visuale**, **Preferenze**, **Conto** e **Flusso di lavoro**.

-   **Visuale:**utilizzare questa opzione per scegliere un tema colori e le dimensioni predefinite per gli elementi delle pagine.
-   **Preferenze:** questa opzione consente di selezionare le impostazioni predefinite per ogni avvio di Dynamics 365 for Operations, inclusa la società, la pagina iniziale e la modalità di visualizzazione/modifica predefinita (che determina se una pagina viene bloccata per la visualizzazione o aperta per la modifica ogni volta che la si apre). Sono inoltre disponibili opzioni per lingua, fuso orario e data, ora e opzioni di formattazione per i numeri. Infine la pagina contiene una serie di preferenze che variano in base alla versione del prodotto.
-   **Conto:**utilizzare per immettere il proprio ID utente e altre opzioni correlate.
-   **Flusso di lavoro:**selezionare le opzioni relative al flusso di lavoro.

## <a name="implicit-personalizations"></a>Personalizzazioni implicite
Le personalizzazioni implicite sono personalizzazioni applicate semplicemente interagendo con alcuni controlli che richiamano il relativo stato visibile corrente. 

**Colonne della griglia**: è possibile regolare la larghezza di una colonna in un elenco selezionando la barra di ridimensionamento a sinistra o a destra dell'intestazione di colonna e facendola scorrere verso destra o verso sinistra fino a raggiungere la larghezza desiderata. Dynamics 365 for Operations memorizzerà la larghezza impostata dall'utente e applicherà alla colonna la stessa larghezza ogni volta che si apre la pagina con tale elenco. 

**Schede dettaglio**: alcune pagine sono dotate di aree espandibili note come schede dettaglio. Dynamics 365 for Operations memorizza le schede dettaglio che l'utente ha espanso e quelle che ha compresso. Ogni volta che l'utente torna alla pagina, verranno espanse o compresse le stesse schede dettaglio, in base all'ultima volta che la pagina è stata utilizzata. In questo articolo, spiegheremo come modificare l'ordine delle sezioni della scheda dettaglio. In alcuni casi, comprimere una scheda dettaglio può migliorare le prestazioni poiché Dynamics 365 for Operations non dovrà recuperare le informazioni relative a tale scheda dettaglio finché questa non viene espansa. 

**Riquadri dettaglio**: alcune pagine includono una sezione chiamata riquadro dettaglio. Questo riquadro contiene informazioni di sola lettura correlate all'argomento corrente della pagina. Ciascuna sezione del riquadro dettaglio è chiamata casella Dettaglio. È possibile espandere o comprimere un riquadro dettaglio e Dynamics 365 for Operations memorizzerà le preferenze. In alcuni casi, comprimere un riquadro dettaglio può migliorare le prestazioni poiché Dynamics 365 for Operations non dovrà recuperare le informazioni relative a tale riquadro dettaglio finché questo non viene espanso.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Personalizzazioni esplicite utilizzando la barra degli strumenti di personalizzazione
Ogni persona e società ha un'opinione diversa su quali dati sono più importanti o su quali dati non sono necessari per il modo in cui si gestiscono le attività. La possibilità di personalizzare il modo in cui interagire con i dati, ordinare o perfino nascondere le informazioni è la chiave essenziale per rendere Dynamics 365 for Operations un'esperienza personalizzata e produttiva. 

Le personalizzazioni esplicite sono quelle che l'utente esegue esplicitamente con l'intento di modificare l'aspetto o il comportamento di un elemento o di una pagina, scegliendo un menu di personalizzazione. La modalità di base per applicare una personalizzazione esplicita consiste nel fare clic con il pulsante destro del mouse su un elemento e selezionare l'opzione **Personalizza**. Tenere presente che non tutti gli elementi nella pagina possono essere personalizzati. Quando si seleziona questo metodo di personalizzazione, verrà visualizzata la finestra delle proprietà dell'elemento. 

[![Personalizzazione delle proprietà di un elemento](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Personalizzare un elemento della pagina in questo modo per modificare semplicemente l'etichetta dell'elemento, nascondere l'elemento in modo che non sia mostrato nella pagina (questo non modifica alcun dato, semplicemente non vengono visualizzate le informazioni), includere informazioni nella sezione riepilogo della scheda dettaglio (se l'elemento si trova in una scheda dettaglio), ignorare il campo durante la tabulazione o fare in modo che non sia possibile modificare i dati contrassegnandoli come "Non modificare". 

Se si desidera spostare o nascondere gli elementi o più apportare modifiche, è possibile utilizzare la barra degli strumenti di personalizzazione, disponibile nella finestra Proprietà degli elementi scegliendo **Personalizza modulo**. La barra degli strumenti di personalizzazione è inoltre disponibile nel riquadro azioni del modulo, nel gruppo Personalizza della scheda **Opzioni**. Selezionare **Personalizza modulo** per visualizzare la barra degli strumenti di personalizzazione. 

[![Barra degli strumenti di personalizzazione](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

La barra degli strumenti di personalizzazione include una serie di azioni di personalizzazione. Selezionare lo strumento **Seleziona** se si desidera selezionare e modificare le proprietà di molti elementi, uno alla volta. Fare clic sullo strumento Seleziona e quindi sull'elemento per cui si desidera modificare le proprietà. Quando si seleziona un elemento, la finestra delle proprietà dell'elemento si apre ed è possibile modificare qualsiasi proprietà di tale elemento. È possibile ripetere il processo per altri elementi del modulo personalizzabili. In alcuni casi, selezionando un elemento si noterà che alcune proprietà non sono modificabili. Ciò significa che in base alla modalità corrente di utilizzo dell'elemento, Dynamics 365 for Operations non consente la modifica delle proprietà. Ad esempio, non è possibile nascondere un campo obbligatorio. 

Selezionare lo strumento **Sposta** se si desidera selezionare e spostare un elemento in un punto diverso all'interno del gruppo corrente di elementi. (Non è possibile spostare un elemento al di fuori del gruppo padre). Fare clic sullo strumento Sposta e quindi sull'elemento per cui si desidera spostare. Quando si fa clic sull'elemento che si desidera spostare, Dynamics 365 for Operations esegue l'analisi del modulo per comprendere se elemento può essere spostato e crea una serie di "aree di rilascio" indicate da una riga colorata in grassetto accanto all'area in cui l'elemento può essere rilasciato quando lo si trascina all'interno del gruppo corrente. 

Selezionare lo strumento **Nascondi** per selezionare e nascondere un elemento. Per nascondere un elemento, selezionare semplicemente lo strumento Nascondi e fare clic sull'elemento da nascondere. Quando si sceglie lo strumento Nascondi, tutti gli articoli attualmente nascosti vengono resi visibili e visualizzati in un contenitore ombreggiato in modo che sia possibile scegliere l'elemento da scoprire. Selezionare lo strumento Seleziona per visualizzare come apparirà la pagina con gli elementi selezionati nascosti. Selezionare lo strumento **Riepilogo** se si desidera che un campo numerico o un campo stringa venga visualizzato nell'area di riepilogo della scheda dettaglio. Lo strumento Riepilogo viene applicato solo ai campi che sono contenuti in una sezione della scheda dettaglio. Quando si sceglie lo strumento Riepilogo, Dynamics 365 for Operations mostra tutti i campi che sono stati selezionati come campi riepilogativi evidenziandoli in un contenitore ombreggiato. È possibile aggiungere e rimuovere in modo interattivo i campi da un riepilogo di una scheda dettaglio facendo clic sul campo. 

Scegliere lo strumento **Ignora** per rimuovere un elemento dalla sequenza di tabulazione della tastiera nella pagina. Quando si sceglie lo strumento Ignora, tutti gli elementi attualmente ignorati verranno visualizzati in un contenitore ombreggiato in modo da poterli scegliere di nuovo per includerli nuovamente nella sequenza di tabulazione selezionando un elemento in precedenza ignorato. 

Selezionare lo strumento **Modifica** se si desidera contrassegnare un articolo come modificabile o non modificabile. Quando si sceglie lo strumento Modifica, tutti gli articoli attualmente non modificabili vengono visualizzati in un contenitore ombreggiato in modo che sia possibile scegliere gli elementi da rendere modificabili. Nota: alcuni campi sono obbligatori e non possono essere resi non modificabili. Questi campi verranno visualizzati con un'icona di lucchetto accanto ad essi. 

Selezionare lo strumento **Aggiungi** per aggiungere un campo nella pagina. Con lo strumento Aggiungere, non è possibile creare un nuovo campo, ma è possibile aggiungere i campi che fanno parte della definizione della pagina corrente, ma non visualizzati nella pagina. Quando si sceglie lo strumento Aggiungi, innanzitutto è necessario selezionare il gruppo o l'area in cui aggiungere un campo. Viene visualizzata una finestra di dialogo con l'elenco dei campi correlati nella sezione selezionata. Nella finestra di dialogo è possibile selezionare uno o più campi da aggiungere e fare clic su Inserisci. Se in seguito si desidera rimuovere un campo in precedenza aggiunto, ripetere il processo, semplicemente deselezionando il campo in precedenza aggiunto. 

Scegliere il pulsante **Gestisci** per visualizzare un elenco di opzioni di gestione correlate a tutte le personalizzazioni per la pagina corrente. 

Scegliere **Cancella** per reimpostare la pagina con le impostazioni predefinite. Tutte le personalizzazioni della pagina corrente saranno cancellate. Non esiste alcuna azione di annullamento, accertarsi quindi di reimpostare la pagina solo se sicuri di questa scelta. 

Scegliere **Importa** per utilizzare una personalizzazione salvata in un file di personalizzazione che l'utente o altre persone hanno precedentemente creato per la pagina. L'importazione di una personalizzazione cancellerà tutte le personalizzazioni eseguite nell'intera pagina e verranno invece utilizzate le personalizzazioni del file selezionato. Se si desidera salvare o condividere una personalizzazione, selezionare l'opzione **Esporta** per salvare le personalizzazioni in un file. 

Scegliere il pulsante **Chiudi** per chiudere la barra degli strumenti e ripristinare nella pagina lo stato interattivo precedente. 

Con la barra degli strumenti di personalizzazione, il salvataggio è implicito. Le personalizzazioni diventano effettive immediatamente non appena apportate e non è necessario di fare clic sul pulsante **Salva**. In alcuni casi, viene visualizzata un'icona a forma di lucchetto accanto a un elemento quando si seleziona uno strumento. Ciò significa che, per il corretto funzionamento della pagina, non è possibile modificare le proprietà correlate allo strumento selezionato. Quando la barra degli strumenti di personalizzazione è aperta, la pagina diventa non-interattiva. Non è possibile immettere i dati o espandere o comprimere le sezioni.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Personalizzazione esplicita: aggiunta di un riquadro o un elenco a un'area di lavoro
Alcune pagine con elenchi includono una funzionalità di personalizzazione aggiuntiva disponibile all'interno del riquadro azioni, nel gruppo di personalizzare della scheda Opzioni. Selezionare **Aggiungi ad area di lavoro** per aprire l'elenco a discesa che consente di visualizzare le informazioni nell'elenco corrente (filtrato e ordinato o predefinito) in un'area di lavoro come un elenco o un riquadro riepilogativo (che possono essere utilizzati per visualizzare il numero di elementi nell'elenco). 

[![Aggiungi ad area di lavoro](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Per aggiungere un elenco a un'area di lavoro, prima ordinare o filtrare l'elenco con le informazioni che si desidera visualizzare nell'area di lavoro, quindi selezionare la finestra di dialogo Aggiungi ad area di lavoro. Selezionare quindi l'area di lavoro desiderata e selezionare **Elenco** dall'elenco a discesa Presentazione. Quando si seleziona **Elenco** si apre una finestra di dialogo per consentire di scegliere le colonne da visualizzare nell'elenco e l'etichetta dell'elenco che verrà visualizzato nell'area di lavoro. 

Per aggiungere un riquadro a un'area di lavoro, filtrare prima l'elenco per rappresentare i dati che si desidera riepilogare (o a cui avere accesso rapido). Quindi aprire la finestra di dialogo a discesa Aggiungi ad area di lavoro. Selezionare quindi l'area di lavoro desiderata e selezionare **Riquadro** dall'elenco a discesa Presentazione. Quando si seleziona **Sezione**, viene visualizzata una finestra di dialogo per fornire un'etichetta per il riquadro e decidere se riquadro mostrerà un conteggio. Una volta posizionato in un'area di lavoro, il riquadro permetterà di aprire la pagina corrente dell'area di lavoro e mostrare l'elenco di informazioni correlate al riquadro. 

Quando il elenco o un riquadro viene aggiunto a un'area di lavoro, è possibile aprire tale area di lavoro e riordinare l'elenco o il riquadro incluso nel gruppo in cui è stato posizionato.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Personalizzazione esplicita: aggiungere un riepilogo da un'area di lavoro a un dashboard
Alcune aree di lavoro contengono riquadri di conteggio, che includono numeri, che possono essere visualizzati nel dashboard. In un'area di lavoro, fare clic con il pulsante destro del mouse su un riquadro di conteggio e selezionare **Personalizza**. Selezionare **Aggiungi a dashboard**. La volta successiva che l'utente esplora (e aggiorna) il dashboard selezionato, il conteggio verrà visualizzato sotto il riquadro di navigazione di tale area di lavoro del dashboard.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Personalizzazione esplicita: personalizzazione del dashboard
Il dashboard è spesso la prima pagina che l'utente visualizza quando si apre Dynamics 365 for Operations. È possibile personalizzare il dashboard per assegnare nuovi nomi i riquadri di navigazione dell'area di lavoro, per mostrare solo le sezioni desiderate, rinominare le sezioni o per organizzare le sezioni nell'ordine preferito. Per personalizzare il dashboard, selezionare qualsiasi riquadro e fare clic con il pulsante destro del mouse su di esso per aprire un menu di scelta rapida. Nel menu di scelta rapida, selezionare **Personalizza**. Se il riquadro selezionato è un riquadro che si desidera nascondere, rinominare o ignorare, è possibile apportare tale modifica direttamente nella finestra della proprietà visualizzata. Se si desidera organizzare i riquadri, selezionare **Personalizza modulo** nella finestra delle proprietà per aprire la barra degli strumenti di personalizzazione. È quindi possibile utilizzare lo strumento Spostamento per organizzare i riquadri.

## <a name="administration-of-personalization"></a>Amministrazione della personalizzazione
È possibile personalizzare una pagina e condividerla con altri utenti semplicemente esportando la pagina personalizzata e chiedendo agli altri utenti di passare alla pagina personalizzata e di importare il file di personalizzazione creato. Se un utente ha privilegi di amministrazione, è inoltre possibile gestire le personalizzazioni per altri utenti nella pagina di **impostazione della personalizzazione**. Spostarsi nella pagina b. Nella pagina **Personalizzazione** sono disponibili due schede, una contrassegnata **Sistema** e una**Utenti**. 

**Sistema:** è possibile disabilitare temporaneamente o "disattivare" tutte le personalizzazioni nel sistema. Questo non comporta l'eliminazione delle personalizzazioni, ma reimposta tutti i moduli allo stato predefinito. È possibile successivamente riabilitare la personalizzazione per applicare nuovamente tutte le personalizzazioni a ogni modulo utente. È anche possibile eliminare tutte le personalizzazioni per tutti gli utenti. Si noti che l'eliminazione delle personalizzazioni non consente di riabilitare in seguito automaticamente le personalizzazioni dal sistema. Assicurarsi di esportare le personalizzazioni che si desidera successivamente importare, prima di eseguire questo passaggio. 

**Utenti:** è possibile decidere per ogni utente se consentire l'esecuzione di personalizzazione implicita o esplicita. È inoltre possibile decidere se ogni utente può eseguire la personalizzazione implicita o esplicita in un modulo specifico. Infine, è possibile importare o esportare o eliminare una personalizzazione per ogni utente. 

**Nota:** nella versione iniziale, l'amministrazione della personalizzazione consente solo di gestire un utente alla volta.



