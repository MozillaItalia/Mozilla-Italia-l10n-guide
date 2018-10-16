# Linee guida di Mozilla Italia

###### Indice
<!-- TOC depthFrom:2 depthTo:5 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Guida di stile](#guida-di-stile)
	- [Ricerca terminologica](#ricerca-terminologica)
		- [Casi particolari: Web e Internet](#casi-particolari-web-e-internet)
			- [Uso aggettivale](#uso-aggettivale)
		- [Casi particolari: le cariche](#casi-particolari-le-cariche)
	- [Interfaccia e messaggi di programma](#interfaccia-e-messaggi-di-programma)
		- [Messaggi del programma](#messaggi-del-programma)
			- [Messaggi di conferma](#messaggi-di-conferma)
			- [Forme di cortesia](#forme-di-cortesia)
			- [Enfasi](#enfasi)
			- [Forme progressive](#forme-progressive)
			- [Personificazione dell’hardware e del software](#personificazione-dellhardware-e-del-software)
		- [Aggettivi e pronomi possessivi](#aggettivi-e-pronomi-possessivi)
		- [Voci di menu/etichette dei pulsanti](#voci-di-menuetichette-dei-pulsanti)
			- [Titoli di finestre](#titoli-di-finestre)
			- [Tooltip (suggerimenti)](#tooltip-suggerimenti)
	- [Documentazione tecnica](#documentazione-tecnica)
- [Nuovi termini: se e quando tradurre](#nuovi-termini-se-e-quando-tradurre)
	- [Non tradurre: i pro e i contro](#non-tradurre-i-pro-e-i-contro)
	- [Tradurre: i pro e i contro](#tradurre-i-pro-e-i-contro)
- [Identità e missione di Mozilla](#identit-e-missione-di-mozilla)
	- [Consigli pratici](#consigli-pratici)

<!-- /TOC -->


## Guida di stile

### Ricerca terminologica
Durante le traduzioni è di fondamentale importanza verificare sempre se un termine ha il suo traducente italiano riconosciuto sul glossario qui di seguito o nelle [memorie di traduzione][transvision] di Mozilla Italia.

Alcuni esempi di scelte terminologiche di Mozilla Italia:

| EN | IT |
|---|---|
|click|clic|
|post|articolo (blog), messaggio (forum)|
|community|comunità|
|login|accesso|
|directory|cartella|
|to encode/decode|codificare/decodificare|
|to encipher/decipher|cifrare/decifrare|
|to encrypt/decrypt|crittare/decrittare|
|encryption|crittografia|

Anche i neologismi usati colloquialmente sono da evitare nella lingua scritta.  
Es.

| No | Sì |
|----|----|
|cliccare|fare clic (senza *k*)|
|postare|pubblicare (un articolo, post ecc.)|
|editare|modificare|
|loggarsi|accedere|

#### Casi particolari: Web e Internet

Anche se è ormai diffuso l’uso di scrivere indifferentemente in minuscolo le parole “internet” e “web”, Mozilla Italia si attiene alla seguente norma vigente.

Come esposto nel [Capitolo 1](../1-Buone_norme_di_traduzione.md#maiuscole-e-minuscole), il sostantivo *Web* va scritto con l’iniziale maiuscola in quanto abbreviazione di *World Wide Web*.

Scrivendo *internet* con l’iniziale minuscola ci si riferisce a reti di qualsiasi dimensione che condividano il medesimo protocollo di comunicazione, ma che non sono necessariamente collegate a **Internet**.

Quando inteso come World Wide Web, Internet dovrebbe essere scritto con la maiuscola, in quanto si riferisce a una rete specifica: la confederazione di tutte le reti tcp/ip direttamente o indirettamente collegate al *backbone* degli Stati Uniti, originata nel progetto ARPAnet.

##### Uso aggettivale
Per motivi descritti precedentemente, quando intesi come sostantivi, si usa il maiuscolo:
es.
>Salviamo il **Web**  
**Internet** è una risorsa per tutti

Quando intesi come aggettivi, vanno invece minuscoli:
es.
>sito **web**  
connessione **internet**

#### Casi particolari: le cariche

I nomi di cariche all’interno di un’organizzazione sono spesso titoli molto specifici e creati ad hoc, di cui non esiste esatto corrispondente in italiano.

In questi casi improvvisare una traduzione arbitraria corre il rischio di causare malintesi sull’effettivo organigramma di un’organizzazione.
Pertanto è consigliabile gestirli alla stregua dei nomi propri e mantenerli in inglese.

Esempi da lasciare invariati:
>Mitchell Baker, Executive Chairwoman  
Chris Beard, Chief Executive Officer  
Mark Surman, President and Executive Director

### Interfaccia e messaggi di programma

**N.B.** Le regole sotto elencate si riferiscono esclusivamente allo stile dell’interfaccia di programma e alla documentazione tecnica (es. [SUMO][SUMO]). Per i contenuti dei siti su *mozilla.org* e iniziative varie è invece opportuno mantenere uno stile più naturale e discorsivo per mettere a proprio agio l’utente.

#### Messaggi del programma

Si tratta dei messaggi che vengono *inviati dal programma all’utente*. È sempre preferibile l’utilizzo dello stile impersonale, evitando quindi il discorso diretto.

>Sì: Visitare la pagina di download per scaricare il programma  
No: Vai alla pagina di download per scaricare il programma

##### Messaggi di conferma

Molto spesso le finestre di dialogo chiedono conferma per una determinata azione contengono la formula “Are you sure you want to…” (*Si è sicuri di volere…*). Di norma tali espressioni non vengono tradotte.

>Sì: Eliminare il file?  
>No: Si è sicuri di voler eliminare il file?

##### Forme di cortesia

Nella lingua inglese sono molto comuni, mentre in italiano le espressioni come *please*, *kindly* ecc. vanno omesse.

>Sì: Per continuare premere OK  
>No: Per continuare si prega di premere OK

##### Enfasi

Le espressioni enfatiche non vengono tradotte e in quei casi si preferisce dare al contenuto una resa più impersonale. Vedi anche la relativa sezione nel [capitolo 1](../1-Buone_norme_di_traduzione.md#punto-esclamativo)

>Sì: Impossibile salvare il file  
>No: Impossibile salvare il file!

##### Forme progressive

Le forme verbali *…ing* + `…` (a volte `…` viene omesso) avvisano l’utente che si sta svolgendo un’operazione in background. Vanno tradotte con il sostantivo relativo all’azione + “in corso…”.

>Loading… : Caricamento in corso…  
Saving…: Salvataggio in corso…  
Exiting… : Uscita dal programma in corso…

**N.B.** Per i puntini di sospensione, utilizzare il carattere `…` invece di premere tre volte di seguito il tasto `.`

##### Personificazione dell’hardware e del software

Da evitare quando possibile, anche volgendo la frase al passivo.

>Sì: Verranno eliminati i dati personali  
>No: Firefox eliminerà i dati personali

#### Possessivi e dimostrativi
Per esigenza di spazio e di utilizzo della forma impersonale, nei messaggi di programma è consigliabile omettere i possessivi (*mio*, *tuo*, *suo* ecc.), ma anche i dimostrativi (*questo* account ecc.) quando l’appartenenza è già implicita.

>Sì: Se il computer non riesce a collegarsi ad Internet  
>No: Se il tuo computer non riesce a collegarsi ad Internet  
>No: Se questo computer non riesce a collegarsi ad Internet

In caso di ambiguità, vanno invece sostituiti con *proprio*, *in uso*, *corrente*  ecc.

>Sì: La versione di Firefox in uso è aggiornata.  
No: La tua versione di Firefox è aggiornata.

>Sì: È necessario effettuare un backup del proprio profilo  
 No: Devi effettuare un backup del tuo profilo

>Sì: All’apertura di Firefox verrà visualizzata la propria pagina iniziale.  
No: Quando apri Firefox, viene visualizzata la tua pagina iniziale.

#### Voci di menu/etichette dei pulsanti

Si tratta delle azioni associate al pulsante o alla voce di menu (oppure il nome della funzione o della finestra di dialogo richiamata al clic del mouse) e possono generalmente essere considerate come *i comandi impartiti dall’utente al programma*. Per questo la forma preferibile è la seconda persona dell’imperativo.

In questa tipologia di contenuto va considerato il fattore *spazio*, per cui la traduzione deve essere il più stringata possibile.

Per questo motivo, vanno evitati quando non strettamente necessari:
- articoli determinativi e indeterminativi
  >No: Invia il messaggio  
	Sì: Invia messaggio

- preposizioni articolate
  >No: Visualizza la sorgente della pagina  
	Sì: Visualizza sorgente pagina

- aggettivi possessivi e dimostrativi
  >No: Salva questa pagina con norme…  
	Sì: Salva pagina con nome…  

  >No: Carica il tuo componente aggiuntivo  
	>Sì: Carica componente aggiuntivo



##### Titoli di finestre

Descrivono l’azione compiuta nella finestra. In mancanza di un nome definito, è preferibile utilizzare il sostantivo relativo all’azione in corso.

>Creating account > Creazione account  
>Saving file > Salvataggio file

##### Tooltip (suggerimenti)

Si tratta dei messaggi descrittivi che compaiono in corrispondenza di un elemento dell’interfaccia al passaggio del puntatore del mouse.

La forma da utilizzare è il presente indicativo, terza persona singolare. Gli articoli determinativi e indeterminativi vanno esclusi solo in casi di eccessiva prolissità (in questi casi potrebbe essere consigliabile anche l’uso di abbreviazioni). Il soggetto è implicitamente l’elemento sotto il cursore.
Esempi:

>Interrompe il caricamento in corso (per il pulsante Stop)  
>Apre una nuova scheda (per il pulsante Nuova scheda)

### Documentazione tecnica

L’informatica è uno degli ambiti in più rapida evoluzione: i termini nascono e cadono in disuso nell’arco di pochi mesi, per questo le lingue diverse dall’inglese stentano a tenere il passo.

Talvolta sembra perfino fatica sprecata ideare un traducente per un termine che magari è destinato a cadere nell'oblio di lì a poco.
In questo ambito se ogni manuale desse la sua personale traduzione dei vari termini, si creerebbero facilmente incomprensioni e ambiguità. Questo è improponibile in un settore dove è richiesta assoluta precisione terminologica.

Spesso il problema della traduzione viene sottovalutato quando si pensa a documentazione per gli sviluppatori. Si ritiene che, lavorando con l’inglese, siano perfettamente in grado di leggere e produrre testi in questa lingua senza sforzo.  
Invece sono molti gli sviluppatori che, non avendo abbastanza confidenza con l’inglese, cercano risorse (spesso tradotte in maniera confusa e poco aggiornata) nella loro lingua madre.

Prova di questa esigenza è il sito [Mozilla Developer Network](MDN), dove gli sviluppatori possono scrivere e *tradurre* articoli tecnici in una vasta gamma di lingue.

È auspicabile, per lo sviluppo di una forte comunità di sviluppatori italiana, oltre che per includere gli sviluppatori che hanno un rapporto problematico con l’inglese, innalzare il livello qualitativo delle traduzioni tecniche, diffondendo le buone pratiche di traduzione, una maggiore attenzione alla forma e consapevolezza dell’utilità di una terminologia italiana.

Per questo l’ideale sarebbe accostare sempre un traduttore, per la parte linguistica e formale, a uno sviluppatore che faccia presente problemi tecnici e soprattutto, in qualità di utente finale, conformi la traduzione alle proprie conoscenze e esigenze.

Può essere utile, per motivi di diffusione internazionale, mantenere in lingua inglese nomi di tecnologie nuove o sconosciute per cui non si è ancora affermato un traducente in lingua italiana. Va considerato che tale documentazione è ad uso e consumo degli sviluppatori, che si muovono in un ambito internazionale e pertanto trovano di maggiore utilità conoscere il termine inglese.

In caso di prodotti o eventi Mozilla, dato che l’associazione ha voce in capitolo sulla decisione, si valuterà insieme di caso in caso se mantenere l’originale o localizzarlo.

## Nuovi termini: se e quando tradurre

Il campo dell’informatica ha senza dubbio adottato come lingua franca l’inglese. Non solo è imprescindibile per gli sviluppatori di tutto il mondo, ma anche nell’esperienza dei comuni utenti entrano con sempre maggiore frequenza parole inglesi, a volte dettate dalle nuove tecnologie, altre da mode e tendenze (es. *selfie*, *tweet* ecc.).

Il compito di un traduttore sembrerebbe chiaro: trasporre tutte queste parole da una lingua all’altra. Eppure al giorno d’oggi appare impensabile convertire in italiano termini come “browser”, “server”, “blog”, “account”.

 Talvolta anche traducenti generalmente accettabili e corretti, come “parola d’ordine” per  *password* o ancora “biscotto” per *cookie*, se utilizzati in ambito informatico genererebbero nell’utente più confusione che altro. Altri termini si sono affermati con un unico traducente, e se tradotti diversamente perdono completamente il riferimento originale. Un esempio è *trash*, che è il *cestino* (la cartella dove si ripongono i file da eliminare), e non “spazzatura”, traduzione pure ugualmente corretta.

Ricapitolando, una traduzione è sempre possibile, ma non necessariamente rappresenta la scelta migliore. La comunità di Mozilla Italia è molto sensibile a questo dilemma.

I prestiti linguistici sono accompagnati da altri fenomeni come i neologismi (cliccare, postare, twittare ecc.) già affrontati a inizio capitolo e le risemantizzazioni, ovvero parole preesistenti che assumono un nuovo significato in un determinato ambito. Alcuni esempi sono l’aggettivo *virale* (non più collegato ai virus, diventa una forma di diffusione di un prodotto in una cerchia di utenti), *meme* (estrapolato dalla biologia, diventa un qualsiasi fenomeno che si diffonde su Internet attraverso l’imitazione spontanea), ma anche il comune termine *amicizia*, che nei social network è diventato sinonimo di essere nella rete di contatti di qualcuno (es. “Ti chiedo l’amicizia su Facebook, così ci teniamo in contatto”.)

Tutti questi fenomeni sono un sintomo positivo della vitalità della lingua che si tiene al passo con le nuove tecnologie, ma devono essere introdotti gradualmente e ponderatamente perché non si trasformino in gergo conosciuto a pochi, escludendo la maggior parte degli utenti.

Di seguito si tenterà di esporre una metodologia per raggiungere un equilibrio, soddisfacendo la necessità di tenere l’utente sempre aggiornato in modo trasparente e intuitivo sui nuovi sviluppi tecnologici, senza però cadere nell’anglofilia o nell’ostentazione fine a se stessa della lingua straniera.

Davanti a un termine in inglese ci sono due strade, entrambe portano i loro vantaggi e svantaggi.

### Non tradurre: i pro e i contro

La prima opzione è lasciare il termine invariato.
Questa scelta è da preferire in caso di termini recentissimi, per i quali non si è ancora affermato un traducente italiano.

Uno dei vantaggi principali di questo metodo è l’ottimizzazione della ricerca per parola chiave e dei *tag* (o “etichette”), perché consente di attingere a risorse contenuti provenienti da qualsiasi parte del mondo.  
Questo, naturalmente, ammesso che l’utente riesca a usufruire di tali risorse  e contenuti nonostante le barriere linguistiche.

>es. Se l’utente digita “wallpaper” (“sfondo scrivania”) in un motore di ricerca, potrà accedere a immagini di sfondi caricate in rete dagli utenti di tutto il mondo. Tuttavia se cerca “digital marketing” troverà articoli, video e altre risorse in una lingua che non è la sua, e ciò potrebbe essergli di scarsa utilità.

Insomma, questo tipo di approccio va a vantaggio degli utenti che hanno una conoscenza almeno funzionale dell’inglese e ne fanno uso in un contesto internazionale.

D’altra parte, anche la strategia di accettare indistintamente tutti i termini inglesi è controproducente.

Data la frequenza con cui compaiono questi termini, alla fine la “traduzione” di certi articoli tecnici o, per citare un altro campo, di marketing, consisterebbe praticamente in un elenco di sostantivi in inglese, interrotti sporadicamente da preposizioni e qualche generico verbo in italiano.

>es. Prima fai il **submit** della **new release** della tua **app** via l’**application form**, poi **posti** una **entry** sul tuo **blog** con tutte le **release notes** e l’**update** della **privacy policy** e **linki** alla **landing page**, e a quel punto fai il più possibile **sharing** sui **social network** e chiedi ai tuoi **followers** di mettere **like** e di fare **retweet**. E non dimenticare di **uppare** anche qualche **screenshoot** per dare una **preview** delle **last features**.

Questo, oltre a risultare in un testo di difficile comprensione, influisce anche sulla capacità espressiva del lettore, che alla lunga impoverirà e banalizzerà il proprio linguaggio. In più si tratta di un compromesso poco soddisfacente per chi conosce l’inglese, che trarrebbe più giovamento dal leggere i contenuti direttamente in lingua originale.

Al contrario favorisce, in chi l’inglese non lo conosce, atteggiamenti non ragionati e snobistici, come ostentare vocaboli inglesi (di cui a volte non si conosce il significato) con la percezione di apparire più professionali e aggiornati, senza però portare a quella consapevolezza e approfondimento che sono traguardo dell’alfabetizzazione web.

### Tradurre: i pro e i contro

L’altra opzione è conferire al termine un traducente italiano.

Le traduzioni in italiano trasparenti e riconoscibili dei termini inglesi hanno il vantaggio “didattico” di portare a una consapevolezza più pragmatica e profonda dei termini.

Al contrario di molti termini stranieri, che spesso l’utente memorizza come una serie di suoni senza significato, i termini italiani riconducono la mente a una forma tangibile, avvicinandola alla tecnologia in modo intuitivo.

> Alcuni esempi sono “cartella” (*directory* o *folder*), “cestino” (*trash*), “casella di posta”(*mailbox*), i comandi “taglia” e “incolla” (*copy*, *paste*), parole che richiamando oggetti e azioni comuni hanno contribuito a trasformare la rivoluzione informatica in uno strumento quotidiano a portata di tutti proprio perché gli utenti dei vari paesi li hanno potuti internalizzare nella propria lingua madre.

Tuttavia per questi termini italiani che hanno avuto tanto successo, altri sono caduti nell'oblio, soppiantati dalla loro controparte inglese. Tra questi ricordiamo “archivio” (*file*), “navigatore” (*browser*), “parola d’ordine” (*password*), “dispositivo di puntamento ottico” (*mouse*).

Dunque dare una “voce italiana” alle nuove tecnologie rientra pienamente nel programma di alfabetizzazione web dell’utente di Mozilla e nei principi dell’Open Source.

Tuttavia, laddove un termine inglese è ormai entrato nell’uso, diventa controproducente tentare di imporre una terminologia italiana,  che rischia al contrario di confondere l'utente.

## Identità e missione di Mozilla

Un discorso a parte va fatto quando un’organizzazione decide di localizzare la *propria* terminologia in diverse lingue, e ne fornisce quindi una traduzione ufficiale.

Delineare una propria terminologia ufficiale, oltre che, perché no, utilizzare la propria posizione di rilevanza per promuovere e arricchire la terminologia del panorama informatico italiano, è un importante passo per sancire la propria identità come organizzazione e costituire un punto di riferimento per la comunità di utenti anche a livello linguistico. Può perfino diventare un momento di aggregazione e uno spunto per discussioni tra i membri della comunità stessa.

Uno dei punti di forza di Mozilla è la localizzazione in numerose lingue di prodotti ed eventi, in modo che gli utenti di ogni dove si sentano “a casa” utilizzandoli.

In conclusione il modus operandi di Mozilla Italia è cercare di armonizzare la chiarezza e la precisione terminologica dei termini internazionali con la scorrevolezza e la semplicità di una spiegazione in lingua italiana.

Tra queste due esigenze ovviamente la comprensione univoca di un termine deve venire sempre al primo posto rispetto all’eleganza di uno stile in bell’italiano.

### Consigli pratici
In caso il glossario ufficiale non offra indicazioni, si può cercare un traducente italiano appropriato e universalmente riconosciuto su altre fonti autorevoli, per esempio [Language Portal][mlp] di Microsoft.

Quando ci si trova davanti a un nuovo termine, per evitare scelte dettate da gusti personali e argomentazioni soggettive, è utile porsi le seguenti domande:
- Il termine presenta già un traducente affermato e riconoscibile in lingua italiana? (Verificare per esempio su [Language Portal][mlp] o altre fonti autorevoli). Se sì, ci sono motivazioni solide per non utilizzarlo?

- Che diffusione e impatto ha il termine? È una parola destinata a comparire con frequenza, oppure un vocabolo che si usa raramente e  in contesti circoscritti?

- Chi è il “lettore ideale” del termine? L’utente comune? Lo sviluppatore?

- Mantenere il termine non tradotto porterebbe dei vantaggi significativi al lettore (es. ottimizzazione nei motori di ricerca, comunicazione con utenti stranieri ecc.)?

- Tradurre il termine in italiano potrebbe dare adito a fraintendimenti o incomprensioni nel lettore?
> Es. “diario web” per *blog*  “soprannome” per *nickname*

- Esiste un traducente trasparente e univoco che lascia intuire senza pericolo di confusione del termine in lingua di partenza?
> Es. *mailbox* > “casella di posta”

- Il termine tradotto stabilisce un legame di familiarità con il lettore e rende il discorso in lingua italiana più fluente e comprensibile?

In presenza di un traducente accettabile, Mozilla Italia preferisce sempre fare uso dei termini italiani e promuoverli in rete sfruttando la sua posizione rilevante per abituare l’utente a un linguaggio più consapevole del significato dei termini e non impoverito dall’uso di anglicismi.

[transvision]:https://transvision.mozfr.org/
[mlp]:https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT
[MDN]:https://developer.mozilla.org/
[SUMO]:https://www.mozillaitalia.org/home/sumo/
