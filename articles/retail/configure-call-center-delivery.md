---
title: "Configurare le modalità e le spese di consegna del servizio clienti"
description: "In questo argomento viene descritto come impostare le modalità di consegna e le spese per un ordine del servizio clienti in Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: dc2ab66bf6e3195e1ebf394f99182f59c3ee2125
ms.openlocfilehash: ebc8ee52da7d10ca18147684a0190e52a495ad5a
ms.contentlocale: it-it
ms.lasthandoff: 05/15/2018

---

# <a name="configure-call-center-delivery-modes-and-charges"></a><span data-ttu-id="c607c-103">Configurare le modalità e le spese di consegna del servizio clienti</span><span class="sxs-lookup"><span data-stu-id="c607c-103">Configure call center delivery modes and charges</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="c607c-104">Quando un ordine cliente viene inserito in Microsoft Dynamics 365 for Retail, se la persona che ha immesso l'ordine cliente è collegata a un canale di servizio clienti, la logica e le regole vengono utilizzate per convalidare la modalità di consegna e per calcolare le spese per l'ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-104">When a sales order is placed in Microsoft Dynamics 365 for Retail, if the person who entered the sales order is linked to a call center channel, logic and rules are used to validate the mode of delivery (delivery mode) and calculate charges for the order.</span></span>

<span data-ttu-id="c607c-105">Quando si crea un ordine cliente, è possibile selezionare una modalità di consegna nell'intestazione dell'ordine cliente e nelle righe dell'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-105">When you create a sales order, you can select a delivery mode on the sales order header and the sales order lines.</span></span> <span data-ttu-id="c607c-106">Per impostazione predefinita, la modalità di consegna che si seleziona nell'intestazione viene utilizzata per tutte le righe di ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-106">By default, the delivery mode that you select on the header is used for all sales order lines.</span></span> <span data-ttu-id="c607c-107">Tuttavia, è possibile sostituire la modalità di consegna predefinita nelle singole righe di vendita in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c607c-107">However, you can override the default delivery mode on individual sales lines as you require.</span></span> <span data-ttu-id="c607c-108">È inoltre possibile definire una modalità di consegna per un record cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-108">You can also define a delivery mode on a customer record.</span></span> <span data-ttu-id="c607c-109">Quando vengono creati ordini per il cliente, viene quindi utilizzata la modalità di consegna per impostazione predefinita nell'intestazione dell'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-109">Then, when orders are created for the customer, that delivery mode is used by default on the sales order header.</span></span>

<span data-ttu-id="c607c-110">Retail include funzionalità che consentono agli utenti di limitare le modalità di consegna in modo che possano essere utilizzate da un canale, le modalità di consegna che possono essere utilizzate per un prodotto e le modalità di consegna che sono valide per destinazioni di spedizione specifiche.</span><span class="sxs-lookup"><span data-stu-id="c607c-110">Retail has capabilities that let users limit the delivery modes that can be used by a channel, the delivery modes that can be used for a product, and the delivery modes that are valid for specific shipping destinations.</span></span> <span data-ttu-id="c607c-111">È possibile inoltre definire le spese in modo che le commissioni aggiuntive vengano aggiunte all'ordine di un cliente, in base alla modalità di consegna selezionata per l'ordine e al valore totale dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-111">Charges can also be defined so that additional fees are added to a customer's order, based on the delivery modes that are selected for the sales order and the total order value.</span></span>

## <a name="define-delivery-modes"></a><span data-ttu-id="c607c-112">Definire le modalità di consegna</span><span class="sxs-lookup"><span data-stu-id="c607c-112">Define delivery modes</span></span>
<span data-ttu-id="c607c-113">Prima di specificare quali modalità di consegna possono essere utilizzate per gli ordini del servizio clienti e prima di definire le regole e le spese associate, è necessario definire le modalità di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-113">Before you specify which delivery modes can be used for call center orders, and define the associated rules and charges, you must define the delivery modes.</span></span> <span data-ttu-id="c607c-114">Passare a **Vendite e marketing \> Impostazioni \> Distribuzione \> Modi di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-114">Go to **Sales and marketing \> Setup \> Distribution \> Modes of delivery**.</span></span> <span data-ttu-id="c607c-115">Selezionare **Nuovo** per creare un nuovo modo di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-115">Select **New** to create a new delivery mode.</span></span> <span data-ttu-id="c607c-116">In alternativa, selezionare un modo di consegna esistente nell'elenco e quindi selezionare **Modifica** per apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="c607c-116">Alternatively, select an existing delivery mode in the list, and then select **Edit** to make changes.</span></span>

<span data-ttu-id="c607c-117">Nel campo **Modo di consegna**, è possibile immettere qualsiasi combinazione di caratteri alfanumerici, in base ai requisiti dell'azienda.</span><span class="sxs-lookup"><span data-stu-id="c607c-117">In the **Mode of delivery** field, you can enter any combination alphanumeric characters, based on your business requirement.</span></span> <span data-ttu-id="c607c-118">È quindi possibile utilizzare il campo **Descrizione** per fornire altro contesto.</span><span class="sxs-lookup"><span data-stu-id="c607c-118">You can then use the **Description** field to provide additional context.</span></span> <span data-ttu-id="c607c-119">I campi **Gruppi di spese** e **Urgente** sono facoltativi e verranno descritti più in dettaglio più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c607c-119">The **Charges group** and **Expedite** fields are optional and will be explained in more detail later in this topic.</span></span>

<span data-ttu-id="c607c-120">Nella Scheda dettaglio **Canali di vendita al dettaglio**, aggiungere qualsiasi canale di vendita al dettaglio che deve poter utilizzare il modo di consegna quando vengono create transazioni di vendita in quel canale.</span><span class="sxs-lookup"><span data-stu-id="c607c-120">On the **Retail channels** FastTab, add any Retail channel that should be allowed to use the delivery mode when sales transactions are created in that channel.</span></span>

<span data-ttu-id="c607c-121">Nella Scheda dettaglio **Prodotti**, è possibile specificare per quali prodotti e/o categorie di prodotti è possibile specificare o meno il modo di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-121">On the **Products** FastTab, you can specify which products and/or product categories the delivery mode can and can't be used for.</span></span> <span data-ttu-id="c607c-122">Ad esempio, se un prodotto non può essere spedito per via aerea a causa delle restrizioni sul materiale pericoloso (hazmat), verificare che il prodotto o la categoria di prodotti venga esclusa da tutti i modi di consegna che implicano il trasporto aereo.</span><span class="sxs-lookup"><span data-stu-id="c607c-122">For example, if a product can't be shipped by air because of hazardous material (hazmat) restrictions, make sure that the product or product category is excluded from all delivery modes that involve air transportation.</span></span>

<span data-ttu-id="c607c-123">Nella Scheda dettaglio **Indirizzi**, è possibile specificare quali paesi o regioni o stati è possibile utilizzare o meno il modo di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-123">On the **Addresses** FastTab, you can specify which countries or regions, or states, the delivery mode can and can't be used for.</span></span> <span data-ttu-id="c607c-124">Ad esempio, gli ordini che vengono spediti alle Hawaii o in Alaska non sono idonei per la consegna per via terrestre.</span><span class="sxs-lookup"><span data-stu-id="c607c-124">For example, orders that are shipped to Hawaii or Alaska aren't eligible for ground delivery.</span></span> <span data-ttu-id="c607c-125">Questi stati devono quindi essere esclusi da qualsiasi modo di consegna che è associato a un servizio di consegna per via terrestre e devono essere inclusi in tutti i modi di consegna che sono associati a un servizio di consegna per via aerea.</span><span class="sxs-lookup"><span data-stu-id="c607c-125">Therefore, these states should be excluded from any delivery mode that is associated with a ground delivery service but included in any delivery mode that is associated with an air delivery service.</span></span>

## <a name="validate-delivery-modes-for-a-call-center-order"></a><span data-ttu-id="c607c-126">Convalidare i modi di consegna per un ordine di servizio clienti</span><span class="sxs-lookup"><span data-stu-id="c607c-126">Validate delivery modes for a call center order</span></span>
<span data-ttu-id="c607c-127">Dopo avere definito i modi di consegna, è necessario eseguire il processo batch **Elabora modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-127">After the delivery modes are defined, you must run the **Process delivery modes** batch job.</span></span> <span data-ttu-id="c607c-128">Questo processo rende disponibili i modi di consegna affinché possano essere utilizzati nei processi di ordine cliente per i canali Retail.</span><span class="sxs-lookup"><span data-stu-id="c607c-128">This job makes the delivery modes available so that they can be used in sales order processes for Retail channels.</span></span> <span data-ttu-id="c607c-129">Per eseguire il processo **Elabora modalità di consegna**, passare a **Retail \> Vendita al dettaglio IT \> Elabora modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-129">To run the **Process delivery modes** job, go to **Retail \> Retail IT \> Process delivery modes**.</span></span> <span data-ttu-id="c607c-130">È consigliabile eseguire questo processo ogni volta che si aggiungono nuovi modi di consegna a un canale di vendita al dettaglio o che si apportano modifiche alle relazioni esistenti tra modo di consegna e canale.</span><span class="sxs-lookup"><span data-stu-id="c607c-130">This job should be run any time that new delivery modes are added to a retail channel or changes are made to existing delivery mode/channel relationships.</span></span>

<span data-ttu-id="c607c-131">Dopo avere eseguito il processo batch **Elabora modalità di consegna**, è possibile passare a **Retail \> Canali \> Servizi clienti \> Tutti i servizi clienti**.</span><span class="sxs-lookup"><span data-stu-id="c607c-131">After you run the **Process delivery modes** batch job, you can go to **Retail \> Channels \> Call centers \> All call centers**.</span></span> <span data-ttu-id="c607c-132">Nella pagina **Tutti i servizi clienti**, nel riquadro delle azioni, nella scheda **Imposta**, selezionare **Modi di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-132">On the **All call centers** page, on the Action Pane, on the **Set up** tab, select **Modes of delivery**.</span></span> <span data-ttu-id="c607c-133">La pagina **Modi di consegna** elenca tutti i modi di consegna validi per il canali di servizio clienti selezionato.</span><span class="sxs-lookup"><span data-stu-id="c607c-133">The **Modes of delivery** page lists all the valid delivery modes for the selected call center channel.</span></span> <span data-ttu-id="c607c-134">Per modificare i modi di consegna esistenti o aggiungerne di nuovi, selezionare **Gestisci modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-134">To edit existing delivery modes or add new delivery modes, select **Manage modes of delivery**.</span></span> <span data-ttu-id="c607c-135">Notare che il processo **Elabora modalità di consegna** deve essere eseguito ogni volta che vengono eseguite modifiche.</span><span class="sxs-lookup"><span data-stu-id="c607c-135">Note that the **Process delivery modes** job must be run whenever changes are made.</span></span>

## <a name="define-charges-for-delivery-services"></a><span data-ttu-id="c607c-136">Definire le spese per i servizi di consegna</span><span class="sxs-lookup"><span data-stu-id="c607c-136">Define charges for delivery services</span></span>
<span data-ttu-id="c607c-137">Quando una società crea ordini cliente per i clienti, potrebbe voler aggiungere che spese che vengono calcolate automaticamente in base ai modi di consegna selezionati per gli ordini.</span><span class="sxs-lookup"><span data-stu-id="c607c-137">When sales orders are created for customers, a company might want to add charges that are automatically calculated based on the delivery modes that are selected for the order.</span></span> <span data-ttu-id="c607c-138">Queste spese possono essere configurate in modo che siano uguali per tutti i clienti e tutti i modi di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-138">These charges can be configured so that they are the same for all customers and delivery modes.</span></span> <span data-ttu-id="c607c-139">In alternativa, le spese possono variare, a seconda del cliente e/o del modo di consegna selezionati per l'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-139">Alternatively, the charges can vary, depending on the customer and/or the delivery modes that are selected for the sales order.</span></span>

<span data-ttu-id="c607c-140">Per definire le spese, passare a **Retail \> Impostazione canale \> Spese \> Spese automatiche**.</span><span class="sxs-lookup"><span data-stu-id="c607c-140">To define the charges, go to **Retail \> Channel setup \> Charges \> Auto charges**.</span></span> <span data-ttu-id="c607c-141">Selezionare **Nuovo** per aggiungere nuove spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-141">Select **New** to add new charges.</span></span> <span data-ttu-id="c607c-142">In alternativa, selezionare una voce esistente e quindi selezionare **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="c607c-142">Alternatively, select an existing entry, and then select **Edit**.</span></span>

<span data-ttu-id="c607c-143">Le spese possono essere definite in modo che vengano calcolate a livello di intestazione ordine o di righe ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-143">Charges can be defined so that they are calculated at the level of either the order header or the order lines.</span></span> <span data-ttu-id="c607c-144">Utilizzare il campo **Livello** per selezionare il livello desiderato.</span><span class="sxs-lookup"><span data-stu-id="c607c-144">Use the **Level** field to select the level desired.</span></span>

<span data-ttu-id="c607c-145">Le spese possono essere definite per un cliente specifico, un gruppo di clienti o tutti i clienti.</span><span class="sxs-lookup"><span data-stu-id="c607c-145">Charges can be defined for a specific customer, a group of customers, or all customers.</span></span> <span data-ttu-id="c607c-146">Nel campo **Codice conto** selezionare **Tabella** per definire le spese che vengono applicate solo a un cliente specifico.</span><span class="sxs-lookup"><span data-stu-id="c607c-146">In the **Account code** field, select **Table** to define charges that are applied only to a specific customer.</span></span> <span data-ttu-id="c607c-147">Selezionare **Gruppo** per definire le spese per uno gruppo di clienti specifico.</span><span class="sxs-lookup"><span data-stu-id="c607c-147">Select **Group** to define charges for a specific customer group.</span></span> <span data-ttu-id="c607c-148">Selezionare **Tutti** per applicare le spese a tutti i clienti che inseriscono un ordine cliente che utilizza il modo di consegna correlato.</span><span class="sxs-lookup"><span data-stu-id="c607c-148">Select **All** to apply the charges to every customer who places a sales order that uses the related delivery mode.</span></span> <span data-ttu-id="c607c-149">Se è stato selezionato **Tabella** o **Gruppo** nel campo **Codice conto**, selezionare il cliente o il gruppo di clienti nel campo **Relazione conto**.</span><span class="sxs-lookup"><span data-stu-id="c607c-149">If you selected **Table** or **Group** in the **Account code** field, select the customer or customer group in the **Account relation** field.</span></span>

<span data-ttu-id="c607c-150">Le spese possono essere configurate in modo che vengano applicate a un modo di consegna specifico, un gruppo di modi di consegna o a tutti i modi di consegna.</span><span class="sxs-lookup"><span data-stu-id="c607c-150">Charges can be configured so that they are applied for a specific delivery mode, a delivery mode group, or all delivery modes.</span></span> <span data-ttu-id="c607c-151">Se si seleziona **Tabella** nel campo **Codice modalità di consegna**, è necessario selezionare un modo di consegna specifico nel campo **Relazione tra modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-151">If you select **Table** in the **Mode of delivery code** field, you must select a specific delivery mode in the **Mode of delivery relation** field.</span></span> <span data-ttu-id="c607c-152">Se si seleziona **Gruppo**, è necessario selezionare un gruppo di modi di consegna nel campo **Relazione tra modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-152">If you select **Group**, you must select a delivery mode group in the **Mode of delivery relation** field.</span></span> <span data-ttu-id="c607c-153">I gruppi di modi di consegna vengono definiti in **Retail \> Impostazione canale \> Spese \> Gruppi di spese di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-153">Delivery mode groups are defined at **Retail \> Channel setup \> Charges \> Delivery charges group**.</span></span> <span data-ttu-id="c607c-154">Possono essere collegati a uno o più modi di consegna nella pagina **Modi di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-154">They can then be linked to one or more delivery modes on the **Modes of delivery** page.</span></span> <span data-ttu-id="c607c-155">Se si seleziona un gruppo quando si definiscono le spese, tutti i modi di consegna che sono collegati al gruppo di consegna selezionato utilizzando queste spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-155">If you select a group when you define charges, any delivery mode that is linked to the selected delivery group uses those charges.</span></span> <span data-ttu-id="c607c-156">Infine, se si seleziona **tutti** nel campo **Codice modalità di consegna**, tutti i modi di consegna utilizzano le spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-156">Finally, if you select **All** in the **Mode of delivery code** field, all delivery modes use the charges.</span></span> <span data-ttu-id="c607c-157">Pertanto non si seleziona un valore nel campo **Relazione tra modalità di consegna**.</span><span class="sxs-lookup"><span data-stu-id="c607c-157">Therefore, you don't select a value in the **Mode of delivery relation** field.</span></span>

<span data-ttu-id="c607c-158">Nella sezione **Righe**, è possibile definire una o più spese per valuta, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c607c-158">In the **Lines** section, you can define one or more charges by currency, as you require.</span></span> <span data-ttu-id="c607c-159">Le spese devono essere collegate a un codice spese che definisce le regole di registrazione finanziarie per le spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-159">Charges must be linked to a charges code that defines the financial posting rules for the charge.</span></span> <span data-ttu-id="c607c-160">Il campo **Categoria** viene utilizzato per definire la modalità di calcolo delle spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-160">The **Category** field is used to define how charges are calculated.</span></span> <span data-ttu-id="c607c-161">Ad esempio, se ai clienti viene addebitata un'aliquota forfettaria di $9,95 per un ordine da spedire con un modo di consegna specifico, utilizzare la categoria **Fisso**.</span><span class="sxs-lookup"><span data-stu-id="c607c-161">For example, if customers should be charged a flat rate of $9.95 to have an order shipped by a specific delivery mode, use the **Fixed** category.</span></span> <span data-ttu-id="c607c-162">Se l'azienda decide di addebitare ai clienti una percentuale del totale dell'ordine per coprire le spese di consegna, utilizzare la categoria **Percentuale**.</span><span class="sxs-lookup"><span data-stu-id="c607c-162">If the business decides to charge customers a percentage of the order total to cover the delivery charges, use the **Percent** category.</span></span> <span data-ttu-id="c607c-163">Le spese effettive ai clienti vengono definite nel campo **Valore spese**.</span><span class="sxs-lookup"><span data-stu-id="c607c-163">The actual charge to the customers is defined in the **Charges value** field.</span></span>

<span data-ttu-id="c607c-164">Le società di vendita al dettaglio spesso configurano le spese a livelli.</span><span class="sxs-lookup"><span data-stu-id="c607c-164">Retail companies often configure tiered charges.</span></span> <span data-ttu-id="c607c-165">In questo caso, l'importo che i clienti pagano per la consegna è basato sul valore dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-165">In this case, the amount that customers pay for delivery is based on the order value.</span></span> <span data-ttu-id="c607c-166">Per configurare le spese a livelli, immettere i valori nei campi **Da importo** e **A importo** oltre a definire le spese stesse nel campo **Valore spese**.</span><span class="sxs-lookup"><span data-stu-id="c607c-166">To configure tiered charges, enter values in the **From amount** and **To amount** fields in addition to defining the charge itself in the **Charges value** field.</span></span> <span data-ttu-id="c607c-167">Ad esempio, per gli ordini con un valore inferiore a $50, un rivenditore addebita $5,95 per una via terra.</span><span class="sxs-lookup"><span data-stu-id="c607c-167">For example, for orders that have a value that is less than $50, a retailer charges $5.95 for ground shipping.</span></span> <span data-ttu-id="c607c-168">Per ordini con un valore uguale o maggiore di $50, ma inferiore a $100 il rivenditore addebita $7,95.</span><span class="sxs-lookup"><span data-stu-id="c607c-168">For orders that have a value that is equal to or more than $50, but less than $100, the retailer charges $7.95.</span></span> <span data-ttu-id="c607c-169">Infine, per ordini con un valore uguale o maggiore di $100, il rivenditore offre la spedizione gratuita.</span><span class="sxs-lookup"><span data-stu-id="c607c-169">Finally, for orders that have a value that is equal to or more than $100, the retailer provides free shipping.</span></span> <span data-ttu-id="c607c-170">Nella seguente figura viene illustrata la configurazione di queste spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-170">The following illustration shows the configuration of these charges.</span></span>

![Esempio di spese a livelli fisse](media/fixedtieredcharges.png)

<span data-ttu-id="c607c-172">È possibile utilizzare un misto di categorie per le spese, in base alle proprie esigenze aziendali.</span><span class="sxs-lookup"><span data-stu-id="c607c-172">You can use a mixture of categories for charges, depending on your business requirements.</span></span> <span data-ttu-id="c607c-173">Ad esempio, per tutti gli ordini con un valore inferiore a $100, si applica un addebito fisso di $9,95 per la spedizione.</span><span class="sxs-lookup"><span data-stu-id="c607c-173">For example, for all orders that have a value that is less than $100, there is a fixed charge of $9.95 for shipping.</span></span> <span data-ttu-id="c607c-174">Quindi, per gli ordini con valore uguale o maggiore di $100, le spese di consegna vengono calcolate al tasso del 5% del valore dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-174">Then, for orders that have a value that is equal to or more than $100, delivery charges are calculated at a rate of 5 percent of the order value.</span></span> <span data-ttu-id="c607c-175">Nella seguente figura viene illustrata la configurazione di queste spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-175">The following illustration shows the configuration of these charges.</span></span>

![Esempio di spese a livelli miste](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a><span data-ttu-id="c607c-177">Applicare modi di consegna durante la registrazione di ordini in un servizio clienti</span><span class="sxs-lookup"><span data-stu-id="c607c-177">Apply delivery modes during order entry in a call center</span></span>
<span data-ttu-id="c607c-178">Quando si crea un nuovo ordine cliente, è necessario specificare un valore nel campo **Modo di consegna** nella Scheda dettaglio **Consegna** dell'intestazione dell'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-178">When a new sales order is created, a value must be specified in the **Mode of delivery** field on the **Delivery** FastTab of the sales order header.</span></span> <span data-ttu-id="c607c-179">Questo campo potrebbe essere compilato automaticamente, in base ai valori predefiniti derivati dal record del cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-179">This field might be filled in automatically, based on default values from the customer record.</span></span>

<span data-ttu-id="c607c-180">Il modo di consegna che viene definito nell'intestazione dell'ordine viene copiato automaticamente nelle righe dell'ordine cliente man mano che vengono create.</span><span class="sxs-lookup"><span data-stu-id="c607c-180">The delivery mode that is defined on the order header is automatically copied to the sales order lines as they are created.</span></span> <span data-ttu-id="c607c-181">È tuttavia possibile modificare l'impostazione del modo di consegna per una riga specifica nella scheda **Consegna** nella sezione **Dettagli riga** della pagina di registrazione dell'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-181">However, you can change the delivery mode setup for a specific line item on the **Delivery** tab in the **Line details** section of the sales order entry page.</span></span>

<span data-ttu-id="c607c-182">Se il modo di consegna selezionato non è valido per il prodotto o per l'indirizzo di consegna definito per l'ordine o la riga dell'ordine, viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c607c-182">If the selected delivery mode isn't valid for the product or the delivery address that is defined for the order or order line, you receive an error message.</span></span> <span data-ttu-id="c607c-183">È quindi necessario selezionare un modo di consegna definito per supportare la configurazione del prodotto o dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c607c-183">You must then select a delivery mode that has been defined to support that product or address configuration.</span></span>

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a><span data-ttu-id="c607c-184">Calcolo delle spese di consegna durante la registrazione dell'ordine</span><span class="sxs-lookup"><span data-stu-id="c607c-184">Calculation of delivery charges during entry of order</span></span>
<span data-ttu-id="c607c-185">Se l'impostazione **Attiva completamento ordine** viene attivata per il canale di servizio clienti, le spese di consegna vengono automaticamente calcolate per gli ordini cliente quando gli utenti selezionano **Completo**.</span><span class="sxs-lookup"><span data-stu-id="c607c-185">If the **Enable order completion** setting is turned on for your call center channel, shipping charges are automatically calculated for sales orders when users select **Complete**.</span></span> <span data-ttu-id="c607c-186">Il messaggio seguente viene visualizzato in cima alla pagina **Riepilogo ordine cliente**: "Spese a livelli calcolate".</span><span class="sxs-lookup"><span data-stu-id="c607c-186">The following message appears at the top of the **Sales order summary** page: "Tiered charges calculated."</span></span> <span data-ttu-id="c607c-187">Le spese calcolate vengono aggiunte al valore del campo **Totale vendite**.</span><span class="sxs-lookup"><span data-stu-id="c607c-187">The charges that are calculated are added to the value of the **Sales total** field.</span></span> <span data-ttu-id="c607c-188">Nella Scheda dettaglio **Importo**, il campo **Spese** mostra l'importo totale di tutte le spese che sono state calcolate per l'ordine e le righe.</span><span class="sxs-lookup"><span data-stu-id="c607c-188">On the **Amount** FastTab, the **Charges** field shows the total amount of all charges that have been calculated for the order and lines.</span></span> <span data-ttu-id="c607c-189">Per vedere una scomposizione dettagliata delle spese, selezionare **Ordine** nella pagina **Riepilogo ordine cliente**, quindi selezionare l'opzione **Spese** per visualizzare, aggiungere o modificare le spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-189">To see a more detailed breakdown of the charges, select **Order** on the **Sales order summary** page, and then select the **Charges** option to view, add, or edit the charges.</span></span> <span data-ttu-id="c607c-190">Notare che il calcolo delle spese di consegna nell'intestazione dell'ordine si basano sul modo di consegna che è collegato all'intestazione.</span><span class="sxs-lookup"><span data-stu-id="c607c-190">Note that the calculation of delivery charges on the order header is based on the delivery mode that is linked to the header.</span></span> <span data-ttu-id="c607c-191">Le spese di consegna a livello di riga vengono calcolate in base al modo di consegna che viene configurato per la riga di vendita.</span><span class="sxs-lookup"><span data-stu-id="c607c-191">Line-level delivery charges are calculated based on the delivery mode that is configured for the sales line.</span></span> <span data-ttu-id="c607c-192">Se per righe differenti vengono utilizzati più modi di consegna, è possibile applicare più spese insieme.</span><span class="sxs-lookup"><span data-stu-id="c607c-192">If multiple delivery modes are used on different lines, multiple charges might be applied and added together.</span></span> <span data-ttu-id="c607c-193">L'importo totale viene quindi mostrato nel campo **Spese** nella pagina **Riepilogo ordine cliente**.</span><span class="sxs-lookup"><span data-stu-id="c607c-193">The total amount is then shown in the **Charges** field on the **Sales order summary** page.</span></span>

<span data-ttu-id="c607c-194">Se l'impostazione **Attiva completamento ordine** è disattivato, gli utenti devono attivare manualmente il calcolo delle spese.</span><span class="sxs-lookup"><span data-stu-id="c607c-194">If the **Enable order completion** setting is turned off, users must manually trigger the calculation of charges.</span></span> <span data-ttu-id="c607c-195">Nella pagina **Ordine cliente**, nel riquadro delle azioni, nella scheda **Vendi**, nel gruppo **Calcola**, selezionare **Spese a livelli**.</span><span class="sxs-lookup"><span data-stu-id="c607c-195">On the **Sales order** page, on the Action Pane, on the **Sell** tab, in the **Calculate** group, select **Tiered charges**.</span></span> <span data-ttu-id="c607c-196">Viene visualizzato il messaggio "Spese a livelli calcolate".</span><span class="sxs-lookup"><span data-stu-id="c607c-196">The "Tiered charges calculated" message appears.</span></span> <span data-ttu-id="c607c-197">È quindi possibile selezionare l'opzione **Spese** nella scheda **Vendi** per visualizzare, modificare o eliminare le spese calcolate.</span><span class="sxs-lookup"><span data-stu-id="c607c-197">You can then select the **Charges** option on the **Sell** tab to view, edit, or delete the calculated charges.</span></span>

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a><span data-ttu-id="c607c-198">Utilizzare i modi di consegna urgenti sugli ordini del servizio clienti</span><span class="sxs-lookup"><span data-stu-id="c607c-198">Use expedited delivery modes on call center orders</span></span>
<span data-ttu-id="c607c-199">È facoltativamente possibile collegare un codice di urgenza a un modo di consegna che si configura.</span><span class="sxs-lookup"><span data-stu-id="c607c-199">You can optionally link an expedite code to any delivery mode that you configure.</span></span> <span data-ttu-id="c607c-200">Questo codice viene utilizzato come priorità di ordinamento e strumento di creazione report.</span><span class="sxs-lookup"><span data-stu-id="c607c-200">This code is used as a prioritization sorting and reporting tool.</span></span> <span data-ttu-id="c607c-201">Attualmente non determina l'aggiunta di altre commissioni da applicare all'ordine.</span><span class="sxs-lookup"><span data-stu-id="c607c-201">It doesn't currently cause additional fees to be applied to the order.</span></span> <span data-ttu-id="c607c-202">Per impostare i codici di urgenza, passare a **Vendite e marketing \> Impostazioni \> Distribuzione \> Codici urgenza**.</span><span class="sxs-lookup"><span data-stu-id="c607c-202">To set up expedite codes, go to **Sales and marketing \> Setup \> Distribution \> Expedite codes**.</span></span>

<span data-ttu-id="c607c-203">Ad esempio, per gli ordini che verranno spediti il giorno successivo per via aerea, il prelievo dal magazzino deve avvenire alle 13.00 di ogni giorno.</span><span class="sxs-lookup"><span data-stu-id="c607c-203">For example, for orders that will be shipped by next-day air, picking must be done in the warehouse by 1 PM every day.</span></span> <span data-ttu-id="c607c-204">In questo caso, è possibile creare un codice di urgenza e collegarlo a un qualsiasi modo di consegna del giorno successivo che viene configurato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c607c-204">In this case, an expedite code can be created, and that code can be linked to any next-day delivery mode that is configured in the system.</span></span> <span data-ttu-id="c607c-205">Quando il magazzino crea l'ondata di prelievi, è possibile utilizzare il codice di urgenza appropriato nel campo **Urgente** come filtro, in modo che il prelievo venga eseguito solo per gli ordini con modi di consegna collegati a quel codice.</span><span class="sxs-lookup"><span data-stu-id="c607c-205">When the warehouse creates its pick wave, the appropriate expedite code in the **Expedite** field can be used as a filter, so that picking is run only for orders that have delivery modes that are linked to that code.</span></span>

<span data-ttu-id="c607c-206">Inoltre, quando viene immesso un ordine di servizio clienti, è possibile applicare manualmente un codice di urgenza all'intestazione dell'ordine cliente o a una singola riga dell'ordine cliente.</span><span class="sxs-lookup"><span data-stu-id="c607c-206">Additionally, when a call center order is entered, an expedite code can be manually applied either to the sales order header or to an individual sales order line.</span></span> <span data-ttu-id="c607c-207">Anche in questo caso, il codice può essere utilizzato per l'ordinamento e i report.</span><span class="sxs-lookup"><span data-stu-id="c607c-207">Again, the code can be used for sorting or reporting purposes.</span></span> <span data-ttu-id="c607c-208">Talvolta un ordine deve essere gestito con attenzione a causa di un problema con il servizio clienti.</span><span class="sxs-lookup"><span data-stu-id="c607c-208">Sometimes, an order must be handled carefully because of a customer service issue.</span></span> <span data-ttu-id="c607c-209">In questo caso, è possibile applicare un codice di urgenza specifico all'intestazione o alle righe ordine per aiutare a identificare e ad assegnare una priorità all'ordine durante il processo di evasione.</span><span class="sxs-lookup"><span data-stu-id="c607c-209">In this case, a specific expedite code can be applied to the order header or lines to help identify and prioritize the order during the fulfillment process.</span></span>
