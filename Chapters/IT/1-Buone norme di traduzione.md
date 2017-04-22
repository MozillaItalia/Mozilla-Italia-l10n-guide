# Buone norme di traduzione tecnica
Questo capitolo raccoglie le cosiddette “buone pratiche”, ovvero un insieme di regole condivise (non solo da Mozilla Italia, ma in tutto il panorama italiano) che contraddistinguono una traduzione tecnica di buona qualità.

Si tratta di un capitolo corposo e dettagliato, in continua espansione. È concepito per essere tenuto a portata di mano durante la traduzione e consultato all’occasione mediante l’[Indice dei contenuti](#indice-dei-contenuti).

## Indice dei contenuti
* [Ortografia](#ortografia)
  - [Punteggiatura](#punteggiatura)
   - [Virgola](#virgola)
   - [Punto](#punto)
   - [Punto esclamativo](#punto-esclamativo)
   - [Apostrofo](#apostrofo)
   - [Virgolette](#virgolette)
   - [Ellissi](#ellissi)
   - [Trattini](#trattini)
  - [Maiuscole e miniscole](#maiuscole-e-minuscole)
  - [Plurale dei vocaboli stranieri](#plurale-dei-vocaboli-stranieri)
  - [Genere dei vocaboli stranieri](#genere-dei-vocaboli-stranieri)
* [Libertà stilistiche e calchi linguistici](#libertà-stilistiche-e-calchi-linguistici)
  - [Lunghezza delle frasi
](#lunghezza-delle-frasi)
  - [Lessico](lessico)
  - [Verbi e sostantivi](#verbi-e-sostantivi)
  - [Aggettivi](#aggettivi)
  - [False friend](#false-friend)
  - [Diatesi](diatesi)
* [Quando tradurre e quando no](#quando-tradurre-e-quando-no)
  - [Nomi comuni](#nomi-comuni)
  - [Nomi propri](#nomi-propri)
  - [Casi particolari](#casi-particolari)

### Ortografia
#### Punteggiatura
##### Virgola
Durante una traduzione è importante essere consapevoli delle sottili differenze nell'uso della punteggiatura tra una lingua e l'altra. Questo è il caso della virgola.

In inglese la virgola viene utilizzata anche dopo le congiunzioni.

es.
>EN: For safety, privacy**, and** freedom on the Web

In italiano, al contrario, avendo entrambe lo stesso ruolo, la congiunzione esclude la virgola e viceversa.

es.
>IT: Per la sicurezza, la privacy **e** la libertà sul Web

Eccezione va fatta naturalmente per il discorso degli incisi.

>Se Marco si lascerà scappare il nostro segreto**, e sono sicuro che prima o poi lo farà,** finiremo tutti nei guai fino al collo.

##### Punto
Le sequenza `.”.`, `.).` e simili sono considerate graficamente sgradevoli e pertanto da evitare.

Dunque, qualora si verificassero, si omette il punto all’interno delle virgolette o parentesi lasciando solo quello esterno.
es.
>Sì: Gli risposi “Ora puoi andare**”.**
<br>No: Gli risposi: “Ora puoi andare**.”.**

Il punto va anche evitato alla fine dei titoli.

es.
>Sì: La guida di localizzazione di Mozilla Italia
<br>No: La guida di localizzazione di Mozilla Italia**.**

##### Punto esclamativo
Viene utilizzato spesso (a volte abusato) nello stile informatico anglofono, specialmente nei messaggi di sistema che notificano un errore.

Nello stile di localizzazione italiano, e a Mozilla Italia in particolare, è da dosare con parsimonia.

es.
>EN: Error 404: page not found**!**
<br>IT: Errore 404: pagina non trovata**.**

In ogni caso, sono *sempre* da evitare le stringhe continue di punti esclamativi o interrogativi come
>No: Collabora con noi!!!!!!!!!!!!!!

In casi eccezionali, per denotare una particolare enfasi saranno sufficienti tre punti esclamativi di seguito `!!!`.

##### Apostrofo
L’apostrofo “diritto” `'` , detto anche dattilografico, è quello più comunemente accessibile sulle tastiere.
Tuttavia, esso viene utilizzato anche in vari tipi di codice, per questo può generare conflitti nei documenti misti di testo e codice.

Meglio dunque utilizzare l’apostrofo curvo, detto anche tipografico `’`.

>Scorciatoie da tastiera per l’apostrofo curvo:
<br>**Windows** `AltGr + Shift + B`
<br>**MacOS** `Alt + Shift + 3`
<br>**Linux** ???

Errori più comuni per l’apostrofo:
>Sì: un altro
<br>No: un'altro

e simili casi di articolo indeterminativo + maschile.

> Sì: Qual è
<br>No: Qual’è

In realtà il dibattito tra i linguisti italiani è ancora aperto, ma per uniformità stilistica scegliamo di adottare la versione priva di apostrofo.

##### Virgolette
Per la stessa ragione dell’apostrofo, preferiamo alle virgolette dritte, quelle curve.

**N.B.** Le virgolette dritte sono intercambiabili, ma quelle curve sono due distinte, una per l'apertura `“` orientata verso sinistra, e una di chiusura, orientata verso destra `”`.

>Scorciatoie da tastiera per le virgolette curve:
<br>**Windows** apertura `AltGr + V`, chiusura `AltGr + B`
<br>**MacOS** apertura `Alt + 2`, chiusura `Alt + Shift + 2`
<br>**Linux** ????

##### Ellissi
Per digitare i puntini di sospensione, chiamati anche ellissi, molti premono semplicemente il tasto `.` tre volte in successione. In realtà il simbolo dell’ellissi ha la sua combinazione di tasti dedicata.

>Scorciatoie da tastiera per ellissi:
<br>**Windows** `Alt + 0133`
<br>**MacOS**  `Alt + ,`
<br>**Linux** ????

Questo accorgimento diventa particolarmente utile in caso di limitazione dei caratteri, per esempio nei *tweet* di Twitter: infatti `…` viene conteggiato come un solo carattere.

##### Trattini
Occorre fare una distinzione tra il trattino corto `-` e il trattino lungo `–`.

Il trattino corto va utilizzato esclusivamente come *trait d’union* in un composto formato da due parole, senza spazi in mezzo.

**N.B.** Alcuni vocaboli, che inizialmente erano composti da due parole distinte col trattino, sono tanto entrate nell’uso che possono venire scritte senza.
Esempi sono le seguenti parole:

>e-mai / email
<br>on-line / online
<br>multi-piattaforma / multipiattaforma

Il trattino lungo è usato per gli incisi, o comunque per separare due frasi, e va sempre preceduto e seguito da uno spazio.

>Scorciatoie da tastiera per il trattino lungo:
<br>**Windows** `Alt + 0151`
<br>**MacOS** `Alt + -`
<br>**Linux** ????

Il trattino lungo viene molto usato in inglese, ma non è altrettanto comune in italiano. Quando possibile è meglio sostituirlo con un altro segno di punteggiatura appropriato al caso.

es.
>EN: Firefox **–** The browser that puts privacy at the first place
<br>IT: Firefox**:** il browser che mette la privacy al primo posto.

oppure

>EN: Firefox **–** the browser that puts privacy at the first place **–** is now available for Android.
<br>IT: Firefox**,** il browser che mette la privacy al primo posto**,** è ora disponibile per Android.

#### Maiuscole e minuscole

Le regole della maiuscola sono diverse in italiano e in inglese. In italiano vanno comunemente scritte con la maiuscola:
- nomi propri
- acronimi <br>es.
>HTML (**H**yper**T**ext **M**arkup **L**anguage)
<br>URL (**U**niform **R**esource **L**ocators)

- abbreviazioni
<br> es.
>Web (World Wide **Web**)

- la prima lettera di ciascun termine che indichi il nome di un tasto della tastiera
- la prima lettera della prima parola di un periodo
- la prima lettera della prima parola di un titolo es.
>EN: **H**ow to **C**ontribute in the **I**talian **C**ommunity
<br>IT: **C**ome collaborare nella comunità italiana

 **N.B.** I titoli *non* terminano mai con `.`

- la prima lettera della prima parola di una funzione o di un’opzione

Ecco alcune categorie di vocaboli scritti sempre con la maiuscola in inglese ma non in italiano:

| Vocaboli | Inglese | Italiano |
| --- | --- | --- |
|Nomi dei giorni della settimana:|Monday, Tuesday, Wednesday ecc.|lunedì, martedì, mercoledì ecc.|
|Nomi dei mesi|January, February, March ecc.|gennaio, febbraio, marzo ecc.|
|Aggettivi di nazionalità| English, Italian, Chinese|italiano, inglese, cinese ecc.|

##### Eccezioni
Si sta diffondendo sempre di più l'uso di scrivere sempre indifferentemente in minuscolo le parole “internet” e “web”, Mozilla si attiene alla seguente norma vigente.

Quando intesi come sostantivi, si usa il maiuscolo:

es.
>Salviamo il **Web**
<br>**Internet** è una risorsa per tutti

Quando intesi come attributi vanno invece minuscoli:

es.
>sito **web**
<br>connessione **internet**

#### Plurale dei vocaboli stranieri
I vocaboli stranieri sono da considerare *invariabili*, ovvero compaiono sempre nella stessa forma indipendentemente che siano al singolare o al plurale. L’articolo (singolare o plurale) sarà sufficiente a indicare il numero del vocabolo.

Es.
> “I CD” e non “i CD**s**”
<br>“I file” e non “I file**s**”
<br>“le password” e non “le pasword**s**”

I motivi di questa regola sono facilmente intuibili: se ogni parola di ogni lingua straniera che entra nella lingua italiana si trascinasse dietro le  proprie regole grammaticali, sarebbe il caos più totale. Si pensi per esempio a lingue come il tedesco, dove una parola non ha solo la forma singolare o plurale, ma va anche declinata a seconda del suo ruolo all’interno della frase.

#### Genere dei vocaboli stranieri
Per l’invariabilità dei vocaboli vale quanto detto per il plurale.
Tuttavia quando un vocabolo straniero entra nella lingua italiana, occorre assegnargli un genere, maschile o femminile.

Di solito è l’uso comune a determinare il genere di un vocabolo straniero. Questa assegnazione avviene secondo un rapporto di tipo associativo con il più vicino corrispondente italiano.

es.
>“la posta / la lettera” diventa “l(a)’email”
<br>“la parola chiave” diventa “la password”

Tuttavia esistono anche note eccezioni, come:
>“la Rete” diventa “il Web”

Per giunta possono esserci diverse interpretazioni a seconda del corrispondente italiano che ciascun individuo ha in mente.
es.
>“canvas” può essere inteso per alcuni al maschile come “canovaccio” e per altri al femminile come “tela”.

>“CPU”, può essere inteso al maschile come “processore centrale” eppure contenendo il termine “unità” può essere anche inteso al femminile come “la CPU”.

Un metodo per ovviare a questa intrinseca soggettività è seguire la convenzione di *considerare di genere maschile tutte le nuove parole straniere*. Naturalmente è un metodo che va temperato dalle eccezioni dell’uso, in quanto è impensabile pretendere di modificare usanze consolidate, per esempio iniziando a scrivere “lo email”.

Non esiste un metodo intrinsecamente più giusto dell’altro, ma è opportuno che ogni organizzazione stabilisca delle convenzioni allo scopo di mantenere la coerenza terminologica interna.

Una soluzione valida è indicare nel glossario dell’associazione, accanto al traducente, il genere da attribuire al termine.

es.
>EN: email > IT: email (f.)


### Libertà stilistiche e calchi linguistici
Ogni lingua possiede il suo modo peculiare di strutturare una frase, per cui nelle traduzioni tecniche non bisogna esitare a rigirare una frase quando questa azione la renderebbe più comprensibile o scorrevole.
Ecco alcune modifiche che possono evitare i calchi linguistici dall’inglese e rendere la traduzione italiana più chiara e scorrevole.

#### Lunghezza delle frasi
L’inglese è notoriamente una lingua che preferisce periodi semplici e collegati paratatticamente.
<br>L’italiano è, al contrario, una lingua famosa per il periodare lungo e complesso, in cui prevale la subordinazione.
<br>Ne consegue che a volte traducendo dall’inglese all’italiano, il periodo che risulta appare fin troppo “elementare”, spezzettato.

Per evitare questo effetto può essere utile unire due periodi brevi in uno più lungo, quando possibile evidenziandone il nesso logico con una proposizione subordinata. Questo darà al discorso un senso di continuità e renderà più facile seguirne il filo logico.

#### Lessico
##### Verbi e sostantivi
Altra caratteristica dell’inglese è la preferenza per un lessico generico, un buon esempio del quale sono i *phrasal verbs*, che uniscono a verbi comuni una preposizione per dargli un nuovo significato, anche quando per quello stesso significato esisterebbe un verbo più specifico.

Fare particolarmente attenzione ai seguenti termini:
>register / sign up
<br>access / sign in

In italiano questa scelta stilistica viene interpretata come povertà lessicale. Per questo è preferibile utilizzare i termini più puntuali possibili senza scadere ovviamente in un linguaggio ingessato o pedante.

es.
>accedi vs. entra
<br>invia vs. manda
<br>sviluppare/progettare (un software) vs. costruire, creare ecc.

È comunque sempre buona norma non abusare dei verbi generici come fare, esserci, dare e dei “sostantivi ombrello” come cosa, fatto ecc.

##### Aggettivi
Anche negli aggettivi ci sono abitudini diverse. In inglese si noterà un massiccio uso di “great”, “powerful”, “best”, “awesome” per descrivere qualsiasi tipo di prodotto, iniziativa o persona.

In italiano sono aggettivi molto generici e danno un'idea di povertà lessicale. Per un testo di buona qualità troviamo meglio sostituire questo generico “potente” con una caratteristica più precisa che specifichi la qualità in cui una cosa è “potente”.

Per esempio un programma “potente” potrebbe essere, a seconda del singolo caso, performante, o versatile, o completo, oppure stabile, o ancora flessibile ecc.

##### False friend
In ultimo bisogna evitare le trappole dei *false friend* (parole straniere che somigliano a termini esistenti italiani, ma hanno un significato diverso). Alcuni dei principali sono:
- submit:
non sottomettere (assoggettare qualcuno al proprio volere), ma sottoporre (ad esame).<br> A seconda dei casi, per esempio in presenza di un modulo per inoltrare file, si possono utilizzare anche inviare o caricare.
es.
>EN: Submit your add-on for review.
<br>IT: Carica il componente aggiuntivo per il processo di revisione.

- application:
attenzione al contesto! Il software è un’“applicazione”, quando si fa domanda per partecipare a un progetto si dice candidatura, proposta o simili.

es.
>EN: Submit your application at the following email address
<br>IT: Invia la candidatura al seguente indirizzo email.

- excited: non “eccitato”, termine dalle connotazioni sessuali o comunque esagerate, ma “entusiasta” (es. siamo entusiasti della nuova versione), o a seconda dei casi “impaziente” (sono impaziente che esca la nuova versione), “orgoglioso” (siamo orgogliosi di presentare la nuova versione) ecc.

es.
>EN: We are all excited for the upcoming release of Firefox.
<br>IT: Attendiamo tutti con impazienza il prossimo aggiornamento di Firefox.

#### Diatesi
Certi usi inglesi del passivo risultano in una traduzione italiana inutilmente macchinosa, specialmente quando si stanno scrivendo istruzioni complesse.
<br>In questi casi è preferibile capovolgere la diatesi trasformando la forma passiva in attiva per maggiore chiarezza.

es.
>Le impostazioni possono essere modificate in un secondo momento.

diventa

>È possibile modificare le impostazioni in un secondo momento.

#### Tema della frase
Un altro accorgimento che facilita il lettore è cercare di mettere l’informazione più importante (o tema) all’inizio della frase.

Specialmente quando il testo descrive una procedura lunga e complessa, l’utente deve essere messo in condizioni di determinare subito quale sia l’argomento trattato.

Da evitare, per esempio, una spiegazione di tre righe con in fondo “per eliminare il tuo account”. Per risultati ottimali è meglio seguire la formula:

*Effetto* > *procedura*,

piuttosto che

 *Procedura* > *effetto*.

 es.
>Accedi a Menu > Componenti aggiuntivi > Aspetto per attivare un nuovo tema.

diventa

>Per attivare un nuovo tema accedi a Menu > Componenti aggiuntivi > Aspetto.

### Quando tradurre e quando no
#### Nomi comuni
In presenza di un traducente accettabile, Mozilla Italia preferisce sempre fare uso dei termini italiani e promuoverli in rete sfruttando la sua posizione rilevante per abituare l’utente a un linguaggio più consapevole del significato dei termini e non impoverito dall’uso di anglicismi.

Per verificare se è come tradurre un termine, è buona norma attenersi al traducente dato nel glossario ufficiale dell’organizzazione per cui si traduce (nel caso di Mozilla Italia, [Transvision](https://transvision.mozfr.org/)).

Alcuni esempi di scelte terminologiche di Mozilla Italia:
> community > comunità
> <br>network > rete di contatti
> <br>report > resoconto ecc.

Anche i neologismi usati colloquialmente sono da evitare il più possibile nella lingua scritta.

Es.
> cliccare > fare clic (senza k)
<br>postare > pubblicare un articolo / un post
<br>editare > modificare
<br>loggarsi > accedere


#### Nomi propri
Caso a parte sono i nomi propri, di prodotti o eventi. Quando esiste un traducente italiano *ufficiale* di un prodotto, va usato quello, altrimenti si lascia la versione originale, senza inventarsi un nome italiano che potrebbe non essere riconosciuto dall’utente finale.

> es. il programma predefinito di visualizzazione Preview nel Mac nel locale italiano è Anteprima.
<br> Invece il programma di elaborazione video iMovie rimane iMovie anche in Italiano.

**N.B.** I nomi di associazioni o prodotti coperti da *trademark* vanno riportati esattamente come scritti nella grafia ufficiale.

es.
>JavaScript e non Javascript o Java Script
<br>PayPal e non Paypal o Pay Pal
<br>iPhone e non iphone o i-Phone

In caso di prodotti o eventi Mozilla, dato che l’associazione ha voce in capitolo sulla decisione, si valuterà insieme di caso in caso se mantenere l’originale o localizzarlo.

#### Casi particolari
I nomi di cariche all’interno di un’organizzazione sono spesso titoli molto specifici e creati ad hoc, di cui non esiste esatto corrispondente in italiano.

In questi casi improvvisare una traduzione arbitraria corre il rischio di causare malintesi sull’effettivo organigramma di un’organizzazione.
Pertanto è consigliabile gestirli alla stregua dei nomi propri e mantenerli in inglese.

Esempi da lasciare invariati:
>Mitchell Baker, Executive Chairwoman
<br>Chris Beard, Chief Executive Officer
<br>Mark Surman, President and Executive Director

Può essere utile, per motivi di diffusione internazionale, mantenere in lingua inglese la documentazione per sviluppatori contenente nomi di tecnologie nuove o sconosciute per cui non si è ancora affermato un traducente in lingua italiana.

Va considerato che tale documentazione è ad uso e consumo degli sviluppatori, che si muovono in un ambito internazionale e pertanto trovano di maggiore utilità conoscere il termine inglese.
