# Markdown Cheatsheet

Questo file è una serie di appunti rivisitati tratti da un file personale che uso come bignamino per il *markdown*.
Mi riprometto di sistemare lo stile in modo sia conforme a quello utilizzato per la guida.


Il *markdown* è uno pseudo-linguaggio creato da [John Gruber][jg] e [Aaron Swartz][as] con lo scopo di avere dei file di testo leggibili e da cui è possibile generare una versione HTML riducendo al minimo la sintassi e utilizzando regole che si sono diffuse nel tempo nei newsgroup e in altri ambienti dove il *plain text* è la regola.

Non avendo una vera standardizzazione come l’HTML, il *markdown* ha visto nel tempo la nascita di diverse estensioni in specifiche piattaforme, senza che però queste estensioni siano adottati da tutti.

Il *markdown* che si usa su  GitHub, denominato *GitHub Flavored Markdown* (GFM, è abbastanza minimale, ad esempio non consente le note a piè pagina, l’inserimento di codice LaTeX, inserimento di testo apice o pedice e molte altre estensioni che sono supportate in altre piattaforme.




## Paragrafi

Nel *markdown*, le righe di testo consecutive sono raggruppate in paragrafi.
Per creare un nuovo paragrafo è necessario inserire una riga vuota e per andare a capo, sempre rimanendo nello stesso paragrafo, è necessario utilizzare il carattere `inserire **due** spazi a fine riga.
Questo permette di evitare righe lunghissime e rende più leggibile il sorgente perché non bisogna fare lo scroll orizzontale (sempre si decida di wrappare il testo).

Di seguito degli esempi pratici: in ognuno verrà riportato prima il codice markdown e poi l'output HTML che il codice genera.

Come detto, è indifferente mettere tutto su una riga o su righe diverse, i due esempi qui di seguito producono lo stesso risultato.


	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.
	
produce lo stesso risultato di:

	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi. *Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Risultato:

Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria:* non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Per mandare a capo, rimanendo all'interno dello stesso paragrafo, cioè forzando un'interuzzione di linea (`<br/>`), si possono mettere due spazi a fine riga (alcune versioni di *markdown accettano anche il carattere \\).

	L'ingresso emanava un lezzo di cavolo bollito e di vecchi e logori stoini.  
	A una delle estremità era attaccato un manifesto a colori, troppo grande per poter essere messo all'interno.
	
(selezionando il testo si dovrebbero vedere i due spazi dopo **stoini.  **)

Il risultato è:
	L'ingresso emanava un lezzo di cavolo bollito e di vecchi e logori stoini.  
A una delle estremità era attaccato un manifesto a colori, troppo grande per poter essere messo all'interno.

Per creare un nuovo paragrafo bisogna mettere una riga bianca:

	Winston si diresse verso le scale.
	
	Tentare con l'ascensore, infatti, era inutile. Perfino nei giorni migliori funzionava raramente e al momento, in ossequio alla campagna economica in preparazione della Settimana dell'Odio, durante le ore diurne l'ero gazione della corrente elettrica veniva interrotta.
	
	L'appartamento era al settimo piano e Winston, che aveva trentanove anni e un'ulcera varicosa alla caviglia destra, procedeva lentamente, fermandosi di tanto in tanto a riprendere fiato.

Risultato:

Winston si diresse verso le scale.

Tentare con l'ascensore, infatti, era inutile. Perfino nei giorni migliori funzionava raramente e al momento, in ossequio alla campagna economica in preparazione della Settimana dell'Odio, durante le ore diurne l'ero gazione della corrente elettrica veniva interrotta. 

L'appartamento era al settimo piano e Winston, che aveva trentanove anni e un'ulcera varicosa alla caviglia destra, procedeva lentamente, fermandosi di tanto in tanto a ri prendere fiato.


## Citazioni

Si quota come nelle email in puro testo, col carattere maggiore:

	>   Su ogni pianerottolo, di fronte al pozzo dell'ascensore, il manifesto con quel volto enorme guardava dalla parete.
	>   Era uno di quei ritratti fatti in modo che, quando vi muovete, gli occhi vi seguono.
	>   
		>   **IL GRANDE FRATELLO VI GUARDA**, diceva la scritta in basso.

	--George Orwell, da 1984.

Risultato:

>   Su ogni pianerottolo, di fronte al pozzo dell'ascensore, il manifesto con quel volto enorme guardava dalla parete.
>   Era uno di quei ritratti fatti in modo che, quando vi muovete, gli occhi vi seguono.
>   
>   **IL GRANDE FRATELLO VI GUARDA**, diceva la scritta in basso.

--George Orwell, da 1984.




Gli spazi dopo il maggiore non vengono considerati, però usare la regola del 4, cioé allineare tutto con 4 caratteri iniziali (il carattere sintattico e 3 spazi rende il codice più leggibile e semplifica con quotazioni e liste annidate).


## Enfasi e grassetto

Il carattere \* viene usato per dare enfasi, un solo asterisco per l'enfasi semplice (di solito resa in corsivo) e due \* per un'enfasi maggiore (di solito grassetto).

	*Corsivo*,, **grassetto** e ***corsivo più grassetto.**

*Corsivo*,, **grassetto** e ***corsivo più grassetto.**

Una brutta cosa del GFM è che non considera i caratteri di formattazione compresi fra caratteri alfanumerici.
In particolare, non si può evidenziare una parte della parola.

## Testo sbarato

per sbarrare il testo utilizzare il carattere tilde (\~):

	~Testo sbarrato~

~Testo sbarrato~



## Intestazioni (Header)

Esistono due sintassi possibili per gli header: Setext e ATX.
La sintassi Setext copre solo i primi due livelli, `<h1>` e `<h2>`.

	Header 1 (Setext
	=================

	Header 2 (Setext
	-----------------

Si possono usare anche solo un uguale o un trattino.

Usando lo stile ATX invece si usano tanti caratteri cancelletto quanto il livello dell'header.

	# Header 1
	# Header 2
	### Header 3
	####Header4
	##### header 5
	###### Header 6
  
## Testo preformattato e codice

per inserire del codice inline si usa il carattere \` (backtick, accento grave).
Quello che è compreso tra due *backtick* non viene interpretato come codice *markdown* e viene mostrato con un carattere a lunghezza fissa.

	`**Questo non è grassetto**`, **questo invece sì**
	`<strong>Questo non è grassetto</strong>`, <strong>questo invece sì</strong>

`**Questo non è grassetto**`, **questo invece sì**
`<strong>Questo non è grassetto</strong>`, <strong>questo invece sì</strong>

I blocchi di codice possono essere inseriti inserendo un carattere di tabulazione (o quattro spazi) a inizio riga.

	hello = function(name){
	  alert('Ciao' + name);
	}

oppure in alternativa separando i blocchi di codice con tre *backtick*:

```javascript
hello = function(name){
	alert('Ciao' + name);
}
```

questa seconda è forse da preferirsi perché consente anche di dire a *markdown* il linguaggio c del codice (in questo caso *JavaScript*), avendo in questo modo l'evidenziazione della sintassi.

## Elenchi

Per gli elenchi puntati si può utilizzare, indifferentemente il trattino, l'asterisco o il più.

	+   Mele
	+   Pere
	+   Arance

+   Mele
+   Pere
+   arance

Sono possibili anche gli elnchi numerati:

1.  Mele
	2.  Pere
	3.  Arance
	
1.  Mele
2.  Pere
3.  Arance

È possibile anche inserire liste annidate su più livelli:
```
Tipi di frutta:

+   Mele. Ci sono diverse varietà di mele, le più diffuse sono:

    +   Annurca - originaria del Sud Italia, questa mela ha la buccia color rosso vinoso, un profumo molto intenso e la polpa croccante, leggermente acidula e succosa.
    +   Fuji - originaria del distretto di Morioka, Giappone. È la mela più coltivata al mondo. Mela dalla buccia rossastra con striature gialle e verdi
    +   Granny Smith - varietà originaria dell’Australia, è la mela verde per antonomasia.
    +   Golden Delicious - Mela dalla buccia gialla usata di solito per le torte alla mela.
    +   Renetta - Varietà dalla buccia gialla con macchie scure. Usata per lo strudel.
+   Pere.
    Le varietà di pere più diffuse sono:
    +   Williams -  La buccia delle pere Williams è verde chiaro, tendente al giallastro, mentre la polpa è di colore bianco avorio, molto zuccherina al palato.
        Si tratta, inoltre, di una varietà di pere molto delicata: per questo è meglio evitare che venga sottoposta a ripetuti sbalzi termici.
    +   Conference - La Conference ha la forma tipica della pera (in questo caso si dice piriforme) ma è leggermente affusolata, con una buccia verde-giallo bronzata e polpa color avorio, dolce, fondente e un tantino acidula
    +   Kaiser - Facilmente riconoscibile per via della sua forma regolare e della buccia uniformemente di colore marrone.
+   Arance.




```

Tipi di frutta:

+   Mele. Ci sono diverse varietà di mele, le più diffuse sono:

    +   Annurca - originaria del Sud Italia, questa mela ha la buccia color rosso vinoso, un profumo molto intenso e la polpa croccante, leggermente acidula e succosa.
    +   Fuji - originaria del distretto di Morioka, Giappone. È la mela più coltivata al mondo. Mela dalla buccia rossastra con striature gialle e verdi
    +   Granny Smith - varietà originaria dell’Australia, è la mela verde per antonomasia.
    +   Golden Delicious - Mela dalla buccia gialla usata di solito per le torte alla mela.
    +   Renetta - Varietà dalla buccia gialla con macchie scure. Usata per lo strudel.
+   Pere.
    Le varietà di pere più diffuse sono:
    +   Williams -  La buccia delle pere Williams è verde chiaro, tendente al giallastro, mentre la polpa è di colore bianco avorio, molto zuccherina al palato.
        Si tratta, inoltre, di una varietà di pere molto delicata: per questo è meglio evitare che venga sottoposta a ripetuti sbalzi termici.
    +   Conference - La Conference ha la forma tipica della pera (in questo caso si dice piriforme) ma è leggermente affusolata, con una buccia verde-giallo bronzata e polpa color avorio, dolce, fondente e un tantino acidula
    +   Kaiser - Facilmente riconoscibile per via della sua forma regolare e della buccia uniformemente di colore marrone.
+   Arance.

Si noti che se si separano i vari elementi della lista con una riga bianca questi verranno inclusi in un paragrafo.

## Link

Sono possibili due stili per i link: i *link inline* (in linea) e i *reference link* (link per riferimento.


	Una [guida](https://daringfireball.net/) alla filosofia e alla sintassi originale del *markdown* è disponibile sul sito di uno dei suoi creatori, John Gruber.
	
Il risultato è:

Una [guida](https://daringfireball.net/) alla filosofia e alla sintassi originale del *markdown* è disponibile sul sito di uno dei suoi creatori, John Gruber. Una guida a una versione estesa del *markdown* che supporta note a piè pagina, codice LaTeX e molto altro è consultabile sul sito di [Pandoc][pm], un'applicazione da riga di comando che consente la conversione tra diversi tipi di testo formattato, tra cui da *markdown a HTML.

Il primo è un *link inline* (testo fra parentesi quadre seguito dal link fra parentesi tonde), il secondo un *link per riferimento* (testo sempre tra parentesi quadre seguito dal riferimento al link anch'esso tra parentesi quadre).
Il *riferimento*, in questo caso `pm`, deve essere presente in fondo al file:

	[pm]: http://pandoc.org/MANUAL.html

È anche possibile, con entrambi gli stili, includere il testo associato alla proprietà `title` del link (il testo mostrato al passaggio del mouse sul link), facendo seguire al link o al riferimento, il testo racchiuso tra virgolette.

	Una [guida](https://daringfireball.net/"Sito di John Gruber") alla filosofia e alla sintassi originale del *markdown* è disponibile sul sito di uno dei suoi creatori, John Gruber. Una guida a una versione estesa del *markdown* che supporta note a piè pagina, codice LaTeX e molto altro è consultabile sul sito di [Pandoc][pm], un'applicazione da riga di comando che consente la conversione tra diversi tipi di testo formattato, tra cui da *markdown a HTML.

Il risultato è:

Una [guida](https://daringfireball.net/"Sito di John Gruber") alla filosofia e alla sintassi originale del *markdown* è disponibile sul sito di uno dei suoi creatori, John Gruber. Una guida a una versione estesa del *markdown* che supporta note a piè pagina, codice LaTeX e molto altro è consultabile sul sito di [Pandoc][pm2], un'applicazione da riga di comando che consente la conversione tra diversi tipi di testo formattato, tra cui da *markdown a HTML.

Per i *link per riferimento* il testo del titolo va specificato quando si definisce il riferimento:

	[pm]: http://pandoc.org/MANUAL.html "Sito di Pandoc"

È anche possibile creare il link a un elemento con `id` nel documento.
Di default vengono associati degli `id` agli header mettendo il loro testo tutto in minuscolo, rimuovendo tutti i caratteri non alfanumerici e sostituendo gli spazi con un trattino.

	[Questo è un link](#intestazioni-header) alla sezione *Intestazioni(Header)* di questo documento.

[Questo è un link](#intestazioni-header) alla sezione *Intestazioni(Header)* di questo documento.

## Immagini

Per inserire un'immagine usare:

	![Logo di Firefox](https://upload.wikimedia.org/wikipedia/commons/thumb/7/76/Mozilla_Firefox_logo_2013.svg/100px-Mozilla_Firefox_logo_2013.svg.png)

![Logo di Firefox](https://upload.wikimedia.org/wikipedia/commons/thumb/7/76/Mozilla_Firefox_logo_2013.svg/100px-Mozilla_Firefox_logo_2013.svg.png)

Il testo racchiuso tra parentesi quadre è il testo alternativo per l'accessibilità.
come per i link, anche con le immagini si può usare la notazione per riferimento per indicare il link.

## Tabelle

Le tabelle si creano con il carattere pipe (|) e i trattini.
La pipe serve per separare le celle, il trattino definisce l'intestazione della tabella e la separa dal corpo.
Non è fondamentale sia tutto perfettamente allineato, però se è tutto allineato (usare sempre un font a larghezza fissa negli editor di testo) il file col sorgente markdown è più leggibile.


```
| Montagna | Continente | Altezza |
| -------- | ---------- | ------- |
| Everest | Asia | 8848 |
| Aconcagua | Sud America | 6962|
| Monte Denali (McKinley), | Nord America | 6194 |
| Kilimangiaro | Africa | 5895 |
| Massiccio Vinson | Antartide | 4897 |
| Puncak Jaya | Oceania | 4884 |
| Monte Bianco | Europa | 4810 |
```

Risultato:

| Montagna | Continente | Altezza |
| -------- | ---------- | ------- |
| Everest | Asia | 8848 |
| Aconcagua | Sud America | 6962|
| Monte Denali (McKinley), | Nord America | 6194 |
| Kilimangiaro | Africa | 5895 |
| Massiccio Vinson | Antartide | 4897 |
| Puncak Jaya | Oceania | 4884 |
| Monte Bianco | Europa | 4810 |


## Caratteri speciali

Ci sono alcuni caratteri speciali che devono essere *escaped* perché siano visualizzati.
Ovviamente sono tutti quelli inclusi nella sintassi del markdown: \\, \*, \~, \`, \+, \# e \-.
Alcuni solo se sono a inizio riga.


## Emoji
Al *markdown* di GitHub mancano molte utili estensioni di altri *markdown*, però in compenso supporta le *emoji*.

Tyger :tiger: ! Tyger :tiger: ! Burning bright
In the forests of the night:
What immortal hand or eye
Could frame thy fearful symmetry?



[as]: https://it.wikipedia.org/wiki/Aaron_Swartz
[jg]: https://daringfireball.net/
[emoji]: https://www.webpagefx.com/tools/emoji-cheat-sheet/
[pm]: http://pandoc.org/MANUAL.html 
[pm2]: http://pandoc.org/MANUAL.html "Sito di Pandoc"


