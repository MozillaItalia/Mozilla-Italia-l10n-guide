# Buone norme di traduzione tecnica

Questo capitolo raccoglie le cosiddette “buone norme”, ovvero un insieme di regole condivise (non solo da Mozilla Italia, ma in tutto il panorama italiano) che contraddistinguono una traduzione tecnica di buona qualità.

Si tratta di un capitolo corposo e dettagliato, in continua espansione. È concepito per essere tenuto a portata di mano durante la traduzione e consultato all’occasione mediante l’Indice dei contenuti o la funzione di ricerca (`Ctrl`+`f`).

N.B. Le scorciatoie da tastiera fanno riferimento al layout della tastiera *italiana*. Layout di tastiera diversi hanno combinazioni diverse. I sistemi operativi Windows, in aggiunta alla combinazione universale `Alt + ####`, hanno scorciatoie da tastiera peculiari per ogni versione di sistema operativo. Vedere nel dettaglio le istruzioni del proprio sistema operativo.

**Indice dei contenuti**
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Buone norme di traduzione tecnica](#buone-norme-di-traduzione-tecnica)
	- [Standard qualitativi](#standard-qualitativi)
	- [Localizzazione](#localizzazione)
		- [Formato delle date](#formato-delle-date)
		- [Formato delle cifre](#formato-delle-cifre)
			- [Billon, trillion ecc.](#billon-trillion-ecc)
	- [Ortografia](#ortografia)
		- [Punteggiatura](#punteggiatura)
			- [Virgola](#virgola)
			- [Punto](#punto)
			- [Punto esclamativo](#punto-esclamativo)
			- [Apostrofo](#apostrofo)
			- [Virgolette](#virgolette)
			- [Ellissi](#ellissi)
			- [Trattini](#trattini)
			- [Formattazione elenchi](#formattazione-elenchi)
				- [Stile testo](#stile-testo)
				- [Stile elenco](#stile-elenco)
		- [Maiuscole e minuscole](#maiuscole-e-minuscole)
		- [Vocaboli stranieri](#vocaboli-stranieri)
			- [Plurale dei vocaboli stranieri](#plurale-dei-vocaboli-stranieri)
			- [Genere dei vocaboli stranieri](#genere-dei-vocaboli-stranieri)
		- [Nomi propri](#nomi-propri)
			- [Marchi registrati](#marchi-registrati)
			- [Titoli di opere](#titoli-di-opere)
	- [Libertà stilistiche e calchi linguistici](#libert-stilistiche-e-calchi-linguistici)
		- [Lessico](#lessico)
			- [Verbi e sostantivi](#verbi-e-sostantivi)
			- [Aggettivi](#aggettivi)
			- [Falsi amici](#falsi-amici)
		- [Lunghezza delle frasi](#lunghezza-delle-frasi)
		- [Diatesi](#diatesi)
		- [Tema della frase](#tema-della-frase)

<!-- /TOC -->
## Standard qualitativi
Per essere definita di qualità adeguata, una traduzione tecnica deve corrispondere ai seguenti requisiti:

1. **Completezza**  
 Il testo originale deve essere tradotto integralmente, senza omissioni (escludendo, naturalmente, le informazioni irrilevanti nella localizzazione) o brani di testo lasciati nella lingua di partenza (a meno che non siano volute, es. citazioni *verbatim*).

 Non solo il testo iniziale deve risultare tradotto al 100%, *anche gli eventuali aggiornamenti devono essere tradotti e integrati* per presentare ai lettori una versione aggiornata e completa nella loro lingua.

2. **Univocità**  
 L’utente non deve nutrire alcun dubbio sul significato di un termine. Se un termine lascia spazio a interpretazioni diverse, deve essere sostituito con uno univoco.

 I traducenti scelti devono essere conformi all’uso comune nella lingua d’arrivo.

 Nel caso di gergo tecnico, è necessario svolgere un’accurata ricerca terminologica su fonti ufficiali o autorevoli, invece bisogna evitare di rimpiazzare i termini tecnici con equivalenti approssimativi o troppo  generici.

 Le convenzioni di formattazione che danno adito ad ambiguità vanno convertite secondo gli usi della lingua d’arrivo (vedi [Localizzazione](#localizzazione) per i dettagli).

3. **Usabilità**  
 Con *usabilità* si intende l’efficacia nell’adempiere a una determinata funzione. La funzione della localizzazione è mettere gli utenti della lingua d’arrivo nella condizione di usufruire dei contenuti tradotti nel modo più semplice e immediato possibile.

 Questo include utilizzare grammatica, ortografia e punteggiatura correttamente, scegliere un linguaggio chiaro e diretto e convertire appropriatamente la formattazione di informazioni rilevanti, come date, misure, ora locale, valuta ecc.

4. **Consistenza**  
 L’inconsistenza terminologica può generare confusione nell’utente e compromettere l’usabilità. Nomi di prodotti, titoli, voci di menu, comandi ecc. all’interno del medesimo progetto di traduzione, oltre che attraverso tutti i progetti correlati, vanno tradotti in maniera consistente.

 I nomi di componenti, pulsanti, voci di menu ecc. che appaiono nelle istruzioni devono corrispondere esattamente a ciò che l’utente troverà nel prodotto reale.

 I traducenti adottati in precedenza devono essere mantenuti, a meno che non contengano errori o siano diventati inadatti per altre ragioni. Quando si sceglie di modificare un traducente, occorre sostituire anche tutte le sue occorrenze nelle traduzioni precedenti.

 Nel caso venga fornito un glossario ufficiale, è buona norma attenersi a esso, salvo i casi in cui andrebbe contro il buon senso.

## Localizzazione
La localizzazione prevede un passaggio in più della semplice traduzione: invece di limitarsi a trasporre un contenuto così com’è in una lingua diversa, lo adatta agli usi e alle convenzioni di uno specifico Paese o regione.

L’insieme di tutti i parametri in uso in una data regione è comunemente noto come *locale*. Ogni lingua è identificata da un [codice ISO][ISO], a cui può aggiungersi un suffisso che indica la variante locale. La sigla per l’inglese è **en**. La variante per l'inglese americano è **en-US**. La sigla per l’italiano è invece **it**.

### Formato delle date
In tutte le lingue, una data può contenere i seguenti elementi: anno (Y, *year*), mese (M, *month*) e giorno (D, *day*). Tuttavia, in regioni diverse del globo, questi elementi cambiano ordine.

Il formato più comune è D/M/Y (giorno, mese, anno) chiamato _little-endian_, ma in estremo Oriente prevale Y/M/D (_big-endian_), mentre negli Stati Uniti viene adottato M/D/Y (_middle-endian_). Ed ancora, nell’informatica la data usata è Y-M-A per comodità (l’ordinamento per data è più preciso).

Nel migliore dei casi, usare un formato diverso da quello della regione di destinazione può apparire come una trascuratezza stilistica, ma in alcuni casi, specialmente quando si esprime la data in cifre, può dare adito a gravi fraintendimenti.  
Per esempio la data *05/07* indica il *7 maggio* in America, ma in italiano verrà interpretata dall’utente come *5 luglio*.

### Formato delle cifre
Anche per la formattazione delle cifre, ogni regione ha le proprie convenzioni che, trascurate, possono portare a gravi fraintendimenti.

Una differenza importante è il marcatore dei decimali.  
Tra i Paesi che utilizzano i numeri arabi, alcuni (es. Stati Uniti, Regno Unito) utilizzano il punto `.` per separare i decimali e la virgola `,` per raggruppare le migliaia.

In altre regioni del globo, Europa inclusa, è l’esatto contrario: la virgola contrassegna i decimali, il punto le migliaia.

**N.B.** Gli standard ISO vigenti raccomandano l’utilizzo di uno spazio bianco per raggruppare le migliaia e virgola o punto esclusivamente per indicare i decimali.

| Regione | Decimali | Migliaia|
|---|---|---|
| USA, UK ecc. | 15.241 | 15,241|
| UE ecc. | 15,241 | 15.241 |
| Standard ISO | 15.241 / 15,241 | 15 241|

#### Billion, trillion ecc.
Un’altra discrepanza, stavolta nelle cifre dell’ordine dei bilioni, trilioni, quadrilioni ecc. è data dai diversi metodi di denominazione numerica usati nel mondo:
- *scala lunga*: ogni termine è 1 000 000 volte più grande del precedente, usata in Europa continentale e paesi di lingua affine;
- *scala corta*: ogni termine è 1000 volte più grande del precedente, usata nei paesi anglofoni e arabi.

Ne si deduce che, quando in un testo in lingua inglese si parla di bilione, si intende un miliardo italiano, e così via. È importante dunque scalare appropriatamente le grandezze per evitare errori dell’ordine di miliardi.

Ecco una tabella delle corrispondenze per i termini più comuni.

| Numero | Scala corta (EN) | Scala lunga (IT)|
|---|---|---|
|1 000 000 000|billion|miliardo|
|1 000 000 000 000|trillion|bilione|
|1 000 000 000 000 000|quadrillion|biliardo (mille bilioni)|
|1 000 000 000 000 000 000|quintillion|trilione|

Approfondimenti e tabella completa: [scala lunga e scala corta][scale].

## Ortografia

### Punteggiatura

#### Virgola

Durante una traduzione è importante essere consapevoli delle sottili differenze nell’uso della punteggiatura tra una lingua e l’altra. Questo è il caso della virgola.

In inglese la virgola viene utilizzata anche prima delle congiunzioni.

>EN: For safety, privacy**, and** freedom on the Web

In italiano, al contrario, la congiunzione solitamente esclude la virgola e viceversa, in quanto, svolgendo lo stesso ruolo coordinativo, sono ridondanti.

>IT: Per la sicurezza, la privacy **e** la libertà sul Web

Eccezione va fatta naturalmente per il discorso degli incisi.

>Se Marco si lascerà scappare il nostro segreto**, e sono sicuro che prima o poi lo farà,** finiremo tutti nei guai fino al collo.

#### Punto

Il punto va omesso alla fine dei titoli.  

>Sì: Guida di localizzazione di Mozilla Italia  
No: Guida di localizzazione di Mozilla Italia**.**

Le sequenze `.”.`, `.).` e simili sono considerate graficamente sgradevoli e pertanto da evitare.

Dunque, qualora si verificassero, si omette il punto all’interno delle virgolette o parentesi lasciando solo quello esterno.  

>Sì: Gli risposi “Ora puoi andare**”.**  
No: Gli risposi: “Ora puoi andare**.”.**

#### Punto esclamativo

Viene utilizzato spesso (a volte abusato) nello stile informatico anglofono, specialmente nei messaggi di sistema che notificano un errore.

Nello stile di localizzazione italiano, e a Mozilla Italia in particolare, è da dosare con parsimonia.

es.
>EN: Error 404: page not found**!**  
IT: Errore 404: pagina non trovata**.**

In ogni caso, sono *sempre* da evitare le stringhe continue di punti esclamativi o interrogativi.
>No: Collabora con noi!!!!!!!!!!!!!!

In casi eccezionali, per denotare una particolare enfasi sono consentiti *tre* punti esclamativi di seguito `!!!`.

#### Apostrofo
L’apostrofo “diritto” `'` , detto anche dattilografico, è quello più comunemente accessibile sulle tastiere.
Tuttavia, esso viene utilizzato anche in vari tipi di codice, per questo può generare conflitti nei documenti misti di testo e codice.

È dunque consigliabile utilizzare l’apostrofo curvo, detto anche tipografico `’`.

>Scorciatoie da tastiera per l’apostrofo curvo:  
**Windows** `Alt + 0146`  
**macOS** `Alt + Shift + 3`  
**Linux** `Alt Gr + Shift + V`

Errori più comuni per l’apostrofo:
>Sì: un altro  
No: un’altro

e simili casi di articolo indeterminativo + maschile.

> Sì: Qual è  
No: Qual’è

#### Accento
L’accento in italiano è "scritto" solitamente sulle lettere finali di parola. Degli esempi possono essere poiché, perché, affinché, ecc.
Si notino, infatti, che gli accenti inseriti su queste parole sono "acuti" e non "gravi".
Alcune parole, se ambigue possono presentare l’accento anche su altre vocali della parola.
In italiano, effettivamente, si hanno tre accenti differenti:
- grave: teoricamente dovrebbe trovarsi solamente sulle vocali aperte, quali à, è e ò
- acuto: dovrebbe trovarsi, in teoria, solamente sulle volali chiuse é, ó, í e ú (tuttavia la í e ú vengono in genere sostituite con la ì e la ù)
- circonflesso: anticamente veniva usato in determinate parole su tutte le vocali (a, e, i, o, u). Al giorno d’oggi, invece, è usato solo in determinate circostanze sulla i (î). L'esempio più ecclatante è, sicuramente, il plurale di _princìpio_, ovvero _princìpii_; in italiano si dovrebbe scrivere _principî_. In verità è sempre più rara questa forma, in favore della singola e "semplice" _i_ (princìpi).

#### Virgolette

Per la stessa ragione dell’apostrofo, preferiamo alle virgolette dritte, quelle curve.

**N.B.** Le virgolette dritte sono intercambiabili, ma quelle curve sono due distinte: una per l’apertura `“` orientata verso sinistra, e una di chiusura, orientata verso destra `”`.

>Scorciatoie da tastiera per le virgolette curve:  
**Windows** apertura `Alt + 0147`, chiusura `Alt + 0148`  
**macOS** apertura `Alt + 2`, chiusura `Alt + Shift + 2`  
**Linux** apertura `Alt Gr + V`, chiusura `Alt Gr + B`

#### Ellissi

Per digitare i puntini di sospensione, chiamati anche ellissi, molti premono semplicemente il tasto `.` tre volte in successione. In realtà il simbolo dell’ellissi ha la sua combinazione di tasti dedicata.

>Scorciatoie da tastiera per ellissi:  
**Windows** `Alt + 0133`  
**macOS**  `Alt + ,`  
**Linux** Unicode `CTRL + SHIFT + U 2026 SPACE`, oppure con COMPOSE `Comp ..`

Questo accorgimento diventa particolarmente utile in caso di limitazione dei caratteri, per esempio nei *tweet* di Twitter: infatti `…` viene conteggiato come un solo carattere.

#### Trattini

Occorre fare una distinzione tra il trattino corto `-` e il trattino lungo `–`.

Il trattino corto va utilizzato esclusivamente come *trait d’union* in un composto formato da due parole, senza spazi in mezzo.

**N.B.** Alcuni vocaboli, che inizialmente erano composti da due parole distinte col trattino, sono tanto entrate nell’uso che possono venire scritte senza.
Esempi sono le seguenti parole:

>e-mail / email  
on-line / online  
multi-piattaforma / multipiattaforma

Il trattino lungo è usato per gli incisi, o comunque per separare due frasi, e va sempre preceduto e seguito da uno spazio.

>Scorciatoie da tastiera per il trattino lungo:  
**Windows** `Alt + 0151`  
**macOS** `Alt + -`  
**Linux** Unicode `CTRL + SHIFT + U 2014 SPACE`, oppure con COMPOSE `Comp ---`

Il trattino lungo viene molto usato in inglese, ma non è altrettanto diffuso in italiano. Quando possibile è meglio sostituirlo con un altro segno di punteggiatura appropriato al caso.

>EN: Firefox **–** The browser that puts privacy at the first place  
IT: Firefox**:** il browser che mette la privacy al primo posto.

oppure

>EN: Firefox **–** the browser that puts privacy at the first place **–** is now available for Android.  
IT: Firefox**,** il browser che mette la privacy al primo posto**,** è ora disponibile per Android.

#### Formattazione elenchi
*Il Nuovo Manuale di Stile* di Lesina elenca due convenzioni. Si può scegliere quella più adatta al contenuto, l’essenziale è mantenere uno stile uniforme all’interno dello stesso elenco.

##### Stile testo
L’elenco prosegue naturalmente il testo corrente, rispettandone la punteggiatura. In particolare:

- l’iniziale è minuscola se la voce prosegue il periodo della frase introduttiva;
- ogni voce termina con il segno di punteggiatura appropriato per la struttura della frase, di solito `,` per le voci singole o brevi, `;` per periodi lunghi o paragrafi;
- l’ultima voce si chiude con il punto.

es.
>Elenchiamo le seguenti voci:
- voce 1,
- voce 2,
- voce 3.

Oppure

>Elenchiamo i seguenti paragrafi:
- paragrafo 1;
- paragrafo 2;
- paragrafo 3.

##### Stile elenco
La lista è un elemento a se stante.

- Tutte le voci hanno iniziale maiuscola.
- Le voci brevi (di una o poche parole, come un elenco di nomi) terminano senza alcun segno di interpunzione, le voci più lunghe (frasi complete, interi paragrafi) terminano tutte con il punto.

es.
>- Voce 1
- Voce 2
- Voce 3

Oppure
>- Paragrafo 1.
- Paragrafo 2.
- Paragrafo 3.

### “d” eufonica

La *d* detta eufonica, che si aggiunge dopo preposizioni (es. *ad*) o congiunzioni (*ed*, *od*) per evitare lo scontro di vocali, sta cadendo in disuso.

È consigliabile  utilizzare *ad* o *ed* unicamente nel caso in cui la parola successiva inizi con la stessa vocale, ovvero “ad a…”, “ed e…”.

es.
>Sì: La conferenza si terrà **ad** Alba.  
>No: La conferenza si terrà **ad** Empoli.  
>Sì: La conferenza si terrà **a** Empoli.

>Sì: Per registrarsi occorrono nome **ed** email.  
>No: Per registrarsi occorrono nome **ed** account Firefox.  
>Sì: Per registrarsi occorrono nome **e** account Firefox.

Invece è buona norma *non* utilizzare mai *od*, ormai desueto.

es.
>Sì: In caso l’argomento risulti difficile **o** ostico.  
>No: In caso l’argomento risulti difficile **od** ostico.

### Maiuscole e minuscole

Le regole della maiuscola sono diverse in italiano e in inglese. In italiano vanno comunemente scritte con la maiuscola:
- nomi propri
- la prima lettera della prima parola di un periodo
- la prima lettera della prima parola di un titolo es.
>EN: **H**ow to **C**ontribute in the **I**talian **C**ommunity  
IT: **C**ome collaborare nella comunità italiana

 **N.B.** I titoli *non* terminano mai con `.`
- acronimi es. HTML (**H**yper **T**ext **M**arkup **L**anguage); URL (**U**niform **R**esource **L**ocators)
- abbreviazioni es. Web (World Wide **Web**)
- la prima lettera del nome di un tasto della tastiera es. Invio, Alt
- la prima lettera della prima parola di una funzione o di un’opzione es. **S**alva nei preferiti; **S**posta nel cestino

Ecco alcune categorie di vocaboli scritti sempre con la maiuscola in inglese ma non in italiano:

| Vocaboli | Inglese | Italiano |
| --- | --- | --- |
|Nomi dei giorni della settimana|Monday, Tuesday, Wednesday ecc.|lunedì, martedì, mercoledì ecc.|
|Nomi dei mesi|January, February, March ecc.|gennaio, febbraio, marzo ecc.|
|Aggettivi di nazionalità| English, Italian, Chinese|italiano, inglese, cinese ecc.|

### Ecc./Ec./Etc.
In italiano, se si ha la necessità di interrompere, abbreviare un’enumerazione di cose, una citazione che non pare necessario o opportuno continuare si utilizza la parola eccetera. Essa può essere abbreviata con ecc., con ec. o, ancora, con etc.
La prima è senza ombra di dubbio la più gettonata. Si può utilizzare, tuttavia, anche la ec. (con una singola c) o la forma latina (**e non inglese** _etcetera_) etc..
**N.B.** ecc./ec./etc. hanno un singolo punto successivamente poiché si indica che la parola non è finita ma è un’abbreviazione; non hanno, quindi, i "tre puntini di sospensione".

Esempi:

>Sì: Una casa può essere grande, piccola, ecc.
No: Una casa può essere grande, piccola, ecc…

### Sì o Si
In italiano la locuzione affermativa "sì" necessita, **obbligatoriamente**, dell’accento (da non confondere con l’apostrofo).
Questo è dovuto al fatto che è la forma abbreviata di _ic est_ (dal latino "così è").

Esempi:

>Sì: Vieni al mare con me? Sì, certamente.
No: Vieni al mare con me? Si, certamente.

### Vocaboli stranieri

#### Plurale dei vocaboli stranieri

I vocaboli stranieri sono da considerare *invariabili*, ovvero compaiono sempre nella stessa forma indipendentemente che siano al singolare o al plurale. L’articolo (singolare o plurale) sarà sufficiente a indicare il numero del vocabolo.  

| No| Sì |
|---|---|
|i CD**s**|i CD|  
|i file**s**|i file|
|le pasword**s**|le password|
|le email**s**|le email|

I motivi di questa regola sono facilmente intuibili: se ogni parola di ogni lingua straniera che entra nella lingua italiana si trascinasse dietro le  proprie regole grammaticali, sarebbe il caos più totale. Si pensi per esempio a lingue come il tedesco, dove una parola non ha solo la forma singolare o plurale, ma va anche declinata a seconda della sua funzione all’interno della frase.

#### Genere dei vocaboli stranieri

Per il genere dei vocaboli vale lo stesso principio di invariabilità.
Tuttavia quando un vocabolo straniero entra nella lingua italiana, occorre assegnargli un articolo, maschile o femminile.

Di solito è l’uso comune a determinare il genere di un vocabolo straniero. Questa assegnazione avviene secondo un rapporto di tipo associativo con il più vicino corrispondente italiano.

>“la posta / la lettera” diventa “l(a)’email”  
“il topo” diventa “il mouse”

Tuttavia esistono anche note eccezioni, come:

>“la Rete” diventa “il Web”

Per giunta possono esserci diverse interpretazioni a seconda del corrispondente italiano che ciascun individuo ha in mente.

>“CPU” può essere inteso al maschile come “processore centrale” oppure, stando la U per *unità*, può essere anche inteso al femminile come “la CPU”.

Un metodo per ovviare a questa intrinseca soggettività è seguire la convenzione di *considerare di genere maschile tutte le nuove parole straniere*. Naturalmente è un metodo che va temperato dalle eccezioni dell’uso, in quanto è controproducente modificare usanze consolidate, per esempio iniziando a scrivere “lo email”.

Non esiste un metodo intrinsecamente più giusto dell’altro, ma è opportuno che ogni organizzazione stabilisca delle convenzioni allo scopo di mantenere la coerenza terminologica interna.

Una soluzione valida è indicare nel glossario dell’associazione, accanto al traducente, il genere da attribuire al termine.

Esempio di voce di glossario:
>EN: email > IT: email (f.)

### Nomi propri

I nomi propri di norma non vanno tradotti.

In caso il nome originale sia scritto in un alfabeto non latino, occorre rispettare la traslitterazione ufficiale (di solito reperibile sui siti aziendali). Se non esiste, procedere applicando le regole di traslitterazione più accreditate.

es.

>Sì: Samsung  
No: 삼성, Samseong, Samsŏng  
Sì: Huawei  
No: 华为, Huáwéi

Un’eccezione alla regola sono le figure storiche, i nomi di città o luoghi geografici famosi la cui traduzione si è già affermata nel linguaggio comune. (es. Alessandro Magno, Parigi, Valle dei re ecc.)

Le denominazioni ufficiali delle nazioni vanno riportate sempre aggiornate e con particolare accuratezza, onde evitare dibattiti politici. Per la loro traduzione è possibile fare riferimento a portali terminologici degli enti ufficiali. [Un esempio][NOCS].

#### Marchi registrati

I nomi di associazioni o prodotti coperti da marchio registrato (*trademark*) vanno riportati esattamente come scritti nella grafia ufficiale, riproducendo eventuali maiuscole, trattini o spazi tra le parole e caratteri speciali.  
es.

| Sì | No |
|----|----|
|JavaScript|Javascript; Java Script|
|PayPal|Paypal; Pay Pal|
|iPhone|iphone; i-Phone|
|macOS|Mac OS; Mac os|

Quando esiste un traducente italiano *ufficiale* di un prodotto, va usato quello, altrimenti si lascia la versione originale.

es.

| Originale | Trad. ufficiale|
|----|----|
|Notepad (Microsoft)|Blocco note|
|Preview (Apple)|Anteprima|
|Photos (Google)|Foto|

#### Titoli di opere

Secondo la stessa logica, libri, film, brani musicali e altre opere vanno citate con il titolo con cui sono state pubblicate in Italia quando possibile, altrimenti con il loro titolo in lingua originale.

>es. *Il giovane Holden*, non *The Catcher in the Ryer*

Se l’opera in questione è edita ma pressoché sconosciuta, oppure più riconoscibile dal titolo originale, si può inserire il titolo originale tra parentesi a fianco del titolo tradotto.

>es. *Il cacciatore di androidi* (*Do Androids Dream of Electric Sheep?*)

Allo stesso modo, se un’opera non è edita in Italia, ma il suo titolo trasmette un significato rilevante per il lettore (specialmente nel caso di studi di settore e articoli tecnico-scientifici) è buona norma accostare al titolo originale una nostra traduzione letterale tra parentesi o in nota.

>es. *Safety Tips for Your Online Life* (*Suggerimenti per la sicurezza della tua vita online*)

Per nessuna ragione si dovrebbe improvvisare una traduzione propria di un marchio o titolo senza citare l’originale, in quanto non permette al lettore di risalire alla fonte.


## Libertà stilistiche e calchi linguistici

Ogni lingua possiede il suo modo peculiare di strutturare una frase, per cui nelle traduzioni tecniche non bisogna esitare a rigirare una frase quando questa azione la renderebbe più comprensibile o scorrevole.
Ecco alcune modifiche che possono evitare i calchi linguistici dall’inglese e rendere la traduzione italiana più chiara e scorrevole.

### Lessico

#### Verbi e sostantivi

In inglese, anche se esistono vocaboli più specifici, si tende spesso a usare un lessico limitato, che assume significati diversi a seconda del contesto. Un esempio sono i *phrasal verbs*, che uniscono a verbi generici una preposizione o un avverbio per dargli un nuovo significato.

Un esempio che può generare confusione:
- sign **up** (registrare un account)
- sign **in** (accedere a un account già esistente)
- sign **out** (disconnettersi dopo aver effettuato l’accesso)

In italiano questa scelta stilistica viene interpretata come povertà lessicale. Per questo è preferibile utilizzare i termini più puntuali possibili senza scadere ovviamente in un linguaggio ingessato o pedante.
Alcuni esempi:

| No | Sì |
|---|---|
|entrare|accedere|
|uscire|disconnettersi|
|mandare|inviare|
|costruire, creare (un software)|sviluppare, progettare|

È comunque sempre buona norma non abusare dei verbi generici come *fare*, *esserci*, *dare* e dei “sostantivi ombrello” come *cosa*, *fatto* ecc.

#### Aggettivi

Anche negli aggettivi ci sono abitudini diverse. In inglese si noterà un massiccio impiego di “great”, “powerful”, “best”, “awesome” per descrivere qualsiasi tipo di prodotto, iniziativa o persona.

In italiano sono aggettivi molto generici e danno un’idea di povertà lessicale. Per un testo di buona qualità troviamo meglio sostituire questo generico “potente” con una caratteristica più precisa che specifichi la qualità in cui una cosa è “potente”.

Per esempio un programma “potente” potrebbe essere, a seconda del singolo caso, performante, o versatile, o completo, oppure stabile, o ancora flessibile ecc.

#### Falsi amici

In ultimo bisogna evitare le trappole dei falsi amici, parole straniere che somigliano a termini esistenti italiani, ma hanno un significato diverso.
Alcuni dei più ricorrenti nel linguaggio sono:
- **application**:
attenzione al contesto! Il software è un’*applicazione*, quando si fa domanda per partecipare a un progetto si dice *candidatura*, *proposta* o simili.

 >EN: Submit your application at the following email address  
IT: Invia la candidatura al seguente indirizzo email.
- **cancel**: non *cancella*, ovvero elimina definitivamente un file, piuttosto il contrario: *annulla* l’operazione in corso, lasciando tutto invariato.
 >EN: Do you really want to delete this file? Delete / Cancel  
 >IT: Eliminare il file? Elimina / Annulla
- **directory**: non *direttorio* ma *cartella*. È sinonimo di *folder*.
>EN: Place the index.htm file in the root directory.  
>IT: Posiziona il file index.html nella cartella principale.
- **excited**: non *eccitato*, termine che denota uno stato di agitazione e ha spesso connotazioni sessuali, piuttosto *entusiasta* (es. siamo entusiasti della nuova versione), o a seconda dei casi *impaziente* (sono impaziente che esca la nuova versione), *orgoglioso* (siamo orgogliosi di presentare la nuova versione) ecc.

 >EN: We are all excited for the upcoming release of Firefox.  
IT: Attendiamo tutti con impazienza il prossimo aggiornamento di Firefox.
- **malicious**: non *malizioso*, bensì *malevolo* o *dannoso*.
>EN: Malicious code detected.  
>IT: Rilevato codice dannoso.
- **(to) process**: non *processare*, bensì *elaborare*.
 >EN: Processing message failed.  
 >IT: Elaborazione del messaggio non riuscita.
- **submit**: non *sottomettere* (assoggettare qualcuno al proprio volere), ma *sottoporre* (a esame / giudizio ecc).  
 A seconda dei casi, per esempio in presenza di un modulo per inoltrare file, si possono utilizzare anche *inviare* o *caricare*.  
>EN: Submit your add-on for review.  
IT: Carica il componente aggiuntivo per il processo di revisione.
- **subject (line)**: può significare *soggetto*, tuttavia nelle email corrisponde al campo *Oggetto* del messaggio.
- **table**: oltre che *tavolo*, significa anche *tabella*.

### Lunghezza delle frasi

L’inglese è notoriamente una lingua che preferisce periodi semplici e collegati paratatticamente (coordinate).  
L’italiano è, al contrario, una lingua famosa per il periodare lungo e complesso, in cui prevale l’ipotassi (subordinate).  
Ne consegue che a volte, traducendo dall’inglese all’italiano, il periodo che risulta appare fin troppo “elementare”, spezzettato.

Per evitare questo effetto può essere utile unire due periodi brevi in uno più lungo, quando possibile evidenziandone il nesso logico con una proposizione subordinata. Questo darà al discorso un senso di continuità e renderà più facile seguirne il filo logico.

### Diatesi

Certi usi inglesi del passivo risultano in una traduzione italiana inutilmente macchinosa, specialmente quando si stanno scrivendo istruzioni complesse (molte guide di stile per la manualistica infatti scoraggiano fortemente l’uso del passivo). In questi casi è preferibile capovolgere la diatesi trasformando la forma passiva in attiva per maggiore chiarezza.  
es.
>No: Le impostazioni possono essere modificate in un secondo momento.  
>Sì: È possibile modificare le impostazioni in un secondo momento.

### Tema della frase

Un altro accorgimento che facilita il lettore è inserire l’informazione più importante (o tema) all’inizio della frase.

Specialmente quando il testo descrive una procedura lunga e complessa, l’utente deve essere messo in condizioni di determinare subito quale sia l’argomento trattato.

Da evitare, per esempio, una spiegazione di tre righe con in fondo “per eliminare il tuo account”. Per risultati ottimali è meglio seguire la formula:

*Effetto* > *procedura* piuttosto che *Procedura* > *effetto*.

 es.
>No: Accedi a Menu > Componenti aggiuntivi > Aspetto per attivare un nuovo tema.

>Sì: Per attivare un nuovo tema accedi a Menu > Componenti aggiuntivi > Aspetto.

[ISO]:https://www.w3schools.com/tags/ref_language_codes.asp
[scale]:https://it.wikipedia.org/wiki/Scala_lunga_e_scala_corta
[NOCS]:http://termportal.fao.org/faonocs/appl/
