# 10. Senza storico e su altri canali

## A cosa serve

Le procedure 02-08 partono da un archivio di post LinkedIn. Al webinar le due domande più frequenti sono state "e se non ho mai pubblicato?" e "funziona anche su Instagram, YouTube, il blog?". La risposta è sì in entrambi i casi: cambia da dove prendi i dati, il metodo resta lo stesso. Prima si costruisce l'archivio, poi si ricavano le regole, poi la skill scrive e le correzioni diventano regole.

## Se non hai uno storico

**1. Parti da chi ti piace leggere.** Scegli un creator, un'azienda o un blog che scrive come vorresti scrivere tu. Su LinkedIn apri il suo profilo, vai su Attività e poi Post, scorri fino a dove ti interessa e copia la pagina. I post pubblici hanno reazioni e commenti visibili, quindi l'agente vede anche quali hanno funzionato.

**2. Separa lo stile dai temi.** Dall'archivio di un altro prendi i formati (come apre, come struttura, come chiude) e non le opinioni. Le opinioni devono essere tue, altrimenti il risultato è una copia.

**3. Dai all'agente qualcosa di tuo.** Bastano pochi testi: un paio di email a clienti, una presentazione, le note di una call, due o tre post anche vecchi. Servono a fargli capire come parli.

**4. Lancia il prompt A6** qui sotto e salva il risultato come `voce.md`. Da lì la procedura 04 è identica.

Lo stesso vale per il blog: se hai un blog, fai leggere all'agente tutti gli articoli; se non ce l'hai, fagli leggere quelli di un blog che ti piace e chiedigli di adattare lo stile al tuo settore. Su Claude Code e Codex l'agente può dividere il lavoro fra più sotto agenti, quindi anche cento articoli si leggono in pochi minuti.

Luca ha fatto così con il formato di storytelling del founder di un'azienda che seguiva: gli ha chiesto di prendere quel formato, applicarlo alla sua voce e aggiungerlo come formato nuovo nella skill LinkedIn.

## Se l'archivio l'hai scritto con l'AI

Se i tuoi post vecchi li ha già scritti un'AI, l'archivio insegna all'agente le abitudini dell'AI. In quel caso tieni solo i post che hai riscritto a mano o che ti somigliano, oppure parti come se non avessi uno storico e usa gli altri solo per i temi.

## Come esportare i dati dalle altre piattaforme

| Piattaforma | Da dove prendi i testi | Da dove prendi i numeri |
|---|---|---|
| LinkedIn | Export dei dati (procedura 02), file Shares.csv | La pagina "Tutte le attività", copiata dopo averla scorsa |
| Instagram e Facebook | Centro gestione account, Le tue informazioni e autorizzazioni, Scarica le tue informazioni: scegli i post e il formato JSON | Gli insights dell'account professionale, oppure la pagina del profilo copiata |
| TikTok | Impostazioni, Account, Scarica i tuoi dati | Analisi nello strumento per i creator |
| YouTube | Google Takeout per l'elenco dei video, i sottotitoli per il testo (vedi sotto) | YouTube Studio, sezione Analytics, con l'export in CSV |
| Blog | Gli articoli pubblicati, letti dall'agente dal sito o dal CMS | Search Console o l'analisi del sito |
| Newsletter | L'archivio dei numeri pubblicati | Aperture e clic dallo strumento di invio |

Se una piattaforma non ha un export comodo, vale la strada di LinkedIn: apri la pagina nel browser, scorri, copia tutto e incollalo all'agente. È meno elegante e funziona.

## Video, reel e YouTube

Per l'agente un video è il suo testo. Per YouTube esistono skill che scaricano i sottotitoli e li passano all'agente (una si chiama `watch`: si trova cercando "watch skill YouTube" su GitHub). Per i video che hai sul computer, la trascrizione la fa lo strumento stesso o un servizio di trascrizione. Da lì l'agente lavora sul testo come sui post: trova i temi, propone idee, scrive i copy e le descrizioni.

Per scegliere una skill o un repository trovato online:

1. Guarda le stelle su GitHub e l'ultima modifica: i repository più usati ne hanno migliaia e sono aggiornati di recente.
2. Prima di installarlo chiedi all'agente di controllarlo: "Leggi questo repository e dimmi cosa fa, a cosa accede e se c'è qualcosa di rischioso".
3. Poi incolla il link e scrivi "installa questo repository nel mio ambiente": l'agente fa il resto.

## Pubblicare sulle altre piattaforme

| Canale | Come ci arriva l'agente |
|---|---|
| LinkedIn | Dal browser (Claude in Chrome o la modalità agente di ChatGPT): nessun connettore ufficiale |
| Instagram e Facebook | Le API di Meta per gli account professionali, attraverso un connettore o uno strumento come Make o n8n |
| Blog (WordPress, Wix, Webflow, Strapi) | Le API del CMS con una chiave, oppure il browser. Salva sempre in bozza |
| Email | Il connettore dello strumento di invio, dove esiste, sempre come bozza da approvare |

In ogni caso l'agente prepara la bozza e si ferma. La pubblicazione la approvi tu (procedura 08).

## Il formato che solo l'archivio permette

Un post che raccoglie in un unico contenuto quello che hai già scritto su un tema: "Cinque cose che ho imparato sul pricing", con un paragrafo e un link per ognuno dei cinque contenuti dell'archivio che le raccontano. A Luca questo formato porta molti salvataggi e clic sui post vecchi, perché chi legge si ritrova una piccola guida. Il prompt è il C3 qui sotto.

## Un evento, quattro contenuti

Da un solo webinar Learnn ha ricavato un articolo del blog, otto lezioni scritte in un corso, un post LinkedIn e l'email a chi si era iscritto. La fonte era la stessa per tutti (registrazione, chat e slide), con una skill per ogni formato. Se tieni in `dati/` le trascrizioni delle tue call, dei tuoi eventi o delle tue presentazioni, ogni evento diventa materiale per più canali.

## Prompt da copiare

**A6. La voce da chi ti piace leggere**

```
Nella cartella dati ci sono i post di [nome del creator o dell'azienda], copiati dalla sua pagina con reazioni e commenti. Alcuni miei testi (email, note, post vecchi) sono in dati/miei-testi.md.

1. Dai post dell'altro ricava i formati: come aprono, come sono strutturati, come chiudono, quanto sono lunghi. Per ogni formato indica i tre post che lo rappresentano meglio e quanto hanno funzionato.
2. Dai miei testi ricava come parlo io: lunghezza delle frasi, parole che uso spesso, tono, cosa non dico mai.
3. Scrivi archivio/voce.md con le regole della mia voce e, in una sezione a parte, i formati presi dall'altro adattati alla mia voce.

Regole: prendi i formati, mai le opinioni o le storie dell'altro. Se una regola della mia voce si basa su pochi esempi, scrivilo.
```

**C3. Il post che raccoglie l'archivio**

```
Voglio un post che raccolga quello che ho già scritto su [tema], nel formato "[numero] cose che ho imparato su [tema]".

Cerca in archivio/post-indice.md e nei miei articoli i contenuti su questo tema e scegli i [numero] con più impression o più utili, senza ripetizioni. Per ognuno scrivi un paragrafo di due o tre righe che dice la cosa imparata e mette il link al contenuto originale.

Usa la skill post-linkedin per voce e apertura, poi passa la bozza alla skill revisione-anti-ai. Salva la bozza in bozze/ con la data.
```

## Errori comuni

- **Copiare le opinioni insieme allo stile.** Il risultato è un post di un altro firmato da te.
- **Mettere nell'archivio i post scritti dall'AI.** L'agente impara le sue stesse abitudini.
- **Installare un repository senza controllarlo.** Fallo leggere all'agente prima.
- **Collegare un canale per pubblicare prima di aver corretto la skill** per qualche settimana.

Prossimo passo: [11. Le domande del webinar](11-domande-frequenti.md).
