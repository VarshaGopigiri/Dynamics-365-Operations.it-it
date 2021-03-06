---
title: Creare un nuovo layout di magazzino
description: Questa procedura consente di visualizzare come impostare le informazioni sulle ubicazioni in un magazzino.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a>Creare un nuovo layout di magazzino

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questa procedura consente di visualizzare come impostare le informazioni sulle ubicazioni in un magazzino. È applicabile solo ai magazzini creati utilizzando "Operazioni di magazzino di base" del modulo Gestione inventario, non ai magazzini creati nel modulo Gestione magazzino. È possibile utilizzare questa procedura nella società di dati dimostrativi USMF oppure nei propri dati.


## <a name="set-the-default-location-capacity"></a>Impostare la capacità dell'ubicazione predefinita
1. Fare clic su Gestione magazzino > Impostazioni > Parametri di gestione articoli e magazzino.
2. Fare clic sulla scheda Ubicazioni.
3. Nel campo Larghezza standard immettere un numero.
4. Nel campo Profondità standard immettere un numero.
5. Nel campo Altezza standard immettere un numero.
6. Fare clic su Salva.
7. Chiudere la pagina.

## <a name="define-the-location-name-format"></a>Definire il formato del nome dell'ubicazione
1. Passare a Gestione inventario > Impostazioni > Suddivisione scorte > Magazzino.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Magazzino.
4. Digitare un valore nel campo Nome.
5. Nel campo Sito fare clic sul pulsante a discesa per aprire la ricerca.
6. Nell'elenco trovare e selezionare il record desiderato.
7. Attiva/disattiva l'espansione della sezione Nomi ubicazioni.
    * Le opzioni di questa sezione definiscono il formato predefinito per i nomi delle ubicazioni. Nel nostro esempio, includeremo il numero di sezione, il numero di scaffale e il numero di ripiano.  
8. Impostare l'opzione Includi sezione su Sì.
9. Impostare l'opzione Includi scaffale su Sì.
10. Nel campo Formato digitare un valore per lo scaffale.
    * Ad esempio: -N  
11. Impostare l'opzione Includi ripiano su Sì.
12. Nel campo Formato digitare un valore per il ripiano.
    * Ad esempio: -N  

## <a name="define-warehouse-locations"></a>Definire le ubicazioni di magazzino
1. Nel riquadro azioni fare clic su Magazzino.
2. Fare clic su Creazione guidata ubicazione.
3. Scegliere Avanti.
4. Deselezionare l'opzione Banchine di uscita
5. Deselezionare l'opzione Ubicazioni di stoccaggio
6. Scegliere Avanti.
7. Scegliere Avanti.
8. Scegliere Avanti.
9. Scegliere Avanti.
10. Scegliere Avanti.
11. Scegliere Avanti.
12. Scegliere Avanti.
    * Si noti che le dimensioni fisiche visualizzate in questa pagina sono quelle impostate all'inizio di questa procedura.  
13. Scegliere Avanti.
14. Scegliere Fine.
15. Chiudere la pagina.
16. Aggiorna la pagina.

