# Sintassi HTML, tipi di file e strumenti di localizzazione

In questo capitolo vedremo brevemente le basi della sintassi HTML e di alcuni formati di file utilizzati nella localizzazione dei prodotti Mozilla.
Nella prima sezione verranno discusse alcune nozioni di base di HTML, che sono necessarie per formattare il testo delle pagine web.
Nella sezione successiva vedremo alcuni caratteri e codici di formattazione che possono essere utilizzati nelle stringhe e daremo delle semplici regole per evitare di generare  errori.
La terza sezione del capitolo discuter� la sintassi di alcuni file utilizzati nella localizzazione e pu� essere ignorata se si utilizza Pontoon come strumento della localizzazione.
Nelle ultime due sezioni infine, vedremo un elenco di software utili per gestire i vari tipi di file e alcuni editor di testo che si possono utilizzare.


## Codice HTML: le basi

Il codice HTML (Hypertext Markup Language) � un linguaggio ipertestuale utilizzato per la formattazione del testo e l'inserimento di contenuti multimediali nelle pagine, anche se non � compito di un localizzatore creare pagine web, la conoscenza di alcuni fondamenti pu� ritornare utile per localizzare correttamente alcune stringhe o personalizzare la formattazione del testo (ad esempio per rendere in grassetto o in corsivo alcuni termini).
Il codice HTML �, come detto, un linguaggio di formattazione del testo utilizzato dalle pagine web.
Il testo  va racchiuso tra alcuni marcatori (tag) che descrivono il tipo di oggetto (testo, immagine, link,, ecc.).
Un tag � delimitato dai sinboli di minore e maggiore e rappresenta un'istruzione per il browser, mentre tutto ci� che viene inserito tra il tag di apertura e chiusura � del testo che verr�, sostanzialmente, mostrato a schermo.
Ad esempio:

	<strong>Grassetto</strong>
	
indicher� al browser di mostrare la parola **Grassetto** in grassetto.
Mentre:

	<em>Corsivo</em>
	
indicher� al browser di visualizzare il testo Corsivo, appunto, in corsivo.
In realt�, lo stile con cui viene visualizzato il testo dipender� dal foglio di stile, per� in linea di massima per i tag principali la formattazione � quella standard.


Ci� che � importante � per� assicurarsi sempre di inserire un tag di apertura e chiusura e non mettere mai simboli di `<` o `>` nelle stringhe, questo perch� il browser potrebbe interpretare ci� che segue come un tag e non visualizzare il testo successivo.
Ma allora come � possibile visualizzare i due caratteri `<` e `>`?
Per questo scopo HTML definisce le cosidette *entity*, ci� delle sequenze delimitate da una `&` e da un `;` che servono per codificare alcuni caratteri speciali.
In particolare:


	&lt; = <
	&gt; = >
	&amp; = &
	
Ne esistono in realt� moltissime altre, per� queste sono quelle che devono essere sempre utilizzate per i tre caratteri sopra indicati.
� vero che i browser moderni sono in grado di interpretare correttamente anche del codice HTML non perfettamente formattato, per� da amanti del Web riteniamo che le cose vadano fatte seguendo tutte le regole del caso.

Un'altra *entity* utile � lo spazio, `&nbsp;`, che visualizza semplicemente uno spazio, con l'importante differenza che forza la visualizzazione della stringa come se fosse un'unica parola.
Questo pu� essere utile quando si vuole che le stringhe non vengano visualizzate su due righe diverse e solitamente si capisce dal contesto e guardando il risultato finale se sia da utilizzare o meno.

Vediamo un altro esempio un po' pi� complesso:

	<p class="red">May the force be with you.</p>
	<p class="red">Che la forza sia con te.</p>
	
Nei tag possono anche essere indicate delle propriet� (in questo caso la propriet� *class* a cui � associato il valore *red*), che, in linea di massima, non vanno mai localizzate perch� sono delle istruzioni (in questo caso per visualizzare il testo in rosso).
Ci sono solo due casi in cui un traduttore pu� tradurre  il valore di una propriet� HTML e sono quelli associati alle propriet� *title* e *alt* che discuteremo pi� avanti parlando delle abbreviazioni, dei link e delle immagini.

Ovviamente l'HTML non � solo del testo in grassetto e corsivo, senza entrare nei particolari vediamo altri tre elementi che si incontrano spesso nella localizzazione: abbreviazioni, immagini e link ipertestuali.

#### Abbreviazioni

Non � un tag molto utilizzato, per� a volte si incontra e pu� essere utile in fase di localizzazione per mettere il significato originale dell'acronimo inglese.
Ad esempio supponiamo di avere la seguente stringa:
	<abbr title="Hypertext Markup Language">HTML</abbr> is the standard markup language for creating web pages and web applications.
	<abbr title="Hypertext Markup Language">HTML</abbr> (linguaggio a marcatore per ipertesto) � il linguaggio standard per la creazione di pagine e applicazioni web.
	
Il valore della propriet� *title* viene visualizzato al passaggio del mouse sulla parola *HTML* e serve per indicare il significato esatto dell'acronimo HTML.
In questo caso il valore va lasciato in inglese perch� l'acronimo non ha significato in italiano, pu� sempre essere utile aggiungere, anche se non presente nell'originale, qualche tag `abbr` che serva a far luce sul significato di vari acronimi che sono abusati da americani e informatici in generale, lasciando magari fra parentesi la traduzione letterale in italiano.

#### Link ipertestuali

I link (collegamenti) sono probabilmente l'oggetto pi� importante in HTML, essi servono per inserire il collegamento a una pagina web, cliccando su tale testo si verr� reindirizzati alla pagina indicata.
Il pi� delle volte, come detto in precedenza, quello che � compreso all'interno del tag non va mai tradotto, in alcuni casi per� questo potrebbe essere utile, ad esempio per rimandare a una versione italiana dello stesso documento.
In caso della presenza della propriet� *title* questa va tradotta perch� � il testo visualizzato al passaggio del mouse sopra il testo del link.


	Mozilla is a free-software community created in 1998 by members of <a href="https://en.wikipedia.org/wiki/Netscape" title="Netscape">"Netscape</a>.
	Mozilla � una comunit� di software libero fondata nel 1998 da membri di <a href="https://it.wikipedia.org/wiki/Netscape_Communications" title="Netscape">Netscape</a>.
	
Come si vede dall'esempio, invece di mettere il link alla pagina di Wikipedia in lingua inglese si � scelto di far puntare il link alla pagina di Wikipedia in italiano.


#### Immagini

Le immagini

A volte oltre al semplice testo vengono incluse anche delle immagini.
Ovviamente un'immagine, a meno che non sia di una schermata del computer, non si pu� tradurre, quello che va tradotto � il valore della propriet� *alt*, il testo ad essa associato infatti viene riprodotto dagli *screen reader* o nel caso l'immagine non sia disponibile e serve per descrivere il contenuto dellimmagine e rendere accessibile la pagina HTML a tutti.
	<img src="/image/firefox.png" alt="Firefox Logo"/>
	<img src="/image/firefox.png" alt="Logo di Firefox"/>
	
Nel caso delle immagini come si vede non ci sono un tag di apertura e chiusura in quanto non ha senso associare del testo a un'immagine e quindi si utilizza chiudere direttamente il tag `/>`.


## Codici di formattazione e stringhe JavaScript

Le applicazioni web solitamente sono composte da una parte lato server (che nel caso di Mozilla � scritta in Python) e di una parte lato client (che utilizza codice HTML e JavaScript).
Mentre il codice HTML viene usato per formattare contenuti statici, JavaScrip e Python vengono utilizzati per inserire dei contenuti dinamici, nel primo caso generati dall'interazione dell'utente con la pagina (ad esempio cliccando un link) e nel secondo caso direttamente dal server.

Solitamente in tutti i progetti Mozilla le stringhe utilizzate all'interno del codice JavaScript vengono raccolte in un file dedicato (di solito dal nome `javascript.po` o varianti).
In questo tipo di stringhe � importante fare attenzione a inserire virgolette o apostrofi perch� potrebbero essere interpretati come delimitatori della stringa stessa e produrre risultati assai indesiderati.
Per essere sicuri di non causare errori al codice, questi caratteri andrebbero preceduti da una `\`, il consiglio che ci sentiamo di dare � quello di utilizzare sempre le virgolette e gli apostrofi tipografici: **���** (si veda l'appendice per digitare questi caratteri nei vari sistemi operativi).

Un altro carattere speciale che si pu� utilizzare � `\n` e server per mandare a capo il testo.

#### Formattazione delle stringhe lato server

Come detto le applicazioni hanno del codice lato server che a volte viene utilizzato per inserire del codice dinamico nelle pagine, ad esempio per indicare l'autore e la data di un commento in articolo.
Le applicazioni Mozilla girano su dei server Django e utilizzano Python come linguaggio lato server, vediamo quindi alcuni caratteri speciali che si possono incontrare nelle stringhe e che sono in realt� delle istruzioni per inserire del testo in maniera dinamica.
Ci sono diverse sintassi per inserire dei valori presi da variabili e la scelta dipende sostanzialmente dallo sviluppatore che scrive il codice.
Vediamo un esempio pratico.


	Published by %s in date %s
	Published by{0} in date {1}
	Published by %(author)s in date %(date)s
	Published by {author} in date {date}
	
Tutte le sintassi sono valide, la prima per� �, da un punto di vista di un localizzatore, una pessima stringa perch� non consente di modificare l'ordine in cui vengono inseriti i due valori.
La seconda invece � poco descrittiva, le due scelte migliori sono le ultime due perch� consentono sia di invertire l'ordine dei due valori sia di avere un'idea di cosa viene inserito al posto della variabile.

In ogni caso, la cosa pi� importante � quella di assicurarsi di indicare sempre questi codici di formattazione se sono presenti e nel caso siano presenti e si voglia inserire un carattere `%` ricordarsi di raddoppiarlo `%%`.

## Tipi di file
