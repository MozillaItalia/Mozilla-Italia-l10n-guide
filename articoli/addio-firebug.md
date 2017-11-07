Lo strumento per lo sviluppo web più avanzato e popolare di sempre.
Firebug è stato un successo straordinario. Nei suoi 12 anni di vita, questo strumento open source ha fatto nascere attorno a sé un vero e proprio culto tra gli sviluppatori web. Quando fu rilasciato per la prima volta nel 2005, Firebug era il primo strumento che consentisse ai programmatori di analizzare, modificare ed effettuare il debug del codice direttamente all’interno di Firefox. Era inoltre in grado di monitorare in tempo reale il codice HTML, CSS e JavaScript nelle pagine web, insomma, rappresentava un gigantesco passo in avanti.
Firebug ha saputo catturare l’interesse degli utenti e tutt’oggi è ancora utilizzato da oltre un milione di fedelissimi.
Per questo motivo è triste apprendere che, con l’uscita di Firefox Quantum (versione 57) il prossimo mese, Firebug cesserà di essere compatibile con il browser Mozilla. La buona notizia è che tutte le funzioni di Firebug adesso sono integrate negli Strumenti di sviluppo di Firefox.

Raccontare la storia di Firefox e Firebug equivale a raccontare la storia dell’ascesa del Web. Abbiamo superato traguardi importanti, cambiando il modo in cui gli sviluppatori analizzano il codice HTML e effettuano il debug del codice JavaScript all’interno del browser. Firebug ha spalancato le porte all’era del Web 2.0. Oggi possiamo ritrovare la tecnologia pionieristica sviluppata dalla comunità di Firebug all’interno degli <a href="https://www.mozilla.org/en-US/firefox/developer/?utm_source=blog&amp;utm_medium=hacks&amp;utm_campaign=switch">Strumenti di sviluppo di Firefox</a>.

image1

<h3>Uno sguardo al futuro e un tuffo nel passato</h3>

Ma prima di lasciarci Firebug alle spalle, vogliamo dedicare un momento a ricordare le tappe più importanti del progetto e condividere alcune storie dei primi membri della comunità di Firebug.

<ul>
<li><b>Gennaio 2006, Firebug 0.2</b> &mdash; Joe rilascia la prima versione, consistente di un singolo pannello <a href="https://youtu.be/JVCioNT-SYE">Console</a> che registrava gli eventi AJAX.</li>
<li><b>Maggio 2006, Firebug 0.4</b> &mdash; Viene aggiunto un pannello di primo livello per il <a href="https://youtu.be/LvdcAm1-4zU">debug</a> del codice JavaScript.</li>
<li><b>Dicembre 2006</b> &mdash; Il codice sorgente di Firebug diventa open source.</li>
<li><b>Gennaio 2007, Firebug 1.0</b> &mdash; Inizio dell’era Web 2.0.</li>
<li><b>Agosto 2008, Firebug 1.2</b> &mdash; Prima versione rilasciata da FWG (Firefox Working Group).</li>
<li><b>Ottobre 2009</b> &mdash; Nasce il formato per esportare i dati HTTP (HAR), presentato <a href="http://www.softwareishard.com/blog/har-12-spec/">in questo articolo</a>.</li>
<li><b>Febbraio 2010, <b>Firebug Lite</b> &mdash; Un bookmarklet <a href="https://blog.getfirebug.com/page/22/">realizzato</a> per Google Chrome.</li>
<li><b>Aprile 2010,</b> &mdash; Introduzione dei breakpoint dinamici e grafici per le pagine web (<a href="https://getfirebug.com/doc/breakpoints/paper/breakpoints.pdf">presentazione in pdf</a>).</li>
<li><b>2011</b>&mdash; Scoppia il boom delle <a href="https://getfirebug.com/wiki/index.php/Firebug_Extensions">estensioni</a> per Firebug.</li>
<li><b>Giugno 2014, Firebug 2.0</b> &mdash; Nuova interfaccia grafica compatibile con Firefox Australis.</li>
<li><b>Giugno 2016</b>,&mdash; <a href="https://blog.getfirebug.com/2016/06/07/unifying-firebug-firefox-devtools/">Integrazione di Firebug negli strumenti di sviluppo di Firefox</a>.</li>
<li><b>Ottobre 2017, &&mdash; Fine dell’avventura Firebug</b>.</li>
</ul>
image2
<em>Firebug 0.2, Console</em>

Vorrei condividere alcuni dei miei ricordi più importanti legati a Firebug, partendo dal momento in cui tutto ebbe inizio.
La primissima versione pubblicata su <a href="https://addons.mozilla.org/cs/firefox/addon/firebug/versions/?page=4#version-0.2">AMO</a> nel gennaio 2006 fu la 0.2, accompagnata da un breve commento di Joe Hewitt:
<blockquote>
Questa è una versione davvero molto preliminare, il codice ha solo un paio di giorni di vita. Attenti al leopardo!
</blockquote>

Più tardi, nel dicembre 2006, Joe prende l’importante decisione di rendere Firebug open source:

<blockquote>
Il primo annuncio che vorrei fare riguarda la licenza del codice sorgente di Firebug. Mentre lavoravo alla versione 1.0 di Firebug, iniziai a chiedermi se dovessi o meno trasformare questa esperienza da mero passatempo a un vero e proprio business. Quando illustrai questa idea sul mio blog, le reazioni furono molto positive e questo rafforzò ulteriormente la mia convinzione che Firebug avrebbe potuto diventare un successo a livello commerciale.
Tuttavia, alla fine, ho sentito che non era quella la cosa giusta da fare. Mi piace lavorare al codice di Firebug per la consapevolezza che mi dà di rendere felici molte persone e avanzare lo sviluppo delle tecnologie web. Questo per me significa molto di più di tutto il resto, perciò ho preso la decisione che <strong>Firebug rimarrà gratuito e open source</strong>.
</blockquote>

Subito dopo aver rilasciato la versione 1.0, Joe Hewitt lasciò il progetto per dedicarsi alla sua nuova esperienza lavorativa in Facebook. Ben presto fu John J. Barton di IBM a interessarsi a Firebug e riprenderne lo sviluppo.

<blockquote>
Ah Firebug, bei tempi quelli! Iniziai come utente e collaboratore, nello specifico lavoravo a oscuri aspetti legati al debugging della funzione <code>eval</code>. Quando Joe Hewitt decise di abbandonare il progetto, iniziai a tampinare i dirigenti di IBM per sondare se ci fosse interesse a proseguire il suo lavoro. A quei tempi, le applicazioni web commerciali stavano appena emergendo e il debug consisteva praticamente nel solo metodo <`code>window.alert</code>`.
Quando anche Jan ‘Honza’ Odvarko entrò nel FWG, il team Rational IDE di IBM diede finalmente il suo appoggio al progetto, realizzai quindi un plugin per Eclipse così da integrare Firebug nel nostro prodotto. Honza e io, utilizzammo come base  il geniale framework realizzato da Joe, adattandolo alla gestione di applicazioni più pesanti e complesse. Aggiungemmo ulteriori test e migliorammo il processo di autenticazione  per il rilascio delle versioni, successivamente passammo a risolvere alcuni bug e a rispondere alle nuove segnalazioni per far sorgere una comunità attorno a Firebug. Ben presto ci ritrovammo con nuovi collaboratori e una crescente raccolta di estensioni. Mike Collins mi affiancò per ciò che riguardava la parte gestionale e io collaborai con Salman Mirghasemi (EPFL) su progetti di ricerca che sfruttavano la tecnologia Firebug.
Sono orgoglioso del lavoro svolto da tutti noi su Firebug in una fase così cruciale per lo sviluppo della tecnologia web. Firebug ha aiutato un numero enorme di sviluppatori a realizzare siti visitati da milioni di persone in tutto il mondo. Oggi ogni browser integra un debugger ispirato alla nostra estensione. Per quanto fossimo un gruppetto disorganizzato che poteva contare solo su stesso, indubbiamente mi mancherà il lavoro di squadra svolto su Firebug, tuttavia lasciamo il campo consapevoli di aver avuto un enorme impatto positivo.
</blockquote>


<em>Firebug 1.2, Net panel</em>



Il successo di un progetto dipende sempre dalla dedizione profusa da sviluppatori, collaboratori e utenti coinvolti. Ma in certi momenti non è stato affatto facile stare al passo con la rapida evoluzione del browser Firefox e dovevamo lavorare alacremente.

Di seguito un piccolo stralcio tratto da un <a href="https://blog.getfirebug.com/2010/03/17/firebug-reflections/">articolo di John J. Barton</a> del marzo 2010:
<blockquote>
Ne abbiamo fatta di strada da quando Joe Hewitt ha rilasciato <b>Firebug 1.0</b>.
Nato alle soglie della rivoluzione del Web 2.0, Firebug ha aiutato gli utenti a capire che il <a href="https://it.wikipedia.org/wiki/Web_2.0">Web 2.0</a> non era solo una moda passeggera e che le “app web” avrebbero coperto un ruolo importante nel futuro. Firebug è stato costretto a crescere in fretta in un momento in cui non comprendevamo appieno tutti gli aspetti del codice, ancor meno comprendevamo il codice di Firefox.
Nonostante il contributo di utenti estremamente dedicati, che hanno saputo rendersi utili, <a href="http://ajaxian.com/archives/firebug-11-and-getfirebugcom">Firebug 1.1</a> non era destinato al successo. In pratica, <a href="http://www.railsjedi.com/posts/24-Firebug-1-2-Excitement">Firebug 1.2</a> è stata la nostra prima versione degna di questo nome dopo l’originale di Joe. Dietro le quinte, abbiamo dovuto lavorare alacremente per risolvere un bug di sicurezza in Firebug. A quell’epoca, non era possibile renderlo pubblico, troppi erano gli utenti a rischio.
</blockquote>

https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2017/10/thumbnail-layout.gif

Firebug è sempre stato un progetto molto popolare e molti sviluppatori cominciarono a lavorare al progetto, sistemando bug e realizzando nuove estensioni. Proprio così, tante nuove estensioni realizzate per estendere un’estensione. Stavamo utilizzando tutti la medesima tecnologia. Una vera soddisfazione per tutta la comunità.
Nel luglio del 2008 ho scritto <a href="http://www.softwareishard.com/blog/firebug/list-of-firebug-extensions/">questo articolo</a> per fare il punto sulle estensioni per Firebug disponibili:

<blockquote>
Vi siete mai chiesti quante estensioni per Firebug esistano?
Se volete conoscere la risposta, continuate a leggere. Francamente, sono stato abbastanza sorpreso di vedere quante estensioni per Firebug ci siano in circolazione.
</blockquote>

Nel 2008 le estensioni per Firebug ammontavano a una decina, nel 2011 erano più di sessanta. Non era affatto facile gestire il codice di un progetto per mantenerlo compatibile con così tante estensioni, credetemi sulla parola!
Iniziai a lavorare su Firebug nel 2007 e affiancai John J. Barton nello sviluppo della versione 1.2. È a quell’epoca che nacque il Firebug Working Group. Ci concentravamo sul codice di Firebug, ma anche sulla creazione di una comunità attorno al progetto.
Furono momenti emozionanti. Il nostro era un gruppo di lavoro relativamente piccolo e sviluppavamo delle funzioni che il giorno dopo venivano utilizzate da milioni di utenti. Ricevemmo un’enorme numero di feedback, accumulando sempre nuove nozioni su come realizzare strumenti grafici per sviluppatori web.
Il primo componente di Firebug su cui ho lavorato è stato il Pannello di rete.
Il monitoraggio delle connessioni HTTP è sempre stata la mia <a href="http://www.softwareishard.com/blog/firebug/introduction-to-firebug-net-panel/">specialità</a> e ben presto rilevammo come molti utenti erano interessati a esportare i dati raccolti dal Pennello di rete. L’implementazione di questa funzionalità non era affatto difficile, la trovata davvero interessante è stata l’introduzione di un nuovo formato per memorizzare i dati esportati. Un paio di anni più tardi, all’incirca nell’ottobre del 2009, assieme a Steve Souders (un guru nel campo dell’analisi delle prestazioni del caricamento delle pagine, nonché autore di YSlow, spesso considerata come la prima estensione per Firebug) e Simon Perkins, presentammo il nuovo formato HTTP Archive (HAR). Questo formato fu un grande successo e sono molti gli strumenti che ancora oggi lo supportano.

image3

Da un <a href="http://www.stevesouders.com/blog/2009/10/19/http-archive-specification-firebug-and-httpwatch/">articolo</a> di Steve Souders del 2009:

<blockquote>
Ho suggerito che, piuttosto che creare l’ennesimo formato proprietario, Firebug collaborasse con HttpWatch per sviluppare un formato aperto, sostenendolo e proponendolo come standard nel settore. Ho presentato Simon Perkins (HttpWatch) a Jan “Honza” Odvarko (il principale responsabile del Pannello di rete), quindi fatto un passo indietro lasciando che i due lavorassero assieme al risultato che annunciamo quest’oggi.
</blockquote>

Ho passato dei bei momenti lavorando assieme a John e ad altre persone al progetto.
Poiché il codice di Firebug era stato ben scritto e la sua architettura era solida, è stato un piacere lavorarci su. Joe ha fatto un ottimo lavoro gettando le fondamenta su cui realizzare decine e decine di estensioni per Firebug.
John J. è stato un bravissimo manager e un ottimo collega, lavorare assieme a lui era un piacere. Uno dei concetti che abbiamo ideato e sviluppato in Firebug è stato un nuovo tipo di breakpoint. Li abbiamo chiamati breakpoint dinamici e breakpoint grafici per le pagine web. Magari qualcuno tra i lettori ne ha già sentito parlare con i nomi di <i>Break on XHR</i>, <i>Break on Next</i>, <i>Break on DOM mutation</i> ecc.

Dal <a href="https://blog.getfirebug.com/2009/11/03/dynamic-and-graphical-web-page-breakpoints/">blog di Firebug</a>:

<blockquote>
Jan “Honza” Odvarko e io abbiamo sottoposto l’articolo accademco <a href="http://getfirebug.com/doc/breakpoints/paper/breakpoints.pdf">Dynamic and Graphical Web Page Breakpoints</a>”, che tratta la versione 1.5 dei breakpoint, per l’evento <a href="http://www2010.org/www/">WWW 2010</a>. In essa sono spiegati i motivi per l’introduzione dei vari breakpoint, viene descritta esperienza utente e implementazione e infine vengono dati i riferimenti a documenti accademici correlati. Per chi preferisce la versione riassunto, ecco una <a href="http://getfirebug.com/doc/breakpoints/demo.html">pagina dimostrativa</a>.
</blockquote>
image4
image5

Firebug 2.0 è stato distribuito nel giugno 2014. Introduceva un’importante aggiornamento dell’interfaccia per renderla compatibile con il nuovo tema di Firefox Australis.
Siamo riusciti a rilasciare Firebug in tempo utile per l’uscita di Firefox Australis e ne andiamo molto fieri, un vero e proprio traguardo per tutta la comunità. Da allora, siamo in “modalità manutenzione”. La versione più recente di Firebug disponibile su AMO è la 2.0.19.

<a href="https://blog.getfirebug.com/2016/06/07/unifying-firebug-firefox-devtools/">L’integrazione di Firebug</a> negli Strumenti di sviluppo di Firefox è iniziata ufficialmente nel 2016, ma in realtà tale processo era stato avviato molto prima. La strategia Mozilla prevedeva di implementare degli strumenti di sviluppo direttamente in Firefox. Strumenti di sviluppo moderni, realizzati da zero. La decisione fu quindi quella di non sviluppare tali strumenti a partire dalla tecnologia di Firebug. Alcuni utenti e collaboratori furono scontenti di quella decisione, ma l’infrastruttura e i requisiti di Mozilla a quei tempi erano diversi. Talvolta è meglio partire da zero nel fare le cose e questo vale soprattutto nel caso di sviluppo software.
Cosa ancora più importante, gli Strumenti di sviluppo di Firefox oggi sono più performanti che mai, realizzati a partire da tecnologie web come React/Redux/Webpack, insomma un sacco di bella roba.
L’architettura è pronta per supportare le estensioni e il team è eccezionale, con numerosi sviluppatori che vantano grande esperienza in materia di sviluppo web. <a href="https://twitter.com/FirefoxDevTools">Ed ecco a voi il fantastico team</a> :-).

Il processo di integrazione di Firebug negli strumenti di sviluppo di Firefox è stato completato nel 2015 con la versione 3.0 di Firebug (aka <a href="https://github.com/firebug/firebug.next">Firebug.next</a>). Il prototipo è stato inizialmente realizzato sotto forma di estensione per gli Strumenti di sviluppo e alla fine integrato con questi ultimi.
I vecchi utenti possono <a href="https://developer.mozilla.org/en-US/docs/Tools/Migrating_from_Firebug">migrare da Firebug</a> agli strumenti di sviluppo nativi.
Per provare gli strumenti di Sviluppo di Firefox, <a href="https://www.mozilla.org/it/firefox/new/">aggiorna la versione di Firefox in uso</a> o <a href="https://www.mozilla.org/it/firefox/developer/">scarica Firefox Developer Edition</a>.

Il supporto delle estensioni classiche (quelle realizzate in XUL) terminerà con Firefox 57, aka Firefox Quantum.
Questo include ovviamente anche Firebug. È stata proprio la cessazione del suo supporto in Firefox l’occasione che mi ha spinto a scrivere questo articolo.
Il Re è morto, lunga vita al Re.



<strong>Elenco dei collaboratori</strong>: Joe Hewitt, John J. Barton (IBM Almaden), Jan Odvarko (Mozilla Corp.), Max Stepanov (Aptana Inc.), Rob Campbell (Mozilla Corp.), Hans Hillen (Paciello Group, Mozilla), Curtis Bartley (Mozilla Corp.), Mike Collins (IBM Almaden), Kevin Decker, Mike Ratcliffe (Mozilla Corp.), Hernan Rodriguez Colmeiro, Austin Andrews, Christoph Dorn, Steven Roussey (Illuminations for Developers), Sebastian Zartner, Harutyun Amirjanyan, Simon Lindholm, Stampolidis Anastasios, Joe Walker (Mozilla Corp.), Vladimir Zhuravlev, Farshid Beheshti, Leon Sorokin, Florent Fayolle, Hector Zhao, Bharath Thiruveedula, Nathan Mische, Belakhdar Abdeldjalil, Jakob Kaltenbrunner, &#8230;
<strong>Elenco dei localizzatori</strong>: Leszek(teo)Zyczkowski (pl-PL), markh (nl), peter3 (sv-SE), AlleyKat (da-DK), Hector Zhao, lovelywcm (zh-CN), Lukas Kucharczyk, Michal Kec (cs-CZ), Team erweiterungen.de, ReinekeFux, Benedikt Langens, Sebastian Zartner (de-DE), l0stintranslation, gonzalopirobutirro, Luigi Grilli (it-IT), alexxed (ro-RO), Nicolas Martin, Franck Marcia (fr-FR), gLes (hu-HU), Xavi Ivars &ndash; Softcatala (ca), gezmen (tr-TR), eternoendless (es-AR), Dark Preacher (ru), Tiago Oliveira, Diego de Carvalho Zimmermann, Alexandre Rapaki (pt-BR), Juan Botias, Alvaro G. Vicario (es-ES), Andriy Zhouck (uk-UA), Hisateru Tanaka, k2jp (ja-JP), Mohsen Shadroo (fa-IR), Eduard Babayan (hy-AM), Helder Magalhaes (pt-PT), Tomaz Macus (sl-SI), Stoyan Stefanov, Alexander Shopov (bg), Kristjan Bjarni Guomundsson (is-IS), NGUYEN Manh Hung (vi-VN), Bwah (hr-HR), Sonickydon (el), David Gonzales (es), DakSrbija (sr), bootleq (zh-TW), Asier Iturralde Sarasola, Julen Irazoki Oteiza (eu), &#8230;

Firebug Team Leader
