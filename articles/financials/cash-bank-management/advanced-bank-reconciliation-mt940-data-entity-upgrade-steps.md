---
title: "Importazione MT940 riconciliazione estratti conto avanzata - Aggiornamento entità di dati compositi"
description: "Un numero progressivo deve essere aggiunto all'entità importazione rendiconto bancario per supportare il formato MT940."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a76558d220e98de85060d23d6e5d8df1c0cd1baf
ms.contentlocale: it-it
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Importazione MT940 riconciliazione estratti conto avanzata - Aggiornamento entità di dati compositi

[!include [banner](../includes/banner.md)]

Un numero progressivo deve essere aggiunto all'entità importazione rendiconto bancario per supportare il formato MT940. 

Effettuare le seguenti operazioni per aggiungere l'entità importazione rendiconto bancario per supportare il formato MT940.

1.  Compilare e sincronizzare quanto segue:
    -   Entità composta\\BankStatementImportEntity
    -   Entità\\BankStatementBalanceEntity
    -   Entità\\BankStatementDocumentEntity
    -   Entità\\BankStatementEntity
    -   Entità\\BankStatementLineEntity
    -   Tabelle\\BankStatementStaging

2.  Gestione dati\\Progetti dati.
    1.  Caricare i progetti di importazione MT940
        1.  Modificare XSLT.
            -   Fare clic su **Visualizza mapping**.
            -   Fare clic su **Visualizza mapping** sul documento di rendiconto bancario.
            -   Fare clic su **Trasformazioni**
            -   Eliminare il file BankReconiliation-to-Composite.xslt.
            -   Aggiungere la nuova versione di BankReconiliation-to-Composite.xsl.

        2.  Esporre **Numero progressivo** sul layout **Dati di origine**.
            1.  Formato dati di origine = Elemento XML.
            2.  Nome entità = Rendiconti bancari.
            3.  Caricare il file di dati = nuova versione SampleBankCompositeEntity.xml.
            4.  Fare clic su **Sì** per sovrascrivere il file esistente.
            5.  Fare clic su **Sì** per generare un nuovo mapping.
            6.  Verificare che S**equenceNumber** sia stato mappato.
                -   Fare clic su **Visualizza mapping** sull'entità rendiconto.
                -   Verificare che **SequenceNumber** sia mappato da Origine a Gestione temporanea.

3.  Importare il nuovo rendiconto.





