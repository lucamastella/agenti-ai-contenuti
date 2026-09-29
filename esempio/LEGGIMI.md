# La cartella di esempio

Questa è la cartella usata nella demo del webinar "Agenti AI per i contenuti". Serve a provare il sistema in pochi minuti prima di costruire il tuo: l'archivio e la voce sono già pronti, quindi puoi passare subito dai dati alla bozza.

## Cosa c'è dentro

| File | Cosa contiene |
|---|---|
| `CLAUDE.md`, `AGENTS.md` | Le istruzioni per l'agente, compilate con i dati di Luca Mastella. Claude Code legge il primo, Codex il secondo |
| `archivio/post-indice.md` | 60 post LinkedIn pubblici di Luca con data, temi, prima riga e link |
| `archivio/voce.md` | Le regole del suo modo di scrivere, ognuna con il dato che la sostiene |
| `dati/domande-webinar-1.md` | Circa 230 domande arrivate in chat al primo webinar dell'Agents Week, raggruppate per tema e senza nomi |
| `dati/domande-webinar-2.md` | Circa 150 domande arrivate in chat al secondo webinar, su altri canali, skill, routine e privacy, raggruppate per tema e senza nomi |
| `.claude/skills/` | Le tre skill: post-linkedin, articolo-blog, revisione-anti-ai |
| `risultati-pronti/` | Quello che l'agente ha prodotto durante la demo, passo per passo |
| `bozze/` | Vuota: qui l'agente salva quello che scrive |

## Come aprirla

- **Claude Code**: dal terminale entra nella cartella (`cd esempio`) e lancia `claude`, oppure scegli la cartella dalla sezione Code dell'app desktop.
- **Cowork**: nell'app desktop di Claude scegli `esempio` come cartella di lavoro e come primo messaggio scrivi "Leggi CLAUDE.md e seguilo".
- **Codex**: apri la cartella nell'app oppure lancia `codex` dal terminale dentro la cartella. Legge da solo `AGENTS.md`.
- **ChatGPT, Gemini, Copilot**: crea un progetto, incolla `CLAUDE.md` nelle istruzioni e carica i file di `archivio/` e `dati/`. Il passo per passo è in `procedure/09-altri-strumenti.md`.

## La demo in quattro prompt

Copiali uno alla volta. Dopo ogni passo confronta quello che ottieni con il file in `risultati-pronti/`: non sarà identico, ma deve avere la stessa forma e gli stessi numeri.

**1. Dalle domande ai gruppi**

```
Leggi dati/domande-webinar-1.md e raggruppa le domande in cinque temi, con quante persone chiedono ciascuno e una frase che le rappresenta.
```

Risultato atteso: `risultati-pronti/01-gruppi-di-domande.md`.

**2. Dai gruppi alle idee**

```
Dai tre temi più chiesti proponimi cinque idee di post LinkedIn. Per ognuna prima riga, formato e il post dell'archivio a cui si collega.
```

Risultato atteso: `risultati-pronti/02-cinque-idee.md`.

**3. Dall'idea al post**

```
Scrivi il post dell'idea 1 con la skill post-linkedin, poi passalo alla skill revisione-anti-ai. Salva in bozze/.
```

Risultato atteso: `risultati-pronti/03-post-bozza.md`.

**4. Dalla correzione alla regola**

Correggi una frase della bozza come la scriveresti tu, poi:

```
Questa correzione aggiungila come regola alla skill post-linkedin.
```

Apri `.claude/skills/post-linkedin/SKILL.md`: in fondo, nella sezione "Regole nate dalle correzioni", trovi la regola nuova con la data. È il meccanismo che fa migliorare il sistema settimana dopo settimana.

## Se l'agente è lento

Apri il risultato pronto del passo e prosegui dal passo dopo: i prompt funzionano anche partendo dai file in `risultati-pronti/`.

## Dopo la prova

Per costruire la tua cartella con i tuoi post segui le procedure in `procedure/`, dalla 01 alla 09. Questa cartella resta come riferimento: quando non sai che forma deve avere un file, guarda qui.
