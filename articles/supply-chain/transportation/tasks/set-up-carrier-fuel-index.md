--- 
title: Impostare un indice carburante vettore
description: Questa guida illustra come creare un paese di indice carburante, un indice carburante e un indice carburante del vettore.
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>Impostare un indice carburante vettore

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questa guida illustra come creare un paese di indice carburante, un indice carburante e un indice carburante del vettore. Il paese di indice carburante specifica il paese in cui l'indice carburante deve essere applicato e l'indice carburante specifica un prezzo del carburante per un periodo specifico. Per riflettere la modifica dei prezzi carburante nel tempo, è possibile associare più indici carburante a un vettore.  Queste attività in genere vengono effettuate da un coordinatore dei trasporti. È possibile utilizzare questa procedura nella società di dati dimostrativi USMF oppure nei propri dati.


## <a name="create-a-fuel-index-region"></a>Creare un paese di indice carburante
1. Andare a Gestione trasporto > Impostazioni > Indici carburante > Paesi indice carburante.
    * È necessario creare prima i diversi paesi in cui si opera e in cui si calcolano i supplementi carburante diversi.  
2. Fare clic su Nuovo.
3. Nel campo Paese digitare un valore.
4. Digitare un valore nel campo Nome.
5. Fare clic su Salva.

## <a name="create-a-fuel-index"></a>Creare un indice carburante
1. Andare a Gestione trasporto > Impostazioni > Indici carburante > Indici carburante.
    * Per i paesi impostati è necessario immettere i prezzi correnti per il carburante.  
2. Fare clic su Nuovo.
3. Nel campo Paese fare clic sul pulsante a discesa per aprire la ricerca.
4. Nell'elenco fare clic sul collegamento nella riga selezionata.
5. Immettere un numero nel campo Prezzo per gallone.
6. Nel campo Data e ora di inizio effettive immettere una data e un'ora.
7. Fare clic su Salva.

## <a name="create-a-carrier-fuel-index"></a>Creare un indice carburante vettore
1. Andare a Gestione trasporto > Impostazioni > Indici carburante > Indici carburante vettore.
2. Fare clic su Nuovo.
3. Nel campo Indice carburante vettore immettere un valore.
4. Nel campo Descrizione digitare un valore.
5. Fare clic su Nuovo.
6. Nel campo Data e ora di inizio effettive immettere una data e un'ora.
7. Nel campo Da PPG immettere un numero.
    * In questo esempio, è possibile impostare il campo Da PPG su 1,95.  
8. Nel campo A PPG immettere un numero.
    * In questo esempio, è possibile impostare il campo A PPG su 2.  
9. Nel campo Percentuale immettere un numero.
    * In questo esempio, è possibile impostare la percentuale su 3.  
10. Nel campo Valuta fare clic sul pulsante a discesa per aprire la ricerca.
11. Nell'elenco trovare e selezionare il record desiderato.
12. Nell'elenco fare clic sul collegamento nella riga selezionata.
13. Fare clic su Salva.


