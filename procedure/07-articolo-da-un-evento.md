# 07. L'articolo da un evento, una call o un webinar

## A cosa serve

Un webinar, una call con un cliente o un intervento a un evento contengono già un articolo: i concetti spiegati, gli esempi pratici e le domande delle persone. Questa procedura li porta per iscritto, per chi non c'era, con la fonte accanto a ogni affermazione.

## Cosa prepari

- La trascrizione dell'evento in `dati/`. La producono gli strumenti di videoconferenza oppure un'app di trascrizione: basta il testo.
- Le domande fatte dalle persone, se ci sono, in un file a parte in `dati/`. Sono l'indice più affidabile dell'articolo.
- La skill `articolo-blog`, in `.claude/skills/articolo-blog/SKILL.md` (lo stesso testo è in `toolkit/03-skill-articolo-blog.md`). Adattala al tuo blog: lunghezza, tono, sezioni fisse.

## Passi

1. **Adatta la skill** al tuo blog, se non l'hai ancora fatto.
2. **Metti trascrizione e domande in `dati/`.**
3. **Lancia il prompt C2**, sostituendo il nome dell'evento.
4. **Controlla le fonti.** Accanto a ogni affermazione c'è il punto della trascrizione da cui viene: apri i passaggi che ti sembrano strani.
5. **Leggi l'elenco delle affermazioni da verificare** che la skill consegna in fondo e verificale una per una.
6. **Correggi e salva le regole**, come nella procedura 05.

## Prompt da copiare

**C2. L'articolo da un evento, una call o un webinar**

```
Nella cartella dati ci sono la trascrizione di [evento] e le domande fatte dalle persone.

Con la skill articolo-blog scrivi un articolo che:
- spiega i concetti dell'evento a chi non c'era;
- risponde alle domande più frequenti in una sezione FAQ;
- riporta per iscritto i prompt o i passaggi pratici mostrati.

Indica accanto a ogni affermazione da quale punto della trascrizione viene. Non aggiungere dati che non sono nei file. Salva la bozza in bozze/.
```

## Cosa ottieni

- L'articolo in bozza in `bozze/`: titolo con la parola che le persone cercano, primo paragrafo che risponde subito, punti chiave, sezioni, passaggi pratici, da otto a dieci domande frequenti e il prossimo passo per chi legge.
- Titolo per i motori di ricerca, descrizione di 150 caratteri e la descrizione delle immagini da creare.
- L'elenco delle affermazioni da verificare prima di pubblicare.

## Errori comuni

- **Domande frequenti inventate.** Le FAQ devono venire dalle domande vere delle persone: se il file delle domande manca, dillo nel prompt e chiedi all'agente di segnalare quali ha dedotto.
- **Parole tecniche non spiegate.** Al primo webinar dell'Agents Week 20 messaggi su 230 dicevano di non capire i termini (`esempio/dati/domande-webinar-1.md`, sezione 2.7). La skill chiede di spiegarli la prima volta che compaiono: controlla che lo faccia.
- **Affermazioni senza fonte.** La regola della skill è netta: se una fonte non c'è, l'affermazione si toglie.
- **Un articolo che segue l'ordine dell'evento.** Chi legge cerca una risposta, non la cronaca: l'ordine lo danno le domande più frequenti.

Prossimo passo: [08. La routine settimanale](08-routine-settimanale.md).
