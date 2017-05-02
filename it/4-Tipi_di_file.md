# Sintassi HTML, tipi di file e strumenti di localizzazione

In questo capitolo vedremo brevemente le basi della sintassi HTML e di alcuni formati di file utilizzati nella localizzazione dei prodotti Mozilla.
Nella prima sezione verranno discusse alcune nozioni di base di HTML, che sono necessarie per formattare il testo delle pagine web.
Nella sezione successiva vedremo alcuni caratteri e codici di formattazione che possono essere utilizzati nelle stringhe e daremo delle semplici regole per evitare di generare errori.
La terza sezione del capitolo discuterà la sintassi di alcuni file utilizzati nella localizzazione e può essere ignorata se si utilizza [Pontoon](3-Flusso%20di%20lavoro.md#pontoon ) come strumento di localizzazione.
Nelle ultime due sezioni infine, vedremo un elenco di software utili per gestire i vari tipi di file e alcuni editor di testo che si possono utilizzare.


## Codice HTML: le basi{#c4s1}

Il codice HTML (Hypertext Markup Language) è un linguaggio ipertestuale utilizzato per la formattazione del testo e l’inserimento di contenuti multimediali nelle pagine, anche se non è compito di un localizzatore creare pagine web, la conoscenza di alcuni fondamenti può ritornare utile per localizzare correttamente alcune stringhe o personalizzare la formattazione del testo (ad esempio per rendere in grassetto o in corsivo alcuni termini).
Il codice HTML è, come detto, un linguaggio di formattazione del testo utilizzato dalle pagine web.
In HTML il testo va racchiuso tra alcuni marcatori (tag) che descrivono il tipo di oggetto (testo, immagine, link,, ecc.).
Un tag è delimitato dai simboli di minore e maggiore e rappresenta un’istruzione per il browser, mentre tutto ciò che viene inserito tra il tag di apertura e chiusura è del testo che verrà, sostanzialmente, mostrato a schermo, con diversa formattazione a seconda del tag utilizzato.
Ad esempio:

	<strong>Grassetto</strong>

indicherà al browser di mostrare la parola **Grassetto** in grassetto.
Mentre:

	<em>Corsivo</em>

indicherà al browser di visualizzare il testo Corsivo, appunto, in corsivo.
In realtà, lo stile con cui viene visualizzato il testo dipenderà dal foglio di stile, però in linea di massima per i tag principali la formattazione è quella standard.
Per ulteriori informazioni sul tag `<strong>` è possibile consultare [questo articolo][c4l1], mentre per il tag `<em>` si può fare riferimento a [quest’altro articolo][c4l2].

Ciò che è importante è però assicurarsi sempre di inserire un tag di apertura e chiusura e non mettere mai simboli di `<` o `>` nelle stringhe, questo perché il browser potrebbe interpretare ciò che segue come un tag e non visualizzare il testo successivo.

Ma allora come è possibile visualizzare i due caratteri `<` e `>`?
Per questo scopo HTML definisce le cosidette *entity*, cioè delle sequenze delimitate da una `&` e da un `;` che servono per codificare alcuni caratteri speciali.
In particolare:


	&lt; = <
	&gt; = >
	&amp; = &

Ne esistono in realtà moltissime altre, però queste sono quelle che devono essere sempre utilizzate per i tre caratteri sopra indicati.
È vero che i browser moderni sono in grado di interpretare correttamente anche del codice HTML non perfettamente formattato, però da amanti del Web riteniamo che le cose vadano fatte seguendo tutte le regole del caso.

Un’altra *entity* utile è lo spazio , `&nbsp;`, che visualizza semplicemente uno spazio, con l’importante differenza che forza la visualizzazione della stringa come se fosse un’unica parola.
Questo può essere utile quando si vuole che due parole non vengano mandate a capo e mostrate su righe diverse e di solito si capisce dal contesto e guardando il risultato finale se sia da utilizzare o meno.
Per un elenco completo delle *entity* HTML consultare [questa pagina][c4l4].

### Paragrafi di testo

In HTMl di solito i paragrafi di testo vengono racchiusi tra i tag `<p>` e `</p>`, un paragrafo di testo altro non è se non del testo che viene mostrato in un unico blocco, sarà il browser a decidere quando andare a capo a seconda delle dimensioni dello schermo.
Ai vari paragrafi, e in generale a qualunque altro tag HTML, possono anche essere associate delle proprietà che serviranno allo sviluppatore per definire alcune specifiche di visualizzazione (colore, spaziatura, interlinea, ecc.), ovviamente un traduttore dovrà concentrarsi solo nella traduzione del testo e non delle proprietà associate all’elemento HTML.

Vediamo un esempio pratico:

	<p class="red">May the force be with you.</p>
	<p class="red">Che la forza sia con te.</p>

Il valore `red` associato alla proprietà `class` indicherà al browser di visualizzare il testo in colore rosso (o per essere precisi rispettando le regole della classe `red` definita nel foglio di stile), e come detto non va assolutamente tradotta.
Ci sono solo due casi in cui un traduttore può tradurre il valore di una proprietà HTML e sono quelli associati alle proprietà `title` e `alt` che discuteremo più avanti parlando delle abbreviazioni, dei link e delle immagini.

Come detto il testo dei paragrafi non va mai a capo, per forzare il testo ad andare a capo è necessario usare il tag `<br>` o, per rispettare le specifiche HTML il tag *selfclosed* `br/>`.
Ad esempio:

	Prima riga<br/>Seconda riga<br/>

Per ulteriori informazioni sul tag `<p>` leggere [questo articolo][c4l4] e [quest’altro][c4l5] per il tag `<br/>`.


### Abbreviazioni

Non è un tag molto utilizzato, però a volte si incontra e può essere utile in fase di localizzazione per indicare il significato originale dell’acronimo inglese.
Ad esempio supponiamo di avere la seguente stringa:

	<abbr title="Hypertext Markup Language">HTML</abbr> is the standard markup language for creating web pages and web applications.
	<abbr title="Hypertext Markup Language">HTML</abbr> (linguaggio a marcatore per ipertesto) è il linguaggio standard per la creazione di pagine e applicazioni web.
	
Il valore della proprietà `title` viene visualizzato al passaggio del mouse sulla parola *HTML* e serve per indicare il significato esatto dell’acronimo HTML.
In questo caso il valore va lasciato in inglese perché l’acronimo non ha significato in italiano, può sempre essere utile aggiungere, anche se non presente nell’originale, qualche tag `abbr` che serva a far luce sul significato di vari acronimi che sono abusati da americani e informatici in generale, lasciando magari fra parentesi la traduzione letterale in italiano.

Per ulteriori informazioni sull’elemento `<abbr>` consultare [questo articolo][c4l6].


### Link ipertestuali

I link (collegamenti) sono probabilmente l’oggetto più importante in HTML, essi servono per inserire il collegamento a una pagina web, cliccando su tale testo si verrà reindirizzati alla pagina indicata.
Il più delle volte, come detto in precedenza, quello che è compreso all’interno del tag non va mai tradotto, in alcuni casi però questo potrebbe essere utile, ad esempio per rimandare a una versione italiana dello stesso documento.
In caso della presenza della proprietà *title* questa va tradotta perché è il testo visualizzato al passaggio del mouse sopra il testo del link.

	Mozilla is a free-software community created in 1998 by members of <a href="https://en.wikipedia.org/wiki/Netscape" title="Netscape">"Netscape</a>.
	Mozilla è una comunità di software libero fondata nel 1998 da membri di <a href="https://it.wikipedia.org/wiki/Netscape_Communications" title="Netscape">Netscape</a>.
	
Come si vede dall’esempio, invece di mettere il link alla pagina di Wikipedia in lingua inglese si è scelto di far puntare il link alla pagina di Wikipedia in italiano.

Per approfondire l’argomento consultare [questo articolo][c4l7].


### Immagini

A volte oltre al semplice testo vengono incluse anche delle immagini.
Ovviamente un’immagine, a meno che non sia di una schermata del computer, non si può tradurre, quello che va tradotto è il valore della proprietà *alt*, il testo ad essa associato infatti viene riprodotto dagli *screen reader* o visualizzato al posto dell’immagine nel caso l’immagine non sia disponibile e serve per descrivere il contenuto dellimmagine e rendere accessibile la pagina HTML a tutti.

	<img src="/image/firefox.png" alt="Firefox Logo"/>
	<img src="/image/firefox.png" alt="Logo di Firefox"/>

Come si vede, per le immagini, come accade per il tag `<br/>`, non ci sono un tag di apertura e chiusura in quanto non ha senso associare del testo a un’immagine e quindi si utilizza chiudere direttamente il tag `/>`.

Per ulteriori informazioni è possibile consultare [questo articolo][c4l8].

Questi sono solo alcuni dei principali tag HTML, diciamo quelli che è più facile incontrare nella localizzazione delle pagine e quindi quelli di cui bisogna avere una minima infarinatura.
Ovviamente ne esistono moltissimi altri e rimandiamo alla documentazione molto ben curata di [Mozilla Developer Netword][c4l9] (MDN) per approfondire la sintassi del linguaggio.
Essendo **MDN** un sito Mozilla, inoltre consigliamo di tradurre qualche pagina nel caso non fosse ancora disponibile in lingua italiana.


## Codici di formattazione Python e stringhe JavaScript{#c4s2}

Le applicazioni web solitamente sono composte da una parte lato server (che nel caso di Mozilla è scritta in Python) e di una parte lato client (che utilizza codice HTML e JavaScript).
Mentre il codice HTML viene utilizzato per formattare contenuti statici, JavaScrip e Python vengono utilizzati per inserire dei contenuti dinamici, nel primo caso generati dall’interazione dell’utente con la pagina (ad esempio cliccando un link) e nel secondo caso direttamente dal server.

Solitamente in tutti i progetti Mozilla le stringhe utilizzate all’interno del codice JavaScript vengono raccolte in un file dedicato (di solito dal nome `javascript.po` o varianti).
In questo tipo di stringhe è importante fare attenzione a inserire virgolette o apostrofi perché potrebbero essere interpretati come delimitatori della stringa stessa e produrre risultati assai indesiderati.
Per essere sicuri di non causare errori al codice, questi caratteri andrebbero preceduti da una `\`, il consiglio che ci sentiamo di dare è quello di utilizzare sempre le virgolette e gli apostrofi tipografici: **“”’** (si veda l’appendice per digitare questi caratteri nei vari sistemi operativi).

Un altro carattere speciale che si può utilizzare è `\n` e serve per mandare a capo il testo.

### Formattazione delle stringhe lato server

Come detto le applicazioni hanno del codice lato server che a volte viene utilizzato per inserire del codice dinamico nelle pagine, ad esempio per indicare l’autore e la data di un commento in un articolo.
Le applicazioni Mozilla girano su dei server Django e utilizzano Python come linguaggio lato server, vediamo quindi alcuni caratteri speciali che si possono incontrare nelle stringhe e che sono in realtà delle istruzioni per inserire del testo in maniera dinamica.


Ci sono diverse sintassi per inserire dei valori presi da variabili e la scelta dipende sostanzialmente dallo sviluppatore che scrive il codice.
Vediamo un esempio pratico.


	Published by %s in date %s
	Published by{0} in date {1}
	Published by %(author)s in date %(date)s
	Published by {author} in date {date}

Che verranno rese con:

	Pubblicato da %s in data %s
	Pubblicato da {0} in data {1}
	Pubblicato da %(author)s in data %(date)s
	Pubblicato da {author} in data {date}

Tutte le sintassi sono valide, la prima però è, da un punto di vista di un localizzatore, una pessima scelta perché non consente di modificare l’ordine in cui vengono inseriti i due valori.
La seconda invece è poco descrittiva, le due scelte migliori sono le ultime due perché consentono sia di invertire l’ordine dei due valori sia di avere un’idea di cosa viene inserito al posto della variabile.
Supponiamo ad esempio di voler trasformare la frase in forma passiva (in alcuni casi è necessario farlo perché mantenere la stessa struttura dell’inglese non rende sempre in italiano).
Come già detto, nel primo caso ciò non sarà possibile, negli altri tre è sufficiente invertire l’ordine dei codici di formattazione:

	In data {1} {0} ha scritto
	In data %(date)s %(author)s ha scritto
	In data {date} {author} ha scritto

In ogni caso, la cosa più importante è quella di assicurarsi di indicare sempre questi codici di formattazione se sono presenti.
Se si utilizza Pontoon come strumento di localizzazione, verrà visualizzato un messaggio di errore se si tenta di immettere una stringa che non contenga i codici di formattazione dell’originale, se invece si sta traducendo direttamente il file con un editor di testo è importante controllare attentamente che i codici siano inseriti correttamente.



## Formati degli archivi di localizzazione{#c4s3}


Per salvare le stringhe delle varie lingue dei siti Mozilla vengono utilizzati tre diversi formati: file `.lang`, file `.properties` e file `.po`.
Vediamo la struttura e la sintassi di questi file che altro non sono se non semplici file di testo con alcune regole di sintassi che servono per essere correttamente interpretati dal codice che si occupa di mostrare il contenuto dei siti nella lingua scelta dal visitatore.
Conoscere la sintassi di questi file non è necessario se si utilizza uno strumento ad hoc come [Pontoon](3-Flusso di lavoro.md#pontoon), la trattazione viene fatta nel caso fosse necessario modificare manualmente i singoli file con un semplice editor di testo.

La prima operazione da fare è quella di munirsi di un editor di testo (vedi ultima sezione per un elenco di applicazioni per i vari sistemi) per aprire e modificare questi file, ricordandosi **sempre** di utilizzare la codifica caratteri [**UTF-8**][utf8].
La codifica è molto importante perché un’errata codifica porterà alla visualizzazione di strani caratteri al posto dei caratteri non ASCII (si pensi ad esempio ai punti di domanda o a strani caratteri che a volte vengono visualizzati al posto delle lettere accentate in alcune pagine).

## File `.properties`

Questo particolare formato viene utilizzato soprattutto per i siti di Mozilla Foundation e ha come svantaggio quello di non poter visualizzare nello stesso file la stringa originale e la stringa tradotta, nonché il fatto di essere un po’ complicato da aggiornare manualmente.
Questi file vanno semplicemente modificati inserendo la traduzione al posto del testo inglese e posizionati in una sottocartella che ha come nome il codice internazionale della lingua della traduzione (per l’italiano è `it`).
Nel caso la cartella `it` non esista va clonata la sottocartella coi file originali (di solito `en-US`) e ridenominata in `it`.
Di solito comunque il localizzatore troverà già una copia dei file originali già pronti per essere tradotti nella giusta posizione.
[Qui][c4l10] è possibile vedere un esempio di file `.properties` originale e [qui][c4l11] la versione localizzata in italiano.

Come è possibile notare ai link precedenti, la sintassi di questi file è molto semplice: in ogni riga va indicato il nome della variabile contenente il testo specificato e per localizzare il file inglese è sufficiente sostituire il testo inglese con la sua traduzione in italiano.
Facendo riferimento ai file `email.properties` di cui sopra, la stringa:

	third_paragraph_email=Thanks again for all that you do to support Mozilla. Together, we will keep the Internet open, accessible, transparent and safe.

viene sostituita con:

	third_paragraph_email=Grazie ancora per tutto ciò che fai per aiutare Mozilla. Assieme riusciremo a mantenere il Web accessibile, aperto, trasparente e sicuro.

Le cose a cui prestare attenzione sono:

1.  non cambiare il nome della variabile (maiuscole e minuscole sono caratteri differenti) e non mettere spazi aggiuntivi tra il nome, il simbolo di uguale e la traduzione vera e propria;
2.  non mettere una stringa su più righe, se serve andare a capo usare `<br/>` o `\n` a seconda che si tratti di una stringa HTML (il 99% dei casi) o JavaScript;
3. salvare il file ricordandosi di utilizzare la codifica [UTF-8][utf8].

Consigliamo comunque di utilizzare Pontoon quando disponibile per questo tipo di file, anche perché con i siti che utilizzano i file `.properties` è possibile avere un’anteprima in tempo reale mentre si sta traducendo.

### File `.lang`

Il formato `.lang` viene utilizzato per molti siti mozilla (ad esempio per il sito `mozilla.org`) o per i messaggi promozionali che appaiono nella pagina `about:home` di Firefox, ed è molto semplice da gestire anche con un semplice editor di testo in quanto la sintassi è poco complessa e consente, contrariamente ai file `.properties` trattati in precedenza, di avere a portata di mano sia la stringa originale che la sua versione tradotta.
Questo oltre a facilitare il compito del localizzatore aiuterà anche i revisori che dovranno effettuare il controllo qualità (o come si usa dire il QA, cioé il *quality assurance*) della traduzione.

Un file `lang` non è altro che un semplice file di testo in cui il testo originale è preceduto da un *punto e virgola* e nella riga sottostanze viene inserito il testo tradotto.
Se il file non è mai stato localizzato in precedenza il testo orginale verrà riporttato due volte, nella prima riga preceduto da un *punto e virgola* e nella seconda così com'è, il localizzatore dovrà sostituire il testo della seconda riga (quella in cui non è preceduto dal *punto e virgola*).
Il testo preceduto dal *punto e virgola* quindi, non andrà **mai** modificato, farlo significherà eliminare completamente i riferimento alla stringa.

Ci sono inoltre altri due tipi di righe: i commenti, che sono preceduti da un carattere cancelletto `#` e delle righe di comando che sono precedute da due caratteri cancelletto `##`.
Le prime sono un aiuto al localizzatore ed è utile leggerle perché viene capito il contesto e vengono date informazioni riguardo alla visualizzazione del testo (ad esempio viene indicato se usare codice HTML o meno), le seconde sono comandi interni, in ambedue i casi non vanno **mai** modificate dal localizzatore.

I singoli blocchi sono, di solito, separati da due righe bianche, questo non è un requisito necessario, però è bene mantenere questo tipo di struttura per una maggiore leggibilità.

Ma, come fatto in precedenza, vediamo un esempio pratico:

	## active ##
	## NOTE: demo page at https://www-dev.allizom.org/firefox/private-browsing
	
	# HTML Title attribute
	;Firefox Web browser — Private Browsing with Tracking Protection — Mozilla
	Browser web Firefox — Navigazione anonima con protezione antitracciamento
	
La prima e seconda riga sono dei comandi interni: la prima indica che la traduzione è stata attivata e la seconda dove è possibile vedere l’anteprima della localizzazione, come detto non vanno assolutamente modificate.

La riga:

	# HTML Title attribute
	
è un commento e informa il localizzatore che si tratta del titolo della pagina web e che quindi non è possibile utilizzare del codice HTML nella localizzazione.
Le altre due riportano la stringa originale e la sua traduzione.

A volte può accadere che si voglia usare lo stesso testo della stringa originale, ad esempio quando viene indicato il nome di un sito web o di un prodotto, per farlo bisogna aggiungere il codice `{ok}` al testo localizzato per informare il software che la traduzione coincide con il testo originale e che non ci si è dimenticati di tradurla.
Ad esempio:

	;Mozilla Firefox
	Mozilla Firefox {ok}

Riepilogando, nella traduzione di un file `.lang` bisogna fare attenzione a:

1.  non modificare mai le righe che iniziano con un *punto e virgola* o con un *cancellletto*;
2.  modificare la riga appena dopo a una che inizia con il *punto e virgola*;
3.  mettere la traduzione sempre su una sola riga, se serve mandare a capo il testo utilizzare il carattere `<br/>`;
4.  se la traduzione coincide col testo originale ricordarsi di aggiungere il codice `{ok}` nella traduzione;
5.  salvare sempre il file con codifica **UTF-8**.


### File `.po`

Il formato `.po` (o per essere più precisi il suo template che ha estensione `.pot`) viene generato dai programmatori del software e raccoglie tutte le stringhe da localizzare.
Il compito del traduttore è quello di modificare il file traducendo le stringhe e generare il file `.mo` che verrà utilizzato per la localizzazione del software.
Nello specifico caso di Mozilla, questo tipo di formato è utilizzato per tradurre la maggior parte dei siti e delle applicazioni web (Persona, addons mozilla, firefox marketplace, ecc…) e non è necessario generare il file .mo compilato in quanto il lavoro viene eseguito automaticamente da un apposito script presente sui server Mozilla.
Quindi l'unica cosa che rimane da fare è quella di modificare il file `.po` traducendo tutte le occorenze e caricare il file sui server Mozilla.

Anche se è possibile utilizzare un editor di testo per tradurre questo tipo di file, si consiglia di utilizzare degli strumenti appositi come [Pontoon](https://pontoon.mozilla.org) o [Poedit](http://www.poedit.net/download.php), che tratteremo brevemente in questa sezione.

L'utilizzo di software appositi permette di dimenticarsi della sintassi di questi file che è molto più complessa dei file `.lang` e `.properties` visti in precedenza.

Una volta scaricato e installato sul proprio computer basterà fare clic sul collegamento nel desktop per avviare il programma.
Se è la prima volta che si utilizza poedit andare su *File &rarr; Preferenze &rarr; Personalizza*.
Inserire le informazioni richieste, il proprio nome, indirizzo email, lingua preferita, ecc.
A questo punto aprire il file .po che contiene le stringhe da tradurre andando su *File &rarr; ]Apri…*.

Aprire il proprio file .po (ad esempio `messages.po`).
Nel caso dei file Mozilla poedit dovrebbe aprire direttamente il file perché i valori di alcuni parametri di localizzazione sono già impostati correttamente, altrimenti verrà chiesto di completare alcuni parametri.
È importante utilizzare i seguenti valori:

	Codifica caratteri: UTF-8
	Lingua: it
	Forma plurale: nplurals=2; plural=(n != 1);

È possibile controllare questi parametri dal menu *Catalogo &rarr; Proprietà*.

Per tradurre le stringhe basta riempire il campo *Traduzione:* e confermare la stringa passando alla successiva finché non si è arrivati alla fine (le stringhe senza traduzione sono riportate in alto).

Quando si sono tradotte tutte le stringhe effettuare una convalida del file e salvarlo.
Se durante il processo di convalida verranno rilevati degli errori, Poedit visualizzerà dei messaggi di avviso indicando quali stringhe non sono state tradotte o contengono errori.

A questo punto inviare a un responsabile del progetto il file .po modificato che verrà caricato sui server Mozilla.

Di seguito alcuni suggerimenti che possono rivelarsi molto utili.

**Marca traduzione come non pronta**

Quando si traducono nuove stringhe in un catalogo `.po` di grandi dimensioni, è utile marcarle in modo che chi le corregga possa controllare solo quelle senza doversi rileggere l'intero catalogo.
Per marcare le stringhe per il processo di revisione, selezionare la stringa in questione e fare clic sul pulsante *Non pronta*, nella barra degli strumenti in alto o con `Ctrl+U`.
La stringa verrà contrassegnata con un colore diverso.

**Memoria di traduzione**

Poedit è dotato di una funzione di memoria che suggerisce la traduzione di stringhe simili già tradotte in precedenza.
Questo fa risparmiare il tempo di digitazione, ma soprattutto favorisce l'uniformità stilistica e terminologica.

Per aggiungere una memoria di traduzione su Poedit:

-   andare su *File &rarr; Preferenze &rarr; Memoria di traduzione (tm)*;
-    fare clic sul pulsante *Aggiungi* e selezionare la lingua (`it`);
-   are clic sul pulsante *Genera database* e nella finestra che appare su *Successivo*;
-   fare clic su *Aggiungi file* e selezionare dalla finestra a comparsa un file po di Mozilla tradotto (almeno parzialmente) da cui si vuole ricavare la memoria di traduzione;
-   fare clic su *Apri…*;
-  fare clic sul pulsante *Fine*.

Poedit esaminerà i file per creare la TM.

Alla prossima apertura del file po con poedit, facendo clic con il tasto destro del mouse (clic + Alt per Mac) su una stringa verranno visualizzate in un menu a comparsa tutte le stringhe che le assomigliano.


## Editor di testo e applicazioni per gestire i cataloghi `.po`{#c4s4}

Come già detto in precedenza più volte, lo strumento più semplice per localizzare i vari progetti Mozilla è Pontoon, nel caso il progetto non sia disponibile per la localizzazione su questa piattaforma o se si preferisce non utilizzarlo, in questa sezione verranno presentati alcuni *editor di testo* e applicazioni per, alternative a Poedit, per gestire i cataloghi `.po` sulle varie piattaforme, Windows, Mac e Linux.
Ovviamente se si utilizza già un proprio editor di testo si può tranquillamente continuare a farlo, l’importante è assicurarsi che consenta di salvare i file con codifica [**UTF-8**][utf8] (senza BOM) (praticamente si può utilizzare qualsiasi editor di testo che non sia il *Notepad* presente sulle vecchie versioni di windows).
Con editor di testo si intende un vero editor di testo, non un editor che salva i documenti con testo formattato (*Rich Text*), evitare quindi applicazioni come Word, Abiword, Writer di OpenOffice/LibreOffice e Wordpad.
Inoltre avere l'evidenziazione della sintassi e un correttore ortografico aiuta molto nel processo di localizzazione.

Di seguito un elenco di editor di testo disponibili sulle varie piattaforme che possono essere utilizzati per l'editing dei file.
Tutti i editor presentati supportano l'evidenziazione della sintassi e, magari previa configurazione, il controllo ortografico.
Alcuni, come Sublime Text e Atom, dispongono inoltre di un discreto numero di moduli aggiuntivi per aggiungere nuove funzioni.

-   [Pspad](http://www.pspad.com/it/download.php) - ottimo editor di testo per la piattaforma Windows.
-   [Notepad++](http://notepad-plus-plus.org/download/) - altro editor molto diffuso per sistemi Windows che estende il Notepad di sistema.
-   [Sublime Text](http://www.sublimetext.com/) - editor di testo mmultipiattaforma (Windows, OS X e Linux).  Per attivare il controllo ortografico leggere [questa guida](http://www.sublimetext.com/docs/2/spell_checking.html). Il software rende facoltativo l'acquisto di una licenza, in ogni caso tutte le funzioni sono disponibili anche senza acquistarne una. Il programma ha inoltre un gran numero di moduli (*package*) che possono essere utilizzati per aggiungere funzionalità aggiuntive. Per ulteriori informazioni sui *package* per sublime text consultare [questa pagina](https://packagecontrol.io/).
-   [Emerald Editor](http://www.crimsoneditor.com/) - altro editor per ambiente Windows, un po’ datato ma funzionante e funziona anche con le vecchie versioni del sistema operativo di casa Microsoft.
-   [Bbedit](http://www.barebones.com/products/bbedit/) - editor di testo per sistemi OS X, la versione senza licenza è perfettamente funzionale, anche se non dispone di alcune funzioni avanzate.
-   [TextMate](http://macromates.com/) - editor di testo a pagamento avanzato per OS X.

-   [Scintilla](http://www.scintilla.org/scitedownload.html) - editor di testo per piattaforma Linux e Windows.
-   [Atom](https://atom.io/) - ottimo editor di testo multi-piattaforma che utilizza tecnologie web (non disponibile per XP e Vista).

Alternativamente, [OmegaT](http://omegat.org/), che verrà discusso più approfonditamente nella prossima sezione,  offre un filtro apposito per i file `.lang` che permette di tradurre in un'interfaccia facilitata senza preoccuparsi delle precedenti regole di sintassi.



- [pootle](http://pootle.translatehouse.org/) - uno strumento online di traduzione partecipativa, prima dell'avvento di pontoon, mozilla ne utilizzava una versione personalizzata chiamata verbatim.

- [virtaal](http://sourceforge.net/projects/translate/files/virtaal/) - altro software open source per tradurre i file .po (non stabile su os x).

- [xgettext per windows](http://gnuwin32.sourceforge.net/packages/gettext.htm) (strumento avanzato e non consigliato)

**n.b.** per la lingua italiana controllare che nelle proprietà del file la codifica sia **utf-8**, che il locale sia **it** e che la forma plurale sia **2**.


in aggiunta ci sono vim e emacs disponibili per tutte le piattaforme e sicuramente con *plugin* appositi per l'editing dei file `.po`, però si sconsiglia, a meno che non si abbia già familiarità con questi strumenti avanzati di editing, l'utilizzo di questi editor che sono un po più complicati e meno intuitivi a un primo approccio.


[c4l1]: https://developer.mozilla.org/it/docs/Web/HTML/Element/strong
[c4l2]: https://developer.mozilla.org/it/docs/Web/HTML/Element/em
[c4l3]: https://dev.w3.org/html5/html-author/charref
[c4l4]: https://developer.mozilla.org/it/docs/Web/HTML/Element/p
[c4l5]: https://developer.mozilla.org/it/docs/Web/HTML/Element/br
[c4l6]: https://developer.mozilla.org/it/docs/Web/HTML/Element/abbr
[c4l7]: https://developer.mozilla.org/it/docs/Web/HTML/Element/a
[c4l8]: https://developer.mozilla.org/it/docs/Web/HTML/Element/img
[c4l9]: https://developer.mozilla.org/it/docs/Web/HTML/
[c4l10]: https://github.com/mozilla/donate.mozilla.org/blob/master/locales/en-US/email.properties
[c4l11]: https://github.com/mozilla/donate.mozilla.org/blob/master/locales/it/email.properties
[utf8]: https://it.wikipedia.org/wiki/UTF-8
