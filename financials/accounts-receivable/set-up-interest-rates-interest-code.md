---
title: Impostare tassi d&quot;interesse per un codice interessi
description: I codici interessi contengono le impostazioni che determinano quando gli interessi vengono addebitati e come vengono calcolati nei conti scaduti.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Impostare tassi d'interesse per un codice interessi

I codici interessi contengono le impostazioni che determinano quando gli interessi vengono addebitati e come vengono calcolati nei conti scaduti.

È possibile impostare un singolo codice interessi e applicarlo a più profili di registrazione cliente, codici di fatturazione o righe specifiche della fattura. Quando i dettagli del codice interessi vengono modificati, tutte le funzionalità che utilizzano il codice implementeranno automaticamente le modifiche nelle nuove transazioni. Per ogni codice interessi, è possibile impostare due tipi di tassi:
-   Tassi per gli interessi attivi - Rappresentano i ricavi ottenuti tramite l'addebito di interessi sulle fatture o sulle note d'interesse.
-   Tassi per gli interessi passivi - Rappresentano un costo pagato per l'interesse sulle note di accredito.

Questi tipi di tassi possono essere utilizzati contemporaneamente e nello stesso codice interessi. I tassi d'interesse possono essere basati su tre tipi di calcolo:
-   Interesse in base a percentuale.
-   Interesse in base a importo.
-   Interesse in base a intervallo, che determina una singola percentuale o un singolo importo.

Quando si utilizza un codice interessi per calcolare gli interessi, viene creata una nota d'interesse separata per ogni tasso d'interesse in vigore nel periodo in cui il pagamento ha superato la scadenza della transazione. Utilizzare la scheda **Redditi** nella pagina **Codice interessi** per impostare i tassi per l'interesse guadagnato con l'addebito di interessi. Per impostare i tassi per gli interessi pagati, utilizzare invece la scheda **Pagamenti**.

## <a name="interest-rates-based-on-a-percentage"></a>Tassi d'interesse in base a una percentuale
È possibile impostare tassi d'interesse che calcolano una percentuale specificata.

-   L'importo degli interessi si applica a tutte le valute.
-   È possibile immettere limiti per l'importo interessi facoltativi.
-   ** Percentuale ** è selezionato ** ** in ** calcolare gli interessi basato su sistemi ** ** impostano i codici interessi ** pagina.

Ad esempio, per impostare un codice interessi che valutano il 5 degli interessi per ogni due mesi che il pagamento della fattura supera la scadenza della transazione, è imposterebbe 2 in ** calcolare gli interessi vengono calcolati ogni ** sistema e selezionare ** ** mese.

## <a name="interest-rates-based-on-amounts"></a>Tassi d'interesse in base agli importi
È possibile impostare tassi d'interesse che calcolano una quantità specificata per valuta.
-   Un importo interessi è specificato per ciascuna valuta relativa al codice interessi.
-   È possibile immettere limiti per l'importo interessi facoltativi.
-   ** Importo ** è selezionato in ** calcolare gli interessi basato su sistemi ** ** impostano i codici interessi ** pagina.

Ad esempio, per impostare un codice interessi che valutano un tasso di interessi pari a 25.00 per ogni 20 giorni per il pagamento della fattura supera la scadenza della transazione, è imposterebbe 20 in ** calcolare gli interessi vengono calcolati ogni ** sistema e selezionare ** ** giorno.

## <a name="interest-rates-based-on-ranges"></a>Tassi d'interesse in base agli intervalli
È possibile impostare tassi d'interesse che variano a seconda dell'importo scaduto e del numero di giorni o mesi accumulati dalla scadenza della fattura.
-   È possibile utilizzare la scheda **Utili per valuta** per definire le impostazioni specifiche degli interessi per ciascuna valuta. Qui è inoltre possibile definire l'intervallo.
-   Utilizzare il pulsante **Intervalli** per aggiungere righe che rappresentano gli intervalli che si desidera impostare. Il valore **Da** rappresenta l'inizio dell'intervallo e il numero in **Valore d'interesse** rappresenta una percentuale o un importo, a seconda della selezione nel campo **Calcola interessi in base a ** nella pagina **Imposta codici interessi**.

## <a name="example-1-interest-by-range--amount"></a>Esempio 1: Interessi in base a intervallo = Importo
Si imposta un codice interessi che valuta gli interessi una volta per ogni tre mesi in cui il pagamento della fattura supera la data di scadenza della transazione. Si desidera basare il calcolo su un valore di interesse percentuale, in base a intervalli di importi graduali. Il valore degli interessi corrisponderà all'1% per gli importi della fattura fino a 1.000,00, al 2% per gli importi da 1.001,00 a 5.000,00 e al 3% per gli importi superiori a 5.000,00. I valori del campo del codice interessi vengono impostati nel modo indicato di seguito.

| **Nome campo**                  | **Valore campo** |
|---------------------------------|-----------------|
| **Codice interessi**               | 3M%ByAmt        |
| **Calcola interessi ogni**    | 3/Month         |
| **Interessi in base a intervallo**           | Importo          |
| **Calcola interessi in base a** | Percentuale      |

Le informazioni sull'intervallo vengono impostate nel modo indicato di seguito.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Esempio 2: Interessi in base a intervallo = Giorni
--------------------------------------------------

Si imposta un codice interessi che valuta gli interessi una volta per ogni 15 giorni in cui il pagamento della fattura supera la data di scadenza della transazione. Si desidera basare il calcolo su un valore di interesse importo, in base a intervalli di giorni graduali. Il valore degli interessi sarà pari a 10,00 per 15 giorni durante i primi 60 giorni, 15,00 per 15 giorni durante l'intervallo di giorni da 61 a 90 e 20,00 per 15 giorni dal giorno 91 in poi. I valori del campo del codice interessi vengono impostati nel modo indicato di seguito.

| **Nome campo**                  | **Valore campo** |
|---------------------------------|-----------------|
| **Codice interessi**               | 15DAmtXDay      |
| **Calcola interessi ogni**    | 15/Giorno          |
| **Interessi in base a intervallo**           | Giorni            |
| **Calcola interessi in base a** | Importo          |

Le informazioni sull'intervallo vengono impostate nel modo indicato di seguito.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Esempio 3: Interessi in base a intervallo = Mesi
----------------------------------------------------

Si imposta un codice interessi che valuta gli interessi una volta per ogni mese in cui il pagamento della fattura supera la data di scadenza della transazione. Si desidera basare il calcolo su un valore di interesse percentuale, in base a intervalli di mesi graduali. Il valore degli interessi sarà dell'1,5% al mese per i primi tre mesi di ritardo, del 2,0% al mese per i tre mesi successivi e del 2,5% al mese per ogni mese successivo ai primi sei. I valori del campo del codice interessi vengono impostati nel modo indicato di seguito.

| **Nome campo**                  | **Valore campo** |
|---------------------------------|-----------------|
| **Codice interessi**               | 1M%ByMth        |
| **Calcola interessi ogni**    | 1/Month         |
| **Interessi in base a intervallo**           | Mesi          |
| **Calcola interessi in base a** | Percentuale      |

Le informazioni sull'intervallo vengono impostate nel modo indicato di seguito.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Funzionalità nuove versioni
I codici interessi contengono una data valida. Se si desidera modificare il tasso d'interesse, è possibile creare una **nuova versione** valida a partire da una data futura.

Per visualizzare versioni diverse, è possibile utilizzare l'opzione di menu **In data** per selezionare la data limite. È inoltre possibile selezionare **Visualizza tutti i record** per visualizzare tutti i codici interessi nella pagina.

