Questa è la traduzione dell’articolo <a href="http://www.erahm.org/2017/09/25/firefox-memory-usage-in-the-quantum-era/" target="_blank">Firefox Memory Usage in the Quantum Era</a> pubblicato sul blog di Eric Rahm.
Traduttore: <a href="https://www.mozillaitalia.org">Sav22999</a>


<h1>Firefox nell’Era Quantum: il consumo di memoria</h1>

	
		This is a continuation of my <em>Are They Slim Yet</em> series. For background see my <a href="firefox-memory-usage-with-multiple-content-processes">previous installment</a>.
La prossima versione di Firefox, 57, punta soprattutto sulle prestazioni. <a href="https://wiki.mozilla.org/Quantum">Quantum</a> ha influenzato molti aspetti di Firefox, ma non abbiamo ancora affrontato l’argomento dell’uso di memoria, che spesso viene lasciato in secondo piano nella ricerca di prestazioni elevate. Da quando il <a href="http://www.erahm.org/2017/05/25/are-we-slim-yet-is-dead-all-hail-are-we-slim-yet/">progetto AWSY</a> è stato incorporato nell’infrastruttura del codice Mozilla, è stato abbastanza facile monitorare l’utilizzo della memoria e le regressioni anche <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1378526">su rami di sviluppo separati</a>.
Il team di sviluppo del nuovo motore per i CSS, Stylo, ha fatto ampio uso di questa funzione, e i risultati si notano. Abbiamo attivato AWSY come impostazione predefinita per il progetto Stylo il giorno 7, a partire dal quale si nota nel grafico una regressione significativa, ma il giorno 16 essa era quasi completamente scomparsa:

<img src="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=660%2C451" alt="" class="aligncenter size-full wp-image-187" srcset="https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?w=857 857w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=300%2C205 300w, https://i1.wp.com/www.erahm.org/wp-content/uploads/2017/09/Screenshot-2017-9-26-Explicit-Memory-summary-opt-stylo-disabled-linux64-stylo-disabled-mozilla-central-and-others.png?resize=768%2C524 768w" sizes="(max-width: 660px) 100vw, 660px" data-recalc-dims="1" />

https://twitter.com/nnethercote/status/908838175891611648

Speriamo questi dati convincano i nostri utenti del grande impegno profuso nel miglioramento delle prestazioni, ma adesso vediamo come Firefox se la cava a livello di consumo di memoria rispetto agli altri browser.

La <a href="are-they-slim-yet-round-2">metodologia utilizzata</a> per la seconda parte dei test è stata la stessa utilizzata anche in precedenza: grazie al codice del <a href="https://github.com/EricRahm/atsy">progetto ATSY</a> sono state aperte una trentina di pagine nei vari browser e misurato l’utilizzo di memoria dei processi avviati per gestire tali operazioni.
<h3>I risultati</h3>

<figure id="attachment_181" style="width: 600px" class="wp-caption aligncenter"><img src="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=600%2C371" alt="Browser Memory Usage." class="size-full wp-image-181" srcset="https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?w=600 600w, https://i2.wp.com/www.erahm.org/wp-content/uploads/2017/09/chart1.png?resize=300%2C186 300w" sizes="(max-width: 600px) 100vw, 600px" data-recalc-dims="1" /><figcaption class="wp-caption-text">Utilizzo della memoria dei web browser in tutti i sistemi operativi.</figcaption></figure>

Edge è il browser che consuma più memoria su Windows, Chrome segue a ruota con un utilizzo che è 1,4 volte superiore a quello di Firefox sui sistemi Windows a 64-bit e quasi il doppio sui sistemi Linux. Per ciò che riguarda i sistemi Mac OS X, Safari è al momento il browser che utilizza più memoria e Chrome e Firefox sono più o meno sullo stesso livello, almeno dai dati delle ultime misurazioni effettuate.
Nel complesso Eric Rham è abbastanza soddisfatto per i risultati raggiunti, ora che il miglioramento delle prestazioni è stato portato a termine lui e il team possono concentrarsi maggiormente sulla diminuzione del consumo di memoria per poi passare al numero di processi utilizzati per gestire i contenuti delle pagine web. Un altro cruccio dell’autore è quello di indagare i risultati non molto soddisfacenti su Mac OS X.
Mi piacerebbe, inoltre, dare un’occhiata più da vicino su cosa è successo su macOS e perchè è stata la nostra più grande regressione.
I browser web inclusi sono Edge 38 su Windows 10, <a href="https://www.google.com/chrome/browser/beta.html">Chrome Beta 62</a> su tutte le piattaforme, <a href="https://www.mozilla.org/firefox/channel/desktop/">Firefox Beta 57</a> su tutte le piattaforme e <a href="https://developer.apple.com/safari/technology-preview/">Safari Technology Preview 40</a> su macOS 10.12.6.

<em>I test su Safari sono stati effettuati una seconda volta manualmente perché, probabilmente a causa delle modifiche negli ultimi aggiornamenti del browser, utilizzando ATSY le pagine venivano caricate tutte in un unico processo.</em>
