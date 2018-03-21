---
title: Modelli di assistenza
description: "È possibile definire un contratto di assistenza come modello e copiare in seguito le righe del modello in un altro contratto di assistenza o in un ordine di assistenza."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: 09f2da382cd7f3e0e3d4bfa389e9cdf74f00b501
ms.openlocfilehash: ade518095b77141fb31b597a955dd23aaae119d7
ms.contentlocale: it-it
ms.lasthandoff: 02/27/2018

---

# <a name="service-templates"></a><span data-ttu-id="9fff2-103">Modelli di assistenza</span><span class="sxs-lookup"><span data-stu-id="9fff2-103">Service templates</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9fff2-104">È possibile definire un contratto di assistenza come modello e copiare in seguito le righe del modello in un altro contratto di assistenza o in un ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9fff2-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="9fff2-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fff2-105">Example</span></span>

<span data-ttu-id="9fff2-106">Un cliente al quale si fornisce assistenza dispone di montacarichi identici presso cinque sedi diverse.</span><span class="sxs-lookup"><span data-stu-id="9fff2-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="9fff2-107">Per il cliente si desidera impostare cinque contratti di assistenza, uno per ciascuna sede.</span><span class="sxs-lookup"><span data-stu-id="9fff2-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="9fff2-108">Per limitare le operazioni ripetitive dell'attività di impostazione e per assicurarsi che le informazioni contenute nei contratti di assistenza siano identiche, è possibile creare un contratto di assistenza e specificarlo come modello delle attività di assistenza relative ai montacarichi.</span><span class="sxs-lookup"><span data-stu-id="9fff2-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="9fff2-109">È ora possibile copiare le righe del modello nei cinque nuovi contratti di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9fff2-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="9fff2-110">Crea un modello</span><span class="sxs-lookup"><span data-stu-id="9fff2-110">Create a template</span></span>

<span data-ttu-id="9fff2-111">Per creare un modello di assistenza, creare un contratto di assistenza, creare le righe desiderate all'interno di esso, quindi collegare il contratto a un gruppo di modelli di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9fff2-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="9fff2-112">È possibile definire un contratto di assistenza come modello solo se ad esso non è collegato alcun ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9fff2-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="9fff2-113">Non è inoltre possibile generare ordini di assistenza da contratti di assistenza definiti come modelli.</span><span class="sxs-lookup"><span data-stu-id="9fff2-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="9fff2-114">Copia righe modello</span><span class="sxs-lookup"><span data-stu-id="9fff2-114">Copy template lines</span></span>

<span data-ttu-id="9fff2-115">È possibile copiare le righe di un modello di assistenza in un altro contratto di assistenza o in un ordine di assistenza.</span><span class="sxs-lookup"><span data-stu-id="9fff2-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="9fff2-116">Quando si copiano le righe del modello in un ordine o in un contratto di assistenza, i gruppi di modelli compaiono in una visualizzazione struttura in cui è possibile espandere ciascun gruppo.</span><span class="sxs-lookup"><span data-stu-id="9fff2-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="9fff2-117">Questo tipo di visualizzazione consente di vedere ogni modello e ogni riga del modello.</span><span class="sxs-lookup"><span data-stu-id="9fff2-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="9fff2-118">Per determinare in modo più semplice le righe del modello da copiare, raggruppare i modelli assegnando ai gruppi un nome che rifletta lo scopo dei modelli stessi.</span><span class="sxs-lookup"><span data-stu-id="9fff2-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fff2-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fff2-119">Related topics</span></span>

[<span data-ttu-id="9fff2-120">Copiare le righe di modelli di assistenza</span><span class="sxs-lookup"><span data-stu-id="9fff2-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
