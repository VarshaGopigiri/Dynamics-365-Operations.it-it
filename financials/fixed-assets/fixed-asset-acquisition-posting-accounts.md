---
title: Conti di registrazione acquisizione cespiti
description: "Questo articolo illustra come impostare i conti di registrazione della contabilità generale per l&quot;acquisizione dei cespiti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: bd7f89a7dbf8aa87794f8d4b57bda54433e5feb1
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Conti di registrazione acquisizione cespiti

Questo articolo illustra come impostare i conti di registrazione della contabilità generale per l'acquisizione dei cespiti.

I conti utilizzati per registrare le acquisizioni cespiti possono variare in base al metodo utilizzato per l'acquisizione del cespite. Nella pagina Profili registrazione cespiti, nella scheda Conti CoGe selezionare Acquisizione e Rettifica acquisizione per impostare i conti cespiti per la registrazione nella contabilità generale. 

Nei giornali di registrazione e negli ordini fornitore il conto COGE costituisce in genere il conto dello stato patrimoniale, dove viene addebitato il valore di acquisizione dei nuovi cespiti. Questo conto non viene visualizzato nel giornale di registrazione e non può essere sostituito nelle transazioni. 

Anche il conto di contropartita è un conto dello stato patrimoniale. Nel giornale di registrazione generale e nel giornale cespiti questo conto corrisponde spesso al conto bancario utilizzato per pagare l'acquisizione del cespite. Il conto di contropartita è un conto utilizzato come predefinito nei giornali di registrazione, dove può essere sostituito da qualsiasi altro conto del piano dei conti o da un conto fornitore se il cespite è stato acquistato da un fornitore. 

Se per le acquisizioni dei cespiti si utilizza il giornale di registrazione fattura o gli ordini fornitore nella Contabilità fornitori, il conto di contropartita per la transazione cespiti viene sostituito dal conto fornitore selezionato per la transazione.

Per le acquisizioni registrate in Contabilità generale utilizzando il giornale di registrazione Scorte a cespiti, il cespite non viene acquistato da origini esterne ma trasferito dalle scorte della società. Di conseguenza, il conto di contropartita per l'articolo di magazzino presente in Gestione articoli è costituito da un conto uscite da magazzino.

Per ulteriori informazioni, vedere [acquisti i cespiti con approvvigionamento acquire-assets-procurement.md] ().

