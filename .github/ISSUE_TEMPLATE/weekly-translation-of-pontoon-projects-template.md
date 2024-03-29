---
name: Weekly Translation of Pontoon Projects template
about: Usare questo modello per le stringhe settimanali di Pontoon
title: 'Weekly Translation of Pontoon Projects (Week #/AAAA)'
labels: Italian, for new volunteers, help wanted, pontoon, translation needed!
assignees: ''

---

# Stringhe della settimana

<!---
Usare il carattere (emoji):
- ✅ per marcare i primi tre campi ("QA richiesto", "In revisione" e "Tradotto")
- ➡️ #issue per indicare che un determinato progetto è stato spostato in un altro issue

Per aggiungere una nuova riga usare questo codice:
| [](): []() | #stringhe |  |  |  |
--->

| Nome progetto (e identificativo stringhe) | Numero stringhe | Traduttore `@username` | QA richiesto |  In revisione | Approvato |
| :-- | :-: | :-- | :-: | :-: | :-: |
| [Nome progetto](link): [Eventuale suddivisione per stringhe/file](link) | #stringhe |  |  |  |  |

❗️  La lista delle stringhe da tradurre viene aggiornata più volte nell'arco della settimana

❕ I seguenti progetti non sono gestiti dal team L10n. **NON** includerli nella lista delle stringhe:
- Seamonkey (responsabile: Iacopo Benesperi)
- SUMO (responsabile: Team SuMo)
- Firefox (sola lettura)

## Informazioni sul progetto
Questo issue serve a gestire le traduzioni dei siti Mozilla sulla piattaforma [Pontoon](https://pontoon.mozilla.org/it/).

Ogni settimana uscirà un nuovo issue con una lista dei progetti che contengono stringhe mancanti. Puoi sempre trovare lo issue della settimana corrente sulla [bacheca del progetto](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/projects/5).
Chi vuole farsi avanti, a seconda della propria disponibilità, si "prenoterà" per le stringhe.
Questo per organizzare meglio l'attività di traduzione ed evitare che più persone lavorino sulle stesse stringhe.

## Istruzioni
#### Prima di iniziare:
* [Registrati](https://accounts.firefox.com/oauth/signin?response_type=code&scope=profile%3Auid%20profile%3Aemail%20profile%3Adisplay_name%20profile%3Auid%20profile%3Adisplay_name%20profile%3Aemail&state=yrvTUh3o4F4c&redirect_uri=https%3A%2F%2Fpontoon.mozilla.org%2Faccounts%2Ffxa%2Flogin%2Fcallback%2F&client_id=76ab66239b5585ad) sulla piattaforma di traduzione Pontoon
  - (Facoltativo) Installa i componenti aggiuntivi [Pontoon Add-on](https://addons.mozilla.org/it/firefox/addon/pontoon-tools/) per ricevere le notifiche sulle stringhe mancanti in tempo reale (più altre chicche) e [MozIta L10n Add-on](https://addons.mozilla.org/it/firefox/addon/mozita-l10n/) per accedere più facilmente ai caratteri speciali come `’ “ ” È` ecc.
* **Leggi i capitoli della guida**, se lo desideri, lascia un feedback nel relativo issue:
  - Capitolo 1 – [Buone norme di traduzione tecnica](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/1-Buone_norme_di_traduzione.md) Feedback: issue #225 
  - Capitolo 2 – [Linee guida di Mozilla Italia](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/2-Linee_guida_di_Mozilla_Italia.md) Feedback: issue #138
  - Capitolo 3 – [Flusso di lavoro](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/3-Flusso_di_lavoro.md) Feedback: issue #24 
  - Capitolo 4 – [Tipi di file](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/4-Tipi_di_file.md) Feedback: issue #31 
  - Capitolo 5  – [Risorse esterne](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/5-Risorse_esterne.md) Feedback: issue #36

#### Prendere in carico il progetto:
* Lascia un messaggio nella sezione Commenti, scrivendo di quale progetto vuoi occuparti (importante per avvisare gli altri che ci stai lavorando tu). Scrivi anche il tuo nome utente accanto al nome del progetto sulla lista qui in alto (usa l'icona `…` nell'angolo in alto a destra per modificare il testo.)
  - Se non sei ancora tra i [Collaborators](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/settings/collaboration) non hai i permessi per modificare la lista. Scrivi solo nei commenti, qualcuno con i permessi aggiungerà il tuo nome alla lista.
* Attieniti alle istruzioni del [capitolo 3](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/3-Flusso_di_lavoro.md) e del [capitolo 4](https://github.com/MozillaItalia/Mozilla-Italia-l10n-guide/blob/master/it/4-Tipi_di_file.md).
* Per qualsiasi problema o domanda scrivi pure in questo issue.
* Quando la tua traduzione è pronta, lascia un commento nello issue per dare l'OK al QA.
* Rimani a disposizione per il QA, ti verrà chiesto se vuoi confermare le modifiche del revisore o proporre un'alternativa.
* e buona traduzione! 🎊 

##### Alcune norme comportamentali da seguire
1. Non usare lo issue per discussioni fuori tema, conversazioni personali, battute umoristiche ecc. (per cui sono disponibili appositi gruppi Telegram e sezioni del forum).
2. Non usare la `@menzione` quando non strettamente necessario, in particolare non menzionare uno o tutti i revisori ogni volta che chiedi il QA (a meno che non desideri il parere di quel revisore specifico).
3. Puoi prenotarti per i progetti a seconda della tua disponibilità, ma ricorda di lasciare anche agli altri volontari occasione di partecipare.
4. Puoi (anzi sei incoraggiato a) aggiornare la lista di stringhe presenti nello issue se noti che sono apparse nuove stringhe su Pontoon e desidera tradurle.
5. Puoi prendere anche solo una parte delle stringhe di un progetto, secondo la tua disponibilità. Basta che inserisci una casella di spunta con rientro `<spazio><spazio>- [ ]` nella riga sotto il progetto in questione, scrivendo accanto il tuo nome e il numero di stringhe che prendi.

## Link Utili
* Server di test -- Per vedere dove andranno a finire le tue traduzioni
  - per le singole pagine di [mozilla.org](https://l10n.mozilla-community.org/langchecker/?action=listpages) 
  - per [AMO](https://addons-dev.allizom.org/it/)
  - per [MDN](https://developer.allizom.org/it/)
  - per [Common Voice](https://voice.allizom.org/it)
  - per [Thunderbird.net](https://www.thunderbird.net/it/) *sito produzione
  - per [Firefox Monitor](https://fx-breach-alerts.herokuapp.com/) + [Modelli email](https://fx-breach-alerts.herokuapp.com/email-l10n)
  - per [Mozilla Donate website](https://donate-wagtail.mofostaging.net/it/) + [Istruzioni test pagamenti](https://groups.google.com/forum/#!topic/mozilla.dev.l10n.web/aEWu_hSnYMU)
* Motori di ricerca per le stringhe
  - [Pontoon: tutti i progetti](https://pontoon.mozilla.org/it/all-projects/all-resources/?utm_source=pontoon-addon&string=66616) -- Cerca simultaneamente tra tutti i progetti di Pontoon in italiano.
  - [Transvision](https://transvision.mozfr.org/) -- Motore di ricerca esterno per le stringhe Mozilla, complementare a Pontoon.
  - [Microsoft Language Portal](https://www.microsoft.com/en-us/language/Search?langID=408&Source=true&productid=0) -- Glossario Microsoft.
* [Transvision Access Key](https://transvision.mozfr.org/accesskeys/) -- Rileva eventuali errori nelle access key (da controllare ogni volta che si traduce una stringa contenente access key)
* [Sezione Localization in Discourse](https://discourse.mozilla.org/c/l10n/547) -- Sezione dedicata alla localizzazione dei prodotti Mozilla.
* [#l10n-community in Matrix](https://chat.mozilla.org/#/room/#l10n-community:mozilla.org) -- Sezione dedicata alla comunità di localizzatori Mozilla su Matrix.
