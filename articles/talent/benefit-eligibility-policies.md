---
title: "Criteri di idoneità benefit"
description: "Questo articolo fornisce le informazioni sui criteri di idoneità ai benefit, che consentono di definire chi è idoneo per ottenere i benefit specifici."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae4be70058e61cdbc1d2b063b346b45b023eb9e9
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="benefit-eligibility-policies"></a>Criteri di idoneità benefit

[!include [banner](includes/banner.md)]

Questo argomento fornisce le informazioni sui criteri di idoneità ai benefit, che consentono di definire chi è idoneo per ottenere i benefit specifici.

Quando si creano benefit, si decide quali benefit saranno disponibili per determinati dipendenti. Nella seguente tabella vengono visualizzati gli esempi di benefit che è possibile rendere disponibili per dipendenti specifici.

| Benefit          | Per chi è disponibile il benefit |
|------------------|---------------------------------|
| Assicurazione sanitaria | Tutti i dipendenti                   |
| Cellulare     | Venditori, dirigenti         |
| Pass di parcheggio   | Dirigenti                      |

I seguenti componenti vengono utilizzati per creare i criteri di idoneità:

-   Tipi di regola dei criteri
-   Criteri di idoneità benefit

I tipi di regola dei criteri consentono di definire i parametri relativi a query utilizzati quando si sviluppano regole dei criteri specifiche. Dopo aver creato i tipi di regola dei criteri, è possibile creare i criteri di idoneità al benefit. I criteri consentono di creare una raccolta di regole applicabili a una o più persone giuridiche. All'interno di ciascun criterio, è possibile visualizzare qualsiasi tipo di regola dei criteri di idoneità al benefit creata in precedenza. 

Definire l'ambito della regola all'interno del criterio. Ad esempio, se si crea un tipo di regola dei criteri di idoneità al benefit denominata **Dirigente**, è possibile specificare come deve essere considerata la regola all'interno di tale criterio. In questo esempio, la regola può prevedere che qualsiasi posizione contenente la parola "dirigente" venga inclusa nella regola. Dopo aver definito i parametri della regola o delle regole incluse nel criterio, è possibile assegnare una regola specifica al benefit.

<a name="additional-resources"></a>Risorse aggiuntive
--------

[Definizione e gestione di un programma di benefit](manage-benefit-program.md)




