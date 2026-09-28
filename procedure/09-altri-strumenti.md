# 09. Usare il sistema con gli altri strumenti

## A cosa serve

Il metodo è lo stesso su tutti gli strumenti: una cartella o un progetto con le fonti, un file di istruzioni, le skill e le correzioni che diventano regole. Cambiano i nomi delle voci e il modo in cui l'agente legge i file. Questa procedura dice dove mettere ogni pezzo su Claude, Codex, ChatGPT, Gemini e Copilot.

## Cosa prepari

- I file della tua cartella di lavoro (archivio, dati, file di istruzioni) oppure quelli di `esempio/`.
- Le skill in file visibili: `toolkit/02-skill-post-linkedin.md`, `toolkit/03-skill-articolo-blog.md`, `toolkit/04-skill-revisione-anti-ai.md`. Sono identiche a quelle in `.claude/skills/`.

## Come si chiamano le cose

| Cosa ti serve | Claude | ChatGPT | Gemini | Copilot |
|---|---|---|---|---|
| Collegare le app | Connettori | App collegate | App Google | Dati di Microsoft 365 |
| Istruzioni salvate | Skill e progetti | Progetti e GPT | Gem | Agenti |
| Lavoro che parte da solo | Routine | Attività pianificate | Azioni programmate | Prompt programmati |
| Agente sui file | Claude Code e Cowork | Codex | Strumenti per sviluppatori | Agent Builder |

## Passi, strumento per strumento

**Claude Code.** Apri la cartella di lavoro (dal terminale con `claude`, oppure dalla sezione Code dell'app desktop). Legge da solo `CLAUDE.md` e carica le skill in `.claude/skills/`. Non serve altro.

**Cowork.** Nell'app desktop di Claude scegli la cartella di lavoro. Come primo messaggio chiedi di leggere il file di istruzioni (prompt qui sotto). Le skill puoi anche installarle tra le skill di Claude, dalle impostazioni: così valgono in ogni conversazione.

**Progetto di Claude.** Senza cartella: incolla `CLAUDE.md` nelle istruzioni del progetto, carica tra i file del progetto archivio e dati, attiva le skill o incolla il loro testo nelle istruzioni.

**Codex.** Apri la cartella nell'app oppure lancia `codex` dal terminale dentro la cartella. Legge da solo `AGENTS.md`, che gli dice di aprire `.claude/skills/<nome>/SKILL.md` quando nomini una skill. Tieni `AGENTS.md` e `CLAUDE.md` uguali se usi entrambi gli strumenti sulla stessa cartella.

**ChatGPT.** Crea un Progetto. Nelle istruzioni del progetto incolla il file di istruzioni e il testo della skill che usi di più. Carica tra i file del progetto `voce.md`, `post-indice.md`, `post-testi.md` e i file di `dati/`. Quando l'agente dovrebbe salvare una bozza in `bozze/`, ti restituisce il testo in chat e lo salvi tu.

**Gemini.** Crea un Gem: nelle istruzioni il file di istruzioni e la skill, tra i file di conoscenza archivio e dati.

**Copilot.** Crea un agente: nelle istruzioni il file di istruzioni e la skill, come fonti i file di archivio e dati.

Se lo strumento non legge i file di una cartella, incolla il contenuto dei file nella conversazione o caricali in un progetto: i prompt funzionano lo stesso.

## Prompt da copiare

Per Cowork e per ogni strumento che non legge da solo il file di istruzioni:

```
Leggi CLAUDE.md in questa cartella e seguilo per tutta la conversazione. Poi dimmi quali skill trovi in .claude/skills/ e aspetta la mia richiesta.
```

Per usare una skill in uno strumento che non la carica da solo:

```
Apri .claude/skills/post-linkedin/SKILL.md e segui quelle istruzioni per questa richiesta: [la richiesta].
```

Nei progetti senza cartella, dove il testo della skill è già nelle istruzioni, basta nominarla: "Con la skill post-linkedin scrivi...".

## Cosa ottieni

Lo stesso sistema su qualsiasi strumento: le fonti, le regole e le skill sono file di testo, quindi li porti da uno strumento all'altro senza riscriverli. Se cambi strumento, cambi solo dove li metti.

## Errori comuni

- **Riscrivere le skill da zero per ogni strumento.** Il testo è lo stesso: cambia solo dove lo incolli.
- **Correzioni salvate in un posto solo.** Se usi due strumenti, le regole nuove vanno nel file della cartella, non nella memoria di uno dei due: così le leggono entrambi.
- **Dimenticare di ricaricare i file aggiornati.** Nei progetti di ChatGPT, Gemini e Copilot i file caricati non si aggiornano da soli: dopo una settimana di correzioni ricarica `voce.md`.
- **Aspettarsi le stesse funzioni ovunque.** Le routine e l'accesso al browser cambiano da strumento a strumento: dove mancano, i passi si fanno a mano e il metodo regge lo stesso.

Torna al [README](../README.md).
