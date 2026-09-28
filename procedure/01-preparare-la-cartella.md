# 01. Preparare la cartella di lavoro

## A cosa serve

L'agente lavora bene quando sa dove trovare le fonti, dove salvare quello che scrive e quali regole rispettare. La cartella di lavoro gli dà tutte e tre le cose. Il primo giorno serve anche a chiedere a LinkedIn l'export dei tuoi dati, l'unico passo che non dipende da te.

## Cosa prepari

- Un account sullo strumento che userai: Claude (Claude Code o Cowork), Codex, ChatGPT, Gemini o Copilot.
- Una cartella nuova sul computer, per esempio `contenuti`. Puoi usare anche la radice di questo repository, che ha già il file di istruzioni e le skill.
- Dieci minuti.

## Passi

1. **Chiedi l'export a LinkedIn.** Impostazioni e privacy, Privacy dei dati, Ottieni una copia dei tuoi dati (in inglese Download my data). Scegli l'archivio completo, non quello veloce. Arriva per email in circa 24 ore e ti servirà nella procedura 02.
2. **Crea le tre cartelle** dentro la cartella di lavoro: `archivio/`, `dati/`, `bozze/`.
3. **Metti il file di istruzioni.** Copia `CLAUDE.md` dalla radice di questo repository (per Codex `AGENTS.md`, che ha lo stesso contenuto) e compila le parti tra parentesi quadre: chi sei, chi ti legge, cosa vuoi che ottenga. Il testo di partenza è anche qui sotto.
4. **Copia le skill.** Porta nella tua cartella la cartella `.claude/skills/` di questo repository. Su Mac le cartelle che iniziano con un punto sono nascoste: nel Finder le mostri con Cmd + Maiusc + punto. Le stesse skill sono in `toolkit/02`, `03` e `04`, in file visibili.
5. **Apri la cartella nello strumento** e controlla con il secondo prompt qui sotto che l'agente abbia letto le istruzioni.

Con ChatGPT, Gemini e Copilot la cartella non si apre: il file di istruzioni va incollato nelle istruzioni del progetto. Il dettaglio è nella procedura 09.

## Prompt da copiare

Il file di istruzioni, da `toolkit/06-file-istruzioni-cartella.md`. Salvalo come `CLAUDE.md` (Claude Code) o `AGENTS.md` (Codex) e compila le parentesi quadre.

```
# Contenuti di [il tuo nome o la tua azienda]

## Chi sono e per chi scrivo

[Due righe: cosa fai, chi ti legge, cosa vuoi che ottenga chi legge.]

## Come è organizzata la cartella

- `archivio/`: i contenuti già pubblicati (indice, testi, metriche, voce.md). Si legge prima l'indice, i testi solo quando servono.
- `dati/`: domande delle persone, trascrizioni, note, numeri. È la fonte delle idee.
- `skills/`: le procedure per ogni formato (post LinkedIn, articolo, revisione).
- `bozze/`: tutto quello che scrivi finisce qui, con la data nel nome del file.

## Regole che valgono sempre

1. Scrivi solo bozze. Non pubblicare, non inviare, non programmare niente senza il mio sì.
2. Non inventare numeri, nomi, citazioni o storie. Se ti manca un dato, chiedilo.
3. Per ogni affermazione indica da quale file o link viene.
4. Non modificare e non cancellare i file in `archivio/` e `dati/`: sono le fonti.
5. Ogni bozza passa dalla skill `revisione-anti-ai` prima di arrivare a me.
6. Quando ti correggo, chiedimi se la correzione va salvata come regola in una skill.

## Cosa non entra mai nella cartella

Password, chiavi di accesso, dati personali di clienti o colleghi, documenti riservati.
```

Se usi Claude Code, sostituisci la riga su `skills/` con `.claude/skills/`, dove Claude Code cerca le skill.

Il controllo, da incollare appena apri la cartella:

```
Leggi il file di istruzioni di questa cartella. Dimmi in cinque righe chi sono, per chi scrivo, dove salverai le bozze, quali skill hai a disposizione e quali regole seguirai.
```

## Cosa ottieni

Una cartella con tre sottocartelle, il file di istruzioni compilato e le tre skill. L'agente che la apre sa chi sei, dove guardare e cosa non deve fare. Fra 24 ore arriva l'export di LinkedIn.

## Errori comuni

- **Aprire come cartella di lavoro tutto il Desktop o la cartella Documenti.** L'agente legge più del necessario, ci mette di più e vede file che non lo riguardano. Una cartella dedicata, con dentro solo quello che serve.
- **Lasciare il file di istruzioni generico.** Le due righe su chi sei e chi ti legge cambiano ogni bozza: scrivile anche se ti sembrano ovvie.
- **Scegliere l'export veloce di LinkedIn.** Serve l'archivio completo, che contiene il file dei post.
- **Salvare password o chiavi in un file della cartella** per comodità. L'agente le legge insieme a tutto il resto.

Prossimo passo: [02. Costruire l'archivio](02-costruire-archivio.md).
