--- 
title: Imposta criteri fatture fornitore
description: I criteri fattura fornitore vengono eseguiti quando si registra una fattura fornitore tramite la pagina Fattura fornitore e quando si apre la pagina violazioni dei criteri per fatture fornitore.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f51c117da75a0382a38e75154ecef758f9a5d6c1
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendor-invoice-policies"></a>Imposta criteri fatture fornitore

[!include [task guide banner](../../includes/task-guide-banner.md)]

I criteri fattura fornitore vengono eseguiti quando si registra una fattura fornitore tramite la pagina Fattura fornitore e quando si apre la pagina violazioni dei criteri per fatture fornitore. È inoltre possibile configurare il flusso di lavoro delle fatture fornitore affinché i criteri fatture fornitore vengano eseguiti ogni volta che si invia una fattura al flusso di lavoro. 

I criteri fatture fornitore non sono applicabili alle fatture create nel registro fatture o nel giornale di registrazione fatture. 

La convalida di abbinamento fatture non utilizza i criteri fatture fornitore, ma viene invece impostata nella pagina Parametri contabilità fornitori.

Questa registrazione utilizza la società dimostrativa USMF. Il ruolo di responsabile della contabilità fornitori o del responsabile della contabilità eseguirebbe le operazioni. Prima di iniziare, assicurarsi che sia selezionata la chiave di configurazione Abbinamento fatture.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Eseguire le operazioni preliminari alla creazione dei criteri fatture fornitore
1. Andare a Contabilità fornitori > Impostazioni > Parametri contabilità fornitori.
2. Fare clic sulla scheda Convalida fattura.
3. Selezionare o deselezionare la casella di controllo Aggiorna automaticamente lo stato dell'intestazione fattura.
4. Fare clic su OK.
5. Nel campo Registra fattura con discrepanze, selezionare un'opzione.
6. Chiudere la pagina.
7. Andare a Contabilità fornitori > Impostazione criteri > Criteri fatture fornitore.
8. Fare clic su Parametri.
9. Fare clic su btnAdd.
10. Chiudere la pagina.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Creare i tipi di regole dei criteri per fatture fornitore
1. Andare a Contabilità fornitori > Impostazione criteri > Tipi di regole dei criteri per le fatture fornitore.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Regola.
4. Nel campo Descrizione digitare un valore.
5. Nel campo Nome query fare clic sul pulsante a discesa per aprire la ricerca.
6. Nell'elenco trovare e selezionare il record desiderato.
7. Nell'elenco fare clic sul collegamento nella riga selezionata.
8. Fare clic su Salva.
9. Chiudere la pagina.

## <a name="define-a-vendor-invoice-policy"></a>Definire una regola dei criteri fattura fornitore
1. Andare a Contabilità fornitori > Impostazione criteri > Criteri fatture fornitore.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Nome.
4. Nel campo Descrizione digitare un valore.
5. Espandere o comprimere la sezione Organizzazioni criteri.
6. Nella struttura selezionare "Contoso Entertainment Systems USA"
7. Scegliere Aggiungi.
8. Espandere o comprimere la sezione Regole dei criteri.
9. Fare clic su Crea regola dei criteri.
10. Nel campo Descrizione regola dei criteri, immettere un valore.
11. Fare clic su Filtro.
12. Scegliere Aggiungi.
13. Nell'elenco contrassegnare la riga selezionata.
14. Nel campo Tabella fare clic sul pulsante a discesa per aprire la ricerca.
15. Nell'elenco fare clic sul collegamento nella riga selezionata.
16. Nel campo Tabella derivata fare clic sul pulsante a discesa per aprire la ricerca.
17. Nell'elenco fare clic sul collegamento nella riga selezionata.
18. Nel campo Campo fare clic sul pulsante a discesa per aprire la ricerca.
19. Digitare un valore nel campo Campo.
20. Chiudere la pagina.
21. Digitare un valore nel campo Criteri.
22. Fare clic su OK.
23. Fare clic su OK.
24. Chiudere la pagina.
25. Chiudere la pagina.


