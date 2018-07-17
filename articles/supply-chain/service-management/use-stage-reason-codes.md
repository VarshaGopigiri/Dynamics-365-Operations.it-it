---
title: Utilizzare i codici motivo fase
description: I codici motivo vengono utilizzati per indicare il motivo dell'annullamento di un accordo sui livelli di servizio (SLA, Service Level Agreement) o il motivo del superamento del limite di tempo definito nell'accordo stesso.
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e42172fe1b484b91e9a3e3d05d438e7e9b0b0eb4
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---


# <a name="use-stage-reason-codes"></a><span data-ttu-id="8ef3b-103">Utilizzare i codici motivo fase</span><span class="sxs-lookup"><span data-stu-id="8ef3b-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8ef3b-104">I codici motivo vengono utilizzati per indicare il motivo dell'annullamento di un accordo sui livelli di servizio (SLA, Service Level Agreement) o il motivo del superamento del limite di tempo definito nell'accordo stesso.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="8ef3b-105">È inoltre possibile specificare che è necessario un codice motivo quando viene risolto un contratto di servizio, o se il limite di tempo supera il tempo specificato nel contratto di servizio per l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="8ef3b-106">Se è stato specificato che è necessario specificare un codice motivo, è necessario immettere un codice motivo nelle seguenti situazioni:</span><span class="sxs-lookup"><span data-stu-id="8ef3b-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="8ef3b-107">Quando un ordine di assistenza viene spostato in una fase durante la quale viene interrotta la registrazione delle ore a fronte dell'accordo sui livelli di servizio per l'ordine stesso.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="8ef3b-108">Quando l'ordine di assistenza viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="8ef3b-109">Quando la registrazione delle ore viene interrotta manualmente.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="8ef3b-110">Imposta i codici causale</span><span class="sxs-lookup"><span data-stu-id="8ef3b-110">Set up reason codes</span></span>

1.  <span data-ttu-id="8ef3b-111">Fare clic su **Gestione assistenza** \> **Impostazione** \> **Ordini di assistenza** \> **Codici motivo fase**.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="8ef3b-112">Nel modulo **Codici motivo fase** fare clic su **Nuovo** per creare un nuovo codice motivo fase.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="8ef3b-113">Nel campo **Codici motivo fase** immettere un codice motivo fase univoco.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="8ef3b-114">Nel campo **Descrizione** immettere una descrizione del codice motivo fase.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="8ef3b-115">Chiudere il modulo per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="8ef3b-116">Richiedere l'indicazione di codici motivo in caso di annullamento di un accordo sui livelli di servizio</span><span class="sxs-lookup"><span data-stu-id="8ef3b-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="8ef3b-117">Fare clic su **Gestione assistenza** \> **Impostazione** \> **Parametri di gestione assistenza**.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="8ef3b-118">Nel modulo **Parametri di gestione assistenza**, fare clic sul collegamento **Generale** e selezionare la casella di controllo **Codice motivo per annullamento**.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="8ef3b-119">Richiedere i codici motivo quando un ordine di assistenza supera il limite di tempo stabilito dall'accordo sui livelli di servizio</span><span class="sxs-lookup"><span data-stu-id="8ef3b-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="8ef3b-120">Fare clic su **Gestione assistenza** \> **Impostazione** \> **Parametri di gestione assistenza**.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="8ef3b-121">Nel modulo **Parametri di gestione assistenza**, fare clic sul collegamento **Generale** e selezionare la casella di controllo **Codice motivo per superamento tempo massimo**.</span><span class="sxs-lookup"><span data-stu-id="8ef3b-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ef3b-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8ef3b-122">See also</span></span>

[<span data-ttu-id="8ef3b-123">Avviare e interrompere la registrazione dell'ora per un ordine di assistenza</span><span class="sxs-lookup"><span data-stu-id="8ef3b-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


