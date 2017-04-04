DAL TOPIC “TRADUTTORI: GET STARTED”

autori misti: flod, gialloporpora, sara\_t.

Questo topic vuole essere un aiuto per tutti i nuovi traduttori, in modo da avere un buon punto di partenza per collaborare alle traduzioni del materiale riguardante Mozilla.
Verranno descritti i vari tipi di file da tradurre e verranno dati dei suggerimenti su strumenti utili a facilitare il lavoro di localizzazione.


Esistono sostanzialmente due tipi di file in cui vengono raccolte le stringhe dei siti Mozilla: i file `.lang` e i file `.po`.

Per i primi è possibile utilizzare un buon editor di testo (vedi un elenco di editor per le varie piattaforme qui di seguito), per i secondi, anche se è ancora possibile utilizzare un editor di testo, esistono strumenti più specifici come ad esempio **PoEdit**.

Entrambi i tipi di file sono ora localizzabili grazie alla nuova piattaforma per la localizzazione di Mozilla, **Pontoon**.

In entrambi i casi, le stringhe contengono solitamente del codice **HTML** di base e qualche elemento di formattazione utilizzato per inserire del testo dinamico (ad esempio la versione di un software o il nome del software).
Senza entrare troppo nel dettaglio, di seguito si cercherà di spiegare brevemente questi due concetti.

#### Un po' di HTML di base


Non è importante conoscere HTML, però, trattandosi di pagine web, una minima infarinatura sul codice HTML è utile per capire cosa si può tradurre e cosa invece non va tradotto.
I tag HTML sono delimitati da un segno di `<>` e, eccetto per le immagini, appaiono sempre in coppia: un tag di apertura e uno di chiusura.
I tag HTML e le loro proprietà non vanno ovviamente tradotti.
Ci sono alcune eccezioni riportate qui di seguito dove è possibile tradurre il testo associato ad alcune proprietà.

**Il testo accessibile per le immagini**

Vediamo un esempio pratico:

``` 
<img src="http://mozilla.com/image.png" alt="Image description"/>
```

È importante tradurre il testo della proprietà `alt`, che viene utilizzato al posto dell’immagine quando quest’ultima non è disponibile o per descrivere il contenuto dell’immagine a persone con problemi visivi.
Nel nostro caso:

``` 
<img src="http://mozilla.com/Descrizione dell'immagine"/>
```

L'unica avvertenza quando si traduce il testo di una proprietà HTML è quello di non usare mai delle virgolette per non generare errori nel codice.

Analogamente vanno di solito tradotti il contenuto della proprietà title dei link e del tag **abbr**.
Per gli altri tag HTML ignorare tutto quello che viene incluso fra i simboli `<` e `>`.\



#### Caratteri special


i seguenti caratteri non possono essere utilizzati traducendo delle stringhe con codice HTML:

-   E commerciale “&”, se si vuole inserire questo simbolo scrivere **&amp;**.

-   Il simbolo di minore “\<”, se si vuole inserire questo simbolo utilizzare **&lt;**.

-   Il simbolo di maggiore “\>”, se si vuole inserire questo simbolo usare **&gt;**.

**I pattern di formattazione**\
\
In alcune stringhe ci sono anche alcuni *pattern di formattazione* utilizzati per inserire del testo in modo dinamico. È importante comprendere cosa viene inserito (solitamente si può intuire ciò che viene inserito guardando il commento o dal contesto della stringa stessa) per poter farne una buona traduzione. I principali pattern che si troveranno sono i seguenti:

-   %s - indica che viene inserita una stringa, può essere un link, la versione di un software, il nome di un'app ecc….

-   `%(something)s` - è lo stesso di %s, però in questo caso il nome della variabile fra parentesi può aiutare a capire di cosa si tratta (ad esempio %(version)s indica un numero di versione). È importante non tradurre la parola fra parentesi.

-   `{0} {1} {something}` - è un modo alternativo (che dipende sostanzialmente dal fatto di utilizzare una versione più recente del software lato server).

-   essendo il simbolo **%** un carattere speciale per stampare il suddetto simbolo è necessario raddoppiarlo, %%. In ogni caso difficilmente si aggiunge un carattere di % se non è già presente nell'originale, quindi basta utilizzare quanto fatto nella stringa en-US.

I pattern possono essere riordinati per adeguarli alle necessità di localizzazione, tranne nel primo caso (più di un %s) che obbliga a mantenere l'ordine della stringa inglese.\
\
\

**File lang**\
I file .lang vengono utilizzati soprattutto per le stringhe del sito mozilla.com e sono molto semplici da gestire. Un file .lang non è altro che un file di testo in cui vengono raccolte le stringhe da tradurre in più righe, ecco come si presenta:

``` 
## Metadato
```

``` 
…
```

``` 
# commento
```

``` 
;Get Firefox
```

``` 
Get
Firefox
```

\
il carattere, singolo, di hashtag indica un commento di solito utile per capire il contesto della stringa o per conoscere l'URL del sito di test, ovviamente non è da tradurre e nemmeno da eliminare.\
I due hashtag **\#\#** indicano un metadato e queste righe non vanno assolutamente modificate.\
Il ; invece introduce la stringa inglese che non va assolutamente modificata, nemmeno se c'è qualche errore ortografico. la traduzione deve essere messa nella riga successiva sostituendo la stringa inglese, ad esempio:\
\
\

``` 
;Get Firefox
```

``` 
Scarica
Firefox
```

\
Nel caso che la traduzione coincida con la stringa inglese va aggiunto {ok}, ad esempio:

``` 
;Download
```

``` 
Download
{ok}
```

\
L'unica altra avvertenza da tenere a mente quando si traduce un file .lang è quella di salvarlo con codifica **UTF-8 senza BOM (Byte Order Mark)**, anche nel caso che l'originale non sia salvato con tale codifica.

**File po**

Il formato **.po** (o per essere più precisi il suo template che ha estensione .pot) viene generato dai programmatori del software e raccoglie tutte le stringhe da localizzare. Il compito del traduttore è quello di modificare il file traducendo le stringhe e generare il file **.mo** che verrà utilizzato per la localizzazione del software.\
\
Nello specifico caso di Mozilla, questo tipo di formato è utilizzato per tradurre la maggior parte dei siti e delle applicazioni web (Persona, Addons Mozilla, firefox Marketplace, ecc…) e non è necessario generare il file .mo compilato in quanto il lavoro viene fatto automaticamente da un apposito script.\
\
Quindi l'unica cosa che rimane da fare è quella di modificare il file **.po** traducendo tutte le occorenze e caricare il file sui server Mozilla. Anche se è possibile utilizzare un editor di testo per tradurre questo tipo di file, si consiglia di utilizzare degli strumenti appositi come Verbatim e PoEdit che sono trattati più dettagliatamente nei prossimi paragrafi.\
\
L'utilizzo di software appositi permette di dimenticarsi della sintassi di questi file che è molto più complessa dei file .lang trattati in precedenza.  Di seguito alcuni dei software più utilizzati per gestire i file .po, Verbatim e PoEdit  verranno trattati più approfonditamente nei prossimi paragrafi:

-   [PoEdit](http://www.poedit.net/download.php)

-   [Better PoEditor](http://sourceforge.net/projects/betterpoeditor/?source=dlp)

-   [Verbatim](https://localize.mozilla.org/it/) - una versione personalizzata da Mozilla di Pootle, uno strumento online di traduzione partecipativa.

-   [Virtaal](http://sourceforge.net/projects/translate/files/Virtaal/) - altro software opensource per tradurre i file .po (non stabile su OS X).

-   [xgettext per Windows](http://gnuwin32.sourceforge.net/packages/gettext.htm) (strumento avanzato e non consigliato)

**Note** le uniche due raccomandazioni, nel caso si scelga di utilizzare un software desktop anziché Verbatim, sono quelle di controllare che nelle proprietà del file la codifica sia **UTF-8**, che il locale sia **it** e che la forma plurale sia **2**.

Come detto per l'editing dei file da localizzare è fondamentale avere un buon editor di testo. la scelta dell'editor da utilizzare è del tutto personale, ma il programma scelto deve supportare obbligatoriamente il formato di codifica caratteri utf-8 (quindi il Notepad di Windows non si può usare. Inoltre avere l'evidenziazione della sintassi e un correttore ortografico aiuta molto nel processo di localizzazione).\
\
**nota**: per i file .lang è fondamentale salvarli con codifica caratteri **utf-8 senza BOM**.\
**NOTA 2**: evitare editor di rich text come Word, AbiWord, Writer di OpenOffice/LibreOffice e WordPad.\
\
Di seguito un elenco di editor di testo disponibili sulle varie piattaforme che possono essere utilizzati per l'editing dei file. Tutti supportano l'evidenziazione della sintassi e, magari previa configurazione, il controllo ortografico.\
\

-   [pspad](http://www.pspad.com/it/download.php) - ottimo editor di testo per la piattaforma windows.

-   [Notepad++](http://notepad-plus-plus.org/download/) - altro editor molto diffuso per sistemi windows che estende il notepad di sistema.

-   [sublimetext](http://www.sublimetext.com/) - editor di testo mmultipiattaforma (windows, os x e linux).  per attivare il controllo ortografico leggere [questa guida](http://www.sublimetext.com/docs/2/spell_checking.html). Il software rende facoltativo l'acquisto di una richiesta, in ogni caso tutte le funzioni sono disponibili anche senza acquistarne una.

-   [Emerald Editor](http://www.crimsoneditor.com/english/download.html) - altro editor per ambiente Windows.\
    [Text Wrangler](http://www.barebones.com/products/textwrangler/) - editor di testo per sistemi OS X

-   [TextMate](http://macromates.com/) - editor di testo a pagamento avanzato per OS X.

-   [Scintilla](http://www.scintilla.org/SciTEDownload.html) - editor di testo per piattaforma Linux e Windows.

In aggiunta ci sono Vim e Emacs disponibili per tutte le piattaforme e sicuramente con plugin appositi per l'editing dei file .po, però si sconsiglia, a meno che non si abbia già famigliarità con questi strumenti avanzati di editing, l'utilizzo di questi editor che sono un po più complicati e meno intuitivi a un primo approccio.

Altri strumenti che possono tornare molto utili per tradurre file sono un software di traduzione, un glossario e altri strumenti per memorizzare la propria fraseologia in modo da non fare lo stesso lavoro più volte.\
\
Come glossari per le traduzioni delle pagine e dei software Mozilla si consiglia di utilizzare il glossario Microsoft e transvision.mozfr.org che permette di trovare i termini all'interno delle stringhe di Firefox, Thunderbird e SeaMonkey.\
\
Esistono sostanzialmente due metodi veloci per cercare all'interno di questi glossari:

-   utilizzare uno smart bookmark

-   installare il relativo search plugin e associarvi una parola chiave

\
Nel caso si scelga di utilizzare uno smart bookmark, aggiungere questi due URL ai propri segnalibri:\
\
\

``` 
http://transvision.mozfr.org/?recherche=%s&locale=it&repo=trunk
```

``` 
http://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT
```

\
una volta aggiunti, aprire la Libreria, cercare il segnalibro e aggiungere una parola chiave per ognuno di essi.\
Se invece si vuole installarli come motori di ricerca [qui ci sono i relativi search plugin](http://www.gialloporpora.altervista.org/searchplugins/). Anche in questo caso è possibile (anzi è consigliabile) associare una parola chiave per una rapida consultazione dalla barra degli indirizzi. Supponendo di aver associato la parola chiave **msg** al glossario Microsoft, basterà digitare nella barra degli indirizzi:

``` 
msg
browse
```

\
per essere rimandati a [questa pagina](http://www.microsoft.com/Language/en-US/Search.aspx?sString=browse&langID=it-IT) e osservare i traducenti più utilizzati per rendere browse (Sfoglia).\
\
\
**Traduttori automatici**\
\
\

-   [Traduttore Google](https://translate.google.com/)

-   [Traduttore Bing](http://www.bing.com/translator/) - utilizzando il glossario Microsoft è forse da preferire a quello di Google.

\
**Memorie di traduzione**\
\
Per le memorie di traduzione ci sono molti software professionali che le gestiscono. Il software open source più diffuso è [OmegaT](http://www.omegat.org/it/downloads.html). Per una introduzione esauriente all'uso di OmegaT leggere [guida in formato PDF](http://www.omegat.org/it/tutorial/OmegaT%20for%20Beginners.pdf).

\
\

Anche se lo strumento consigliato per la localizzazione dei file .po dei vari progetti è Verbatim, si possono utilizzare anche altri software. PoEdit è il software più diffuso per la gestione dei cataloghi .po. Il software è multi piattaforma e liberamente scaricabile.\
\
Una volta scaricato e installato sul proprio computer basterà fare clic sul collegamento nel desktop per avviare il programma. A questo punto aprire il file .po che contiene le nostre stringhe da tradurre. Se è la prima volta che si utilizza PoEdit andare su *File \> Preferenze ? Personalizza* e\
\
A questo punto sarà sufficiente aprire un file .po dal menu File \> Apri…\
\
Aprire il proprio file .po (ad esempio messages.po). Nel caso dei file Mozilla PoEdit dovrebbe aprire direttamente il file perché i valori di alcuni parametri di localizzazione sono già impostati correttamente, altrimenti verrà chiesto di completare alcuni parametri. È importante utilizzare i seguenti valori:\
\
Carattere: UTF-8\
Lingua: IT\
Forma plurale: nplurals=2; plural=(n != 1);\
\
È possibile controllare questi parametri dal menu *Catalogo ? Proprietà*:\
\
Per tradurre le stringhe basta riempire il campo *Traduzione:* e confermare la stringa passando alla successiva finché non si è arrivati alla fine (le stringhe senza traduzione sono riportate in alto). Quando si sono tradotte tutte le stringhe effettuare una Convalida del file e salvarlo.\
\
A questo punto inviare a un responsabile del progetto il file .po modificato che verrà caricato sui server Mozilla.\
\
**Marca traduzione come non pronta**\
\
Quando si traducono nuove stringhe in un catalogo po di grandi dimensioni, è utile marcarle in modo che chi le corregge possa controllare solo quelle senza rileggere l'intero catalogo.\
Per marcare le stringhe per il processo di revisione, selezionare la stringa in questione e fare clic sul pulsante *Non pronta* nella barra degli strumenti in alto o con CTRL+U. La stringa verrà contrassegnata con un colore diverso.\
\
**Memoria di traduzione**\
\
Poedit è dotato di una funzione di memoria che suggerisce la traduzione di stringhe simili già tradotte in precedenza. Questo fa risparmiare il tempo di digitazione, ma soprattutto favorisce l'uniformità stilistica e terminologica.\
\
Per aggiungere una memoria di traduzione su Poedit:

-   Andare su *File ? Preferenze ? Memoria di traduzione (TM)*.

-   -Fare clic sul pulsante *Aggiungi* e selezionare la lingua (it).

-   Fare clic sul pulsante *Genera database* e nella finestra che appare su *Successivo*.

-   Fare clic su *Aggiungi file* e selezionare dalla finestra a comparsa un file po di Mozilla tradotto (almeno parzialmente) da cui si vuole ricavare la TM. Fare clic su *Apri…*.

-     Fare clic sul pulsante *Fine*. Poedit esaminerà i file per creare la TM.

\
\
Dalla prossima apertura del file po con Poedit, facendo clic con il tasto destro del mouse (clic + alt per Mac) su una stringa sarà possibile visualizzare la traduzione di tutte le stringhe a essa somiglianti in un menu a comparsa.

\
\

**OmegaT**\
[Omega T](http://www.omegat.org/) è uno strumento di traduzione assistita (CAT) multipiattaforma e gratuito che permette di utilizzare la memoria di traduzione precedente nonché un glossario durante il processo di traduzione.\
\
**Compatibilità file:** OmegaT traduce file nei formati di testo semplice, formattato (anche con le estensioni di Open e Libre Office, Microsoft Office),  HTML, PO e molti altri (per una lista completa fare riferimento al *Manuale dell'utente* nel menu *Aiuto*).\
Per tradurre gli articoli di SUMO o di una wiki con Omega T è quindi possibile salvare il testo inglese nel proprio editor di testo preferito, tradurre il file in OmegaT e incollare la traduzione ottenuta nel browser.\
\
N.B. I testi formattati appariranno come testo semplice, e i loro attributi (grassetto, corsivo, tag HTML, XLM ecc.) appariranno sotto forma di tag delimitati da "\<" e "\>". È importante riportare accuratamente tutti i tag nella traduzione, una mancata corrispondenza può impedire la creazione del file di arrivo.\
**\
Abilitare la funzione di correzione ortografica:**\
Dalla barra del menu selezionare *Opzioni* \> *Correzione ortografica*\
Selezionare un percorso in cui installare il file del dizionario con il pulsante *Scegli…*\
Premere il pulsante *Installa nuovo dizionario…*\
Selezionare dalla lista il file it-IT e premere *Installa*\
**\
Impostare una traduzione:**\
All'apertura di OmegaT la schermata iniziale fornisce un mini-tutorial iniziale per impostare una traduzione.\
Selezionare dalla barra del menu *Progetto* \> *Nuovo*.\
Nella finestra scegliere un nome per il progetto e un percorso dove salvarlo.\
Selezionare le lingue di partenza (EN) e arrivo (IT-IT) e premere *OK*.\
Nella finestra *File del progetto* premere *Copia i file nella cartella di partenza…* e selezionare il percorso del file da tradurre.\
Le stringhe da tradurre compariranno nel pannello più grande della traduzione.\
**\
Caricare la memoria di traduzione e il glossario:**\
Per aggiungere la memoria di traduzione e il glossario aprire la cartella dove il progetto è stato salvato.\
Copiare il glossario di Mozilla in formato .txt all'interno della sottocartella *glossary* e la memoria di traduzione in formato .tmx nella sottocartella *tm*. Chiudere e riaprire il progetto su OmegaT.\
\
Le parole presenti nel glossario appariranno ora sottolineate, e la loro definizione verrà visualizzata nel pannello in basso a destra.\
Per inserire il traducente dal glossario nel campo della traduzione premere *ctrl*+spazio in Windows o *Esc* in Mac.\
\
Le concordanze con la stringa selezionata verranno visualizzate nel pannello in alto a destra della schermata di OmegaT.\
Per inserire una concordanza premere *ctrl*+R (*cmd*+R su Mac).\
Prima di convalidare la traduzione con Invio assicurarsi che la traduzione corrisponda completamente al testo di partenza (tag inclusi) e apportare le eventuali modifiche.\
**\
Ottenere il file tradotto:**\
Una volta terminata la traduzione selezionare *Progetto* \> *Crea i documenti di arrivo* (o premere *ctrl* +D per Windows, *cmd*+D per Mac), e il file tradotto verrà salvato nella sottocartella *target* del progetto.

Di seguito alcuni link a discussioni e altri materiali che potrebbero tornare utili. Se hai altre risorse, strumenti o suggerimenti su come migliorare questa breve guida puoi aprire una discussione nella sezione traduzioni del forum e non mancheremo di apportare le dovute modifiche.\
\
**Discussioni sul forum**

-   [Discussione dove vengono segnalate nuove stringhe da tradurre](http://forum.mozillaitalia.org/index.php?board=8.0) — puoi attivare le notifiche cliccando sull'apposito pulsante in basso.

**memorie di traduzione**\
Se si vuole utilizzare come memoria di traduzione (vedi sopra) con Poedit o Omegat i file che comprendono l'insieme di tutti i progetti già localizzati su Verbatim, [a questo link](https://www.dropbox.com/sh/odlh109rugbovnr/OA8NTEkZ0b) si possono trovare i file necessari. I file per Omegat hanno estensione **tmx** mentre quelli da utilizzare con Poedit hanno, ovviamente, estensione **po**.\
Descirzione dei file:

-   firefox.po, firefox.lang, firefox.tmx — sono dei cataloghi in vari formati che contengono tutta la traduzione di Firefox, utile per trovare come è stata resa una stringa.

-   amo.txt — un glossario in un file di testo tabulato che utilizziamo per la terminologia di AMO+Marketplace.

-   gaia1.2.tmx — un file per OmegaT che contiene la traduzione di Firefox OS, utile per trovare la traduzione di una stringa se non si possiede un dispositivo Firefox OS o il simulatore.

-   memoria.po, memoria.lang, memoria.tmx — un mega catalogo, in diversi formati, delle stringhe di mozilla.com, FHR (Firefox Health Report) e tutti i progetti già tradotti su Verbatim (Amo, firefox Input, ecc…).

\
Su [transvision.mozfr](http://transvision.mozfr.org/downloads/) è possibile scaricare i file aggiornati per OmegaT della localizzazione di Firefox e Firefox OS.
