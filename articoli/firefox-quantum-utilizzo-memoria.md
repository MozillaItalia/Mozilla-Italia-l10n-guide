Questa è la traduzione dell’articolo <a href="http://www.erahm.org/2017/09/25/firefox-memory-usage-in-the-quantum-era/" target="_blank">Firefox Memory Usage in the Quantum Era</a> pubblicato sul blog di Eric Rahm.
Traduttore: <a href="https://www.mozillaitalia.org">Sav22999</a>


<h1>Utilizzo della memoria in Firefox nell’Era Quantum</h1>

	
		This is a continuation of my <em>Are They Slim Yet</em> series. For background see my <a href="firefox-memory-usage-with-multiple-content-processes">previous installment</a>.
La prossima versione, 57, di Firefox ha un enorme focalizzazione sulle prestazioni. <a href="https://wiki.mozilla.org/Quantum">Quantum</a> ha influenzato molti aspetti ma non abbiamo veramente parlato dell’uso della memoria, la quale spesso fa precipitare nella ricerca di prestazioni. Fortunatamente, da quando abbiamo portato <a href="are-we-slim-yet-is-dead-all-hail-are-we-slim-yet">AWSY in albero</a>, è stato abbastanza facile monitorare l’utilizzo della memoria e le regressioni anche <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1378526">su rami di sviluppo separati</a>.
Il team di Stylo è stato un grande utilizzatore di questo e lo dimostra; abbiamo abilitato Stylo in modo predefinito intorno al settimo e si può vedere una lunga regressione, ma si nota, ancora di più, intorno al sedicesimo:

<img src="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=660%2C451" alt="" class="aligncenter size-full wp-image-187" srcset="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?w=857 857w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=300%2C205 300w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=768%2C524 768w" sizes="(max-width: 660px) 100vw, 660px" data-recalc-dims="1" />

https://twitter.com/nnethercote/status/908838175891611648

Speriamo fiduciosamente che tutto questo ti abbia convinto riguardo il duro lavoro impiegato per migliorare le prestazioni; ora vediamo il comportamento della memoria comparando Firefox agli altri web browser.

La <a href="are-they-slim-yet-round-2">metodologia per il test</a> è la stessa delle versioni precedenti: E’ stato usato il <a href="https://github.com/EricRahm/atsy">progetto ATSY</a> per caricare 30 pagine e misurare l’utilizzo della memoria dei vari processi che ogni web browser genera nel tempo.
<h3>I risultati</h3>

<figure id="attachment_181" style="width: 600px" class="wp-caption aligncenter"><img src="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=600%2C371" alt="Browser Memory Usage." class="size-full wp-image-181" srcset="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?w=600 600w, https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=300%2C186 300w" sizes="(max-width: 600px) 100vw, 600px" data-recalc-dims="1" /><figcaption class="wp-caption-text">Utilizzo della memoria dei web browser in tutti i sistemi operativi.</figcaption></figure>

Edge ha il più alto uso della memoria su Windows, Chrome è con 1,4X di memoria usata rispetto a Firefox 64-bit su Windows e con circa 2X su Linux. Su macOS Safari è ora di gran lunga il peggiore nell’uso della memoria, mentre Chrome e Firefox sono più o meno uguali con Firefox che usa un po’ più di memoria rispetto all’ultima misurazione effettuata.
Nel compleso sono abbastanza felice per dove siamo, ma ora che la nostra grande spinta è terminata, vorrei focalizzarmi di più sulla riduzione dell’uso di memoria così possiamo iniziare a spingere verso il numero di processi.
Mi piacerebbe, inoltre, dare un’occhiata più da vicino su cosa è successo su macOS e perchè è stata la nostra più grande regressione.
I web browser inclusi sono Edge 38 su Windows 10, <a href="https://www.google.com/chrome/browser/beta.html">Chrome Beta 62</a> su tutte le piattaforme, <a href="https://www.mozilla.org/firefox/channel/desktop/">Firefox Beta 57</a> su tutte le piattaforme e <a href="https://developer.apple.com/safari/technology-preview/">Safari Technology Preview 40</a> su macOS 10.12.6.

<em>Notare: Ho dovuto eseguire nuovamente il test con Safari manualmente, perchè sembra che abbiano apportato alcune modifiche che causano il caricamento di tutte le pagine del test nello stesso processo.</em>
