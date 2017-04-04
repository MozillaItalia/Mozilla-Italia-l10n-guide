La maggioranza dei progetti Mozilla è traducibile attraverso lo strumento di traduzione online di Mozilla, [Pontoon](https://pontoon.mozilla.org/).\
Pontoon estrapola tutto il contenuto traducibile di un sito web e lo divide in piccole unità, chiamate "stringhe", permettendoci di inserire la traduzione corrispondente a ciascuna stringa, poi ricaricano la nostra traduzione sul sito web.\
Questa interfaccia di permette a chiunque di tradurre in modo intuitivo, mentre tradurre direttamente il codice sorgente del sito web richiederebbe una buona esperienza con il codice html che non tutti possiedono.\
Chi desidera tradurre un progetto deve dunque registrarsi gratuitamente a Pontoon, utilizzando un account Firefox (se non se ne possiedi già uno, si può crearlo direttamente da Pontoon).\
\
In quanto siamo un'organizzazione con un'identità ben definita, tutti i nostri prodotti devono conformarsi a certi standard, terminologici e linguistici. Per questo motivo tutte le traduzioni devono passare attraverso un processo di revisione (aka QA) da parte dei localizzatori senior. Questo vuol dire che le traduzioni dei volontari verranno inserite come provvisorie e in seguito approvate se sono accettabili, oppure verrà chiesto ai volontari stessi di correggerle per uniformarle ai nostri standard.

\
Il lavoro di localizzazione non si esaurisce nello scrivere la traduzione a fronte di una stringa e poi andarsene.\
Prima c'è tutto un lavoro di ricerca della terminologia non solo corretta, ma anche coerente con lo stile Mozilla e con i prodotti localizzati in precedenza.\
Dopo, invece, c'è tutto il processo di QA, che prende quasi più tempo della traduzione stessa. In questa fase i localizzatori più anziani proporranno modifiche e correzioni spiegandone la motivazione. Il volontario dovrà dunque tornare sulle proprie traduzioni e apportare le correzioni, oppure proporre una nuova versione tenendo conto dei problemi che gli sono stati fatti notare.\
Infine occorre tener conto che un progetto non è mai tradotto una volta per tutte: vengono sempre aggiunte nuove stringhe mano a mano che il sito viene aggiornato. Per questo unirsi al team di localizzazione significa non solo tradurre le stringhe presenti ma prendersi l'impegno di seguire il progetto a lungo termine, controllando regolarmente gli aggiornamenti.\
\
Anche se il programma è molto intuitivo, esiste una guida di Pontoon (in inglese):\
https://developer.mozilla.org/it/docs/Mozilla/Localization/Localizing_with_Pontoon
\
Di seguito le informazioni necessarie per sfruttare appieno le potenzialità di Pontoon nella traduzione collaborativa.\
\
**Tracciabilità** è possibile inserire una traduzione solo se si è registrato un account, questo vuol dire che è possibile tracciare con precisione chi ha tradotto cosa, dove e quando, soprattutto si può lavorare in più persone allo stesso progetto aggiornato in tempo reale.\
\
**Opzione filtro** (l'icona ad imbuto in alto a sinistra) permette di estrapolare le stringhe d’interesse. I filtri sono:

Missing (non ancora tradotte)

Fuzzy (sono state tradotte automaticamente usando la memoria informatica, ma hanno bisogno di revisione umana)

Suggested (proposta di traduzione in attesa di revisione)

Translated (stringhe tradotte, approvate e pronte per essere pubblicate)

\

**Altre opzioni**

Sotto la stringa si trovano i 3 tab History (tutte le traduzioni che sono state date per quella stringa finora), Machinery (traduzioni automatiche), Locales (come la stringa è stata tradotta in altre lingue).\
\
- *Machinery* è una funzione molto preziosa, ma mai da prendere per oro colato. Bisogna sempre guardare la fonte delle soluzioni che propone, in grigio sopra la traduzione.\
\
--Il tag "Machine translation" : traduzioni automatiche di Bing, il più delle volte non sono degne di considerazione;\
--Il tag "Translation Memory" : traduzioni UMANE prese dal database di Mozilla. Ovviamente se ha senso nel contesto, è bene attenersi il più possibile a quella traduzione per coerenza terminologica (es. se vedi che Privacy Policy è stato tradotto Informativa sulla Privacy, non mettere Legge sulla Privacy o simile);\
N.B. *La percentuale accanto al tag esprime il grado di corrispondenza, per esempio 100% è una stringa identica, 80% magari cambia una preposizione, un plurale ecc. e quindi va adeguata di conseguenza.*\
\
Machinery può anche essere usata come glossario o dizionario usando la barra di ricerca in alto. Basta digitare la parola interessata e appariranno varie traduzioni prese da fonti diverse:\
--Tag "Mozilla" è preso dal database di Mozilla (https://transvision.mozfr.org/), quindi è quella da privilegiare se è disponibile;\
--Tag "Microsoft" è presa dal glossario ufficiale della Microsoft ([https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT](https://www.microsoft.com/Language/en-US/Search.aspx?sString=%25s&langID=it-IT)) N.B. Questo glossario sarà molto utile anche fuori da Mozilla per chi traduce professionalmente nel campo dell'informatica;\
--Tag "Translation Memory" è estrapolata dal database di Pontoon;\
--Tag "Open Source" è presa da un glossario comunemente condiviso nel mondo dell'Open Source (Linux ecc.)\
\
\
**Workflow di traduzione e revisione usando il filtro**\
Poniamo di avere un progetto molto voluminoso con metà stringhe già tradotte e metà ancora no.

\
**Fase 1 Traduzione**\
Traduttore:\
- Esegue l'accesso\
- Va nelle sue impostazioni (icona ingranaggio sotto l'icona in alto a destra) e seleziona la modalità "Make suggestion"\
- Va al progetto\
- Dal filtro seleziona "Missing", così da poter accedere direttamente alle stringhe senza traduzione\
- Traduce e conferma con il pulsante blu "Suggest". La stringa apparirà ora sotto il tag History, con il nome del traduttore e l'ora di immissione.\
\

**Fase 2 Revisione**\
Revisore:\
- Esegue l'accesso\
- Va al progetto\
- Dal filtro seleziona "Suggested", così da ritrovarsi le stringhe che il traduttore gli ha lasciato da revisionare\
- Se la traduzione è buona, preme il pulsante "Save", confermando la stringa come "Translated". Se ha in mente una soluzione alternativa invece, scrive la sua versione e preme il pulsante Suggest. La sua versione finisce in cima alla lista, sopra quella del traduttore, nel tab History.\
\

**Fase 3 Correzione**\
Traduttore:\
- Nel progetto seleziona dal filtro "Suggested" e confronta tutti i cambiamenti fatti dal revisore con la sua versione.\
- Dà l'OK alla correzione del revisore oppure propone un'altra versione in suggerimento (che apparirà sempre in cima alle altre nel tab History) finché non si trova un comune accordo tra i due.\
\
Questo è un sistema che abbiamo collaudato nel tempo per lavorare in tandem impiegando meno tempo e riducendo il rischio di lasciare qualcosa non tradotto.\
\
Un ultimo scontato quanto prezioso consiglio: la differenza tra una traduzione mediocre e una eccellente sta spesso nel contesto. Quindi ogni volta che si trova una frase di cui non si riesce bene ad afferrare il senso, una ambigua che magari abbia più traduzioni possibili, la cosa migliore da fare è cercarla sulla pagina del sito e vederla nel suo contesto originale per dare la traduzione più appropriata.
