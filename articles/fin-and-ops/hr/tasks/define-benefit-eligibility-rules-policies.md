--- 
title: "Definire regole e criteri di idoneità ai benefit"
description: "Questa registrazione indicherà come è possibile creare regole e criteri di idoneità di benefit e come assegnare le regole ai benefit."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: it-it
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definire regole e criteri di idoneità ai benefit

[!include [task guide banner](../../includes/task-guide-banner.md)]

Questa registrazione indicherà come è possibile creare regole e criteri di idoneità di benefit e come assegnare le regole ai benefit.  

La società di dati dimostrativi utilizzata per creare questa registrazione è USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Creare il tipo di regola dei criteri di idoneità al benefit
1. Andare a Risorse umane > Benefit > Idoneità > Tipi di regole dei criteri di idoneità al benefit.
2. Fare clic su Nuovo.
3. Digitare un valore nel campo Regola.
4. Nel campo Descrizione digitare un valore.
5. Nel campo Nome query fare clic sul pulsante a discesa per aprire la ricerca.
6. Nell'elenco fare clic sul collegamento nella riga selezionata.
7. Fare clic su Salva.
8. Chiudere la pagina.

## <a name="benefit-eligibility-policy"></a>Criteri di idoneità al benefit
1. Andare a Risorse umane > Benefit > Idoneità > Criteri di idoneità benefit.
2. Selezionare uno dei criteri di benefit esistenti.
3. Nell'elenco fare clic sul collegamento nella riga selezionata.
4. Attivare/disattivare l'espansione delle sezioni Organizzazioni criteri.  In questo punto è possibile aggiungere o rimuovere tutte le organizzazioni da includere nei criteri.
5. Espandere o comprimere la sezione Regole dei criteri.
6. Nell'elenco individuare la regola dei criteri creata in precedenza.
7. Fare clic su Crea regola dei criteri.
8. Nel campo Data di validità immettere la data in cui si desidera che i criteri diventino effettivi.
    * Se si impostano le date di validità e di fine, è possibile apportare modifiche future alle regole dei criteri ed eliminare la necessità di tornare ai criteri quando si desidera che le modifiche siano effettive.  
9. 
    * Se ad esempio si desidera che la regola venga applicata solo ai responsabili delle vendite, è possibile creare la clausola WHERE nel modo seguente: WHERE descrizione posizione corrisponde al responsabile vendite.  È possibile utilizzare l'operatore And oppure Or in più istruzioni WHERE nella regola.  
10. Fare clic su OK.
11. Chiudere la pagina.
12. Chiudere la pagina.

## <a name="assign-rule-to-benefit"></a>Assegnare la regola al benefit
1. Andare a Risorse umane > Benefit > Benefit.
2. Nell'elenco trovare e selezionare il record desiderato.
3. Nell'elenco fare clic sul collegamento nella riga selezionata.
4. Espandere o comprimere la sezione Regole di idoneità.
5. Fare clic su Modifica.
6. Nel campo Idoneità selezionare Basato su regole.
7. Nel campo Tipo di regola fare clic sul pulsante a discesa per aprire la ricerca.
8. Nell'elenco individuare e selezionare la regola creata in precedenza.
9. Nell'elenco fare clic sul collegamento nella riga selezionata.
10. Fare clic su Salva.
11. Chiudere il modulo.


