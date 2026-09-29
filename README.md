# Agenti AI per i contenuti

Il toolkit del webinar "Agenti AI per i contenuti" della Agents Week di Learnn: prompt, skill, procedure e una cartella di esempio per costruire un sistema che porta post LinkedIn e articoli del blog dai dati alla bozza. La revisione e la pubblicazione restano a te.

Funziona con Claude Code, Cowork, Codex, ChatGPT, Gemini e Copilot.

## Il webinar

- La registrazione: [youtube.com/watch?v=yWZa1UZzoBA](https://www.youtube.com/watch?v=yWZa1UZzoBA)
- Le slide: [canva.link/ubdcoa0gl7nciv6](https://canva.link/ubdcoa0gl7nciv6)
- Il foglio Google con prompt, skill e checklist, da copiare con File, Crea una copia: [Toolkit per creare contenuti con un agente AI](https://docs.google.com/spreadsheets/d/1rx9xRtLZRMupLdK975Hy7Pj5nZB_eaNzy07BjSeSvK8/edit)
- Tutte le sessioni dell'Agents Week: [learnn.com/agents-week/programma](https://learnn.com/agents-week/programma/)

Le domande arrivate in chat hanno le loro risposte in [procedure/11-domande-frequenti.md](procedure/11-domande-frequenti.md). Chi non ha uno storico di post o lavora su Instagram, YouTube o un blog parte da [procedure/10-senza-storico-e-altri-canali.md](procedure/10-senza-storico-e-altri-canali.md).

## A chi serve

A chi scrive con regolarità per lavoro (professionisti, freelance, founder, chi fa marketing in una piccola azienda) e vuole che l'AI scriva con la sua voce invece che con quella di tutti. Non serve saper programmare: bastano un account su uno degli strumenti e una cartella sul computer.

L'idea di fondo: i post scritti dall'AI si somigliano tutti perché il modello scrive con le regole generiche di internet. Il rimedio sono i tuoi testi con i loro numeri, una skill che li rilegge ogni settimana e le tue correzioni, che diventano regole. Un prompt più lungo cambia poco.

## Cosa trovi

| Cartella o file | Cosa contiene | Quando lo usi |
|---|---|---|
| `esempio/` | Una cartella di lavoro già pronta: archivio e regole di voce dai post LinkedIn pubblici di Luca Mastella, le domande dei due webinar, i risultati attesi | Il primo giorno, per provare il sistema in cinque minuti |
| `procedure/` | Undici procedure: nove in ordine, dalla cartella vuota alla routine del lunedì, più i casi senza storico o su altri canali e le domande del webinar | Quando costruisci la tua cartella |
| `toolkit/` | I materiali del webinar così come li abbiamo distribuiti: prompt per ogni fase, tre skill, checklist, file di istruzioni | Come riferimento oppure per copiare le skill in file visibili |
| `.claude/skills/` | Le tre skill (post-linkedin, articolo-blog, revisione-anti-ai) nel formato che Claude Code carica da solo | Ogni volta che scrivi |
| `CLAUDE.md`, `AGENTS.md` | Il file di istruzioni per l'agente, da compilare con i tuoi dati: Claude Code legge il primo, Codex il secondo | Il primo giorno |

## Scaricare il repository

- **Senza terminale**: pulsante verde Code, poi Download ZIP. Estrai lo zip dove vuoi.
- **Con git**: `git clone https://github.com/lucamastella/agenti-ai-contenuti.git`

Su Mac le cartelle che iniziano con un punto, come `.claude`, sono nascoste: nel Finder le mostri con Cmd + Maiusc + punto.

## Avvio rapido in cinque minuti

Il primo giro si fa sulla cartella `esempio/`, che ha già archivio, voce e domande. I quattro prompt della demo sono in `esempio/LEGGIMI.md`.

### Claude Code

1. Dal terminale: `cd agenti-ai-contenuti/esempio` e poi `claude`. Dall'app desktop: sezione Code, scegli la cartella `esempio`.
2. Claude Code legge da solo `CLAUDE.md` e carica le skill in `.claude/skills/`. Per controllare chiedi: "Quali skill hai a disposizione?"
3. Incolla il primo prompt di `esempio/LEGGIMI.md` e confronta il risultato con `esempio/risultati-pronti/`.

### Cowork

1. Nell'app desktop di Claude apri Cowork e scegli la cartella `esempio` come cartella di lavoro.
2. Come primo messaggio: "Leggi CLAUDE.md in questa cartella e seguilo per tutta la conversazione. Poi dimmi quali skill trovi in .claude/skills/ e aspetta la mia richiesta."
3. Prosegui con i quattro prompt di `esempio/LEGGIMI.md`.

### Codex

1. Apri la cartella `esempio` nell'app Codex, oppure lancia `codex` dal terminale dentro la cartella.
2. Codex legge da solo `AGENTS.md`, che gli dice di aprire `.claude/skills/<nome>/SKILL.md` quando nomini una skill.
3. Parti dal primo prompt di `esempio/LEGGIMI.md`.

### ChatGPT, Gemini e Copilot

Questi strumenti non lavorano su una cartella del computer, quindi i file si caricano a mano.

1. Crea un Progetto (ChatGPT), un Gem (Gemini) o un agente (Copilot).
2. Nelle istruzioni incolla `esempio/CLAUDE.md` e il testo della skill che ti serve: `toolkit/02-skill-post-linkedin.md` e `toolkit/04-skill-revisione-anti-ai.md` per la demo.
3. Carica tra i file `esempio/archivio/voce.md`, `esempio/archivio/post-indice.md` e `esempio/dati/domande-webinar-1.md`.
4. Usa i prompt di `esempio/LEGGIMI.md`. Quando l'agente dovrebbe salvare in `bozze/`, ti restituisce il testo in chat e lo salvi tu.

Il dettaglio per ogni strumento è in `procedure/09-altri-strumenti.md`.

## Dalla prova al tuo sistema

Dopo il giro sull'esempio costruisci la tua cartella seguendo le procedure in ordine. Puoi lavorare nella radice di questo repository, dove `CLAUDE.md`, `AGENTS.md` e le skill sono già al loro posto, oppure in una cartella nuova.

| Procedura | Cosa fai | Tempo |
|---|---|---|
| [01. Preparare la cartella](procedure/01-preparare-la-cartella.md) | Chiedi l'export a LinkedIn, crei le cartelle, compili il file di istruzioni | 10 minuti, più 24 ore di attesa per l'export |
| [02. Costruire l'archivio](procedure/02-costruire-archivio.md) | Dall'export all'indice dei post con i loro numeri | 30 minuti |
| [03. Le regole della voce](procedure/03-regole-della-voce.md) | Ricavi dai tuoi testi le regole del tuo modo di scrivere, con i dati | 30 minuti |
| [04. Creare la skill](procedure/04-creare-la-skill.md) | La skill che aggiorna l'archivio, propone il piano e scrive i post | 20 minuti |
| [05. Scrivere e correggere](procedure/05-scrivere-e-correggere.md) | Il primo post e le correzioni che diventano regole | Ogni post |
| [06. Dalle domande alle idee](procedure/06-dalle-domande-alle-idee.md) | Dalle domande di chi ti segue alle idee di post | 15 minuti |
| [07. L'articolo da un evento](procedure/07-articolo-da-un-evento.md) | Da una trascrizione a un articolo con FAQ e fonti | 30 minuti |
| [08. La routine settimanale](procedure/08-routine-settimanale.md) | Il piano del lunedì che arriva da solo | Dopo tre o quattro settimane |
| [09. Gli altri strumenti](procedure/09-altri-strumenti.md) | Dove mettere ogni pezzo su Claude, Codex, ChatGPT, Gemini e Copilot | Quando serve |
| [10. Senza storico e su altri canali](procedure/10-senza-storico-e-altri-canali.md) | Se non hai mai pubblicato oppure lavori su Instagram, Facebook, TikTok, YouTube e blog | Quando serve |
| [11. Le domande del webinar](procedure/11-domande-frequenti.md) | Le risposte alle domande più frequenti della chat | Quando serve |

Le cartelle `archivio/`, `dati/` e `bozze/` nella radice sono escluse da git (vedi `.gitignore`): i tuoi post e i tuoi dati restano sul tuo computer anche se pubblichi una copia del repository.

## Struttura delle cartelle

```
agenti-ai-contenuti/
├── README.md
├── CLAUDE.md                 istruzioni per Claude Code, da compilare
├── AGENTS.md                 le stesse istruzioni per Codex
├── .claude/skills/
│   ├── post-linkedin/SKILL.md
│   ├── articolo-blog/SKILL.md
│   └── revisione-anti-ai/SKILL.md
├── procedure/                01-09 in ordine, poi 10 e 11 quando servono
├── toolkit/                  00-06, i materiali originali del webinar
└── esempio/                  la cartella della demo, già compilata
    ├── LEGGIMI.md            la demo in quattro prompt
    ├── CLAUDE.md, AGENTS.md
    ├── .claude/skills/
    ├── archivio/             post-indice.md, voce.md
    ├── dati/                 domande-webinar-1.md, domande-webinar-2.md
    ├── risultati-pronti/     i risultati attesi di ogni passo
    └── bozze/                qui l'agente salva le bozze
```

Quando lavori sul tuo sistema, nella radice si aggiungono `archivio/`, `dati/` e `bozze/`.

## Il flusso, dal dato alla bozza

```
export LinkedIn -> archivio (indice, testi, metriche) -> voce.md -> skill post-linkedin
domande delle persone -> gruppi di temi -> idee -> scegli tu
idea scelta -> bozza -> revisione anti-AI -> correggi tu -> pubblichi tu
differenza fra bozza e pubblicato -> regola nuova in voce.md -> bozza migliore la settimana dopo
```

Le quattro fasi hanno quattro strumenti: i **dati** sono l'archivio e le fonti collegate, le **skill** scrivono con la tua voce, la **revisione** resta tua, la **routine** fa girare tutto ogni settimana senza un prompt. La differenza con una skill che scrive "alla tua maniera" sta nei dati: con l'archivio l'agente sa cosa hai già detto su un tema e cosa ne pensi, quindi due persone che usano la stessa skill ottengono due post diversi.

L'ultimo passaggio è quello che fa la differenza: la skill impara solo da quello che correggi. Dopo quattro o cinque settimane le correzioni diventano poche e puoi mettere tutto in una routine che il lunedì ti fa trovare il piano della settimana.

## Regole di sicurezza

- **Solo bozze.** L'agente prepara, tu pubblichi. Nessuna pubblicazione, nessun invio e nessuna programmazione senza il tuo sì: la regola è già scritta nel file di istruzioni e nelle skill.
- **Niente dati personali.** Nomi, email e numeri di telefono di clienti, colleghi o partecipanti restano fuori dalla cartella. Se lavori su domande o commenti, il prompt B1 chiede all'agente di toglierli: anonimizza anche il file di partenza se lo tieni.
- **Niente password, chiavi API o token**, né nei file della cartella né nei prompt. Gli accessi agli strumenti si concedono dalle impostazioni dei connettori.
- **Connettori con i permessi minimi.** Collega email, Drive o Notion solo quando una procedura li usa.
- **Ogni bozza passa dalla checklist** in `toolkit/05-checklist-revisione-bozza.md` prima di uscire.
- **Misura quanto viene letto**, non solo quanto produce l'agente.

## Uso

Uso libero per sperimentare, adattare e condividere. Se riprendi il metodo in un contenuto pubblico, cita il Team Learnn con il link alla guida.

## Per approfondire

- La guida completa, con i prompt spiegati passo per passo: [Post LinkedIn con l'AI: il processo che impara dal tuo stile](https://learnn.com/blog/post-linkedin-ai)
- I dieci agenti che usiamo in Learnn: [10 agenti AI che lavorano per te](https://teamlearnn.substack.com/p/10-agenti-ai)
- Il metodo di scrittura prima dell'AI: il corso [LinkedIn Content](https://learnn.com/corso/linkedin-content/) di Luca Mastella

## Crediti

A cura del Team Learnn per la Agents Week. L'archivio e le regole di voce in `esempio/` vengono dai post LinkedIn pubblici di Luca Mastella, founder di Learnn.
