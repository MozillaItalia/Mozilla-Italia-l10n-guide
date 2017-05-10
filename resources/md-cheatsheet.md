# Markdown Cheatsheet

Questo file è una serie di appunti tratti da un file personale che uso come bignamino per il *markdown*.
Mi riprometto di sistemare lo stile in modo sia conforme a quello utilizzato per la guida.


Il *markdown* è uno pseudo-linguaggio creato da [John Gruber][jg] e [Aaron Swartz][as] con lo scopo di avere dei file di testo leggibili e da cui è possibile generare una versione HTML riducendo al minimo la sintassi e utilizzando regole che si sono diffuse nel tempo nei newsgroup e in altri ambienti dove il *plain text* è la regola.

Non avendo una vera standardizzazione come l’HTML, il *markdown* ha visto nel tempo la nascita di diverse estensioni in specifiche piattaforme, senza che però queste estensioni siano adottati da tutti.

Il *markdown che si usa su *GitHub* è abbastanza minimale, ad esempio non consente le note a piè pagina, l’inserimento di codice LaTeX, inserimento di testo apice o pedice e molte altre estensioni che sono supportate in altre estensioni.

La differenza principale rispetto ad altri *markdown* è la gestione dei paragrafi e degli a capo.


La versione del *markdown* di GitHub infatti, raggruppa in un'unico paragrafo tutte le righe che non sono separate da una riga vuota.
Per andare a capo, sempre rimanendo nello stesso paragrafo, è necessario utilizzare il carattere `\` o inserire uno spazio a fine riga.
Questo permette di evitare righe lunghissime e rende più leggibile il sorgente perché non bisogna fare lo scroll orizzontale (sempre si decida di wrappare il testo).

Di seguito degli esempi pratici: in ognuno verrà riportato prima il codice markdown e poi l'output HTML che il codice genera.


## Paragrafi (specifica GitHub)

	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria:* non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Come mandare a capo i due periodi:

	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi. 
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.
Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi. 
*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Metodo alternativo per andare a capo tra i due periodi:

	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.\
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.\
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Separare i due periodi in due paragrafi:

	Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
	
	*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.

*Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

## Citazioni

Si quota come nelle email in puro testo, col carattere maggiore:

	>   Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
	>   *Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

>   Era una luminosa e fredda giornata d'aprile, e gli orologi battevano tredici colpi.
>   *Winston Smith*, tentando di evitare le terribili raffiche di vento col mento affondato nel petto, scivolò in fretta dietro le porte di vetro degli Appartamenti *Vittoria*: non così in fretta, tuttavia, da impedire che una folata di polvere sabbiosa entrasse con lui.

Gli spazi dopo il maggiore non vengono considerati, però usare la regola del 4, cioé allineare tutto con 4 caratteri iniziali (il carattere sintattico e 3 spazi rende il codice più leggibile e semplifica con quotazioni e liste annidate).

## Enfasi e grassetto

Il carattere \* viene usato per dare enfasi, un solo asterisco per l'enfasi semplice (di solito resa in corsivo) e due \* per un'enfasi maggiore (di solito grassetto).

	*Corsivo,*, **grassetto** e ***corsivo più grassetto.**

*Corsivo,*, **grassetto** e ***corsivo più grassetto.**

Una brutta cosa del *markdown* di GitHub è quella che non interpreta correttamente gli asterischi se compresi fra caratteri alfanumerici o punteggiatura.
In particolare, non si può evidenziare una parte della parola e bisogna mettere enfasi anche alla punteggiatura, contrariamente al *markdown* di *Pandoc*.

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

## Link













[as]: https://it.wikipedia.org/wiki/Aaron_Swartz
[jg]: https://daringfireball.net/

