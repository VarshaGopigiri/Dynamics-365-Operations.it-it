---
title: "Pianificazione generale e funzionalità multisito"
description: Nella pianificazione generale devono essere prese in considerazione le impostazioni delle dimensioni inventariali relative al sito e al magazzino.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6800668741bfd86555b72faf8cce01f73cb9a278
ms.contentlocale: it-it
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-and-multisite-functionality"></a>Pianificazione generale e funzionalità multisito

[!include [banner](../includes/banner.md)]

Nella pianificazione generale devono essere prese in considerazione le impostazioni delle dimensioni inventariali relative al sito e al magazzino. 

La dimensione sito è obbligatoria ed è possibile impostare la dimensione magazzino come obbligatoria.

Quando una dimensione è obbligatoria, è necessario immettere un valore di dimensione in tutte le operazioni di magazzino. Pertanto, durante la pianificazione principale, il sito e il magazzino per la domanda iniziale sono noti. La dimensione sito è inoltre una dimensione coerente. Di conseguenza, durante l'esplosione della domanda a livello inferiore, il valore del sito rimane invariato.

Quando invece il magazzino non è impostato come obbligatorio, potrebbe non essere ricavabile dalla domanda iniziale. Il motore di pianificazione dovrà determinare il magazzino da utilizzare in base alle impostazioni definite per l'articolo, i singoli magazzini e i dettagli della riga dell'ordine.

Negli argomenti riportati di seguito viene descritta la logica in base alla quale il motore di pianificazione determina il magazzino da utilizzare a seconda delle impostazioni definite.

[Pianificazione generale: copertura a livello di sito magazzino, magazzino obbligatorio](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Pianificazione generale: copertura a livello di sito, magazzino obbligatorio](master-plan-site-coverage-warehouse-mandatory.md)

[Pianificazione generale: copertura a livello di sito magazzino, magazzino non obbligatorio](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Pianificazione generale: copertura a livello di sito, magazzino non obbligatorio](master-plan-site-coverage-warehouse-not-mandatory.md)

[Pianificazione generale - Come determinare la versione DBA](master-plan-bom-version-determined.md)




