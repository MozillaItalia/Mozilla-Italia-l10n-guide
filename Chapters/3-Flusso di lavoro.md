# Flusso di lavoro
In quanto siamo un'organizzazione con un'identità ben definita, tutti i nostri prodotti devono conformarsi a certi standard, terminologici e linguistici.
>Per questo motivo tutte le traduzioni devono passare attraverso un processo di revisione (a.k.a. QA – Quality Analysis) da parte dei localizzatori senior.

Questo vuol dire che le traduzioni dei volontari verranno inserite come provvisorie e in seguito approvate se sono accettabili, oppure verrà chiesto ai volontari stessi di correggerle per uniformarle ai nostri standard.

Il lavoro di localizzazione non si esaurisce nello scrivere la traduzione a fronte di una stringa e poi andarsene.
Prima c'è tutto un lavoro di ricerca della terminologia non solo corretta, ma anche coerente con lo stile Mozilla e con i prodotti localizzati in precedenza.

Dopo, invece, c'è tutto il processo di QA, che prende quasi più tempo della traduzione stessa. In questa fase i localizzatori più anziani proporranno modifiche e correzioni spiegandone la motivazione. Il volontario dovrà dunque tornare sulle proprie traduzioni e apportare le correzioni, oppure proporre una nuova versione tenendo conto dei problemi che gli sono stati fatti notare.

Infine occorre tener conto che un progetto non è mai tradotto una volta per tutte: vengono sempre aggiunte nuove stringhe mano a mano che il sito viene aggiornato. Per questo unirsi al team di localizzazione significa non solo tradurre le stringhe presenti ma prendersi l'impegno di seguire il progetto a lungo termine, controllando regolarmente gli aggiornamenti.

Un ultimo, scontato quanto prezioso, consiglio: la differenza tra una traduzione mediocre e una eccellente sta spesso nel contesto. Quindi ogni volta che si trova una frase di cui non si riesce bene ad afferrare il senso, una ambigua che magari abbia più traduzioni possibili, la cosa migliore da fare è cercarla sulla pagina del sito e vederla nel suo contesto originale per dare la traduzione più appropriata.

## Indice
  * [Pontoon](#pontoon)
  * [Poedit](#poedit)
  * [Wiki](#wiki)
  * [Documenti di testo vari](#documenti-di-testo-vari)

## Pontoon
La maggioranza dei progetti Mozilla è traducibile attraverso lo strumento di traduzione online di Mozilla, [Pontoon](https://pontoon.mozilla.org/).

Pontoon estrapola tutto il contenuto traducibile di un sito web e lo divide in piccole unità, chiamate "stringhe", permettendoci di inserire la traduzione corrispondente a ciascuna stringa, poi ricaricano la nostra traduzione sul sito web.
Questa interfaccia permette a chiunque di tradurre in modo intuitivo, mentre tradurre direttamente il codice sorgente del sito web richiederebbe una buona esperienza con il codice HTML che non tutti possiedono.

### Impostazioni e interfaccia
Per tradurre un progetto è necessario registrarsi gratuitamente a Pontoon, utilizzando un [account Firefox](https://www.mozilla.org/it/firefox/accounts/) (se non se ne possiedi già uno, si può crearlo direttamente la prima volta che si accede a Pontoon).

Di seguito le informazioni necessarie per sfruttare appieno le potenzialità di Pontoon nella traduzione collaborativa.

**Tracciabilità:** è possibile inserire una traduzione solo se si è registrato un account, questo vuol dire che è possibile rintracciare con precisione chi ha tradotto cosa, dove e quando, soprattutto si può lavorare in più persone allo stesso progetto aggiornato in tempo reale.

**Opzione filtro:** (l'icona ad imbuto in alto a sinistra) permette di estrapolare le stringhe d’interesse. I filtri sono:

- Missing (non ancora tradotte)

- Fuzzy (sono state tradotte automaticamente usando la memoria informatica, ma hanno bisogno di revisione umana)

- Suggested (proposta di traduzione in attesa di revisione)

- Translated (stringhe tradotte, approvate e pronte per essere pubblicate)

**Altre opzioni**

Sotto la stringa si trovano i 3 tab
- *History* (tutte le traduzioni che sono state date per quella stringa finora),
- *Machinery* (traduzioni automatiche),
- *Locales* (come la stringa è stata tradotta in altre lingue).

*Machinery* è una funzione molto preziosa, ma mai da prendere per oro colato. Bisogna sempre guardare la fonte delle soluzioni che propone, in grigio sopra la traduzione.

- Il tag `Machine translation` : traduzioni automatiche di Bing, il più delle volte non sono degne di considerazione.
- Il tag `Translation Memory`: traduzioni date da esseri umani, prese dal database di Mozilla. Ovviamente se ha senso nel contesto, è bene attenersi il più possibile a quella traduzione per coerenza terminologica (es. se vedi che Privacy Policy è stato tradotto Informativa sulla Privacy, non mettere Legge sulla Privacy o simile).<br>
**N.B.** La percentuale accanto al tag esprime il grado di corrispondenza, per esempio `100%` è una stringa identica, `80%` magari cambia una preposizione, un plurale, un tag ecc. e quindi va adeguata di conseguenza.*

*Machinery* può anche essere utilizzato come glossario o dizionario grazie alla barra di ricerca in alto. Basta digitare la parola interessata e appariranno varie traduzioni prese da fonti diverse:
- Tag `Mozilla` è preso dal [database di Mozilla](https://transvision.mozfr.org/), quindi è quella da privilegiare se è disponibile.
- Tag `Microsoft` è presa dal [Microsoft Language Portal](https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT)
<br> **N.B.** Questo glossario sarà molto utile anche fuori da Mozilla per chi traduce professionalmente nel campo dell'informatica.
- Tag `Translation Memory` è estrapolata dal database di Pontoon.
- Tag `Open Source` è presa da un glossario comunemente condiviso nel mondo dell'Open Source (Linux ecc.)

### Workflow di traduzione e revisione usando il filtro
Poniamo di avere un progetto molto voluminoso con metà stringhe già tradotte e metà ancora no.

#### Fase 1: Traduzione
Il traduttore:
1. Esegue l'accesso
2. Va nelle sue impostazioni (icona ingranaggio sotto l'icona in alto a destra) e seleziona la modalità "Make suggestion"
3. Va al progetto
4. Dal filtro seleziona "Missing", così da poter accedere direttamente alle stringhe senza traduzione.
5. Traduce e conferma con il pulsante blu "Suggest". La stringa apparirà ora sotto il tag History, con il nome del traduttore e l'ora di immissione.

#### Fase 2: Revisione
Il revisore:
1. Esegue l'accesso
2. Va al progetto
3. Dal filtro seleziona "Suggested", così da ritrovarsi le stringhe che il traduttore gli ha lasciato da revisionare
4. Se la traduzione è buona, preme il pulsante "Save", confermando la stringa come "Translated". Se ha in mente una soluzione alternativa invece, scrive la sua versione e preme il pulsante Suggest. La sua versione finisce in cima alla lista, sopra quella del traduttore, nel tab History.

#### Fase 3: Correzione
Il traduttore:
1. Nel progetto seleziona dal filtro "Suggested" e confronta tutti i cambiamenti fatti dal revisore con la sua versione.
2. Dà l'OK alla correzione del revisore oppure propone un'altra versione in suggerimento (che apparirà sempre in cima alle altre nel tab History) finché non si trova un comune accordo tra i due.

Questo è un sistema che abbiamo collaudato nel tempo per lavorare in tandem impiegando meno tempo e riducendo il rischio di lasciare qualcosa non tradotto.

## Poedit
[PoEdit](https://poedit.net/) è il software più diffuso per la gestione dei cataloghi .po. È un software multipiattaforma scaricabile gratuitamente nella sua versione di base.

A Mozilla è preferibile tradurre i file .po dalla piattaforma online Pontoon, che è aggiornata in tempo reale. <br>Tuttavia in molti casi, come per esempio le piccole associazioni che non possiedono una piattaforma di traduzione dedicata, un piccolo progetto su cui lavora una persona alla volta o in assenza di connessione ad Internet, la versione gratuita di Poedit rappresenta un ottimo strumento con tutte le funzioni necessarie per un progetto di traduzione collaborativa.

### Impostazioni
#### Impostare i dati personali del traduttore
Per impostare le proprie preferenze e inserire nome e email che compariranno nei metadati delle stringhe, accedere al menu *Poedit > Preferenze > Generale*.

È consigliabile selezionare anche la casella *Controllo ortografico*.

#### Impostare la lingua del progetto
Dal menu *File > Apri…* selezionare il file .po che contiene le stringhe da tradurre.

Dal menu *Catalogo > Proprietà* controllare che i seguenti parametri per la traduzione in lingua italiana siano impostati correttamente (nel caso dei file Mozilla i valori dovrebbero già essere impostati automaticamente).

```
Lingua: italiano (it-IT)
<br>Forme plurali: nplurals=2; plural=(n != 1);
<br>Set di caratteri: UTF-8
```

#### Impostare la memoria di traduzione

Poedit, al pari di Pontoon, è dotato di una funzione di memoria che suggerisce stringhe simili o identiche tradotte in precedenza.
<br>La differenza è che, mentre Pontoon attinge automaticamente alla versione più aggiornata di tutte le memorie di traduzione di Mozilla, in Poedit è l'utente a dover caricare e tenere aggiornate le proprie memoria di traduzione.

Per aggiungere una memoria di traduzione su Poedit:
- Andare su *Poedit > Preferenze > MT*.
- Selezionare la casella *Usa la memoria di traduzione* **N.B.** Da questo momento le tutte le traduzioni svolte verranno salvate nella memoria di traduzione per riferimenti futuri.
- Fare clic sul pulsante *Impara dai file…* e selezionare dalla finestra a comparsa un file .po almeno parzialmente tradotto da cui si vuole estrapolare la TM^. Poedit estrapolerà le stringhe tradotte per utilizzarle come suggerimento nei progetti futuri.

Dalla prossima apertura del file po con Poedit, sarà possibile visualizzare la traduzione di tutte le stringhe a essa somiglianti nella colonna *Suggerimenti di traduzione*.
<br>Sotto ogni concordanza suggerita si trova il grado di concordanza con la stringa, espresso in percentuale. Un suggerimento con concordanza 100% è identico nel testo sorgente, fino a 75-80% è molto simile al testo sorgente, ma il testo di arrivo richiederà aggiustamenti minimi (un termine, un plurale ecc.). Sotto la soglia di 60% il suggerimento ha un valore puramente contestuale, ovvero può suggerire i traducenti di parte dei termini utilizzati, ma non la traduzione completa.
N.B. Anche in caso di corcondanze al 100%, il traduttore deve sempre verificare l'appropriatezza della traduzione rispetto al contesto.

^ Idealmente sarebbe un file contenente le traduzioni precedenti del medesimo progetto o della medesima organizzazione, tuttavia potrebbe anche trattarsi di un testo di argomento simile di cui si desidera prendere a modello stile e glossario, per esempio chi sviluppa un progetto open source potrebbe utilizzare una memoria di traduzione di Linux.

### Interfaccia e navigazione
L'interfaccia di Poedit presenta una tabella di tre colonne:
- Testo sorgente: il testo originale da tradurre
- Traduzione: dove viene visualizzata la traduzione
- Suggerimenti di traduzione: contiene i suggerimenti presi dalla memoria di traduzione del progetto o commenti vari.

In fondo alla finestra sono presenti un campo con il testo sorgente della stringa correntemente selezionata e un altro campo sottostante dove digitare il testo della traduzione.

#### Contrassegnare le stringhe per la revisione

Quando si lavora su un catalogo .po di grandi dimensioni già parzialmente tradotto, è utile, per non dire essenziale, marcarle in modo che chi le corregge possa controllare solo quelle senza rileggere l'intero catalogo.

Per marcare le stringhe per il processo di revisione, selezionare la stringa in questione e fare clic sul pulsante Non pronta nella barra degli strumenti in alto o con CTRL+U. La stringa verrà contrassegnata con un colore diverso.

È possibile scorrere tutte le stringhe di cui è composto il progetto, oppure ordinare le stringhe in modo da ordinare per prime quelle non tradotte. dal menu *Visualizza > Prima voci non tradotte* (opzione caldamente consigliata in caso ci si occupi di un progetto già iniziato).



### Fase 1: Traduzione
Il traduttore:
1. Apre il file .po
2. Se è un file parzialmente tradotto, filtra  le stringhe da tradurre dal menu *Visualizza > Prima voci non tradotte*
3. Inserisce la traduzione nell'apposito campo
4. Marca la traduzione per la revisione <br>(dal menu *Modifica > La traduzione richiede una verifica*, scorciatoia da tastiera `Cmd`+`U`, o premendo l'apposito pulsante nell'angolo in alto a destra del campo *Traduzione:* )
5. Fa un rapido controllo automatico dal menu Catalogo > Verifica traduzioni
5. Salva il file dal menu *File > Salva*
6. Trasmette il file .po salvato al revisore via email o altro canale concordato.

### Fase 2: revisione
Il revisore:
1. apre il file .po
2. filtra le stringhe contrassegnate per la revisione dal menu *Visualizza > Prima voci non tradotte*
3. si trova davanti due possibilità:
  -  se la traduzione è accettabile, la conferma dal menu *Vai > Applica e prosegui*, scorciatoia da tastiera `cmd`+`Enter`, o premendo il pulsante nell'angolo in alto a destra sopra il campo *Traduzione:*.
  - se ha in mente una soluzione alternativa, inserisce la sua versione e ricontrassegna la stringa per la revisione.
4. Fa un rapido controllo automatico dal menu Catalogo > Verifica traduzioni
5. Salva il file dal menu *File > Salva*. Se tutte le stringhe sono state tradotte, carica il file online, se invece ha apportato delle correzioni, risottopone il file al traduttore per la terza fase.

### Fase 3: Correzione
Fase 3: Correzione
Il traduttore:

1. Apre la versione più recente del file .po inviatogli dal revisore.
2. Filtra le stringhe revisionate dal menu *Visualizza > Prima voci non tradotte*
2.Dà l'OK alla correzione del revisore oppure propone un'altra versione in suggerimento (che apparirà sempre in cima alle altre nel tab History) finché non si trova un comune accordo tra i due.
3. Si trova davanti due possibilità:
  -  se la revisione è accettabile, la conferma dal menu *Vai > Applica e prosegui*, scorciatoia da tastiera `cmd`+`Enter`, o premendo il pulsante nell'angolo in alto a destra sopra il campo *Traduzione:*.
  - se ha in mente una soluzione alternativa invece, scrive la sua versione e ricontrassegna la stringa per la revisione.
4. Fa un rapido controllo automatico dal menu Catalogo > Verifica traduzioni
5. Salva il file dal menu *File > Salva*. Se ha apportato nuove modifiche rispetto alla versione del revisore, si ripete il processo dalla fase 2 finché il progetto non sarà tradotto al 100%.

## MDN
[Mozilla Developer Network](https://developer.mozilla.org) è una piattaforma in stile wiki su cui chiunque può contribuire con documentazione sull'Open Web.

MDN prospera non solo grazie al contributo degli sviluppatori che scrivono i loro articoli, ma anche ai volontari che traducono tali articoli nella loro lingua, permettendo agli sviluppatori loro connazionali di accedervi.

Data la sua natura di documentazione tecnica, il traduttore deve conoscere a sufficienza la materia e il processo di QA per MDN deve essere particolarmente rigoroso. Inoltre la documentazione di MDN è in continua evoluzione, per cui è necessario aggiornare frequentemente gli articoli di cui ci si prende carico.

### Impostazioni e interfaccia
MDN è una piattaforma stile [wiki](https://it.wikipedia.org/wiki/Wiki), ovvero si tratta di una raccolta di testi online (articoli) che possono essere modificati o tradotti in varie lingue da collaboratori registrati.

Per registrare un profilo di collaboratore occorre autenticarsi con le credenziali di GitHub. Chi non lo ha ancora può [creare un account su GitHub](https://github.com/join?return_to=%2Flogin%2Foauth%2Fauthorize%3Fclient_id%3D21df88df73c82ea9fd75%26redirect_uri%3Dhttps%253A%252F%252Fdeveloper.mozilla.org%252Fusers%252Fgithub%252Flogin%252Fcallback%252F%26response_type%3Dcode%26scope%3Duser%253Aemail%26state%3D6RALVyGgStTO&source=oauth) gratuitamente.
Una volta effettuato l'accesso è possibile compilare il proprio profilo facendo clic sul nome utente in alto a destra.
MDN tiene traccia di tutti i contribuiti e ogni articolo tradotto rimanderà al profilo dell'utente che lo ha tradotto o modificato.

Ora si è pronti ad esplorare MDN in cerca di un articolo da tradurre, o ancora meglio, mettersi in contatto con la comunità e chiedere quali articoli hanno la maggiore priorità.

La traduzione degli articoli avviene attraverso un editor di testo online che utilizza un linguaggio di markup semplificato.

Guardiamo le varie sezioni della pagina di traduzione:
#### Translate description
 È una parte brevissima ma importante che serve a tradurre i metadati.
 In particolare:
- Title: il titolo dell'articolo
- Slug: la parte finale dello URL dell'articolo italiano, idealmente dovrebbe riportare le parole del titolo separate dal carattere `_`

#### Translate content
Il corpo dell'articolo, tecnicamente la traduzione vera e propria.
Il contenuto è incasellato in un editor di testo che utilizza il linguaggio markdown.
Il testo sorgente è a fronte del testo da tradurre, in modo da poterli confrontare in qualsiasi momento.

Ciascuno ha le sue preferenze per gestire questa parte della traduzione.

La soluzione più semplice è intervenire direttamente sull'editor online, sostituendo il testo inglese con quello italiano senza intaccare la formattazione.

Chi si trova a proprio agio con il codice di markdown può premere il tasto *Sorgente* in alto a sinstra del campo di traduzione per modificare direttamente il codice sorgente.

Altri preferiscono copiare il corpo dell'articolo e incollarlo nel loro programma di scrittura preferito per tradurlo con calma offline. Una volta terminato, copia la traduzione e la incolla nuovamente nell'editor.

Un passo successivo: per sfruttare risorse come memorie di traduzione e glossari, oltre che per essere facilitati all'aggiornamento di un articolo senza ritradurre tutto da capo, è utilizzare OmegaT.

#### Translate tags
I tag aiutano gli utenti a raggiungere contenuti rilevanti. Tradurre i tag non è una scienza esatta: invece che tradurre i tag alla lettera, bisogna piuttosto pensare a quali parole chiave cercano gli utenti italiani interessati all'articolo in traduzione.
#### Version notes
- Localization flags: seleziona la casella *Localization in progress - not completely translated yet.*
- Review needed: seleziona il tipo di revisione che richiede l'articolo: Editorial è il solito QA di tipo grammaticale e stilistico, Technical può essere selezionato se è richiesto un parere tecnico.
- Revision comment: è buona norma che a ogni salvataggio l'utente inserisca un breve messaggio che spieghi cosa ha fatto. Per esempio il traduttore scriverà "Prima bozza dell'articolo", il revisore alla fine della sua revisione scriverà "corretta la terminologia in base al glossario ufficiale" o altre modifiche fatte.


### Fase 1: Traduzione
Il traduttore:
1. Si autentica su MDN
2. Naviga fino all'articolo da tradurre
3. Fa clic sul pulsante *Languages* in alto a destra. Qui ha due possibilità:
  * se la sua lingua è già nella lista del menu a comparsa, una traduzione esiste già. Selezionare la lingua desiderata per leggere la versione tradotta: può darsi che siano necessari dei miglioramenti.

   * se la sua lingua non è presente in elenco, selezionare *Add a translation* e scegliere la lingua da aggiungere.

4. Compilare i vari campi dell'articolo e digitare la traduzione nell'apposito editor.

5. Nella sezione *Localization flags* controllare che la casella *Localization in progress - not completely translated yet.* sia selezionata.

6. Nella sezione *Review needed* selezionare la casella * Editorial*. Se si cerca un parere tecnico, selezionare anche *Technical*.

7. Lasciare un commento, es. "Prima bozza", nella sezione *Revision Comment*.

8. Preme il pulsante *PUBLISH* in alto a destra.

9. Contattare il revisore tramite il canale concordato.

### Fase 2: Revisione
Il revisore:
1. Si autentica su MDN
2. Naviga fino all'articolo da revisionare
3. Fa clic sul pulsante *EDIT*
4. Inserisce le opportune modifiche.
5. Nella sezione *Localization flags* controllare che la casella *Localization in progress - not completely translated yet.* sia selezionata.
6. Lascia un commento nella sezione *Revision Comment*, riassumendo a grandi linee le modifiche.
7. Preme il pulsante *PUBLISH* in alto a destra.
8. Contatta il traduttore tramite il canale concordato.

Fase 3: Correzione
Il traduttore:
1. Si autentica su MDN
2. Naviga fino all'articolo revisionato.
3. Controlla le modifiche.
 * Un modo molto pratico per farlo è andare sull'icona dell'ingranaggio in alto a destra, selezionare *Visualizza storico*.
 Selezionare le versioni da confrontare: la prima bozza e la revisione e premere *Confronta le traduzioni selezionate*. Verrà generato un file, detto *diff*, dove sono evidenziate tutte le aggiunte, le elisioni e le modifiche effettuate dal revisore.
4. Torna all'articolo e preme il pulsante *EDIT* in alto a destra.
5. Ci sono due possibilità:
 * se le modifiche del revisore sono accettabili, deseleziona la casella *Localization in progress* e preme nuovamente *PUBLISH* per marcare l'articolo come completo.
 * se le modifiche non vanno bene, effettua nuove modifiche.
 5. Nella sezione *Localization flags* controlla che la casella *Localization in progress* sia selezionata.

 6. Lascia un commento spiegando in linea generale le modifiche, nella sezione *Revision Comment*.

 7. Preme il pulsante *PUBLISH* in alto a destra.

 9. Contattare il revisore tramite il canale concordato.

 E il ciclo si ripete finché non si trova una versione che soddisfi entrambi. Il revisore può usare a sua volta lo storico per individuare le modifiche successive.

## SuMo
Per il momento fare riferimento a [questo topic](https://forum.mozillaitalia.org/index.php?topic=32659.0)
