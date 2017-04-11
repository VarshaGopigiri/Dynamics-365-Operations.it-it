---
title: Impostazioni di visualizzazione per il dispositivo mobile del magazzino
description: In questo articolo viene descritto come impostare l&quot;aspetto di visualizzazione del dispositivo mobile e come mappare i tasti di scelta rapida ai controlli, ad esempio i pulsanti.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Impostazioni di visualizzazione per il dispositivo mobile del magazzino

In questo articolo viene descritto come impostare l'aspetto di visualizzazione del dispositivo mobile e come mappare i tasti di scelta rapida ai controlli, ad esempio i pulsanti. 

Questo articolo viene applicato alle funzionalità per le operazioni di magazzino avanzate in Gestione magazzino. I dispositivi mobili possono essere utilizzati per molte delle attività che gli addetti magazzino devono svolgere.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Specificare gli stili e eseguire il mapping delle scelte rapide
Nell'ambito della configurazione dei dispositivi mobili, è possibile definire layout differenti per questi dispositivi. A questo scopo, è necessario conoscere il nome del file CSS e del file della pagina ASPX. I file predefiniti vengono impostati nell'ambito dell'installazione del Portale dei dispositivi mobili del magazzino. Se non si conoscono i nomi file, chiedere all'amministratore di sistema. È possibile definire un nuovo stile nella pagina **Impostazioni visualizzazione dispositivo mobile**:

-    Nel campo **File CSS** immettere il nome del file CSS. Includere l'estensione del nome del file .css.
-   Nel campo **Visualizzazione impostazioni dispositivo mobile** specificare il file ASPX. **Non** includere l'estensione del nome del file .aspx.

I file CSS e ASPX devono trovarsi in una specifica directory, affinché l'applicazione Internet Information Services (IIS) riesca a caricarli. Potrebbe essere utile definire differenti file CSS se si esegue la funzionalità dei dispositivi mobili in browser differenti o in differenti generi di hardware che richiedono un differente controllo del layout. Le impostazioni semplici, quali il colore di sfondo, il tipo di carattere e la dimensione del carattere per il testo, la larghezza e il comportamento dei pulsanti, possono essere facilmente controllate da un utilizzo differente dei file CSS. Il file ASPX viene utilizzato per visualizzare il sito mobile nell'applicazione ASP.NET sul lato server. Il file controlla il modo in cui viene disposta la struttura complessiva dell'HTML. È buona norma personalizzare questa funzionalità solo in caso di seri problemi strutturali con HTML e JavaScript e nel caso sia necessario modificare questo codice per dispositivi specifici. Per eseguire il mapping dei controlli HTML nella pagina dei dispositivi mobili alle scelte rapide da tastiera, nella pagina **Impostazioni visualizzazione dispositivo mobile**, nel campo **Tasto di scelta rapida**, assegnare i codici numerici per i tasti. È possibile utilizzare il menu **Visualizza codici per i tasti di scelta rapida** nel dispositivo mobile per trovare i codici di carattere numerici. Si noti che i mapping possono differire a seconda dell'hardware utilizzato. È necessario utilizzare la sintassi seguente per creare il mapping:

&lt;selezionare il codice&gt;di =key&lt;di nome (&gt;nome chiave&lt;)&gt;;

Di seguito vengono descritte le parti della sintassi:

-   **&lt;nome di controllo&gt;** il contatto del controllo, ad esempio un pulsante) che viene aggiunto in formato HTML.
-   ** (&lt;nome chiave&gt;) ** immettere il nome della chiave di mappature tastiera che si sta creando il collegamento.
-   **&lt;Codice chiave&gt;** il codice carattere numerico per la chiave da utilizzare come tasto di scelta rapida.

Ecco un esempio:

Annulla(Esc)=27; Full(F2)=113

In tutte le pagine che includono il pulsante **Annulla**, il pulsante avrà il testo:

**Annulla (ESC)**

La pressione del tasto ESC sulla tastiera attiverà il pulsante **Annulla**. Per applicare le impostazioni di scelta rapida e di stile a uno specifico dispositivo, è necessario creare un mapping nel campo **Criteri**. È necessario utilizzare un'espressione regolare .NET per creare il mapping e l'espressione deve essere costituita da tre sezioni separate da una barra verticale (|), come mostrato qui:

Host&lt;l'indirizzo Internet di Request.UserHostAddress=user&gt;_=_Nome host&lt;di HostName=user&gt;_=_Agente&lt;di Request.UserAgent=user&gt;

Di seguito vengono descritte le parti dell'espressione:

-   **&lt;address host dell'&gt;utente ** - un'espressione rettificare .NET che corrisponde l'indirizzo IP del richiedente.
-   **&lt;nome host di l&gt;** - un'espressione rettificare .NET che corrisponde al nome di rete del richiedente.
-   **&lt;user&gt;agent ** - un'espressione rettificare .NET che corrisponde all'identificatore del browser che utilizza il richiedente.

Nel seguente esempio viene abilitato l'utilizzo di Internet Explorer 8:

Request.UserHostAddress=.\*_=_HostName=.\*_=_Request.UserAgent=MSIE\\s8\\.0

È possibile utilizzare il menu **Visualizza configurazione server per impostazioni di visualizzazione** nel dispositivo mobile per trovare le informazioni sull'impostazione.

## <a name="define-text-colors-for-messages"></a>Definire i colori del testo per i messaggi
È possibile utilizzare la pagina **Colori testo del dispositivo mobile** per controllare i vari colori che sono utilizzati nei messaggi generati dal sistema, quali i messaggi di errore. Ad esempio, il colore del testo può indicare lo scopo o la gravità del messaggio. Vengono mostrati i seguenti tipi di messaggi.

| Tipo di messaggio | Descrizione                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valori predefiniti      | I messaggi predefiniti utilizzano le impostazioni di colore predefinite per tutti i messaggi, come definito dal file CSS per il Portale dei dispositivi mobili del magazzino.                                                   |
| Errore        | I messaggi di errore indicano un problema che l'utente deve risolvere prima di poter continuare.                                                                                             |
| Operazione completata      | I messaggi di operazione completata confermano il completamento di un'azione.                                                                                                                                |
| Avviso      | I messaggi di avviso informano il lavoratore della presenza di un problema o di un problema che potrebbe verificarsi qualora il lavoratore continuasse l'operazione. Tuttavia, non è necessario che il lavoratore risolva il problema per continuare. |

Per selezionare il colore, nella pagina **Seleziona colore**, fare clic sulla tavolozza o digitare un codice colore esadecimale.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Definire il formato della data da utilizzare sui dispositivi mobili
È possibile estendere l'elenco dei formati della data accettati per ogni installazione. Questa funzionalità può essere utile se, ad esempio, si desidera impostare un formato che semplifica l'immissione di date in un dispositivo mobile. Il formato predefinito è determinato dalla lingua predefinita dell'utente, la quale viene specificata nel campo **Lingua** della pagina **Opzioni utente**. La stessa pagina viene inoltre utilizzata per associare un dipendente con un utente specifico di lavoro del magazzino.) ** nota: ** I dispositivi mobili portali del magazzino non viene utilizzata l'impostazione ** tempo di date e formato numerico ** del campo ** preferenze di paese e della lingua ** nella pagina. Per modificare un formato di data, è necessario acquisire familiarità con le espressioni regolari in Microsoft .NET Framework. Per ulteriori informazioni, vedere [Espressioni regolari di .NET Framework](http://go.microsoft.com/fwlink/?LinkId=391260). Per definire i formati di date, modificare il file di Dates.ini situato le impostazioni contente\\Dates.ini\\sul server del portale dei dispositivi mobili di magazzino. Questo file utilizza le espressioni regolari .NET per specificare il formato di data. L'espressione regolare deve contenere sottoespressioni che creano gruppi denominati per giorno, mese e anno (GGMMAA), come mostrato nell'esempio che segue:

^ (?&lt;giorno&gt;\\d {2} (?)&lt;mese&gt;\\d {2} (?)&lt;anno&gt;\\d {2} EUR)

Ogni sottoespressione richiede una o due cifre per il giorno e il mese e una o quattro cifre per l'anno. Ad esempio, la seguente sottoespressione definisce un gruppo denominato per un anno e richiede un minimo di due cifre o un massimo di quattro cifre:

(?&lt;anno&gt;\\d {2,4})

È possibile specificare più di un'espressione nello stesso file. Ogni espressione deve essere su una riga separata. La prima espressione che viene abbinata viene utilizzata per analizzare la data.

<a name="see-also"></a>Vedere anche
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)

