---
title: Tenere traccia dei risultati dei report generati e confrontarli con i valori di base
description: In questo argomento vengono fornite informazioni su come confrontare i risultati dei report di ER generati con i valori di report di base.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: it-it
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a><span data-ttu-id="70357-103">Tenere traccia dei risultati dei report generati e confrontarli con i valori di base</span><span class="sxs-lookup"><span data-stu-id="70357-103">Trace generated report results and compare them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="70357-104">È possibile tenere traccia dei risultati dei formati di ER che generano i documenti elettronici in uscita.</span><span class="sxs-lookup"><span data-stu-id="70357-104">You can trace the results of ER formats that generate outgoing electronic documents.</span></span> <span data-ttu-id="70357-105">Quando si attiva la generazione della traccia (parametro dell'utente ER **Esegui in modalità di debug**), viene generato un nuovo record di traccia nel registro di esecuzione del formato di ER ogni volta che viene eseguito un report di ER.</span><span class="sxs-lookup"><span data-stu-id="70357-105">When trace generation is turned on (ER user parameter **Run in debug mode**), a new trace record is generated in the ER format execution log every time that an ER report is run.</span></span> <span data-ttu-id="70357-106">I dettagli seguenti vengono archiviati in ogni traccia generata:</span><span class="sxs-lookup"><span data-stu-id="70357-106">The following details are stored in each trace that is generated:</span></span>

- <span data-ttu-id="70357-107">Tutti gli avvisi generati dalle regole di convalida</span><span class="sxs-lookup"><span data-stu-id="70357-107">All warnings that were generated by validation rules</span></span>
- <span data-ttu-id="70357-108">Tutti gli errori generati dalle regole di convalida</span><span class="sxs-lookup"><span data-stu-id="70357-108">All errors that were generated by validation rules</span></span> 
- <span data-ttu-id="70357-109">Tutti i file generati archiviati come allegati del record di traccia</span><span class="sxs-lookup"><span data-stu-id="70357-109">All generated files that are stored as attachments of the trace record</span></span>

<span data-ttu-id="70357-110">È possibile archiviare i singoli file di applicazione di base per qualsiasi formato di ER.</span><span class="sxs-lookup"><span data-stu-id="70357-110">You can store individual baseline application files for any ER format.</span></span> <span data-ttu-id="70357-111">I file vengono considerati file di base quando descrivono i risultati previsti di report che vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="70357-111">Files are considered baseline files when they describe the expected results of reports that are run.</span></span> <span data-ttu-id="70357-112">Se un file di base è disponibile per un formato di ER eseguito mentre la generazione di traccia era attivata, la traccia archivia, oltre ai dettagli menzionati in precedenza, il risultato del confronto tra il documento elettronico generato e il file di base.</span><span class="sxs-lookup"><span data-stu-id="70357-112">If a baseline file is available for an ER format that was run while trace generation was turned on, the trace stores, in addition to the details that were mentioned earlier, the result of the comparison of the generated electronic document to the baseline file.</span></span> <span data-ttu-id="70357-113">Con un semplice clic è inoltre possibile ottenere il documento elettronico generato e il relativo file di base in un unico file con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="70357-113">In one click, you can also get the generated electronic document and its baseline file in a single zip file.</span></span> <span data-ttu-id="70357-114">È quindi possibile effettuare il confronto dettagliato utilizzando uno strumento esterno come Windiff.</span><span class="sxs-lookup"><span data-stu-id="70357-114">You can then do detailed comparison by using an external tool such as Windiff.</span></span>

<span data-ttu-id="70357-115">È possibile valutare la traccia per analizzare se i documenti elettronici generati includono il contenuto previsto.</span><span class="sxs-lookup"><span data-stu-id="70357-115">You can evaluate the trace to analyze whether the electronic documents that are generated include the expected content.</span></span> <span data-ttu-id="70357-116">È possibile effettuare questa valutazione in un ambiente di test di accettazione utenti (UAT) quando viene modificata la base di codice, ad esempio quando è stata effettuata la migrazione a una nuova istanza dell'applicazione, sono stati installati gli hotfix o sono state distribuite modifiche al codice.</span><span class="sxs-lookup"><span data-stu-id="70357-116">You can do this evaluation in a user acceptance testing (UAT) environment when the code base has been changed (for example, when you migrated to a new instance of the application, installed hotfix packages, or deployed code modifications).</span></span> <span data-ttu-id="70357-117">In questo modo, è possibile assicurarsi che la valutazione non influisca sull'esecuzione dei report di ER utilizzati.</span><span class="sxs-lookup"><span data-stu-id="70357-117">In this way, you can make sure that the evaluation doesn't affect the execution of ER reports that are used.</span></span> <span data-ttu-id="70357-118">Per molti report di ER, la valutazione può essere effettuata in modalità automatica.</span><span class="sxs-lookup"><span data-stu-id="70357-118">For many ER reports, the evaluation can be done in unattended mode.</span></span>

<span data-ttu-id="70357-119">Per ulteriori informazioni su questa funzionalità,, riprodurre le guide attività **ER Generare report e confrontare i risultati (Parte 1)** e **ER Generare report e confrontare i risultati (Parte 2)**, che fanno parte del processo aziendale **7.5.4.3 Eseguire test di soluzioni/servizi IT (10679)** e che possono essere scaricate dall'[Area download Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="70357-119">To learn more about this feature, play the **ER Generate reports and compare results (Part 1)** and **ER Generate reports and compare results (Part 2)** task guides, which are part of the **7.5.4.3 Test IT services/solutions (10679)** business process, and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="70357-120">Queste guide attività illustrano in dettaglio il processo di configurazione del framework di ER per utilizzare file di base per valutare documenti elettronici generati.</span><span class="sxs-lookup"><span data-stu-id="70357-120">These task guides walk you through the process of configuring the ER framework to use baseline files to evaluate generated electronic documents.</span></span>
