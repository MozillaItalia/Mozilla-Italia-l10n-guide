# Capitolo 5 - Risorse esterne

Altri strumenti che possono tornare molto utili per tradurre file sono un software di traduzione, un glossario, dizionari e strumenti per memorizzare la propria fraseologia in modo da non ripetere lo stesso lavoro più volte. Nella prima sezione di questo capitolo vedremo i tre glossari principali a cui fare riferimento per la traduzione dei termini tecnici e delle voci dell’interfaccia dei vari prodotti Mozilla e spiegheremo dove trovare le memorie di traduzione da utilizzare in Poedit e OmegaT. Nella seconda parte daremo alcuni consigli su traduttori automatici, dizionari online e altre risorse utili nel processo di localizzazione. Nell’ultima parte daremo uno sguardo più da vicino agli strumenti online di casa Mozilla che consentono di rimanere aggiornati sullo stato della localizzazione dei vari prodotti. Nell’appendice finale sono descritti alcuni concetti correlati nel caso il lettore ne fosse digiuno.

## indice dei contenuti

* [Glossari e memorie](5-risorse_esterne.md#glossari-e-memorie)
  * [Glossari](5-risorse_esterne.md#glossari)
  * [Le memorie di traduzione dei prodotti Mozilla](5-risorse_esterne.md#le-memorie-di-traduzione-dei-prodotti-mozilla)
* [Traduttori automatici, dizionari e altri strumenti](5-risorse_esterne.md#traduttori-automatici-dizionari-e-altri-strumenti)
  * [Traduzione automatica \(MT\)](5-risorse_esterne.md#traduzione-automatica-mt)
  * [Dizionari bilingui inglese-italiano](5-risorse_esterne.md#dizionari-bilingui-inglese-italiano)
  * [Corpora](5-risorse_esterne.md#corpora)
  * [Dizionari monolingui di italiano, sinonimi e contrari](5-risorse_esterne.md#dizionari-monolingui-di-italiano-sinonimi-e-contrari)
  * [Coniugazione verbi](5-risorse_esterne.md#coniugazione-verbi)
  * [Dizionari monolingui di inglese](5-risorse_esterne.md#dizionari-monolingui-di-inglese)
  * [Dizionario per il correttore ortografico](5-risorse_esterne.md#dizionario-per-il-correttore-ortografico)
* [Come rimanere aggiornati](5-risorse_esterne.md#come-rimanere-aggiornati)
  * [Mozilla L10n Web Dashboard](5-risorse_esterne.md#mozilla-l10n-web-dashboard)
  * [Il forum italiano](5-risorse_esterne.md#il-forum-italiano)
  * [Etherpad](5-risorse_esterne.md#etherpad)    +   [Account Firefox](5-risorse_esterne.md#account-firefox)
  * [Bugzilla](5-risorse_esterne.md#bugzilla)
  * [Mozillians](5-risorse_esterne.md#mozillians)
  * [Blog L10n](5-risorse_esterne.md#blog-l10n)
* [Appendice](5-risorse_esterne.md#appendice)
  * [Ricerche rapide in Firefox](5-risorse_esterne.md#ricerche-rapide-in-firefox)
  * [Caratteri](5-risorse_esterne.md#caratteri)

## Glossari e memorie

Un glossario è uno strumento fondamentale per un traduttore, esso permette di avere sotto mano un elenco di termini tecnici e la loro traduzione nell’ambito di riferimento. Questo è ancor più importante nel contesto informatico dove alcuni termini sono risemantizzazione di parole preesistenti che vanno ad assumere un significato completamente diverso da quello originale e in cui le scelte fatte inizialmente per rendere il concetto in altre lingue potrebbe discostarsi dalla mera traduzione letterale. È inoltre molto importante mantenere la terminologia utilizzata nei vari sistemi operativi, per rendere gli stessi concetti in modo che siano il più possibile comprensibili per l’utente.

Un ottimo glossario per i vari termini tecnici è il database terminologico Microsoft, nel quale è possibile trovare tutte le stringhe dei vari prodotti \(sistemi Windows, Microsoft Office, Visual C++, ecc\). Oltre alla localizzazione delle varie stringhe all’interno dei vari prodotti Microsoft, esso fornisce una definizione \(in lingua inglese\) di alcuni termini tecnici utilizzati.

Un analogo del glossario Microsoft per i prodotti Mozilla è disponibile sul sito della comunità francofona `transvision.mozfr.org`.

Il modo più facile per utilizzarli è aggiungerli come motori di ricerca o come _smart bookmark_, per vedere come fare consultare la sezione [Ricerche rapide in Firefox](5-risorse_esterne.md#ricerche-rapide-in-firefox).

Nel caso si scelga di utilizzare uno _smart bookmark_, aggiungere questi due URL ai propri segnalibri:

```text
https://transvision.mozfr.org/?recherche=%s&locale=it&repo=trunk
```

per cercare all’interno delle stringhe già tradotte dei software Mozilla e:

```text
https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT
```

per cercare all’interno delle stringhe dei prodotti di casa Microsoft.

Se invece si preferisce installarli come motori di ricerca [qui ci sono i relativi search plugin](http://www.gialloporpora.altervista.org/searchplugins/). Anche in questo caso è possibile \(anzi è consigliabile\) associare una parola chiave per una rapida consultazione dalla barra degli indirizzi, come spiegato nella sezione [Ricerche rapide in Firefox](5-risorse_esterne.md#ricerche-rapide-infirefox)

In aggiunta a questi due glossari di riferimento, è possibile consultare [questo](https://github.com/mozillaitalia/l10n-guide/tree/4dcec87d3f809cf8382c7adc3df085d7f902c017/resources/glossari/glossario.txt) piccolo file di testo che raccoglie i principali termini incontrati nella traduzione del sito `addons.mozilla.org` e altri siti correlati. Il file viene aggiornato non appena vengono incontrati nuovi termini e la versione aggiornata sarà sempre disponibile alla pagina appena indicata. Ogni riga del file è costituita da tre elementi separati tra di loro da un carattere di tabulazione. Il primo elemento è il termine inglese, il secondo il traducente più utilizzato \(nell’ambito delle localizzazioni riguardanti Mozilla\) e il terzo, se presente, contiene ulteriori spiegazioni del termine o traducenti alternativi. Se si vuole proporre un termine alternativo a quelli suggeriti o fare aggiunte, aprire una discussione sul forum o un [issue](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/issues) su GitHub.

### Le memorie di traduzione dei prodotti Mozilla

Per chi utilizzasse software desktop, come Poedit o OmegaT, che supportino le memorie di traduzione, qui di seguito ci sono i riferimenti a dove trovare delle memorie di traduzione create utilizzando le stringhe di Firefox e altri progetti Mozilla. Se si vuole utilizzare come memoria di traduzione con Poedit o OmegaT i file che comprendono l’insieme di vari progetti Mozilla, a [questo link](https://transvision.mozfr.org/downloads/) è possibile scaricare un file `.tmx` creato utilizzando tutte le traduzioni attive dei vari progetti. È sufficiente selezionare la lingua e i progetti a cui si è interessati e scaricare il file. Per conoscere come utilizzare le memorie di traduzione in Poedit e OmegaT fare riferimento al capitolo precedente.

A [quest’altro link](https://www.dropbox.com/sh/odlh109rugbovnr/OA8NTEkZ0b) sono inoltre disponibili i file `.tmx` del Progetto Firefox OS. Nonostante il progetto non sia più attivamente sviluppato, la traduzione italiana può essere utilizzata come riferimento perché si trattava comunque di un’ottimo lavoro. La memoria di traduzione di Firefox OS è denominata `gaia1.2.tmx`, gli altri file non sono aggiornati e si consiglia di scaricare l’ultima versione disponibile dal sito `transvision.mozfr.org`.

## Traduttori automatici, dizionari e altri strumenti

### Traduzione automatica \(MT\)

La traduzione automatica, o MT \(Machine Translation\) è utile per cercare frasi o termini già tradotti in precedenza \(ad esempio una formula comune o singole parole\). Bisogna comunque tenere presente che l’intelligenza artificiale non è in grado di riconoscere aspetti importanti quali il contesto e la coerenza logica. Per questo una traduzione automatica va sempre revisionata da un traduttore umano che la confronti con il testo sorgente. In più è da tenere presente che più il testo da tradurre sarà breve e comune, più i risultati saranno accurati, più il testo sarà lungo e l’argomento originale, più i risultati saranno scarsi. Per questa ragione la traduzione automatica darà risultati migliori cercando composti brevi e piccole porzioni di frase, invece di incollare l’intero testo da tradurre.

Se ci si affida a questo tipo di strumenti, il consiglio è quello di registrare un account e accedervi sempre con quel profilo perché sarà possibile memorizzare le traduzioni effettuate in precedenza e il software tenderà ad imparare e ad adeguarsi al contesto delle traduzioni effettuate.

I migliori strumenti online per la traduzione automatica sono [Google Translate](https://translate.google.com/) e [Microsoft Translator](http://www.bing.com/translator/).

Esistono anche estensioni specifiche per integrarli direttamente in Firefox o in altri browser. Per ciò che riguarda Firefox, fare riferimento alle estensioni nella categoria [Supporto lingue](https://addons.mozilla.org/it/firefox/extensions/language-support/) del sito `addons.mozilla.org`.

### Dizionari bilingui inglese-italiano

Ovviamente, traducendo da materiale in lingua inglese \(o per non far arrabbiare troppo i sudditi di sua maestà, in anglo-americano\), uno degli strumenti più importanti è il dizionario bilingua inglese-italiano. Ne esistono molti in rete, e rimane sempre valido il consiglio di acquistare un vero dizionario cartaceo o digitale, senza elncarli tutti, tre dei più utilizzati sono i dizionari inglese italiano del [Cambridge Dictionary](https://dictionary.cambridge.org/it/dizionario/inglese-italiano/), di [WordReference](http://www.wordreference.com/) e l’[Hoepli](http://dizionari.repubblica.it/inglese.php) ospitato sul sito della Republica.

### Corpora

Oltre ai veri e propri dizionari, è possibile cercare nei cosidetti _Corpora_, ossia dei motori di ricerca che presentano dei risultati di traduzioni già effettuate prese da libri, materiale online, film ecc. Ovviamente la traduzione proposta va filtrata, ne va capito il contesto e ricontestualizzata utilizzando la forma e il registro del materiale che si sta traducendo; rappresentano comunque un buon punto di partenza e ispirazione. Anche in questo caso ci limitiamo a citarne tre: [My Memory](https://mymemory.translated.net/), [Linguee](https://www.linguee.com/english-italian) e [Reverso](http://context.reverso.net/traduzione/).

### Dizionari monolingui di italiano, sinonimi e contrari

Esistono un sacco di dizionari veri e propri e di sinonimi e contrari online, se si sta già utilizzando uno di questi servizi e si ha una certa dimestichezza con lo strumento, il consiglio è quello di continuare ad usare la risorsa che si sta già utilizzando. In Firefox, ad esempio, di default viene fornito il dizionario Hoepli, ma altri possono essere aggiunti visitando il sito del dizionario e aggiungendo il relativo motore di ricerca, se disponibile \(come spiegato nella sezione [Ricerche rapide in Firefox](5-risorse_esterne.md#ricerche-rapide-in-firefox).

Un ottimo dizionario che ci sentiamo di consigliare è quello Treccani, per aggiungerlo come _smart bookmark_ \(fare riferimento alla sezione [Ricerche rapide in Firefox](5-risorse_esterne.md#ricerche-rapide-in-firefox)\), aggiungere questo link ai segnalibri:

```text
http://www.treccani.it/vocabolario/%s
```

e il rispettivo dizionario di sinonimi e contrari:

```text
http://www.treccani.it/vocabolario/%s_(Sinonimi-e-Contrari)/
```

Si faccia però attenzione quando si cercano le parole con lettere accentate, il motore di ricerca non riconosce le lettere acentate, quindi per cercare, ad esempio il significato o un sinonimo di _accessibilità_ digitare `accessibilita` sostituendo la `a` finale con una `a` normale.

Un altro ottimo dizionario è il [De Mauro](http://dizionario.internazionale.it/), ospitato sul sito del quotidiano Internazionale.

Altri due degni di menzione sono il [Sabatini Coletti](http://dizionari.corriere.it/dizionario_italiano/) ospitato sul sito del Corriere della sera e il [Garzanti online](http://www.garzantilinguistica.it/) \(registrazione, gratuita, richiesta\).

Ancor meglio sarebbe utilizzare un dizionario cartaceo o digitale professionale, che rispetto alla versione online è certamente più ricco e curato.

In ogni caso, fare sempre molta attenzione al sinonimo eventualmente scelto, non sempre i sinonimi hanno, soprattutto nell’ambito tecnico-informatico, l’esatto significato della parola che si vuole sostituire.

### Coniugazione verbi

In realtà, a un madrelingua, questo non dovrebbe servire, però, in caso di dubbi, il sito WordReference ha un [ottimo strumento](http://www.wordreference.com/conj/ItVerbs.aspx) per i tempi e i modi verbali. Basterà ricercare il verbo all’infinito e si verrà rimandati a una pagina in cui sono indicate tutte le coniugazioni del verbo nei vari tempi e modi verbali \(anche il congiuntivo :-P\).

### Dizionari monolingui di inglese

Talvolta è utile controllare la definizione in lingua inglese di un termine per meglio scegliere il traducente in lingua italiana da utilizzare. A questo scopo, i migliori dizionari madrelingua inglese sono: [Merriam-Webster](https://www.merriam-webster.com), [Cambridge Dictionary](https://dictionary.cambridge.org/) e [The Free Dictionary](http://www.thefreedictionary.com/).

Il terzo, forse meno autorevole rispetto ai primi due, è però molto aggiornato con parole e acronimi del gergo di Internet e nei progetti Mozilla non si sta traducendo opere di Shakespeare ma stringhe di testo scritte da programmatori.

Un altro modo, più veloce ma meno preciso, per controllare il significato di un termine senza installare ulteriori motori di ricerca è sfruttare i comandi avanzati di ricerca dei classici motori già presenti di default in Firefox, ad esempio DuckDuckGo e Google. È possibile infatti cercare utilizzando il comando `define:parola`, per visualizzare prima dei risultati una breve definizione del termine. Ad esempio, cercando `define:browser` con DuckDuckGo, si aprirà [questa pagina](https://duckduckgo.com/?q=define%3Abrowser&t=ffab&yeg=B&ia=definition), dove, prima dei risultati di ricerca, viene riportata una breve definizione del termine. Google funziona in modo analogo e così anche gli altri motori di ricerca.

Un’altra risorsa molto utile, soprattutto per capire il significato di acronimi tecnici e nuove parole inventate dagli informatici, è la Wikipedia inglese. Wikipedia è molto aggiornata e molte volte, uardando nella sezione di sinistra dove appaiono le lingue in cui è disponibile la pagina potremo essere così fortunati da trovare la scritta _Italian_. Aprendo il collegamento si verrà rimandati al corrispettivo articolo sulla pagina italiana e si potrà vedere come è stato tradotto. A volte la traduzione può non essere totalmente letterale perché scritto senza basarsi sulla versione inglese o meno aggiornato rispetto all’originale, in ogni modo è un ottimo punto di partenza per capire il concetto e vedere come i vari termini sono stati tradotti.

Nella versione di Firefox in italiano è presente solo il motore della Wikipedia italiana, comunque basta visitare la home page della Wikipedia inglese e aggiungere il motore di ricerca in lingua inglese.

### Dizionario per il correttore ortografico

Uno strumento utilissimo nella traduzione, e più in generale nella scrittura, è il correttore ortografico, esso consente di non commettere errori banali di digitazione. Qualunque browser o editor di testo che si rispetti supporta lo _spell checking_ evidenziando \(di solito sottolineando in rosso\) le parole non correttamente digitate. Però, quasi nessun software integra nativamente i file necessari per la lingua italiana. Il dizionario di riferimento è quello realizzato dal PLIO \(Progetto Linguistico Italiano OpenOffice.org\) e ha visto il suo ultimo aggiornamento nel 2008. Per aggiungerlo a Firefox è sufficiente installare [questa estensione](https://addons.mozilla.org/it/firefox/addon/dizionario-italiano/), per integrarlo in altri editor di testo invece consigliamo di fare riferimento alla documentazione del software utilizzato. L’ultima versione può essere scaricata da [questa pagina](https://sourceforge.net/project/showfiles.php?group_id=128318&package_id=141110).

## Come rimanere aggiornati

Il lavoro di un traduttore non termina quando ha completato la traduzione di un sito. I siti, come i software, sono aggiornati molto spesso e nuove stringhe vengono aggiunte, altre vengono aggiornate ed è importante tenere la traduzione al passo con l’evoluzione del progetto. In aggiunta a questo, nuovi siti vengono creati, nuove campagne avviate ed è importante che la traduzione del progetto sia disponibile unitamente al lancio dello stesso.

### Mozilla L10n Web Dashboard

Mozilla ha uno strumento in cui è possibile controllare lo stato della traduzione dei vari progetti, la cosidetta [_L10n Web Dashboard_](https://l10n.mozilla-community.org/webdashboard/?locale=it). Ogni lingua ha la sua pagina dedicata in cui sono indicati i vari progetti, lo stato della traduzione, la data per cui la traduzione dovrebbe essere pronta, il tipo di priorità e le eventuali stringhe non ancora tradotte. Accanto ad alcuni progetti potrebbe inoltre apparire la scritta _Opt-in_. Ciò significa che questi progetti non sono ancora stati attivati per la lingua in questione e che sono considerati _facoltativi_ e di minore importanza rispetto agli altri. Facendo clic sul link _Opt-in_ si verrà rimandati a un modulo su Bugzilla per aprire la richiesta di attivazione. All’interno della comunità italiana è prassi consolidata discutere sul forum l’aggiunta di nuovi progetti, quindi il consiglio è quello di aprire una discussione e lasciare che sia uno dei moderatori a occuparsi dell’apertura del bug.

Molto utile è la possibilità di sottoscrivere il [feed RSS](https://l10n.mozilla-community.org/webdashboard/?locale=it&rss=1) che consente di essere aggiornati in tempo reale quando ci sono nuove stringhe da tradurre.

### Il forum italiano

Il forum italiano è da sempre il principale luogo dove chiedere aiuto e discutere dei vari progetti di localizzazione che riguarda l’ecosistema Mozilla. In particolare la sezione [Traduzioni](https://forum.mozillaitalia.org/index.php?board=8.0) è interamente dedicata a raccogliere tutte le discussioni inerenti la localizzazione: proposta di nuovi progetti, segnalazioni di errori nella localizzazione italiana, discussioni terminologiche e molto altro. La registrazione al forum richiederà solo pochi minuti e consentirà di intervenire attivamente nelle varie discussioni. Sarà inoltre possibile attivare le notifiche per tutte le nuove discussioni aperte nelle singole sezioni e ricevere via email le notifiche alle discussioni a cui si è partecipato.

### Etherpad

L’[Etherpad](https://public.etherpad-mozilla.org/) è uno strumento dove poter creare documenti da condividere e modificare assieme, può essere utilizzato per raccogliere opinioni o per segnalare la propria disponibilità per partecipare a eventi o semplicemente per apportare modifiche a un documento che si vuole pubblicare. Chiunque può aprire un nuovo etherpad e condividerlo con chi desideri. Lo strumento presenta un editor in stile _WYSIWYG_ e nella colonna di destra una _chat_ per discutere in tempo reale con chi sta visualizzando il documento in quel momento.

Per partecipare alla modifica del file e entrare nella chat, fare clic sul pulsante in alto a destra e inserire il proprio nome o nickname. A ogni partecipante verrà assegnato un colore e le modifiche da lui apportate nel documento verranno visualizzate col colore in questione.

### Account Firefox

Probabilmente chi utilizza Firefox possiede già un account Firefox per utilizzare il servizio di sincronizzazione del profilo tra più dispositivi, nel caso non fosse così, consigliamo di crearne uno perché consentirà di registrarsi in modo facile e rapido ad alcuni servizi Mozilla descritti di seguito. La procedura è semplicissima, ma per tutti i chiarimenti del caso si può consultare [questo articolo](http://mzl.la/1k1AwkA).

### Bugzilla

Bugzilla è una piattaforma di gestione dei _ticket_ sviluppata da Mozilla e utilizzata da molti progetti software open source per tenere traccia dei _bug_ dei vari prodotti. Bug che non sono da intendersi nel senso classico, cioè errori e malfunzionamenti del software, ma anche richieste di nuove funzioni, attivazione di nuove lingue e in generale tutto ciò che riguarda il lavoro di un’azienda che deve essere tracciato.

Mozilla stessa utilizza una propria versione del software Bugzilla per uso interno sul sito [bugzilla.mozilla.org](https://bugzilla.mozilla.org/). Prima di tutto bisognerà registrarsi, ad esempio utilizzando il proprio account Firefox, e una volta registrati si potranno aprire nuove richieste \(bug\). Prima di farlo è importante cercare se il bug esista già sulla piattaforma, giusto per non far perdere tempo agli sviluppatori e non riempire la piattaforma con richieste multiple.

Quando un nuovo bug viene aperto il suo stato iniziale sarà _UNCONFIRMED_ \(NON CONFERMATO\), ciò significa che c’è una nuova richiesta di cui, il responsabile del prodotto a cui la richiesta fa riferimento dovrà leggerla e dare una risposta.

Se la richiesta che è aperta viene riconosciuta come già presente verrà marcata come _DUPLICATE_ e non verrà più presa in considerazione.

Nel caso la richiesta venga accettata \(confermato un bug in Firefox, implementazione di una nuova funzione, attivazione di una nuova lingua\) lo stato passerà a _NEW_ \(NUOVO\) e, nel minor tempo possibile verrà assegnato \(ASSIGNED\) alla persona che se ne dovrà occupare realmente.

A seconda della difficoltà che richiedere soddisfare la richiesta passerà del tempo prima che venga contrassegnato come _FIXED_ \(RISOLTO\). Alcuni bug di Firefox e Thunderbird sono stati aperti anche una decina di anni prima di giungere a una risoluzione, di solito comunque le richieste di attivazione o altre richieste riguardanti la localizzazione vengono evase in tempi rapidissimi.

Per non abusare della risorsa e non far perdere tempo a nessuno, prima di aprire un nuovo bug consigliamo di discuterne nel forum e vedere se si tratta davvero di bug o solo di malfunzionamento del proprio sistema o di qualche configurazione non corretta. Lo stesso dicasi per eventuali richieste riguardanti la localizzazione dei siti \(inutile aprire una richiesta per localizzare un nuovo sito se non ci sono abbastanza persone disponibili a collaborare o se il sito non è di interesse per il pubblico italiano\).

### Mozillians

Tutti noi volontari Mozilla siamo orgoliosi di definirci _mozilliani_ e per ribadire il concetto è possibile registrarsi sul sito [Mozillians](http://mozillians.org/). Oltre che per ribadire l’orgoglio di far parte della comunità Mozilla, il sito ha una sua utilità pratica che è quella di raccogliere tutti i contatti dei volontari e delle persone coinvolte nel progetto.

Una volta registrati, sarà possibile scegliere una serie di interessi: localizzazione \(lingue parlate\), programmazione \(linguaggi conosciuti\), ecc. e iscriversi a specifici gruppi di interesse.

Ci sono diversi livelli di essere un _mozilliano_ e a seconda del livello si riceveranno comunicazioni più o meno riservate da parte del gruppo dirigente Mozilla \(un numero molto limitato\).

L’importante è comunque fare il primo passo ed aprire l’account, a seconda del livello di partecipazione i membri con privilegi più elevati potranno garantire e aiutarvi a aumentare di livello.

### Blog L10n

Mozilla tiene inoltre, in lingua inglese, [un blog](https://blog.mozilla.org/l10n/) specificatamente dedicato alla localizzazione, in cui vengono trattati argomenti di vario genere e viene data notizia di novità riguardanti gli strumenti di localizzazione come Pontoon.

## Appendice

### Ricerche rapide in Firefox

Esistono sostanzialmente due metodi veloci per cercare all’interno dei siti:

1. utilizzare uno _smart bookmark_.
2. installare il plugin di ricerca.

Uno _smart bookmark_ è un segnalibro il cui URL contiene al suo interno il segnaposto `%s` e a cui viene associata una _parola chiave_. Una volta aggiunto ai segnalibri sarà possibile richiamarlo dalla barra degli indirizzi digitando la parola chiave seguita da un termine con cui verrà sostituito il segnaposto. Questo permette di aprire più pagine con un unico segnalibro.

Per aggiungere la parola chiave in fase di aggiunta del segnalibro e evitare la procedura descritta qui di seguito è possibile [applicare la personalizzazione](https://forum.mozillaitalia.org/index.php?topic=52004.msg339521#msg339521) descritta in questa discussione. Una volta aggiunto uno di questi URL ai segnalibri, per associare una parola chiave procedere come segue:

1. Aprire la _Libreria_.
2. Cercare il segnalibro \(il consiglio è di posizionarli tutti su un’unica cartella per trovarli velocemente\).
3. Selezionare il segnalibro.
4. Fare clic su _Più dati_ e inserire la parola chiave.

È anche possibile aggiungere uno _smart bookmark_ di una ricerca facendo clic col tasto destro sul campo di ricerca e scegliendo _Aggiungi una parola chiave a questa ricerca_. Firefox genererà automaticamente l’URL dello _smart bookmark_ analizzando la struttura del campo di ricerca e aprirà il pannello di aggiunta nuovo segnalibro.

Supponendo di aver associato la parola chiave `gms` Glossario Microsoft\) allo _smart bookmark_ per cercare nel glossario Microsoft \(come visto nella sezione [Glossari](5-risorse_esterne.md#glossari-e-memorie)\) basterà digitare nella barra degli indirizzi `msg browse` per essere rimandati a [questa pagina](https://www.microsoft.com/Language/en-US/Search.aspx?sString=browse&langID=it-IT) e osservare i traducenti più utilizzati per rendere _Browse_ \(Sfoglia\). Ulteriori informazioni in [questo articolo](http://mzl.la/1BAQnZV). Per aggiungere un motore di ricerca invece, dalla pagina del sito a cui si è interessati, fare clic sulla lente di ricerca nella barra degli indirizzi e, se presente, selezionare _Aggiungi questo motore di ricerca_. Se non è disponibile il plugin di ricerca, provare a cercarlo sul sito [Mycroft Project](http://mycroftproject.com/).

Per aggiungere a una ricerca una parola chiave come fatto per gli _smart bookmark_, procedere come segue:

1. Aprire il menu _Opzioni_ di Firefox \(pagina `about:preferences`\);
2. Dal pannello di sinistra selezionare _Ricerca_.
3. Individuare il motore di ricerca desiderato tra quelli visualizzati, fare doppio clic e inserire la parola chiave.

Adesso sarà possibile effettuare ricerche veloci utilizzando il motore di ricerca come descritto nel caso degli _smart bookmark_.

### Caratteri

Questa sezione è in corso di stesura e sarà integrata in questo capitolo quando sarà completata. Per il momento è possibile consultare una prima bozza di questa sezione in [questa pagina]()

