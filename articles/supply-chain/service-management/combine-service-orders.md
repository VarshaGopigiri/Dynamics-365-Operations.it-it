---
title: Combina ordini di assistenza
description: "È possibile combinare ordini di assistenza"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: it-it
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a>Combina ordini di assistenza   

[!include [banner](../includes/banner.md)]


Quando si creano automaticamente le righe dell'ordine di assistenza nel modulo **Contratti di assistenza**, è possibile scegliere una delle opzioni seguenti per specificare la modalità di raggruppamento desiderata:

  - **In base al contratto di assistenza**

  - **In base all'attività di assistenza**

  - **In base al dipendente**

  - **In base all'oggetto assistenza**

## <a name="example"></a>Esempio

Viene creato un contratto di assistenza con data di inizio il 31/03/2007. Nel campo **Combina ordini di assistenza** specificare **In base all'oggetto assistenza**. Vengono quindi create le seguenti righe del contratto di assistenza:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Numero riga contratto</p></th>
<th><p>Tipo di transazione</p></th>
<th><p>descrizione</p></th>
<th><p>Intervallo</p></th>
<th><p>Oggetto assistenza</p></th>
<th><p>Data di inizio</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Ore</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Ogni settimana</p></td>
<td><p>X-1</p></td>
<td><p>01/04/2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Ore</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Bisettimanale</p></td>
<td><p>X-2</p></td>
<td><p>01/04/2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Ore</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Ogni settimana</p></td>
<td><p>X-2</p></td>
<td><p>01/04/2007</p></td>
</tr>
</tbody>
</table>


Non viene specificato alcun intervallo di tempo per le righe del contratto di assistenza. Di conseguenza, le righe degli ordini di assistenza non verranno spostate dal giorno calcolato in cui cadono.

Vengono quindi generate le righe degli ordini di assistenza per il periodo compreso tra il 01/04/2007 e il 30/04/2007 mediante il modulo **Crea ordini di assistenza**.

Vengono creati complessivamente 10 ordini di assistenza. Poiché l'impostazione selezionata per la combinazione degli ordini di assistenza è **In base all'oggetto assistenza**, per tutti gli ordini di assistenza creati sono presenti solo righe con un oggetto assistenza specifico. Le righe degli ordini di assistenza generate in base al contratto di assistenza e con la stessa data di assistenza e lo stesso oggetto vengono combinate in un unico ordine di assistenza.


> [!NOTE]
> <P>In questo esempio il calendario specificato nel modulo <STRONG>Parametri di gestione assistenza</STRONG> non prevede giorni di chiusura.</P>



Ulteriori raggruppamenti delle righe negli ordini di assistenza vengono eseguiti in base agli intervalli di tempo specificati nelle righe del contratto di assistenza.

## <a name="see-also"></a>Vedere anche

[Creare ordini di assistenza automaticamente](create-service-orders-automatically.md)

  



