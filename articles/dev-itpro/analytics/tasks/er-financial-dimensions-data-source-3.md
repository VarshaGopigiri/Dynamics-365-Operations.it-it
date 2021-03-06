--- 
title: Progettare un report per utilizzare le dimensioni finanziarie come origine dati per la creazione di report elettronici (ER)
description: "I passaggi seguenti descrivono come un utente con ruolo di amministratore di sistema o di sviluppatore per la creazione di report elettronici può configurare un modello per la creazione di report elettronici in modo che utilizzi dimensioni finanziarie come origine dati per i report elettronici."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: it-it
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Progettare un report per utilizzare le dimensioni finanziarie come origine dati per la creazione di report elettronici (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

I passaggi seguenti descrivono come un utente con ruolo di amministratore di sistema o di sviluppatore per la creazione di report elettronici può configurare un modello per la creazione di report elettronici in modo che utilizzi dimensioni finanziarie come origine dati per i report elettronici. Questi passaggi possono essere eseguiti in qualsiasi società.

Per effettuare questi passaggi, è innanzitutto necessario completare i passaggi nella procedura 'ER Usare dimensioni finanziarie come origine dati (parte 2: mapping del modello)'.


## <a name="design-a-report-to-present-financial-dimensions"></a>Progettare un report per presentare dimensioni finanziarie
1. Passare a Amministrazione organizzazione > Reporting elettronico > Configurazioni.
2. Nella struttura selezionare 'Modello di esempio dimensioni finanziarie'.
3. Fare clic su Crea configurazione per aprire la finestra di dialogo a discesa .
4. Nel campo Nuovo immettere 'Formato basato sul modello dati Modello di esempio dimensioni finanziarie'.
    * Utilizzare il modello creato in anticipo come origine dati per il nuovo report.  
5. Nel campo Nome digitare 'Report dei giornali di registrazione di contabilità generale'.
6. Selezionare Voce nel campo Definizione modello dati.
7. Fare clic su Crea configurazione.
8. Fare clic su Progettazione.
9. Fare clic su Aggiungi radice per aprire la finestra di dialogo a discesa.
10. Nella struttura selezionare "XML\Elemento".
11. Digitare 'Nodo principale' nel campo Nome.
12. Fare clic su OK.
13. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
14. Nella struttura selezionare "XML\Attributo".
15. Nel campo Nome digitare "Società".
16. Fare clic su OK.
17. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
18. Nella struttura selezionare "XML\Elemento".
19. Digitare 'Giornale di registrazione' nel campo Nome.
20. Fare clic su OK.
21. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML'.
22. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
23. Nella struttura selezionare "XML\Attributo".
24. Digitare 'Batch'. nel campo Nome.
25. Fare clic su OK.
26. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
27. Nella struttura selezionare "XML\Elemento".
28. Nel campo Nome digitare 'Transazione'.
29. Fare clic su OK.
30. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML'.
31. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
32. Nella struttura selezionare "XML\Attributo".
33. Digitare 'Giustificativo' nel campo Nome.
34. Fare clic su OK.
35. Fare clic su Aggiungi attributo.
36. Digitare 'Data' nel campo Nome.
37. Fare clic su OK.
38. Fare clic su Aggiungi attributo.
39. Nel campo Nome digitare "Valuta".
40. Fare clic su OK.
41. Fare clic su Aggiungi attributo.
42. Nel campo Nome digitare 'Dare'.
43. Fare clic su OK.
44. Fare clic su Aggiungi attributo.
45. Nel campo Nome digitare 'Avere'.
46. Fare clic su OK.
47. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
48. Nella struttura selezionare "XML\Elemento".
49. Digitare 'Dimensioni' nel campo Nome.
50. Fare clic su OK.
51. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dimensioni: Elemento XML'.
52. Fare clic su Aggiungi per aprire la finestra di dialogo a discesa.
53. Nella struttura selezionare "XML\Attributo".
54. Digitare 'Codice' nel campo Nome.
55. Fare clic su OK.
56. Fare clic su Aggiungi attributo.
57. Nel campo Nome digitare 'Valore'.
58. Fare clic su OK.
59. Fare clic su Aggiungi attributo.
60. Nel campo Nome digitare 'Descrizione'.
61. Fare clic su OK.

## <a name="map-report-elements-to-data-sources"></a>Mappare gli elementi del report alle origini dati
1. Fare clic sulla scheda Mapping.
2. Nella struttura, espandere 'modello: Modello dati Modello di esempio dimensioni finanziarie'.
3. Nella struttura, espandere 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record'.
4. Nella struttura, espandere 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record'.
5. Nella struttura, espandere 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dati dimensioni: Elenco di record'.
6. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dimensioni: Elemento XML\Descrizione: Attributo XML'.
7. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dati dimensioni: Elenco di record\Descrizione: Stringa'.
8. Fare clic su Associa.
9. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dimensioni: Elemento XML\Valore: Attributo XML'.
10. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dati dimensioni: Elenco di record\Codice: Stringa'.
11. Fare clic su Associa.
12. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dimensioni: Elemento XML\Codice: Attributo XML'.
13. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dati dimensioni: Elenco di record\Nome: Stringa'.
14. Fare clic su Associa.
15. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dati dimensioni: Elenco di record'.
16. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dimensioni: Elemento XML'.
17. Fare clic su Associa.
18. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Avere: Attributo XML'.
19. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Avere: Reale'.
20. Fare clic su Associa.
21. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Dare: Attributo XML'.
22. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Dare: Reale'.
23. Fare clic su Associa.
24. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Valuta: Attributo XML'.
25. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Valuta: Stringa'.
26. Fare clic su Associa.
27. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Data: Attributo XML'.
28. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Data: Data'.
29. Fare clic su Associa.
30. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML\Giustificativo: Attributo XML'.
31. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record\Giustificativo: Stringa'.
32. Fare clic su Associa.
33. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Transazione: Elemento XML'.
34. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Transazione: Elenco di record'.
35. Fare clic su Associa.
36. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML\Batch: Attributo XML'.
37. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record\Batch: Stringa'.
38. Fare clic su Associa.
39. Nella struttura selezionare 'Nodo principale: Elemento XML\Giornale di registrazione: Elemento XML'.
40. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Giornale di registrazione: Elenco di record'.
41. Fare clic su Associa.
42. Nella struttura selezionare 'Nodo principale: Elemento XML\Società: Attributo XML'.
43. Nella struttura, selezionare 'modello: Modello dati Modello di esempio dimensioni finanziarie\Società: Stringa'.
44. Fare clic su Associa.
45. Fare clic su Salva.
46. Chiudere la pagina.


