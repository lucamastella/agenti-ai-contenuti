# Contenuti di [il tuo nome o la tua azienda]

Da compilare: sostituisci le parti tra parentesi quadre con i tuoi dati. Un esempio già compilato, con Luca Mastella come autore, è in `esempio/AGENTS.md`. Questo file ha lo stesso contenuto di `CLAUDE.md`: Codex legge questo, Claude Code l'altro. Se ne modifichi uno, copia la modifica anche nell'altro.

## Chi sono e per chi scrivo

[Due righe: cosa fai, chi ti legge, cosa vuoi che ottenga chi legge. Esempio: "Sono consulente marketing per negozi di arredamento. Scrivo su LinkedIn per i titolari che vogliono più clienti in negozio senza un'agenzia."]

## Come è organizzata la cartella

- `procedure/`: nove procedure in ordine, dalla cartella vuota alla routine settimanale, con i prompt da copiare. Se chi lavora non sa da dove partire, proponigli `procedure/01-preparare-la-cartella.md`.
- `toolkit/`: i materiali originali del webinar. Si leggono, non si modificano.
- `esempio/`: una cartella di prova già compilata. È un riferimento per la forma dei file: non mescolare i suoi contenuti con quelli di chi lavora.
- `.claude/skills/`: le skill post-linkedin, articolo-blog e revisione-anti-ai.
- `archivio/`: i contenuti già pubblicati (indice, testi, metriche, voce.md). Si legge prima l'indice, i testi solo quando servono. Se non esiste, si crea con la procedura 02.
- `dati/`: domande delle persone, trascrizioni, note, numeri. È la fonte delle idee.
- `bozze/`: tutto quello che scrivi finisce qui, con la data nel nome del file.

Le cartelle `archivio/`, `dati/` e `bozze/` sono escluse da git: restano sul computer di chi lavora.

## Le skill

Claude Code carica da solo le skill in `.claude/skills/`. Con gli altri strumenti, quando ti chiedo di usare una skill, apri `.claude/skills/<nome>/SKILL.md` e segui quelle istruzioni come se fossero parte di questo file.

## Regole che valgono sempre

1. Scrivi solo bozze. Non pubblicare, non inviare, non programmare niente senza il mio sì.
2. Non inventare numeri, nomi, citazioni o storie. Se ti manca un dato, chiedilo.
3. Per ogni affermazione indica da quale file o link viene.
4. Non modificare e non cancellare i file in `archivio/`, `dati/`, `toolkit/` ed `esempio/`: sono le fonti.
5. Ogni bozza passa dalla skill `revisione-anti-ai` prima di arrivare a me.
6. Quando ti correggo, chiedimi se la correzione va salvata come regola in una skill.

## Cosa non entra mai nella cartella

Password, chiavi di accesso, token, dati personali di clienti o colleghi, documenti riservati. Se ne trovi uno in un file, non copiarlo altrove e avvisami.
