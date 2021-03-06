--- 
title: Identificare e risolvere conflitti di separazione dei compiti
description: "È possibile impostare le regole per separare le attività che devono essere eseguite da utenti diversi."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identificare e risolvere conflitti di separazione dei compiti

[!include [task guide banner](../../includes/task-guide-banner.md)]

È possibile impostare le regole per separare le attività che devono essere eseguite da utenti diversi. Questo concetto è denominato separazione dei compiti. Quando la definizione di un ruolo di sicurezza o le assegnazioni ruoli di un utente violano le regole, il conflitto viene annotato. Tutti i conflitti devono essere risolti dall'amministratore. Completare la procedura riportata di seguito per identificare e risolvere i conflitti. La società di dati dimostrativi utilizzata per creare questa procedura è USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Verificare se le assegnazioni utente-ruolo sono conformi alle nuove regole di separazione dei compiti
1. Scegliere Amministrazione sistema > Sicurezza > Separazione dei compiti > Verifica conformità delle assegnazioni utente-ruolo.
2. Fare clic su OK.
    * I risultati della convalida vengono visualizzati in una notifica.     Se è presente un conflitto, è possibile aprire la pagina Utenti e modificare le assegnazioni ruoli utente. Anche i conflitti vengono registrati nella pagina Conflitti di separazione dei compiti.     Per eseguire il processo di verifica come processo batch, selezionare Elaborazione batch, quindi impostare gli altri parametri batch. Dopo che viene eseguito il processo batch, è possibile esaminare i conflitti nella pagina Conflitti di separazione dei compiti.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Visualizzare e risolvere assegnazioni di ruoli utente in conflitto
1. Scegliere Amministrazione sistema > Sicurezza > Separazione dei compiti > Conflitti di separazione dei compiti.
    * Selezionare un conflitto, quindi fare clic su uno dei pulsanti seguenti: Nega assegnazione - Consente di negare l'assegnazione dell'utente al ruolo di sicurezza aggiuntivo. Se l'utente rifiuta un'assegnazione ruoli automatica, viene contrassegnato come escluso dal ruolo. All'utente escluso non viene concesso l'accesso associato al ruolo e l'utente non può essere assegnato al ruolo fino a che l'amministratore non elimina l'esclusione.     Consenti assegnazione - Consente di ignorare il conflitto e di assegnare l'utente a entrambi i ruoli di sicurezza. Se si ignora un conflitto, è necessario immettere un motivo nel campo Motivo per ignorare.  
2. Chiudere la pagina.
3. Scegliere Amministrazione sistema > Sicurezza > Separazione dei compiti > Conflitti di separazione dei compiti non risolti.
    * Selezionare un conflitto, quindi fare clic su uno dei pulsanti seguenti: Nega assegnazione - Consente di negare l'assegnazione dell'utente al ruolo di sicurezza aggiuntivo. Se l'utente rifiuta un'assegnazione ruoli automatica, viene contrassegnato come escluso dal ruolo. All'utente escluso non viene concesso l'accesso associato al ruolo e l'utente non può essere assegnato al ruolo fino a che l'amministratore non elimina l'esclusione.     Consenti assegnazione - Consente di ignorare il conflitto e di assegnare l'utente a entrambi i ruoli di sicurezza. Se si ignora un conflitto, è necessario immettere un motivo nel campo Motivo per ignorare.    
4. Chiudere la pagina.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Verificare se i ruoli esistenti sono conformi alle nuove regole di separazione dei compiti
1. Scegliere Amministrazione sistema > Sicurezza > Separazione dei compiti > Regole di separazione dei compiti.
    * Selezionare una regola.  
2. Fare clic su Convalida compiti e ruoli.
    * Se i ruoli esistenti violano la regola selezionata, verrà visualizzato un messaggio contenente il nome del ruolo e i nomi dei compiti in conflitto. L'amministratore deve indicare l'attenuazione per il rischio di sicurezza o modificare il ruolo in modo che non violi le regole per la separazione dei compiti.     Se nessun ruolo viola la regola selezionata, verrà visualizzato un messaggio per indicare che tutti i ruoli sono conformi.  


