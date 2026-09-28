# 06. Dalle domande delle persone alle idee

## A cosa serve

Le domande di chi ti segue sono la fonte di idee più affidabile che hai: dicono cosa le persone non capiscono, con le loro parole. Questa procedura le raggruppa per tema, le incrocia con l'archivio e ne ricava idee di post che rispondono a un bisogno vero.

## Cosa prepari

Un file in `dati/` con le domande o i commenti. Va bene qualsiasi raccolta: la chat di un webinar, i commenti ai post, le email dei clienti, le recensioni, le domande fatte a una call di vendita. Copia il testo in un file markdown o di testo.

Per provare subito c'è `esempio/dati/domande-webinar-1.md`, con circa 230 domande arrivate in chat al primo webinar dell'Agents Week.

## Passi

1. **Metti il file in `dati/`.** Se contiene nomi o email, il prompt B1 li toglie: tienili fuori da qualsiasi file che condividi.
2. **Raggruppa le domande** con il prompt B1.
3. **Leggi i gruppi.** Guarda soprattutto la colonna delle parole che le persone non capiscono: è materiale per un post a sé.
4. **Chiedi le idee** con il prompt B2.
5. **Scegli.** L'agente si ferma e aspetta: tieni le idee che ti convincono e passa alla procedura 05 per scriverle.

## Prompt da copiare

**B1. Dalle domande delle persone ai temi**

```
Nel file dati/[nome del file] ci sono le domande e i commenti delle persone che seguono il mio lavoro.

Leggilo tutto e raggruppa le domande per tema. Per ogni gruppo scrivi: quante domande contiene, due o tre domande riportate parola per parola, la parola o il concetto che le persone non capiscono, se ce n'è uno.

Ordina i gruppi dal più grande al più piccolo. Togli nomi, email e qualsiasi dato personale. Salva il risultato in dati/gruppi-di-domande.md.
```

**B2. Dai temi alle idee di contenuto**

```
Leggi dati/gruppi-di-domande.md e archivio/post-indice.md.

Proponimi cinque idee di post LinkedIn che rispondono ai gruppi più grandi. Per ogni idea: la domanda da cui nasce, tre aperture diverse, il formato, i post dell'archivio sullo stesso tema da linkare e il motivo per cui secondo i numeri dell'archivio può funzionare.

Non scrivere ancora i post. Aspetta che ti dica quali tengo.
```

## Cosa ottieni

- `dati/gruppi-di-domande.md`: i temi ordinati per numero di domande, con le frasi originali e i concetti da spiegare. Un esempio è `esempio/risultati-pronti/01-gruppi-di-domande.md`.
- Cinque idee di post, ognuna collegata alla domanda da cui nasce e ai post dell'archivio da linkare. Un esempio è `esempio/risultati-pronti/02-cinque-idee.md`.

## Errori comuni

- **Lasciare nomi e contatti nel file.** Anche se il prompt li toglie dal risultato, il file di partenza resta nella cartella: anonimizzalo prima se lo tieni a lungo.
- **Far scrivere subito i post.** Scegliere prima le idee costa un minuto e risparmia cinque bozze da buttare.
- **Contare le persone invece dei messaggi.** Chi scrive tre volte la stessa domanda pesa tre volte: se il numero conta, scrivi nel prompt cosa stai contando.
- **Ignorare i gruppi piccoli.** Un gruppo di cinque domande su un tema che nessuno tratta può valere più di un gruppo grande su un tema affollato.

Prossimo passo: [07. L'articolo da un evento](07-articolo-da-un-evento.md).
