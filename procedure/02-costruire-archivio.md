# 02. Costruire l'archivio dei tuoi post

## A cosa serve

Un modello linguistico lasciato da solo scrive nel modo più probabile, quindi come tutti. Con davanti i tuoi post pubblicati e i numeri che hanno fatto smette di indovinare: vede come apri, quanto sei lungo e quali temi funzionano per il tuo pubblico. L'archivio è la parte che conta di più di tutto il sistema.

L'archivio sta in due file: un indice con una riga per post, che l'agente legge tutto in un colpo; un file con i testi integrali, che apre solo per i post che gli servono. Così non riempie la memoria della conversazione.

## Cosa prepari

- L'export di LinkedIn richiesto nella procedura 01. Dentro c'è `Shares.csv`, con data, link e testo di ogni post: mettilo in `archivio/`.
- La pagina "Tutte le attività" del tuo profilo LinkedIn, che mostra reazioni, commenti e impression sotto ogni post. L'export non contiene questi numeri.

## Passi

1. **Dall'export all'indice.** Incolla il prompt A1 con `Shares.csv` nella cartella (o allegato, se lo strumento non legge le cartelle).
2. **Controlla il riepilogo**: quanti post, che periodo, quali tag. Se i tag non ti convincono, chiedi di rifarli adesso: dopo li userai ovunque.
3. **Copia le metriche.** Apri "Tutte le attività", scorri fino in fondo perché LinkedIn carica i post a blocchi, seleziona tutto e copia.
4. **Aggancia i numeri** con il prompt A2, incollando la pagina al posto della riga tra parentesi quadre.
5. **Segnati la mediana delle impression.** Da qui in avanti "un post che funziona" vuol dire un post sopra la tua mediana, non sopra quella di qualcun altro.

## Prompt da copiare

**A1. Dall'export di LinkedIn all'indice**

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

**A2. Le metriche**

```
Qui sotto incollo la pagina "Tutte le attività" del mio profilo LinkedIn, copiata dopo averla scrollata fino in fondo.

Per ogni post trova reazioni, commenti, condivisioni e impression. Abbina ogni post alla riga giusta di post-indice.md confrontando le prime parole del testo, non la data. Aggiungi all'indice le colonne Reazioni | Commenti | Condivisioni | Impression. Dove un dato non c'è lascia la cella vuota: vuoto vuol dire "non disponibile", non zero.

Poi dammi la mediana delle impression, i 20 post con più impression e i 10 con più commenti in rapporto alle impression.

[incolla qui la pagina]
```

## Cosa ottieni

- `archivio/post-indice.md`: una riga per post con data, tag, apertura, link e numeri. Un esempio è in `esempio/archivio/post-indice.md`.
- `archivio/post-testi.md`: i testi integrali, ritrovabili dall'ancora.
- La mediana delle impression e le due classifiche: i post più visti e quelli che fanno parlare di più.

## Errori comuni

- **Abbinare i numeri per data.** La pagina "Tutte le attività" mostra date approssimative come "3 sett.": l'abbinamento si fa sulle prime parole del testo, come chiede il prompt.
- **Trattare le celle vuote come zeri.** Un post senza impression visibili abbassa la mediana se lo conti come zero. Vuoto vuol dire che il dato non c'è.
- **Preoccuparsi dei post vecchi senza numeri.** Per i post di qualche anno fa spesso le impression non ci sono più: i testi servono lo stesso a ricavare la voce.
- **Chiedere all'agente di correggere i testi.** L'archivio deve restare com'è: i refusi e le abitudini sono parte della tua voce.

Se non hai mai pubblicato, costruisci l'archivio con contenuti di altri che ti piacciono e accanto a ognuno scrivi perché ti piace. È un punto di partenza più debole, ma funziona.

Prossimo passo: [03. Le regole della voce](03-regole-della-voce.md).
