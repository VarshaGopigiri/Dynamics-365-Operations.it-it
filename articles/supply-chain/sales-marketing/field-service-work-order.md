---
title: Sincronizzare gli ordini di lavoro in Field Service con gli ordini cliente in Finance and Operations
description: "In questo argomento vengono descritti i modelli e le attività sottostanti che vengono utilizzati per sincronizzare gli ordini di lavoro in Field Service con gli ordini cliente in Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 854240bef9d6193c8f0f608687b68e6842fe272c
ms.contentlocale: it-it
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Sincronizzare gli ordini di lavoro in Field Service con gli ordini cliente in Finance and Operations

[!include[banner](../includes/banner.md)]

Questo argomento descrive i modelli e le attività sottostanti che vengono utilizzati per sincronizzare gli ordini di lavoro in Microsoft Dynamics 365 for Field Service con gli ordini cliene in Microsoft Dynamics 365 for Finance and Operations.

[![Sincronizzazione dei processi aziendali tra Finance and Operations e Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

In questo argomento vengono descritti i modelli e le attività sottostanti che vengono utilizzati per sincronizzare gli ordini di lavoro in Field Service con gli ordini cliente in Finance and Operations.

## <a name="templates-and-tasks"></a>Modelli e attività

I seguenti modelli e le attività sottostanti vengono utilizzati per sincronizzare gli ordini di lavoro in Field Service con gli ordini cliente in Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>Nomi dei modelli in Integrazione dati

Il modello **Ordini di lavoro a ordini cliente (da Field Service a Fin and Ops)** viene utilizzato per eseguire la sincronizzazione.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Nomi delle attività nel progetto di Integrazione dati

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Le attività di sincronizzazione seguenti sono necessarie prima di eseguire la sincronizzazione delle intestazioni e delle righe dell'ordine cliente:

- Prodotti Field Service (da Fin and Ops a Field Service)
- Conti (da Sales a Fin and Ops) - Diretti

## <a name="entity-set"></a>Insieme di entità

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | Intestazioni ordine cliente CDS |
| msdyn_workorderservices | Righe ordine cliente CDS   |
| msdyn_workorderproducts | Righe ordine cliente CDS   |

## <a name="entity-flow"></a>Flusso di entità

Gli ordini di lavoro vengono creati in Field Service. Se gli ordini di lavoro includono solo prodotti gestiti esternamente e se il valore in **Stato ordine di lavoro** è diverso da **Aperto - Non programmato** e **Chiuso - Annullato**, gli ordini di lavoro possono essere sincronizzati con Finance and Operations tramite un progetto di integrazione dati CDS. Gli aggiornamenti agli ordini di lavoro verranno sincronizzati come ordini cliente in Finance and Operations. Gli aggiornamenti includono le informazioni sul tipo di origine e sullo stato.

## <a name="estimated-versus-used"></a>Stimato rispetto a Utilizzato

In Field Service, i prodotti e i servizi negli ordini di lavoro hanno entrambi i valori **Stimato** e **Utilizzato** per le quantità e gli importi. Tuttavia, in Finance and Operations, negli ordini cliente i valori **Stimato** e **Utilizzato** non hanno lo stesso significato. Per supportare l'allocazione di prodotti che utilizza la quantità prevista nell'ordine cliente in Finance and Operations e per mantenere al contempo la quantità utilizzata che deve essere consumata e fatturata, due insiemi di attività sincronizzano i prodotti e i servizi nell'ordine di lavoro. Un insieme di attività è per i valori **Stimati** e l'altro insieme è per i valori **Utilizzati**.

Questo comportamento supporta scenari in cui i valori stimati vengono utilizzati per l'allocazione o la prenotazione in Finance and Operations, mentre i valori utilizzati vengono utilizzati per il consumo e la fatturazione.

### <a name="estimated"></a>Stimato

Per la sincronizzazione di righe di prodotti, i valori **Stimato** vengono utilizzati quando il valore di **Stato riga** è **Stimato**, l'opzione **Allocato** è impostata su **Sì** e **Stato sistema** non è impostato su **Chiuso - Registrato**.

Per la sincronizzazione di righe di servizi, i valori **Stimato** vengono utilizzati quando il valore di **Stato riga** è **Stimato** e il valore di **Stato sistema** non è **Chiuso - Registrato**.

### <a name="used"></a>Ratei utilizzati

I valori **Utilizzato** vengono utilizzati per il consumo e la fatturazione. In questi casi, i valori **Utilizzato** vengono sincronizzati.

Nella seguente tabella viene fornita una panoramica delle diverse combinazioni per le righe di prodotti.

| Stato sistema <br>(Field Service) | Stato riga <br>(Field Service) | Allocato <br>(Field Service) |Valore sincronizzato <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Aperto - Programmato   | Stimato   | Sì       | Stimato                       |
| Aperto - Programmato   | Stimato   | No        | Ratei utilizzati                            |
| Aperto - Programmato   | Ratei utilizzati        | Sì       | Ratei utilizzati                            |
| Aperto - Programmato   | Ratei utilizzati        | No        | Ratei utilizzati                            |
| Aperto - In corso | Stimato   | Sì       | Stimato                       |
| Aperto - In corso | Stimato   | No        | Ratei utilizzati                            |
| Aperto - In corso | Ratei utilizzati        | Sì       | Ratei utilizzati                            |
| Aperto - In corso | Ratei utilizzati        | No        | Ratei utilizzati                            |
| Aperto - Completato   | Stimato   | Sì       | Stimato                       |
| Aperto - Completato   | Stimato   | No        | Ratei utilizzati                            |
| Aperto - Completato   | Ratei utilizzati        | Sì       | Ratei utilizzati                            |
| Aperto - Completato   | Ratei utilizzati        | No        | Ratei utilizzati                            |
| Chiuso - Registrato    | Stimato   | Sì       | Ratei utilizzati                            |
| Chiuso - Registrato    | Stimato   | No        | Ratei utilizzati                            |
| Chiuso - Registrato    | Ratei utilizzati        | Sì       | Ratei utilizzati                            |
| Chiuso - Registrato    | Ratei utilizzati        | No        | Ratei utilizzati                            |

Nella seguente tabella viene fornita una panoramica delle diverse combinazioni per le righe di servizi.

| Stato sistema <br>(Field Service) | Stato riga <br>(Field Service) | Valore sincronizzato <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Aperto - Programmato   | Stimato   | Stimato |
| Aperto - Programmato   | Ratei utilizzati        | Ratei utilizzati      |
| Aperto - In corso | Stimato   | Stimato |
| Aperto - In corso | Ratei utilizzati        | Ratei utilizzati      |
| Aperto - Completato   | Stimato   | Stimato |
| Aperto - Completato   | Ratei utilizzati        | Ratei utilizzati      |
| Chiuso - Registrato    | Stimato   | Ratei utilizzati      |
| Chiuso - Registrato    | Ratei utilizzati        | Ratei utilizzati      |

La sincronizzazione dei valori **Stimato** rispetto ai valori **Utilizzato** viene gestita mediante i due insiemi di attività per le righe di prodotti e le righe di servizi. L'attività corretta viene attivata da filtri predefiniti e il mapping sottostante aiuta a garantire che vengano sincronizzati i valori corretti per **Atteso** rispetto a **Utilizzato**.

### <a name="example"></a>Esempio

1. Viene creato e programmato un ordine di lavoro in Field Service.

    Il valore di **Stato sistema** è **Aperto - Programmato**.

    - **Riga prodotto:** Qtà stimata = 5ea, Qtà utilizzata = 0ea, Stato riga = Stimato, Allocato = No
    - **Riga servizio:** Qtà stimata = 2h, Qtà utilizzata = 0h, Stato riga = Stimato

    In questo esempio, il valore di **Qtà utilizzata** del prodotto pari a **0** (zero) e il valore di **Qtà stimata** del servizio pari a **2h** vengono sincronizzati in Finance and Operations.

2. I prodotti vengono allocati in Field Service.

    Il valore di **Stato sistema** è **Aperto - Programmato**.

    - **Riga prodotto:** Qtà stimata = 5ea, Qtà utilizzata = 0ea, Stato riga = Stimato, Allocato = Yes
    - **Riga servizio:** Qtà stimata = 2h, Qtà utilizzata = 0h, Stato riga = Stimato

    In questo esempio, il valore di **Qtà stimata** del prodotto pari a **5ea** e il valore di **Qtà stimata** del servizio pari a **2h** vengono sincronizzati in Finance and Operations.

3. Il tecnico dell'assistenza inizia a lavorare all'ordine di lavoro e registra un utilizzo di materiali pari a 6.

    Il valore di **Stato sistema** è **Aperto - In corso**.

    - **Riga prodotto:** Qtà stimata = 5ea, Qtà utilizzata = 6ea, Stato riga = Utilizzato, Allocato = Yes
    - **Riga servizio:** Qtà stimata = 2h, Qtà utilizzata = 0h, Stato riga = Stimato

    In questo esempio, il valore di **Qtà utilizzata** del prodotto pari a **6** e il valore di **Qtà stimata** del servizio pari a **2h** vengono sincronizzati in Finance and Operations.

4. Il tecnico dell'assistenza completa l'ordine di lavoro e registra il tempo impiegato pari a 1,5 ore.

    Il valore di **Stato sistema** è **Aperto - Completato**.

    - **Riga prodotto:** Qtà stimata = 5ea, Qtà utilizzata = 6ea, Stato riga = Utilizzato, Allocato = Yes
    - **Riga servizio:** Qtà stimata = 2h, Qtà utilizzata = 1,5h, Stato riga = Utilizzato

    In questo esempio, il valore di **Qtà utilizzata** del prodotto pari a **6** e il valore di **Qtà stimata** del servizio pari a **1,5h** vengono sincronizzati in Finance and Operations.

## <a name="sales-order-origin-and-status"></a>Origine dell'ordine cliente e stato

### <a name="sales-origin"></a>Origine vendite

Per tenere traccia degli ordini cliente in Finance and Operations che hanno origine da ordini di lavoro, è possibile creare un'origine vendite dove l'opzione **Assegnazione tipo di origine** è impostata su **Sì** e il campo **Tipo di origine vendite** è impostato su **Tipo di origine vendite**.

Per impostazione predefinita, il mapping seleziona l'origine vendite per il tipo di origine vendite **Integrazione ordine di lavoro** per tutti gli ordini cliente creati da ordini di lavoro. Questo comportamento può risultare utile quando si lavora a un ordine cliente in Finance and Operations. È necessario assicurarsi che gli ordini cliente che derivano da ordini di lavoro non vengano sincronizzati nuovamente in Field Service come ordini di lavoro.

Per ulteriori informazioni su come impostare correttamente l'origine vendite in Finance and Operations, vedere la sezione "Prerequisiti e impostazioni di mapping" in questo argomento.

### <a name="status"></a>Stato

Quando l'ordine cliente ha origine da un ordine di lavoro, il campo **Stato ordine di lavoro esterno** viene visualizzato nella scheda **Impostazioni** nell'intestazione dell'ordine cliente. Questo campo mostra lo stato di sistema dall'ordine di lavoro in Field Service, per aiutare a tenere traccia dello stato dell'ordine di lavoro sincronizzato degli ordini cliente in Finance and Operations. Questo campo aiuta inoltre l'utente di Finance and Operations a determinare quando l'ordine cliente deve essere spedito o fatturato.

Il campo **Stato ordine di lavoro esterno** può contenere i valori seguenti:

- Aperto - Programmato
- Aperto - In corso
- Aperto - Completato
- Chiuso - Registrato

## <a name="field-service-crm-solution"></a>Soluzione CRM Field Service

Per supportare l'integrazione tra Field Service and Finance e Operations, sono richieste delle funzionalità aggiuntive nella soluzione CRM Field Service. La soluzione include le modifiche seguenti.

### <a name="work-order-entity"></a>Entità ordine di lavoro

Il campo ***Solo prodotti gestiti esternamente** è stato aggiunto all'entità **Ordine di lavoro** e appare nella pagina. Viene utilizzato per controllare in modo coerente se un ordine di lavoro è costituito interamente da prodotti gestiti esternamente. Un ordine di lavoro include solo prodotti gestiti esternamente quando tutti i prodotti correlati vengono gestiti in Finance and Operations. Questo campo impedisce agli utenti di sincronizzare ordini di lavoro che hanno prodotti sconosciuti in Finance and Operations.

### <a name="work-order-product-entity"></a>Entità ordine di lavoro prodotto

- Il campo **L'ordine ha solo prodotti gestiti esternamente** è stato aggiunto all'entità **Ordine di lavoro prodotto** e appare nella pagina. Viene utilizzato per controllare in modo coerente se l'ordine di lavoro prodotto viene gestito in Finance and Operations. Questo campo impedisce agli utenti di sincronizzare ordini di lavoro prodotto sconosciuti in Finance and Operations.
- Il campo ***Stato sistema intestazione** è stato aggiunto all'entità **Ordine di lavoro prodotto** e appare nella pagina. Viene utilizzato per controllare in modo coerente lo stato di sistema dell'ordine di lavoro e garantisce il corretto filtraggio quando i prodotti ordine di lavoro vengono sincronizzati in Finance and Operations. Quando si impostano filtri sulle attività di integrazione, le informazioni contenute in **Stato sistema intestazione** vengono utilizzate anche per determinare se i valori stimati o utilizzati devono essere sincronizzati.
- Il campo **Importo unitario fatturato** mostra l'importo che viene fatturato in base all'unità effettiva utilizzata. Questo valore viene calcolato come il valore di **Importo totale** diviso per il valore di **Quantità effettiva**. Il campo viene utilizzato per l'integrazione con sistemi che non supportano valori diversi per la quantità utilizzata e la quantità fatturata. Questo campo non appare nell'interfaccia utente (UI). 
- Il campo **Importo sconto fatturato** viene calcolato come il valore di **Importo sconto** più l'arrotondamento del calcolo del valore di **Importo sconto fatturato**. Questo campo viene utilizzato per l'integrazione e non è presente nell'interfaccia utente.
- Il campo **Quantità decimale** memorizza il valore del campo **Quantità** come numero decimale. Questo campo viene utilizzato per l'integrazione e non è presente nell'interfaccia utente. 
- Il valore nei campi **Utilizzato** viene reimpostato su **0** (zero) se il valore di **Stato riga** dell'ordine di lavoro prodotto viene modificato da **Utilizzato** in **Stimato**. Questa modifica previene situazioni in cui una quantità utilizzata immessa erroneamente viene utilizzata per la sincronizzazione quando il valore di **Stato riga** è **Stimato** e l'opzione **Allocato** è impostata su **No**.

### <a name="work-order-service-entity"></a>Entità ordine di lavoro assistenza

- Il campo **L'ordine ha solo prodotti gestiti esternamente** è stato aggiunto all'entità **Ordine di lavoro assistenza** e appare nella pagina. Viene utilizzato per controllare in modo coerente se l'ordine di lavoro assistenza viene gestito in Finance and Operations. Questo campo impedisce agli utenti di sincronizzare ordini di lavoro assistenza sconosciuti in Finance and Operations.
- Il campo ***Stato sistema intestazione** è stato aggiunto all'entità **Ordine di lavoro assistenza** e appare nella pagina. Viene utilizzato per controllare in modo coerente lo stato di sistema dell'ordine di lavoro e garantisce il corretto filtraggio quando gli ordini di lavoro assistenza vengono sincronizzati in Finance and Operations. Quando si impostano filtri sulle attività di integrazione, le informazioni contenute in **Stato sistema intestazione** vengono utilizzate anche per determinare se i valori stimati o utilizzati devono essere sincronizzati.
- Il campo **Durata in ore** memorizza il valore del campo **Durata** dopo che il valore è stato convertito da minuti in ore. Questo campo viene utilizzato per l'integrazione e non è presente nell'interfaccia utente.
- Il campo **Durata stimata in ore** memorizza il valore del campo **Durata stimata** dopo che il valore è stato convertito da minuti in ore. Questo campo viene utilizzato per l'integrazione e non è presente nell'interfaccia utente.
- Il campo **Importo unitario fatturato** memorizza l'importo che viene fatturato in base all'unità effettiva utilizzata. Questo valore viene calcolato come il valore di **Importo totale** diviso per il valore di **Quantità effettiva**. Questo campo viene utilizzato per l'integrazione con sistemi che non supportano valori diversi per la quantità utilizzata e la quantità fatturata. Il campo non appare nell'interfaccia utente.
- Il campo **Importo sconto fatturato** viene calcolato come il valore di **Importo sconto** più l'arrotondamento del calcolo del valore di **Importo sconto fatturato**. Questo campo viene utilizzato per l'integrazione e non è presente nell'interfaccia utente.
- Il campo **Ordine righe esterne** è un numero di ordine di riga negativo calcolato che può essere utilizzato nei sistemi esterni quando si combinano righe di ordine di lavoro prodotto e assistenza. Questo campo consente ai prodotti dell'ordine di lavoro che sono stati immessi di avere numeri di riga positivi e ai servizi dell'ordine di lavoro di avere numeri di riga negativi. Il valore di questo campo viene calcolato come il valore di **Ordine riga** moltiplicato per -1. Questo campo non appare nell'interfaccia utente.
- Il valore nei campi **Utilizzato** viene reimpostato su **0** (zero) se il valore di **Stato riga** dell'ordine di lavoro assistenza viene modificato per qualche ragione da **Utilizzato** in **Stimato**. Questa modifica previene situazioni in cui una quantità utilizzata immessa erroneamente viene utilizzata per la sincronizzazione quando il valore di **Stato riga** è **Stimato** e il valore di **Stato sistema intestazione** è **Chiuso - Registrato**.

## <a name="preconditions-and-mapping-setup"></a>Prerequisiti e impostazioni di mapping

Prima di sincronizzare gli ordini di lavoro, è importante aggiornare le impostazioni seguenti nei sistemi.

### <a name="setup-in-field-service"></a>Impostazione in Field Service

- Verificare che la serie numerica utilizzata per gli ordini di lavoro in Field Service non si sovrapponga alla sequenza numerica che viene utilizzata per gli ordini cliente in Finance and Operations. In caso contrario, è possibile che gli ordini clienti esistenti vengano aggiornati in modo errato in Field Service o Finance and Operations.
- Il campo **Creazione fattura ordine di lavoro** deve essere impostato su **Mai** in quanto la fattura sarà eseguita dall'interno di Finance and Operations. Passare a **Field Service** \> **Impostazioni** \> **Amministrazione** \> **Impostazioni di Field Service** e assicurarsi che il campo **Creazione fattura ordine di lavoro** sia impostata su **Mai**.

### <a name="setup-in-finance-and-operations"></a>Impostazione in Finance and Operations

L'integrazione dell'ordine di lavoro richiede l'impostazione dell'origine vendite. L'origine vendite viene utilizzata per distinguere gli ordini cliente in Finance and Operations che sono stati creati da ordini di lavoro in Field Service. Quando un ordine cliente ha un'origine vendite di tipo **Integrazione ordine di lavoro**, il campo **Stato ordine di lavoro esterno** viene visualizzato nell'intestazione dell'ordine cliente. L'origine vendite aiuta inoltre a garantire che gli ordini client che sono stati creati da ordini di lavoro in Field Service vengano filtrati durante la sincronizzazione degli ordini cliente da Finance and Operations verso Field Service.

1. Passare a **Vendite e marketing** \> **Impostazioni** \> **Ordini cliente** \> **Origine vendite**.
2. Selezionare **Nuovo** per creare una nuova origine vendite.
3. Nel campo **Origine vendite** immettere un nome per l'origine, ad esempio **WorkOrder**.
4. Nel campo **Descrizione** immettere una descrizione, ad esempio **Ordine di lavoro Field Service**.
5. Selezionare la casella di controllo **Assegnazione tipo di origine**.
6. Impostare il campo **Tipo di origine vendite** su **Integrazione ordine di lavoro**.
7. Selezionare **Salva**.

### <a name="template-mapping-in-data-integration"></a>Mapping dei modelli in Integrazione dati

(Presto disponibile)
