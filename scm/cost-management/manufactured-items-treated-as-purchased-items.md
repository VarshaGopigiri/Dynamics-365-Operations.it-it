---
title: "Impostare i prodotti che è possibile ottenere prodotti o"
description: I prodotti possono essere originari in vari modi - possono essere prodotti () o quindi possibile ottenere acquistato (). Questo articolo descrive alcuni punti tipici da considerare quando si configurano i prodotti per supportare l&quot;approvvigionamento multiplo.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5360c7b1475763b8e33205bff560393e9ee51882
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-products-that-can-be-produced-or-procured"></a>Impostare i prodotti che è possibile ottenere prodotti o

I prodotti possono essere originari in vari modi - possono essere prodotti () o quindi possibile ottenere acquistato (). Questo articolo descrive alcuni punti tipici da considerare quando si configurano i prodotti per supportare l'approvvigionamento multiplo. 

L'approvvigionamento multiplo è in genere utilizzato per un articolo acquistato che viene prodotto occasionalmente oppure quando un articolo che era principalmente un articolo prodotto viene modificato e diventa principalmente un articolo acquistato. L'articolo viene inizialmente designato come articolo prodotto allo scopo di definire le informazioni relative alla distinta base e al ciclo di lavorazione e di supportare gli ordini di produzione ad esso relativi. Il tipo di produzione deve essere impostato su **DBA** (o, per l'elaborazione della produzione, **Formula** o **Co-prodotto**).

Quando si utilizza il costo standard, il record relativo al costo dell'articolo può essere calcolato per l'articolo prodotto. Tuttavia, il record relativo al costo dell'articolo potrebbe non corrispondere al costo standard desiderato ai fini degli acquisti. In tal caso, il costo standard deve essere immesso e attivato manualmente per il record relativo al costo dell'articolo. Per il calcolo dei costi, si studi la possibilità di utilizzare una DBA e un ciclo di lavorazione speciali che rappresentino la combinazione di forniture del prodotto nel corso di un periodo fiscale, per ridurre gli scostamenti nel tempo. Un articolo prodotto presso un sito può inoltre essere trasferito a un altro sito, in modo che il relativo costo debba essere immesso e attivato manualmente per il sito a cui l'articolo viene trasferito. Quando si utilizza l'articolo prodotto come componente di prodotti di livello superiore, i costi del componente devono essere considerati come un articolo acquistato e tale linea guida si applica indipendentemente dal fatto che siano stati calcolati oppure immessi manualmente. In altri termini, in un calcolo DBA i costi dell'articolo devono essere trattati come un componente acquistato anziché essere calcolati in base alle informazioni della distinta base e del ciclo di lavorazione. Per impedire l'esecuzione del calcolo, selezionare il flag **Interrompi esplosione** incorporato nel gruppo di calcolo DBA assegnato all'articolo. Per impedire che i calcoli della programmazione generale facciano esplodere i fabbisogni in relazione all'articolo, impostare l'intervallo di esplosione su 0 (zero) giorni nella copertura articoli o nel gruppo di copertura. Il calcolo della programmazione generale considererà quindi l'articolo come un articolo acquistato e non verranno eseguiti ulteriori calcoli per le informazioni sulla distinta base e il ciclo di lavorazione dell'articolo.



