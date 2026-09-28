# 03. Ricavare le regole della tua voce

## A cosa serve

Prima della skill serve un terzo file: `voce.md`, le regole del tuo modo di scrivere ricavate dai tuoi testi. Il trucco è chiedere il dato accanto a ogni regola. "Apri con una frase breve" è un consiglio da manuale. "N dei tuoi 50 post migliori aprono con una frase sotto le 15 parole" è una regola tua: l'agente la rispetta perché la vede misurata.

## Cosa prepari

- `archivio/post-indice.md` con le metriche e `archivio/post-testi.md`, dalla procedura 02.
- Mezz'ora per leggere il risultato con attenzione.

## Passi

1. **Lancia il prompt A3** nella cartella di lavoro.
2. **Leggi `voce.md` regola per regola.** Per ognuna chiediti se la riconosci. Se una regola ti sembra sbagliata, chiedi all'agente i post da cui l'ha ricavata.
3. **Cerca le sorprese nella sezione "Cosa funziona".** Qui escono i dati che contraddicono le regole che si danno per scontate.
4. **Togli quello che non ti somiglia** e aggiungi a mano le parole che non useresti mai, anche se l'agente non le ha trovate.

## Prompt da copiare

**A3. Le regole della tua voce**

```
Leggi post-indice.md e il testo integrale in post-testi.md dei 50 post con più impression e dei 50 più recenti.

Scrivi il file voce.md con le regole del mio modo di scrivere, ricavate dai miei testi e non da regole generiche di copywriting. Accanto a ogni regola metti il dato che la sostiene (quanti post la rispettano) e due esempi presi dai miei post. Copri almeno: come apro (lunghezza della prima riga, numeri, domande), lunghezza media di post e paragrafi, parole che uso spesso, parole che non uso mai, come chiudo, quante emoji uso e dove, se e come metto i link.

Aggiungi una sezione "Cosa funziona" con i temi e i formati sopra e sotto la mediana delle impression, con i numeri.

Non inventare dati: se un confronto si regge su meno di 10 post, scrivilo accanto.
```

## Cosa ottieni

`archivio/voce.md`, con le regole della tua scrittura, il dato che sostiene ciascuna e gli esempi presi dai tuoi post. Un esempio completo è `esempio/archivio/voce.md`: la prima regola dice dove Luca mette la negazione nei contrasti ("X, non Y" in 56 casi, "non solo X, ma anche Y" in 3), con cinque frasi prese dai suoi post.

Un esempio di sorpresa, dall'archivio di Luca: la regola secondo cui i link nel testo tolgono visibilità non regge. I post con un link nel corpo fanno 22.546 impression di mediana contro 19.178 di quelli senza, su 27 casi. Da quel dato è nato un formato nuovo, il post che riprende cinque post vecchi sullo stesso tema con i loro link.

## Errori comuni

- **Accettare regole senza numero.** Una regola senza dato accanto è un consiglio generico: chiedi di misurarla o di toglierla.
- **Fidarsi dei confronti su pochi post.** Il prompt chiede di segnalare quelli sotto i 10 post: trattali come ipotesi da verificare.
- **Scrivere voce.md a mano da zero.** Le regole che credi di seguire spesso sono diverse da quelle che segui nei post. Parti dai dati e poi correggi.
- **Mescolare canali diversi.** Le regole di LinkedIn non valgono per una newsletter o per il blog: se scrivi su più canali, fai un file di voce per ognuno.

Prossimo passo: [04. Creare la skill](04-creare-la-skill.md).
