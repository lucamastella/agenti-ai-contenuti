# 11. Le domande del webinar

Le risposte alle domande arrivate più spesso in chat durante il webinar del 29 settembre, con quello che Luca ha risposto in diretta e quello che non c'è stato tempo di dire. Le domande raggruppate per tema, senza nomi, sono in `esempio/dati/domande-webinar-2.md`.

## Le basi

### Che differenza c'è tra skill, agente e routine?

La **skill** è una procedura scritta: dice all'agente come si fa un lavoro (un post, un articolo, un'immagine). L'**agente** è il modello che lavora su una cartella, legge i tuoi strumenti e usa le skill. La **routine** è l'agente che parte da solo a un orario con un compito preciso: mette insieme più skill. La skill da sola ti restituisce un risultato che poi sistemi tu. Con la routine l'agente fa il lavoro fino alla bozza e tu approvi.

### Non è la stessa cosa di un Progetto con istruzioni e file?

Per un solo tipo di lavoro ci si avvicina. Le differenze si vedono quando cresci: più skill si usano insieme nella stessa conversazione (post, immagine e articolo in un colpo), la skill si aggiorna con le correzioni e la routine parte senza che tu apra la chat.

### Dove si creano le skill?

Nella chat del tuo strumento: scrivi "creami una skill per [lavoro]" e l'agente la crea. In Claude Code finisce in `.claude/skills/` dentro la cartella, nelle altre app di Claude tra le skill delle impostazioni, in ChatGPT e Gemini nelle istruzioni del progetto. Il metodo che consiglia Luca è nella procedura 04: invece di dettare le regole, dai all'agente i tuoi testi e gli chiedi di scoprirle.

### Le skill vanno richiamate ogni volta?

No. Sono sempre disponibili: se chiedi un post LinkedIn, l'agente cerca da solo la skill giusta. Nominarla con la barra (`/post-linkedin`) serve quando ne hai tante, per essere sicuro che usi quella. In Learnn ce ne sono 65 e ne usiamo davvero una quindicina.

### Una skill per tutto o una per ogni cosa?

Una per output. Il post e l'immagine sono due output diversi, quindi due skill: l'immagine serve anche per le slide, le email, le lezioni. La skill di un canale chiama quella delle immagini quando le serve. Le skill che servono a tutti i canali (immagini, revisione, pubblicazione) si scrivono una volta sola.

### Ho più clienti: una skill per cliente?

La procedura resta una, cambiano i dati. Tieni una cartella per cliente, con il suo file di istruzioni, il suo archivio e la sua `voce.md`. La skill `post-linkedin` resta la stessa. Quando lavori per quel cliente apri la sua cartella.

### Come aggiorno una skill?

Correggendo. Ogni volta che il risultato non va, dillo all'agente e chiudi con "aggiorna la skill con questa regola". Se vuoi aggiungere un formato visto da un altro creator, dai all'agente i suoi post e chiedi di aggiungere quel formato alla skill (procedura 10).

## I dati

### Non ho mai pubblicato: come faccio?

Parti da chi ti piace leggere: copi i post di un creator, ne prendi i formati e li applichi alla tua voce, ricavata da pochi testi tuoi. Il passo per passo è nella procedura 10.

### Funziona su Instagram, Facebook, TikTok, YouTube?

Sì. Cambia l'export dei dati (tabella nella procedura 10), il resto è identico. Per i video l'agente lavora sulla trascrizione.

### Come fa a leggere LinkedIn se non c'è un connettore?

Dal browser. Claude in Chrome usa il Chrome dove hai già fatto l'accesso, ChatGPT ha la modalità agente con un browser suo. L'agente apre la pagina "Tutte le attività", scorre e legge i numeri come li leggeresti tu. Se non ci riesce, ti chiede di incollare la pagina.

### E per pubblicare su LinkedIn?

Anche dal browser: l'agente apre LinkedIn, incolla il testo, carica l'immagine e programma il post. Lo fa solo dopo il tuo sì, perché il prompt della routine gli dice di fermarsi prima.

### Se riparto sempre dal passato, non evolvo mai?

L'archivio serve a sapere cosa hai già detto, per non contraddirti e non ripeterti. I post nuovi restano nuovi: nascono dalle domande di chi ti segue, dalla tua settimana e dal mercato (procedura 08). Se vuoi un post che non tiene conto dell'archivio, basta dirlo nel prompt.

## Le routine

### Se metto la modalità automatica, pubblica senza chiedermi niente?

La modalità automatica decide se l'agente ti chiede il permesso a ogni passo (leggere un file, aprire una pagina). Cosa fa alla fine lo decide il prompt. Nel prompt E1 il compito finisce con le bozze e l'agente si ferma: con la modalità automatica arriva fino alle bozze senza interromperti, poi aspetta il tuo sì. Se nel prompt scrivessi "pubblica", pubblicherebbe.

### Cosa succede se lascio una routine attiva e non la guardo?

Ripete gli stessi errori ogni settimana: se ha il permesso di pubblicare li pubblica. Per questo la pubblicazione resta tua e la routine si guarda ogni volta che parte: Luca la controlla a ogni esecuzione e corregge la skill quando qualcosa non va.

### Quanto consuma una routine? E la finestra di contesto?

Dipende da quanto legge. Tre accorgimenti tengono basso il consumo: l'archivio in tre livelli (l'agente legge l'indice e apre solo i testi che servono), un compito per routine invece di una routine che fa tutto, i sotto agenti per i lavori lunghi (partono con un contesto pulito e restituiscono solo il risultato).

### Le routine girano a computer spento?

Le routine locali dell'app desktop di Claude (anche da Cowork) girano solo con il computer acceso. Quelle che non hanno bisogno dei file del tuo computer si possono far girare nel cloud. Scegli un orario in cui il computer è acceso.

### Le routine si possono condividere con il team?

Il prompt della routine e le skill sì: in Learnn stanno in un repository su GitHub condiviso: ognuno le trova nella sua cartella. Un repository è una cartella condivisa con la storia di tutte le modifiche, come una cartella di Drive per il testo.

## Privacy e azienda

### Collegare Gmail o Drive è sicuro?

Collega solo quello che una procedura usa e con i permessi minimi. Controlla nelle impostazioni del piano se i tuoi dati si usano per l'addestramento: nei piani aziendali di solito sono esclusi. Luca tiene Gmail collegato e lo usa pochissimo. Se in una casella ci sono dati di clienti, non collegarla: esporta tu i messaggi che servono e togli nomi ed email.

### L'IT dell'azienda non mi attiva i connettori. Come faccio?

Di solito l'IT deve essere sicuro di due cose: che i dati non vengano usati per l'addestramento e che l'uso sia conforme alle regole interne. Porta la richiesta per un connettore alla volta, con il lavoro preciso che ti serve e i permessi minimi. Nel frattempo puoi lavorare con i file esportati a mano nella cartella.

### Cosa dice l'AI Act su un'automazione che pubblica post?

Un post che l'agente prepara e tu rivedi e pubblichi è un testo di cui rispondi tu. Per i contenuti generati con l'AI e pubblicati senza una revisione umana valgono obblighi di trasparenza. Per il caso della tua azienda chiedi a un legale: su Learnn c'è un corso sull'AI Act con l'avvocato Alessandro Vercellotti.

### LinkedIn penalizza i post scritti con l'AI?

Il problema che si vede nei numeri è la somiglianza: post con le stesse aperture e le stesse frasi di tutti. Tutto il metodo serve a evitarlo, con i tuoi dati, le tue regole e la revisione anti-AI.

## Gli strumenti

### Claude o Codex?

Al primo webinar il 60% delle persone in chat usava Claude. Luca usa Claude per quasi tutto e dice che Codex è migliorato molto. Il metodo di questo repository funziona su entrambi: `CLAUDE.md` per Claude Code, `AGENTS.md` per Codex. Luca consiglia l'app desktop rispetto al terminale.

### Cowork o Claude Code?

Cowork è più semplice da usare e lavora su una cartella come Claude Code. Claude Code dà più controllo sui file e sulle skill. Per questo metodo vanno bene tutti e due.

### Skill e routine sostituiscono n8n e Make?

In buona parte. Secondo Luca, n8n e Make servono soprattutto dove non c'è un connettore o una chiave API ufficiale per collegare un servizio. Il vantaggio della routine è che poi continui in chat con l'agente sul risultato.

### Posso usare Claude per il testo e un altro strumento per le immagini?

Sì. Claude non genera immagini: in Learnn le immagini sono schemi costruiti da una skill a partire da modelli grafici del brand. Per le immagini generate l'agente può scriverti il prompt da portare nello strumento che preferisci, oppure usarlo attraverso un connettore o una chiave API.

### Come ottengo un italiano scritto bene e non tradotto dall'inglese?

Con le regole. La skill `revisione-anti-ai` di questo repository toglie gli errori tipici dell'italiano scritto dall'AI: la virgola prima di "e", il trattino lungo, "non solo X ma anche Y", il gerundio a inizio frase. Aggiungi le tue ogni volta che correggi una bozza.

### Come scrivi i prompt?

Parlando, quasi sempre. Il prompt descrive cosa vuoi ottenere e perché, più che la lista dei passaggi: "voglio post che aumentino la reach del mio profilo e portino persone su Learnn" funziona meglio di "scrivi cinque post con queste virgole". Le regole di dettaglio stanno nella skill.

## Da dove iniziare se è tutto nuovo

Prima la cartella di esempio (cinque minuti, avvio rapido nel README), poi le procedure 01-05 in ordine. Per le basi ci sono i corsi di Learnn [AI da Zero](https://learnn.com/corso/ai-da-zero/) e [Prompt & Skill Engineering](https://learnn.com/corso/prompt-skill-engineering/) oltre alla registrazione del primo webinar dell'Agents Week con Filippo Greco.

Torna al [README](../README.md).
