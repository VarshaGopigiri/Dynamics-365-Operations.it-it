---
title: Panoramica sugli avvisi
description: "Vengono fornite informazioni generali sugli avvisi in Microsoft Dynamics 365 for Finance and Operations. È possibile utilizzare avvisi per essere informati sugli eventi di cui si desidera tenere traccia durante la giornata lavorativa."
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ad9373faa19761cccca2b5d581de05f0ac9dd165
ms.contentlocale: it-it
ms.lasthandoff: 04/13/2018

---

# <a name="alerts-overview"></a>Panoramica sugli avvisi

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Informazioni sugli avvisi
Gli avvisi costituiscono un sistema di notifica per gli eventi critici in Microsoft Dynamics 365 for Finance and Operations. È possibile utilizzare avvisi per essere informati sugli eventi di cui si desidera tenere traccia durante la giornata lavorativa. È possibile creare facilmente una serie di regole di avviso allo scopo di ricevere avvisi relativi a consegne scadute, ordini eliminati, prezzi modificati o altri eventi per i quali è necessario intraprendere un'azione.

Nella pianificazione delle risorse aziendali (ERP, Enterprise Resource Planning), esistono diversi scenari tipici in cui la funzionalità Avvisi di Finance and Operations può essere utilizzata. Di seguito sono riportati alcuni esempi.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Scenario 1: creare una regola di avviso per nuovi ordini cliente
1. Aprire la pagina **Tutti gli ordini cliente**.
2. Nel riquadro azioni della scheda **Opzioni** del gruppo **Condividi**, selezionare **Crea avviso personalizzato**.
3. Nella finestra di dialogo **Crea regola di avviso**, nella Scheda dettaglio **Invia avviso quando**, nel campo **Evento**, selezionare **Record creato**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Scenario 2: creare una regola di avviso per il posticipo di una data di consegna
1. Aprire la pagina **Tutti gli ordini fornitore**.
2. Selezionare un ID di ordine fornitore per accedere ai dettagli dell'ordine fornitore.
3. Espandere la Scheda dettaglio **Intestazione ordine fornitore**.
4. Nel riquadro azioni della scheda **Opzioni** del gruppo **Condividi**, selezionare **Crea avviso personalizzato**.
5. Nella finestra di dialogo **Crea regola di avviso**, nella Scheda dettaglio **Invia avviso quando**, nel campo **Campo**, selezionare **Data di consegna**.
6. Nel campo **Evento**, selezionare **è stato posticipato**.
    
Dopo avere chiuso la finestra di dialogo **Crea regola di avviso**, la regola viene visualizzata nella pagina **Gestisci regole di avviso**. È possibile utilizzare la pagina **Gestisci regole di avviso** per aggiornare le regole di avviso esistenti. Ad esempio, è possibile modificare i trigger di eventi, aggiornare le notifiche di evento e le date di scadenza. Per aprire la pagina **Gestisci regole di avviso**, utilizzare il pulsante **Invia avviso** nella scheda **Opzioni** del riquadro azioni.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Risultato della creazione di una regola di avviso
Quando si creano regole di avviso, è possibile associare un evento predefinito a un campo specifico. Ad esempio, l'arrivo della data specificata nel campo o la modifica dei contenuti del campo. In alternativa, è possibile associare un evento ai record in una pagina specifica. Ad esempio, viene creato un record oppure viene eliminato.

Quando si verifica l'evento selezionato per il campo o per un record nella pagina, si riceve un avviso. Ad esempio, si crea una regola dove si associa il campo **Data di consegna** in una specifica riga di ordine fornitore all'evento **scaduto dal periodo di tempo indicato**. Impostare l'intervallo di tempo a cinque giorni. In questo caso, un avviso viene inviato cinque giorni dopo la data di consegna di quella riga ordine fornitore.

Inoltre, è possibile ottimizzare le regole di avviso impostando le condizioni. Ad esempio, è possibile ricevere un avviso sui nuovi ordini fornitore creati per i conti fornitore specifici.

## <a name="preparing-for-an-alert"></a>Preparazione per un avviso
Prima di impostare una regola di avviso, è necessario decidere quando o in quali situazioni si desidera ricevere avvisi. Dopo avere individuato l'evento per il quale si desidera ricevere una notifica, in Finance and Operations, trovare la pagina in cui vengono visualizzati i dati che causano l'evento. L'evento può essere una data prossima o una specifica modifica che si verificherà. Di conseguenza, è necessario individuare la pagina in cui è specificata la data o dove viene visualizzato il campo che cambia o il nuovo record creato. Una volta ottenute queste informazioni, sarà possibile creare la regola di avviso.

## <a name="components-of-an-alert-rule"></a>Componenti di una regola di avviso
Una regola di avviso include cinque componenti:

- **Evento** - L'evento che attiva una regola di avviso può essere l'arrivo di una data o il verificarsi di una modifica specifica. Gli eventi vengono definiti nella Scheda dettaglio **Invia avviso tramite posta elettronica in caso di modifiche allo stato del processo** della finestra di dialogo **Crea regola di avviso**.
- **Condizione** - Nella Scheda dettaglio **Invia avviso per** della finestra di dialogo **Crea regola di avviso** è possibile selezionare l'ambito della condizione, per controllare quando si viene avvisati del verificarsi di eventi. È possibile applicare la regola solo al record corrente o a tutti i record visibili nella pagina. Se la regola vale per tutte le persone giuridiche, è possibile impostare l'opzione **A livello di organizzazione** su **Sì**.
- **Scadenza della regola** - Nella Scheda dettaglio **Invia avviso fino a** della finestra di dialogo **Crea regola di avviso** è possibile specificare per quanto tempo deve essere attiva la regola di avviso.
- **Contenuti** - Nella Scheda dettaglio **Invia avviso con** della finestra di dialogo **Crea regola di avviso** è possibile specificare l'oggetto e il testo del messaggio utilizzati nei messaggi di avviso.
- **Utente** - Nella Scheda dettaglio **Destinazione avviso** della finestra di dialogo **Crea regola di avviso** è possibile specificare l'utente destinatario dei messaggi di avviso. Per impostazione predefinita, è selezionato il proprio ID utente.

    > [!NOTE]
    > Questa opzione è limitata agli amministratori dell'organizzazione.

## <a name="email-notifications-from-alerts"></a>Notifiche e-mail da avvisi
Le notifiche e-mail da avvisi non sono ancora attivate. Questa funzionalità verrà attivata in un aggiornamento futuro.

