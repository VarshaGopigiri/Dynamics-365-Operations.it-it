---
title: Moduli di impostazione
description: In questo argomento viene fornita una panoramica dell&quot;impostazione del modulo Cespiti.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Moduli di impostazione

In questo argomento viene fornita una panoramica dell'impostazione del modulo Cespiti.

<a name="overview"></a>Panoramica
--------
I parametri controllare il comportamento generale dei cespiti.

I gruppi cespite consentono di raggruppare i cespiti e specificare gli attributi predefiniti per ciascun cespite assegnato a un gruppo. I libri sono assegnati a gruppi cespite. I libri tengono traccia del valore finanziario di un cespite nel tempo utilizzando la configurazione di ammortamento definita nel profilo di ammortamento.

I cespiti vengono assegnati a un gruppo nel momento in cui vengono creati. Per impostazione predefinita, i libri assegnati al gruppo cespite vengono assegnati al cespite. I libri configurati per la registrazione nella contabilità generale sono associati a un profilo di registrazione. I conti CoGe vengono definiti per libro nel profili di registrazione e vengono utilizzati nella registrazione delle transazioni cespiti. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Profili di ammortamento
I profili di ammortamento devono essere impostati per primi. Nel profilo di ammortamento, configurate in che modo il valore di un cespite viene ammortizzato nel tempo. È necessario definire il metodo di ammortamento, l'anno di ammortamento (anno di calendario o anno fiscale) e la frequenza di ammortamento.

## <a name="books"></a>Libri
Dopo aver impostato i profili di ammortamento, è necessario creare i libri necessari per i cespiti. Ciascun libro tiene traccia di un ciclo di vita finanziario indipendente di un cespite. I libri possono essere configurati per registrare le transazioni associate nella contabilità generale. Questa configurazione è l'impostazione predefinita, poiché viene utilizzata in genere per i report finanziari aziendale. I libri che non vengono registrate da registrare nella contabilità generale solo al giornale di registrazione secondario del cespite e in genere vengono utilizzati ai fini delle dichiarazioni fiscali.

Un profilo di ammortamento primario viene assegnato a ciascun libro. I libri hanno anche un profilo di ammortamento alternativo, se questo tipo di profilo è applicabile. Per includere automaticamente il libro cespiti nelle esecuzioni di ammortamento, è necessario abilitare l'opzione Calcola ammortamento. Se l'opzione non è selezionata per un cespite, la proposta di ammortamento salta il cespite.

È inoltre possibile impostare libri derivati. Le transazioni derivate specificate vengono registrate come copia esatta della transazione primaria rispetto ai libri derivati. Di conseguenza, le transazioni derivate sono impostate in genere per le acquisizioni e le dismissioni, non per le transazioni di ammortamento.

## <a name="fixed-asset-posting-profiles"></a>Profili registrazione cespiti
Una volta impostato il libro, è possibile creare il profilo di registrazione. Il profilo di registrazione deve essere definito per libro, ma può anche essere definito a livello più dettagliato. Ad esempio, è possibile definire il profilo di registrazione per la combinazione di libro e gruppo cespite, o persino per un singolo libro cespiti. Per impostazione predefinita, i conti CoGe definiti vengono utilizzati per le transazioni cespiti.

È necessario definire i conti CoGe utilizzati durante i processi di dismissione, sia vendita per dismissione che scarti per dismissione. Al momento della dismissione, le transazioni cespiti precedentemente registrate vengono stornate dai conti originali e gli importi netti vengono spostati nel conto appropriato di profitti e perdite per la dismissione di cespiti. Per contribuire a garantire che le transazioni siano stornate correttamente, è necessario impostare conti per ogni tipo di transazione utilizzato nella società. Il conto principale deve essere il conto originale impostato per il tipo di transazione nel profilo di registrazione, mentre il conto di contropartita deve essere il conto profitti e perdite per la dismissione. L'eccezione è il valore contabile netto. In questo caso, il conto principale e il conto di contropartita devono essere impostati sul conto profitti e perdite per la dismissione.

## <a name="fixed-asset-groups"></a>Gruppi cespite
Gruppo cespite è l'unico campo obbligatorio quando si crea un cespite. Il valore di questo campo determina il valore predefinito dei diversi campi informativi per il cespite. I libri vengono impostati in modo da assegnare un libro predefinito a ciascun cespite in un gruppo. È quindi possibile impostare gli attributi dei libri specifici per un gruppo di cespiti, ad esempio Vita utile e Convenzione di ammortamento.

È inoltre possibile definire i fondi di ammortamento speciale, o ammortamento aggiuntivo, per una specifica combinazione di gruppo cespite e libro. È necessario assegnare una priorità al fondo di ammortamento speciale per specificare l'ordine in cui i fondi vengono calcolati quando più fondi vengono assegnati a un libro.

## <a name="fixed-asset-parameters"></a>Parametri Cespiti
L'ultimo passaggio è l'aggiornamento dei parametri del cespite.

Il campo Soglia di capitalizzazione determina i cespiti che verranno ammortizzati. Se una riga di acquisto è selezionata come cespite, ma non corrisponde al valore soglia di capitalizzazione, il cespite è ancora stato creato o aggiornato, ma l'opzione di ammortamento calcolo è impostata su No. Di conseguenza, il cespite non verrà ammortizzato automaticamente come parte delle proposte di ammortamento.

Una importante opzione è Crea automaticamente importi di rettifica all'ammortamento con dismissione. Quando si imposta questa opzione su Sì, l'ammortamento del cespite viene rettificato automaticamente, in base alle impostazioni di ammortamento al momento della dismissione. Un'altra opzione consente di detrarre gli sconti di cassa dall'importo di acquisizione quando si acquistano i cespiti utilizzando una fattura fornitore.

Nella scheda dettaglio Ordini fornitore, è possibile configurare la modalità secondo cui i cespiti vengono creati durante il processo di acquisto. La prima opzione è Consenti acquisizione cespiti da Acquisto. Se si imposta questa opzione su Sì, l'acquisizione del cespite verrà applicata quando viene registrata la fattura. Se si imposta questa opzione su No, è comunque possibile inserire un cespite in un ordine fornitore (PO) e in fattura, ma l'acquisizione non verranno registrate. La registrazione deve essere eseguita come passaggio separato dal giornale di registrazione cespiti. Cespite di creazione dell'opzione di registrazione della fattura o dell'entrata prodotti consente di creare "" riavviare un nuovo cespite durante la registrazione, in modo che non sia impostato come cespite prima della transazione. L'ultima opzione, Verifica creazione cespiti durante l'immissione riga, si applica solo alle richieste di acquisto.

I codici motivo possono essere configurati come necessari per le modifiche a un cespite o per transazioni cespiti specifiche.

Infine, nella scheda Sequenze numeriche, è necessario definire le sequenze numeriche per i cespiti. La sequenza numerica cespiti può essere sostituita dalla sequenza numerica del gruppo cespite è stata specificata.

