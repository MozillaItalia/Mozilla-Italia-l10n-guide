# Altri strumenti per i localizzatori

Altri strumenti che possono tornare molto utili per tradurre file sono un software di traduzione, un glossario e altri strumenti per memorizzare la propria fraseologia in modo da non fare lo stesso lavoro più volte.
Nella prima sezione di questo capitolo vedremo i due glossari principali a cui fare riferimento per la traduzione dei termini tecnici e delle voci dell’interfaccia dei vari prodotti Mozilla e spiegheremo come utilizzarli in modo veloce.
Nella seconda parte daremo alcuni consigli su traduttori automatici, dizionari online e altre risorse utili nel processo di traduzione.
Nell’ultima parte daremo uno sguardo più da vicino agli strumenti online di casa Mozilla che consentono di rimanere aggiornati sullo stato della localizzazione dei vari prodotti.


## Glossari

Un glossario è uno strumento fondamentale per un traduttore, esso permette di avere sotto mano un elenco di termini tecnici e la loro traduzione nell’ambito di riferimento.
Questo è ancor più importante nel contesto informatico dove alcuni termini sono risemantizzazione di parole preesistenti che vanno ad assumere un significato completamente diverso da quello originale e in cui le scelte fatte inizialmente per rendere il concetto in altre lingue potrebbe discostarsi dalla mera traduzione letterale.
È inoltre molto importante mantenere la terminologia utilizzata nei vari sistemi operativi, per rendere gli stessi concetti in modo che siano il più possibile comprensibili per l’utente.

Un ottimo glossario per i vari termini tecnici è il dizionario Microsoft, nel quale è possibile trovare tutte le stringhe dei vari prodotti, da Windows a Office.

Un analogo del glossario Microsoft per i prodotti Mozilla è disponibile sul sito della comunità francofona `transvision.mozfr.org`.

Il modo più facile per utilizzarli è aggiungerli come motori di ricerca o come *smart bookmark*, qui di seguito vedremo come fare.

#### Integrazione delle ricerche in Firefox

Esistono sostanzialmente due metodi veloci per cercare all’interno di questi glossari:

1.  utilizzare uno *smart bookmark*.
2.  installare il plugin di ricerca.

Nel caso si scelga di utilizzare uno *smart bookmark*, aggiungere questi due URL ai propri segnalibri:

	https://transvision.mozfr.org/?recherche=%s&locale=it&repo=trunk

per ciò che riguarda le stringhe dei prodotti Mozilla e:

	https://www.microsoft.com/Language/en-US/Search.aspx?sString=%s&langID=it-IT

per ciò che riguarda le stringhe dei prodotti Microsoft.

Una volta aggiunti, aprire la *Libreria*, cercare il segnalibro e aggiungere una parola chiave per ognuno di essi.
A questo punto sarà sufficiente digitarla seguita dal termine che si vuole cercare nella barra degli indirizzi per essere rimandati alla relativa pagina.
Supponendo di aver associato la parola chiave `msg` al glossario Microsoft, basterà digitare nella barra degli indirizzi `msg browse` per essere rimandati a [questa pagina](https://www.microsoft.com/Language/en-US/Search.aspx?sString=browse&langID=it-IT) e osservare i traducenti più utilizzati per rendere *Browse* (Sfoglia).

Se invece si preferisce installarli come motori di ricerca [qui ci sono i relativi search plugin](http://www.gialloporpora.altervista.org/searchplugins/).
Anche in questo caso è possibile (anzi è consigliabile) associare una parola chiave per una rapida consultazione dalla barra degli indirizzi.

Ulterriori informazioni su come associare parole chiave a *smart bookmark* e plugin di ricerca sono disponibili in [questo articolo][smartsearch].

In aggiunta a questi due glossari di riferimento, è possibile consultare [questo](/resources/glossari/glossario.txt) piccolo file di testo che raccoglie i principali termini incontrati nella traduzione del sito `addons.mozilla.org` e altri siti correlati.
Il file viene aggiornato non appena vengono incontrati nuovi termini e la versione aggiornata sarà sempre disponibile alla pagina appena indicata.


## Traduzione automatica (MT)

La traduzione automatica, o MT (Machine Translation) è utile per cercare frasi o termini già tradotti in precedenza (ad esempio una formula comune o singole parole).
Bisogna comunque tenere presente che l’intelligenza artificiale non è in grado di riconoscere aspetti importanti quali il contesto e la coerenza logica.
Per questo una traduzione automatica va sempre revisionata da un traduttore umano che la confronti con il testo sorgente.
In più è da tenere presente che più il testo da tradurre sarà breve e comune, più i risultati saranno accurati, più il testo sarà lungo e l’argomento originale, più i risultati saranno scarsi.
Per questa ragione la traduzione automatica darà risultati migliori cercando composti brevi e piccole porzioni di frase, invece di incollare l’intero testo da tradurre.

Se ci si affida a questo tipo di strumenti, il consiglio è quello di registrare un account e accedervi sempre con quel profilo perché sarà possibile memorizzare le traduzioni effettuate in precedenza e il software tenderà ad imparare e ad adeguarsi al contesto delle traduzioni effettuate.


I migliori strumenti online per la traduzione automatica sono:

-   [Google Translate](https://translate.google.com/)
- [Microsoft Translator](http://www.bing.com/translator/)

Esistono anche estensioni specifiche per integrarli direttamente in Firefox o in altri browser.
per ciò che riguarda Firefox, fare riferimento alle estensioni nella categoria [Supporto lingue][estensioni] del sito `addons.mozilla.org`.

### Dizionari, sinonimi e contrari

Esistono un sacco di dizionari veri e propri e di sinonimi e contrari online, se si sta già utilizzando uno di questi servizi e si ha una certa dimestichezza con lo strumento , il consiglio è quello di continuare a farlo.
In Firefox, ad esempio, di default viene fornito il dizionario Oepli, ma altri possono essere aggiunti visitando il sito [Mycroft Project][http://mycroftproject.com/).
Un ottimo dizionario di sinonimi e contrari che ci sentiamo di consigliare è quello Treccani, per aggiungerlo come *smart bookmark* (fare riferimento alla sezione precedente), aggiungere questo link ai segnalibri:

	http://www.treccani.it/vocabolario/%s_(Sinonimi-e-Contrari)/


### Dizionario per il correttore ortografico

Uno strumento utilissimo nella traduzione, e più in generale nella scrittura, è il correttore ortografico, esso consente di non commettere errori banali di digitazione.
Qualunque browser o editor di testo che si rispetti supporta lo *spell checking* evidenziando (di solito sottolineando in rosso) le parole non correttamente digitate.
Però, quasi nessun software integra nativamente i file necessari per la lingua italiana.
Il dizionario di riferimento è quello realizzato dal PLIO (Progetto Linguistico Italiano OpenOffice.org) e ha visto il suo ultimo aggiornamento nel 2008.
Per aggiungerlo a Firefox è sufficiente installare [questa estensione][dizionario-ext], per integrarlo in altri editor di testo invece consigliamo di fare riferimento alla documentazione del software utilizzato.
L’ultima versione può essere scaricata da [questa pagina][dizionario].



#### Le memorie di traduzione dei prodotti Mozilla

Per chi utilizzasse software desktop, come Poedit o OmegaT, che supportino le memorie di traduzione, qui di seguito ci sono i riferimenti a dove trovare delle memorie di traduzione create utilizzando le stringhe di Firefox e altri progetti Mozilla.
Se si vuole utilizzare come memoria di traduzione con poedit o omegat i file che comprendono l’insieme di vari progetti Mozilla, a [questo link][tmx] è possibile scaricare un file `.tmx` creato utilizzando tutte le traduzioni attive dei vari progetti.
È sufficiente selezionare la lingua e i progetti a cui si è interessati e scaricare il file.
Per conoscere come utilizzare le memorie di traduzione in Poedit e OmegaT fare riferimento al capitolo precedente.

A [quest’altro link§[oldtmx] sono inoltre disponibili i file `.tmx` del Progetto Firefox OS.
Nonostante il progetto non sia più attivamente sviluppato, la traduzione italiana può essere utilizzata come riferimento perché si trattava comunque di un’ottimo lavoro.
La memoria di traduzione di Firefox OS è denominata `gaia1.2.tmx`, gli altri file non sono aggiornati e si consiglia di scaricare l’ultima versione disponibile dal sito `transvision.mozfr.org`.
# Come rimanere aggiornati

Il lavoro di un traduttore non termina quando ha completato la traduzione di un sito.
I siti, come i software, sono aggiornati molto spesso e nuove stringhe vengono aggiunte, altre vengono aggiornate ed è importante tenere la traduzione al passo con l’evoluzione del progetto.
In aggiunta a questo, nuovi siti vengono creati, nuove campagne avviate ed è importante che la traduzione del progetto sia disponibile unitamente al lancio dello stesso.

Mozilla ha uno strumento in cui è possibile controllare lo stato della traduzione dei vari progetti, la cosidetta [*L10n Web Dashboard*](https://l10n.mozilla-community.org/webdashboard/?locale=it).
Ogni lingua ha la sua pagina dedicata in cui sono indicati i vari progetti, lo stato della traduzione, la data per cui la traduzione dovrebbe essere pronta, il tipo di priorità e le eventuali stringhe non ancora tradotte.
Accanto ad alcuni progetti potrebbe inoltre apparire la scritta *Opt-in*.
Ciò significa che questi progetti non sono ancora stati attivati per la lingua in questione e che sono considerati *facoltativi* e di minore importanza rispetto agli altri.
Facendo clic sul link *Opt-in* si verrà rimandati a un modulo su Bugzilla per aprire la richiesta di attivazione.
Per quanto riguarda la comunità italiana preferiamo sempre discutere sul forum l’aggiunta di nuovi progetti, quindi il consiglio è quello di aprire una discussione e lasciare che sia uno dei moderatori a occuparsi dell’apertura del bug.
Molto utile è la possibilità di sottoscrivere il [feed RSS](https://l10n.mozilla-community.org/webdashboard/?locale=it&rss=1) che consente di essere aggiornati in tempo reale quando ci sono nuove stringhe da tradurre.

#### Il forum italiano

Il forum italiano è da sempre il principale luogo dove chiedere aiuto e discutere dei vari progetti di localizzazione che riguarda l’ecosistema Mozilla.
In particolare la sezione [Traduzioni][forum-traduzioni] è interamente dedicata a raccogliere tutte le discussioni inerenti la localizzazione: proposta di nuovi progetti, segnalazioni di errori nella localizzazione italiana, discussioni terminologiche e molto altro.
La registrazione al forum richiederà solo pochi minuti e consentirà di intervenire attivamente nelle varie discussioni.
Sarà inoltre possibile attivare le notifiche per tutte le nuove discussioni aperte nelle singole sezioni e ricevere via email le notifiche alle discussioni a cui si è partecipato.

Mozilla tiene inoltre, in lingua inglese, [un blog][l10nblog] specificatamente dedicato alla localizzazione, in cui vengono trattati argomenti di vario genere e viene data notizia di novità riguardanti gli strumenti di localizzazione come Pontoon.










[smartsearch]: http://mzl.la/1BAQnZV

[l10nblog]: https://blog.mozilla.org/l10n/
[forum-traduzioni]: https://forum.mozillaitalia.org/index.php?board=8.0
[lavori]: https://forum.mozillaitalia.org/index.php?topic=59196.0
[estensioni]: https://addons.mozilla.org/it/firefox/extensions/language-support/
[dizionario-ext]: https://addons.mozilla.org/it/firefox/addon/dizionario-italiano/
[dizionario]: https://sourceforge.net/project/showfiles.php?group_id=128318&package_id=141110
[tmx]: https://transvision.mozfr.org/downloads/
[oldtms]: https://www.dropbox.com/sh/odlh109rugbovnr/OA8NTEkZ0b