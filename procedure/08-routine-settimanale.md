# 08. La routine settimanale

## A cosa serve

Fin qui ogni passo lo lanci tu. La routine è un'attività che parte da sola ogni settimana a un orario fisso: aggiorna l'archivio, impara dalle correzioni, cerca i temi nei tuoi strumenti e sul web e ti fa trovare il piano editoriale pronto. La tua settimana si riduce a due momenti: il lunedì scegli dal piano, prima di pubblicare correggi.

Da usare solo quando le procedure 02-07 funzionano a mano da tre o quattro settimane. Una routine costruita su una skill che non hai ancora corretto ripete gli stessi errori ogni lunedì.

## Cosa prepari

- La skill `post-linkedin` con qualche settimana di correzioni.
- L'archivio aggiornato e la cartella `bozze/`.
- Su Claude: l'app desktop e, per leggere LinkedIn, Claude in Chrome, l'estensione che usa il browser dove hai già fatto l'accesso. I connettori gli aprono email, calendario, Drive e Notion.
- Su ChatGPT: un Progetto con l'archivio, la ricerca web e le app collegate (Drive, Notion, Gmail) attivate dalle impostazioni. Per aprire LinkedIn serve la modalità agente, che usa un browser suo: la prima volta l'accesso lo fai tu.

## Passi

1. **Su Claude**: app desktop, sezione Routines, pulsante New routine. Scegli la cartella con l'archivio, imposta giorno e orario e incolla il prompt E1. Le routine locali girano solo con il computer acceso e collegato, quindi scegli un orario in cui lo usi già.
2. **Su ChatGPT**: crea un'attività pianificata dentro il Progetto con l'archivio e incolla lo stesso prompt.
3. **Collega solo gli strumenti che servono**, con i permessi minimi.
4. **Il primo lunedì controlla ogni passo** del riepilogo: cosa ha letto, quali regole ha aggiunto, da dove vengono i temi.
5. **Scegli i post**: l'agente si ferma al passo 5 e aspetta la tua scelta prima di scrivere.

Se la routine non riesce ad aprire LinkedIn, ti chiede di incollare la pagina e il resto va avanti uguale.

## Prompt da copiare

**E1. Il piano dei post del lunedì**

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

## Cosa ottieni

Ogni lunedì un riepilogo e un piano di cinque post, ognuno con la fonte da cui nasce e il numero dell'archivio che lo giustifica. A Luca la routine propone sette post a settimana, tre ripresi dall'archivio e quattro nuovi, con formati che un prompt da solo non inventa: cinque strategie di pricing con i link ai cinque post che le raccontano, oppure due post vecchi combinati in uno nuovo con i numeri aggiornati.

## Errori comuni

- **Attivare la routine il primo giorno.** Prima tre o quattro settimane a mano, poi l'automazione.
- **Lasciarle pubblicare da sola.** La routine prepara le bozze e si ferma: la pubblicazione resta tua, sempre.
- **Computer spento all'orario della routine.** Le routine locali di Claude non partono: scegli un orario in cui il computer è acceso.
- **Collegare tutto per comodità.** Ogni connettore in più è un posto in più dove l'agente legge. Collega solo quello che il prompt usa.
- **Misurare quanto produce e non quanto viene letto.** Accanto al numero di post guarda le impression: un agente che scrive tanto e non viene letto è lavoro sprecato.

Prossimo passo: [09. Gli altri strumenti](09-altri-strumenti.md).
