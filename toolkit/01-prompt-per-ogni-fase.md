# I prompt per ogni fase

Copiali nella conversazione con il tuo agente, dentro la cartella di lavoro. Le parti tra parentesi quadre sono da sostituire.

## Dove farli girare

- **Claude**: Cowork, che lavora su una cartella del computer, oppure un Progetto con le skill attive. Per la routine: app desktop, sezione Routines, pulsante New routine. Le routine locali girano solo con il computer acceso. Per leggere LinkedIn serve Claude in Chrome, l'estensione che usa il browser dove hai già fatto l'accesso.
- **ChatGPT**: un Progetto, con i file tra i file del progetto e il testo della skill nelle istruzioni. Per la routine: le attività pianificate dentro il Progetto. Per aprire LinkedIn serve la modalità agente, che usa un browser suo: la prima volta l'accesso lo fai tu.

Se lo strumento non riesce ad aprire una pagina, ti chiede di incollarla e il resto va avanti uguale.

---

## A. L'archivio dei tuoi contenuti

### A1. Dall'export di LinkedIn all'indice

Scarica i tuoi dati da LinkedIn (Impostazioni, Privacy dei dati, Scarica i tuoi dati) e metti Shares.csv nella cartella archivio.

```
Ti allego l'export dei miei dati LinkedIn. Il file che mi interessa è Shares.csv: contiene data, link e testo di ogni post che ho pubblicato.

Crea due file markdown.

1. post-indice.md: una tabella con una riga per post, dal più recente, con le colonne Data | Tema | Apertura | Link | Ancora.
   - Tema: da uno a tre tag, presi da un elenco chiuso di massimo 15 tag che proponi tu dopo aver letto tutti i post.
   - Apertura: la prima riga del post, tagliata a 120 caratteri.
   - Ancora: un identificativo unico del post, che ritrovo nel secondo file.
2. post-testi.md: il testo integrale di ogni post, uno sotto l'altro, ognuno con un titolo che contiene ancora, data e link.

Regole: copia i testi come sono, senza correggerli. Togli le condivisioni senza un mio testo. Alla fine dimmi quanti post hai trovato, che periodo coprono e l'elenco dei tag con il numero di post per ognuno.
```

### A2. Le metriche

Apri la pagina "Tutte le attività" del tuo profilo, scorri fino in fondo, copia tutto e incollalo.

```
Qui sotto incollo la pagina "Tutte le attività" del mio profilo LinkedIn, copiata dopo averla scrollata fino in fondo.

Per ogni post trova reazioni, commenti, condivisioni e impression. Abbina ogni post alla riga giusta di post-indice.md confrontando le prime parole del testo, non la data. Aggiungi all'indice le colonne Reazioni | Commenti | Condivisioni | Impression. Dove un dato non c'è lascia la cella vuota: vuoto vuol dire "non disponibile", non zero.

Poi dammi la mediana delle impression, i 20 post con più impression e i 10 con più commenti in rapporto alle impression.

[incolla qui la pagina]
```

### A3. Le regole della tua voce

```
Leggi post-indice.md e il testo integrale in post-testi.md dei 50 post con più impression e dei 50 più recenti.

Scrivi il file voce.md con le regole del mio modo di scrivere, ricavate dai miei testi e non da regole generiche di copywriting. Accanto a ogni regola metti il dato che la sostiene (quanti post la rispettano) e due esempi presi dai miei post. Copri almeno: come apro (lunghezza della prima riga, numeri, domande), lunghezza media di post e paragrafi, parole che uso spesso, parole che non uso mai, come chiudo, quante emoji uso e dove, se e come metto i link.

Aggiungi una sezione "Cosa funziona" con i temi e i formati sopra e sotto la mediana delle impression, con i numeri.

Non inventare dati: se un confronto si regge su meno di 10 post, scrivilo accanto.
```

### A4. Dalla voce alla skill

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

---

## B. Le idee dai dati

### B1. Dalle domande delle persone ai temi

Funziona con qualsiasi raccolta di domande: la chat di un webinar, i commenti ai post, le email dei clienti, le recensioni.

```
Nel file dati/[nome del file] ci sono le domande e i commenti delle persone che seguono il mio lavoro.

Leggilo tutto e raggruppa le domande per tema. Per ogni gruppo scrivi: quante domande contiene, due o tre domande riportate parola per parola, la parola o il concetto che le persone non capiscono, se ce n'è uno.

Ordina i gruppi dal più grande al più piccolo. Togli nomi, email e qualsiasi dato personale. Salva il risultato in dati/gruppi-di-domande.md.
```

### B2. Dai temi alle idee di contenuto

```
Leggi dati/gruppi-di-domande.md e archivio/post-indice.md.

Proponimi cinque idee di post LinkedIn che rispondono ai gruppi più grandi. Per ogni idea: la domanda da cui nasce, tre aperture diverse, il formato, i post dell'archivio sullo stesso tema da linkare e il motivo per cui secondo i numeri dell'archivio può funzionare.

Non scrivere ancora i post. Aspetta che ti dica quali tengo.
```

---

## C. La bozza

### C1. Il post dall'idea scelta

```
Scrivi il post dell'idea [numero] con la skill post-linkedin. Poi passa la bozza alla skill revisione-anti-ai e mostrami le due versioni affiancate, con l'elenco delle frasi che hai cambiato e perché.
```

### C2. L'articolo da un evento, una call o un webinar

```
Nella cartella dati ci sono la trascrizione di [evento] e le domande fatte dalle persone.

Con la skill articolo-blog scrivi un articolo che:
- spiega i concetti dell'evento a chi non c'era;
- risponde alle domande più frequenti in una sezione FAQ;
- riporta per iscritto i prompt o i passaggi pratici mostrati.

Indica accanto a ogni affermazione da quale punto della trascrizione viene. Non aggiungere dati che non sono nei file. Salva la bozza in bozze/.
```

---

## D. Le correzioni diventano regole

### D1. Dopo aver pubblicato

```
Questa è la bozza che mi hai proposto e questa è la versione che ho pubblicato.
Elenca le differenze. Per ognuna dimmi se secondo te è una regola generale del mio modo di scrivere o vale solo per questo post.
Aggiungi a voce.md solo quelle generali, con la data e l'esempio. Poi mostrami il file aggiornato.

BOZZA:
[incolla]

PUBBLICATO:
[incolla]
```

### D2. Una correzione al volo

```
Salva questa correzione nella skill [nome] come regola, con il motivo e un esempio prima e dopo: [la correzione].
```

---

## E. La routine

Da usare solo quando le fasi A-D funzionano a mano da qualche settimana.

### E1. Il piano dei post del lunedì

```
Crea una routine che parte ogni lunedì alle 8 e usa la skill post-linkedin. Ogni volta fai questi passi in ordine e alla fine scrivimi un riepilogo di cosa hai fatto.

1. Aggiorna l'archivio. Apri dal browser la pagina "Tutte le attività" del mio profilo LinkedIn, leggi i post pubblicati dall'ultimo aggiornamento e aggiungili a post-indice.md e post-testi.md. Aggiorna reazioni, commenti, condivisioni e impression dei post delle ultime quattro settimane. Se non riesci ad aprire la pagina, fermati su questo passo e chiedimi di incollartela.

2. Impara dalla settimana scorsa. Confronta le bozze in bozze.md con i post che ho pubblicato davvero e aggiorna voce.md con le correzioni che si ripetono. Dimmi quali regole hai aggiunto.

3. Cerca i temi della settimana in tre posti.
   - I miei strumenti collegati (email, calendario, Drive, Notion) e la cartella di lavoro: cosa ho fatto, lanciato, deciso o imparato negli ultimi sette giorni.
   - Il web: le novità degli ultimi sette giorni sui temi che nel mio archivio stanno sopra la mediana delle impression.
   - L'archivio: post sopra la mediana di più di sei mesi fa da aggiornare, oppure da tre a cinque post sullo stesso tema da combinare in uno.
   Per ogni tema trovato cerca nell'archivio i post che ho già scritto sull'argomento.

4. Proponimi il piano editoriale della settimana: cinque post, uno per giorno lavorativo, con temi presi dalla mia settimana, dal mercato e dall'archivio. Per ogni post: giorno, tema, fonte (il file, la mail o il link da cui nasce), tre aperture diverse, formato e il numero dell'archivio che giustifica la scelta.

5. Fermati e aspetta. Quando ti dico quali post tengo, scrivili con la skill post-linkedin seguendo voce.md, ognuno con la descrizione dell'immagine. Salva le bozze in bozze.md con la data.

Regole: non pubblicare mai niente da solo e non inventare fatti, numeri o citazioni. Ogni tema preso dal web ha il suo link. Se ti manca un dato, chiedimelo.
```

I prompt A1-A4, D1 ed E1 vengono dall'articolo del blog di Learnn "Post LinkedIn con l'AI: il processo che impara dal tuo stile" (https://learnn.com/blog/post-linkedin-ai), dove sono spiegati passo per passo con gli esempi.
