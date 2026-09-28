# 05. Scrivere il primo post e correggerlo

## A cosa serve

Le prime bozze non saranno perfette e va bene così. La skill impara da quello che cambi: ogni post che pubblichi senza toccarlo le insegna che andava bene. Questa procedura trasforma le tue correzioni in regole, così dopo quattro o cinque settimane le correzioni diventano poche.

## Cosa prepari

- La skill `post-linkedin` (procedura 04) e la skill `revisione-anti-ai`, già pronta in `.claude/skills/revisione-anti-ai/SKILL.md` (lo stesso testo è in `toolkit/04-skill-revisione-anti-ai.md`).
- Un'idea di post: dal piano proposto dalla skill oppure dalla procedura 06.
- La checklist `toolkit/05-checklist-revisione-bozza.md`.

## Passi

1. **Fai scrivere la bozza** con il prompt C1. La skill di revisione toglie le frasi che suonano scritte da una macchina e ti mostra cosa ha cambiato.
2. **Correggi tutto quello che non diresti tu**: una parola, un'apertura, una chiusura troppo furba. Non accettare niente per stanchezza.
3. **Passa la checklist** in cinque minuti: fatti, voce, forma.
4. **Pubblica tu**, dal tuo account.
5. **Rimanda la differenza all'agente** con il prompt D1, subito dopo aver pubblicato.
6. **Per una correzione al volo** mentre lavori, usa il prompt D2.

## Prompt da copiare

**C1. Il post dall'idea scelta**

```
Scrivi il post dell'idea [numero] con la skill post-linkedin. Poi passa la bozza alla skill revisione-anti-ai e mostrami le due versioni affiancate, con l'elenco delle frasi che hai cambiato e perché.
```

**D1. Dopo aver pubblicato**

```
Questa è la bozza che mi hai proposto e questa è la versione che ho pubblicato.
Elenca le differenze. Per ognuna dimmi se secondo te è una regola generale del mio modo di scrivere o vale solo per questo post.
Aggiungi a voce.md solo quelle generali, con la data e l'esempio. Poi mostrami il file aggiornato.

BOZZA:
[incolla]

PUBBLICATO:
[incolla]
```

**D2. Una correzione al volo**

```
Salva questa correzione nella skill [nome] come regola, con il motivo e un esempio prima e dopo: [la correzione].
```

## Cosa ottieni

- Un post pubblicato, scritto dall'agente e corretto da te.
- Le regole nuove in `voce.md` o nella sezione "Regole nate dalle correzioni" della skill, ognuna con data ed esempio.
- Un esempio di bozza passata dalle due skill è in `esempio/risultati-pronti/03-post-bozza.md`.

## Errori comuni

- **Pubblicare la prima bozza così com'è.** La skill la registra come giusta e la ripropone uguale.
- **Correggere senza dirlo all'agente.** Se la versione pubblicata non torna nella cartella, la skill non impara niente.
- **Trasformare in regola ogni correzione.** Una correzione che vale per un solo post, salvata come regola generale, peggiora i post successivi. Il prompt D1 chiede di distinguere: controlla la sua risposta.
- **Farsi correggere le frasi che hai scritto tu.** La skill di revisione lascia com'è una frase scritta o approvata dall'autore: se la cambia, ripristinala e ricordaglielo.

Prossimo passo: [06. Dalle domande alle idee](06-dalle-domande-alle-idee.md).
