## File `.po`


Questa sezione sar� integrata nel capitolo 4 della guida.

I file `.po` sono dei semplici file di testo utilizzati come cataloghi per raccogliere tutte le stringhe di un determinato progetto.
In questa sezione ne analizzeremo la struttura e vedremo come sia possibile modificarli anche con un semplice editor di testo (anche se l�utilizzo di strumenti *ad-hoc* riduce la possibilit� di errori e semplifica le operazioni di modifica).

Il formato`.po` non ha una vera standardizzazione, per� il [manuale GetText][gtm] rappresenta una sorta di bozza operativa per l�implementazione e la codifica del formato.
Originalmente nato nel mondo Linux per l�internazionalizzazione del sistema operativo, ha visto una rapida integrazione in moltissimi linguaggi di programmazione come PHP, Python e moltissimi altri, grazie alla disponibilit� di librerie open source che potevano essere facilmente riutilizzate anche in questi linguaggi.
Attualmente � utilizzato sia per l�internazionalizzazione di applicazioni native che per siti e applicazioni web.

Il suo utilizzo permette agli sviluppatori di marcare le stringhe utilizzate in un progetto e, grazie a uno strumento apposito, generare automaticamente un *template* (file con estensione `.pot`) che verr� poi distribuito ai localizzatori che dovranno modificarlo e generare un file binario (file con estensione `.mo`) che una volta caricato render� il progetto disponibile in altre lingue.
Per ci� che riguarda i progetti Mozilla, il localizzatore deve solamente modificare il file `.po`, l�operazione di creazione del file `.mo` viene gestita in modo automatico grazie a degli *script* lato server.

Ma, dopo questa breve premessa, iniziamo subito a vedere come il catalogo `.po` � strutturato.

La prima sezione � detta intestazione e contiene informazioni generali (nome del traduttore, data di creazione, lingua, ecc.) e verr� analizzata pi� compiutamente in seguito.

La prima stringa significativa � quella che contiene un `msgid` non vuoto.

Inizialmente, il *template* (file `.pot`) avr� tutti i campi della traduzione vuoti, compito del localizzatore sar� quello di riempirli tutti con il testo tradotto.
Se invece il catalogo � gi� stato tradotto in precedenza, molte stringhe saranno gi� presenti e il localizzatori dovr� limitarsi a controllare quelle non ancora localizzate.

Ogni blocco ha una forma simile alla seguente:

```
#
: src/olympia/reviews/templates/reviews/reply.html src/olympia/reviews/templates/reviews/report_review.html
msgid "Submit"
msgstr "Invia"
```

La prima riga, quella che inizia con i due caratteri `#:`, �, sostanzialmente, un commento e indica il file e talvolta anche la riga dove � posizionata la stringa nel codice sorgente.
Tutte le stringhe uguali, come si nota dall'esempio, vengono raggruppate assieme.
Questo significa (vedremo pi� avanti un *escamotage*) che non � possibile tradurre in modo differenti una stessa stringa.
Questo � uno dei motivi per cui molti progetti utilizzano pi� cataloghi separati e non un unico catalogo per raggruppare tutte le stringhe presenti.

La riga, pur non essendo rilevante ai fini della localizzazione (si potrebbe anche togliere, anche se sconsigliamo ovviamente di farlo), d� subito delle informazioni utili al traduttore.
Da essa infatti � possibile vedere in quali file si trovi: dal nome � possibile capire di che tipo di pagina o funzione si tratti, dall'estensione del file quale sia il linguaggio con cui viene generata: nel nostro caso si tratta di due file HTML.

Oltre a questo, conoscere il percorso esatto del file e non solo il nome ci aiuta a risalire al file in questione.

Ad esempio, nel caso visto in precedenza, la stringa fa parte del catalogo [django.po][djangopoit] che raccoglie tutte le stringhe del sito `addons.mozilla.org` (AMO).
Come tutti i progetti Mozilla, anche il codice di AMo � disponibile liberamente su GitHub a questo indirizzo:

	https://github.com/mozilla/addons-server

Nel nostro caso basta aggiungere `/blob/master/` seguito dal percorso relativo indicato nel commento per trovare il file sorgente:

	https://github.com/mozilla/addons-server/blob/master/src/src/olympia/reviews/templates/reviews/reply.html
	https://github.com/mozilla/addons-server/blob/master/src/olympia/reviews/templates/reviews/report_review.html

Nel primo caso, con una veloce ricerca (cercare la stringa fra virgolette o apostrofi) si trova che la riga di codice che la genera � la numero 14:

	<input type="submit" value="{{ _('Submit') }}">
	
e si intuisce che si tratta di un pulsante con cui viene inviata la risposta (in questo caso era facile intuirlo anche dal nome del file).


Vediamo un'altra string:

```
#: src/olympia/addons/templates/addons/popups.html
msgid ""
"<strong>How to Install in Thunderbird</strong> <ol> <li>Download and save the file to your hard disk.</li> <li>In Mozilla Thunderbird, open Add-ons from the Tools menu.</li> <li>From the options "
"button next to the add-on search field, select \"Install Add-on From File...\" and locate the downloaded add-on.</li> </ol>"
msgstr ""
"<strong>Come installare in Thunderbird</strong> <ol> <li>Scarica e salva il file sul tuo disco fisso.</li> <li>In Mozilla Thunderbird seleziona Componenti aggiuntivi nel menu Strumenti.</li> "
"<li>Seleziona �Installa componente aggiuntivo da file�� dal pulsante Opzioni accanto al campo di ricerca e individua il file scaricato.</li> </ol>"
```

Si tratta dell�avviso visualizzato quando si tenta di installare un�estensione per Thunderbird.

Qui notiamo che le stringhe sono *wrapped*, cio� sono di uo messe su pi� righe e la loro lunghezza non pu� superare un certo numero caratteri.
Questa � puramente una scelta per rendere pi� leggibile il file, nessuno ci vieta di tenere la stringa tutta su una riga.
Tutte queste righe devono per� iniziare con un `msgstr` vuoto e essere tutte racchiuse tra virgolette.

Le virgolette, come si nota dall�originale `en-US`, devono essere *escaped`, proprio per evitare che il software le legga come carattere di fine riga.

Nella traduzione italiana abbiamo per� utilizzato le virgolette tipografiche che non danno problemi.
Se avessimo voluto mantenere le normali virgolette - e questo pu� essere necessario se descrivono dei valori di propriet� dell'elemento HTML - avremo dovuto fare l'*escape del carattere utilizzando `\"`.
Questo � uno dei motivi per cui utilizzare un software come Poedit o Pontoon evita un sacco di problemi.


[gtm]: https://www.gnu.org/software/gettext/manual/gettext.html
[amo-it]: https://github.com/mozilla/addons-server/tree/master/locale/it/LC_MESSAGES
[djangopoit]: https://github.com/mozilla/addons-server/blob/master/locale/it/LC_MESSAGES/django.po
[addhtml]: https://github.com/mozilla/addons-server/blob/master/src/olympia/reviews/templates/reviews/add.html
https://github.com/mozilla/addons-server/tree/master/src/olympia/reviews/templates/reviews/reply.html

