# 04. Creare la skill che scrive i post

## A cosa serve

Una skill è un file di istruzioni che l'agente rilegge ogni volta che gli chiedi quel lavoro, insieme ai file collegati. La differenza con un prompt salvato è che la skill cresce: la aggiorni tu o la aggiorna l'agente quando glielo chiedi. Questa aggiorna l'archivio, impara dalle tue correzioni, propone il piano della settimana e scrive post e immagini.

## Cosa prepari

- `archivio/post-indice.md`, `archivio/post-testi.md` e `archivio/voce.md`, dalle procedure 02 e 03.
- La cartella `bozze/` vuota.

## Passi

Hai tre strade, che portano allo stesso file. Quella che usa Luca è la prima.

**Strada 0: lasci che l'agente scopra le regole (consigliata).**

Se detti tu le regole ("fai A, B, C"), la skill sa solo quello che hai già notato. Se le fai scoprire all'agente dai tuoi post, trova anche le abitudini che non vedi: le virgolette sulle parole da evidenziare, l'emoji nella prima riga, le aperture che rendono di più.

1. Lancia il prompt A5 con i tuoi post (l'archivio della procedura 02, oppure la pagina "Tutte le attività" copiata).
2. Chiedi: "Cosa hai imparato? Quali formati hai trovato nei miei post?". Leggi la risposta e correggi: "questo formato non lo uso più", "questo è il mio preferito, partiamo da qui".
3. Chiedi un post di prova su un tema che conosci bene. Riscrivilo come lo scriveresti tu e ridaglielo: "Ecco la mia versione, aggiorna la skill con quello che hai cambiato".
4. Ripeti il passo 3 due o tre volte. Poi completa la skill con i cinque punti del prompt A4 (archivio, correzioni, piano, rilettura, scrittura).

Se non hai uno storico, parti dai post di chi ti piace leggere: procedura 10.

**Strada A: l'agente crea la skill dai tuoi file.**

1. Lancia il prompt A4 nella cartella di lavoro.
2. Leggi la skill che ti mostra e l'esempio di piano per la settimana.
3. Controlla dove l'ha salvata: in Claude Code deve stare in `.claude/skills/post-linkedin/SKILL.md`.

**Strada B: adatti la skill pronta.**

1. Apri `.claude/skills/post-linkedin/SKILL.md` (lo stesso testo è in `toolkit/02-skill-post-linkedin.md`).
2. Sostituisci le parti tra parentesi quadre: il tuo nome, chi ti legge, un esempio di prima riga preso da un tuo post, come chiudi, le parole che non usi mai (le trovi in voce.md).
3. Cancella gli esempi che non ti somigliano.

In entrambi i casi, lascia vuota la sezione finale "Regole nate dalle correzioni": la riempirà l'agente nella procedura 05.

Dove va la skill negli altri strumenti:

| Strumento | Dove si mette |
|---|---|
| Claude Code | `.claude/skills/post-linkedin/SKILL.md` nella cartella di lavoro, la carica da solo |
| Cowork e app di Claude | tra le skill nelle impostazioni di Claude, oppure si chiede all'agente di leggere il file SKILL.md |
| Codex | resta in `.claude/skills/`: `AGENTS.md` gli dice di aprirla quando la nomini |
| ChatGPT, Gemini, Copilot | il testo si incolla nelle istruzioni del progetto, del Gem o dell'agente |

## Prompt da copiare

**A5. La skill scoperta dai tuoi post**

```
Nella cartella archivio ci sono i miei post LinkedIn con i loro numeri (impression, reazioni, commenti).

Creami una skill che si chiama "post-linkedin" per scrivere post come i miei. Non ti do regole: ricavale tu dai post. Guarda come apro, quanto sono lunghi i paragrafi, che parole uso e quali evito, come chiudo, come uso punteggiatura, emoji ed elenchi. Dividi i post in formati (per esempio opinione con un dato, storia, lista di lezioni) e per ogni formato indica i tre post che lo rappresentano meglio e come hanno funzionato rispetto alla mediana.

Quando hai finito non salvare ancora niente: raccontami cosa hai imparato, quali formati hai trovato e quali regole vuoi scrivere nella skill. Le decidiamo insieme.
```

**A4. Dalla voce alla skill**

```
Crea una skill che si chiama "post-linkedin". Usa come materiale post-indice.md, post-testi.md e voce.md.

Ogni volta che la uso deve fare queste cose, in quest'ordine.

1. Aggiornare l'archivio: aggiungere i post nuovi e aggiornare le metriche di quelli delle ultime quattro settimane, che continuano a crescere. Se non può aprire LinkedIn da sola, mi chiede di incollarle la pagina "Tutte le attività".
2. Imparare dalle mie modifiche: salva ogni bozza che mi propone in bozze.md con la data. Quando trova il post pubblicato, confronta la sua bozza con la mia versione. Ogni correzione che si ripete in almeno due post (una parola che tolgo sempre, un'apertura che accorcio, un finale che taglio) diventa una regola nuova in voce.md, con data ed esempio.
3. Proporre il piano editoriale della settimana: cinque post, uno per giorno lavorativo. Due ripresi dall'archivio (post sopra la mediana pubblicati più di sei mesi fa, da aggiornare o da combinare con altri sullo stesso tema) e tre nuovi, sui temi che funzionano. Per ogni post: tema, tre aperture diverse, formato e il motivo della proposta, con il numero dell'archivio che la giustifica.
4. Prima di scrivere su un tema, rileggere tutti i post che ho già pubblicato su quel tema, per non contraddirmi e per linkare quelli giusti.
5. Scrivere i post che scelgo seguendo voce.md e per ognuno descrivere l'immagine da abbinare: cosa mostra, il testo esatto (massimo 25 parole), formato 4:5.

Regole: mai inventare numeri, storie o citazioni, se serve un dato che non hai me lo chiedi. Le regole di voce.md vincono sulle regole generiche di scrittura.

Quando hai finito mostrami la skill e un esempio di piano per questa settimana.
```

## Cosa ottieni

La skill `post-linkedin`, che l'agente usa ogni volta che chiedi un post, un piano editoriale o la revisione di una bozza per LinkedIn. Insieme alla skill ricevi un primo piano per la settimana, con i numeri dell'archivio che giustificano ogni proposta.

Le altre due skill del repository funzionano allo stesso modo: `articolo-blog` (procedura 07) e `revisione-anti-ai` (procedura 05).

## Errori comuni

- **Una skill senza i file collegati.** Se l'agente non trova voce.md e l'indice, scrive con le regole generiche e il risultato torna quello di tutti. Controlla che i percorsi nella skill corrispondano alle tue cartelle.
- **Togliere il punto 4.** Rileggere i post già pubblicati sullo stesso tema è il passaggio che si nota meno e protegge di più: con qualche centinaio di post alle spalle capita di dire una cosa e, due anni dopo, il contrario.
- **Togliere la regola sui numeri inventati.** Senza, l'agente riempie i vuoti con cifre plausibili.
- **Dettare le regole invece di farle scoprire.** La skill resta ferma a quello che sapevi già di te.
- **Mettere tutto in una skill sola.** Testo e immagini sono due output diversi: una skill per ognuno. Quella del post chiama quella delle immagini quando serve.
- **Aspettarsi post perfetti dal primo giorno.** La skill migliora con le correzioni della procedura 05.

Prossimo passo: [05. Scrivere e correggere](05-scrivere-e-correggere.md).
