---
title: "Creare relazioni di attività di assistenza tecnica"
description: "È possibile associare le attività di assistenza tecnica a contratti di assistenza o ordini di assistenza in modo da descrivere l'attività di assistenza tecnica da completare per il contratto o l'ordine."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
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
ms.openlocfilehash: 0892161605401420c0817b3b644271357446a99b
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-task-relations"></a><span data-ttu-id="3ba0d-103">Creare relazioni di attività di assistenza tecnica</span><span class="sxs-lookup"><span data-stu-id="3ba0d-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ba0d-104">È possibile associare le attività di assistenza tecnica a contratti di assistenza o ordini di assistenza in modo da descrivere l'attività di assistenza tecnica da completare per il contratto o l'ordine.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="3ba0d-105">Queste informazioni sono disponibili ai tecnici e ai clienti.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="3ba0d-106">Creare una relazione con un contratto di assistenza</span><span class="sxs-lookup"><span data-stu-id="3ba0d-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="3ba0d-107">Fare clic su **Gestione assistenza** \> **Comune** \> **Contratti di assistenza** \> **Contratti di assistenza**.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="3ba0d-108">Selezionare un contratto di assistenza esistente o crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="3ba0d-109">Nel riquadro azioni fare clic sul pulsante **Attività di assistenza tecnica**.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="3ba0d-110">Nel modulo **Attività di assistenza tecnica** premere CTRL+N per creare una nuova riga, quindi selezionare dall'elenco **Attività di assistenza tecnica** l'attività di assistenza tecnica da collegare al contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="3ba0d-111">Nella scheda **Descrizione** immettere le descrizioni di note interne o esterne nei campi a testo libero.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="3ba0d-112">Chiudere il modulo per salvare il record.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-112">Close the form to save the record.</span></span>

<span data-ttu-id="3ba0d-113">Ripetere la procedura finché non saranno state create tutte le relazioni di attività di assistenza tecnica necessarie per il contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="3ba0d-114">Sarà quindi possibile specificare queste attività da qualsiasi riga del contratto collegato.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="3ba0d-115">Una relazione di attività di assistenza tecnica creata in un contratto di assistenza è disponibile da tutti gli ordini di assistenza collegati a quel contratto.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="3ba0d-116">Creare una relazione con un ordine di assistenza</span><span class="sxs-lookup"><span data-stu-id="3ba0d-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="3ba0d-117">Fare clic su **Gestione assistenza** \> **Comune** \> **Ordini di assistenza** \> **Ordini di assistenza**.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3ba0d-118">Selezionare un ordine di assistenza esistente o crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="3ba0d-119">Nel riquadro azioni fare clic sul pulsante **Attività di assistenza tecnica**.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="3ba0d-120">Nel modulo **Attività di assistenza tecnica** premere CTRL+N per creare una nuova riga, quindi selezionare dall'elenco **Attività di assistenza tecnica** le attività di assistenza tecnica da collegare al contratto di assistenza.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="3ba0d-121">Nella scheda **Descrizione** immettere le descrizioni di note interne o esterne nei campi a testo libero.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="3ba0d-122">Chiudere il modulo per salvare il record.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-122">Close the form to save the record.</span></span>

<span data-ttu-id="3ba0d-123">Ripetere la procedura finché non saranno state create tutte le relazioni di attività di assistenza tecnica necessarie per l'ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="3ba0d-124">Sarà quindi possibile, quando si creano righe dell'ordine di assistenza, selezionare l'attività per la quale è stata creata la relazione.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="3ba0d-125">Le relazioni di attività di assistenza tecnica create in un ordine di assistenza sono disponibili nell'ordine stesso.</span><span class="sxs-lookup"><span data-stu-id="3ba0d-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ba0d-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3ba0d-126">See also</span></span>

[<span data-ttu-id="3ba0d-127">Attività di assistenza tecnica </span><span class="sxs-lookup"><span data-stu-id="3ba0d-127">Service tasks</span></span>](service-tasks.md)


  


