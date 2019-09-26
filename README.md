## Articolo programmazione funzionale

**ricetta per fare la torta in modo imperativo :**
```sh
1) Preriscalda il forno a 175 gradi C. Grasso e farina Teglie rotonde da 2 - 8 pollici. In una piccola ciotola, sbatti insieme farina, bicarbonato di sodio e sale; accantonare.
2) In una grande ciotola, burro alla panna, zucchero bianco e zucchero di canna fino a quando leggero e soffice. Sbattere le uova, una alla volta. Mescolare le banane. Aggiungi il composto di farina alternativamente con il latticello al composto alla crema. Mescolare le noci tritate. Versare la pastella nelle padelle preparate.
3) Cuocere in forno preriscaldato per 30 minuti. Togliere dal forno e posizionare su un canovaccio umido per raffreddare.
```
ricetta in modo funzionale 
```sh
1)  Una torta è una torta calda che è stata raffreddata su un canovaccio umido, dove una torta calda è una torta preparata che è stata cotta in un forno preriscaldato per 30 minuti.
2)  Un forno preriscaldato è un forno che è stato riscaldato a 175 gradi C.
3)  Una torta preparata è una pastella che è stata versata in padelle preparate, dove la pastella è una miscela che ha mescolato le noci tritate. Dove la miscela è burro, zucchero bianco e zucchero di canna che è stato cremato in una grande ciotola fino a quando leggero e soffice.
```
quello che posssiamo vedere , è che si esprime come fare la ricetta in modi diversi, diciamo "opposti", nel primo caso passaggio sopo passaggio, nel secondo descrivendo come sono interconesse "le cose" definite altrove. 

Con questo esempio, appare più chiara la prima lettura imperativa rispetto a quella funzionale, che qualcuno direbbe sembra dover mettere insieme un puzzle, questo è l'effetto da chi proviene dalla tradizionale programma dichirativa sequenziale. 

Possiamo però fare un altro più tipico esempio che mette in luce subito il vantaggio della programmazione funzionale : 

Istruiamo la bambina alice a fare le cose : 

vestirsi : 
```sh
Alice:
1) togliti il pigiama
2)  prendi la prima gonna a destra nel armadio e infilatela e allacciala,
3) prendi la maglietta nel secondo cassetto e infilatela alzando le braccia,
4) prendi le calze nel terzo cassetto, e mettile 
5) prendi le scarpe sotto il letto e allacciale.
```
Mettere a posto i giocattoli :
```sh
Alice, 
1)  dal cesto vai dritto 
2)  prendi il trenino che incontri con la mano destra lo prendi
3)  torni indietro e lo butto nel cesto, 
4)  fai un passo avanti ti giri di 90 vai avanti
5)  con la mano destra prendi la bambola 
6)  prosegui e con la mano sinistra prendi la corda , 
 ... 
```

anche qui abbiamo un elenco di azioni sequenziali imperative, ma il concetto è questo, io ad alice mi devo limitare a dire :
```sh
Alice , metti a posto i giocatolli e quando hai finito, vestiti. 
```
leggo la frase , che chiama le funzioni metti_a_posto, e vestiti, in sequenza, particolare sulla frequenza : si preferisce far mettere a posto prima i giocatolli , magari cosi si trovano i vestiti con meno disordine, in programmazione potrebe essere una lista "oggetti_nella_stanza" che si trova meno elementi da ciclare per ottimizzare le prestazioni, diversamente il risultato finale non varierebbe, ma parafrasando... alice ci metterebbe di più a vestirsi, perdendo tempo a cercarli tra i giocattoli, se per caso non si trovano in ordine nei cassetti perchè già utilizzati".

Ho messo in luce , il problema della sequenzialità delle azioni che chiamamo il work flow del programma, cosa può cambiare pur avendo lo stesso esatto risultato,cioè l'abbassamento di prestazioni, nella programmazione funzionale, è facile gestire il carico delle prestazioni. 


il nome delle funzioni e la conoscenza anche solo di cosa servono senza guardare il come, mi bastano e avanzano per capire tutto.
nel mondo reale significa che alice, una volta che ha imparato a vestirsi e mettere a posto i giocattoli (funzioni di libreria), io mi limiterò a dirgli COSA deve fare e non COME deve farlo. 

questo è l'esempio più facile per comprendere il cambio di paradgma concetualle con la programmazione funzionale, fare esempi di questo tipo, sui piccoli problemi , limita però il far notare i vantaggi, estendiamo il problema precedente facendo fare più attività  : 
```sh
Alice : svegliati, metti a posto, lavati, vestiti, prepara la cartella, vai a scuola , torna da scuola, mangia , riposa, fai i compiti, gioca, ecc ecc 
```
estendendo ancora e seguendo il concetto di prima funzionale rispetto al imperativo , inizierò a leggere su un programma per alice più esteso :

```sh
preparati per andare a scuola , mangia e fai i compiti dopo il riposo prima di  poter giocare 
```

elencare minuziosamente invece , passaggio dopo passaggio, comportava di dover leggere una sorta di libro per capire cosa deve fare in generale alice , i commenti possono aiutare , ma nel caso più funzionale , non cè bisogno dei commenti, la giusta nomenclatore da sola fa anche da commento se vogliamo.

come esempio dei lego, è come o costrire passaggio dopo passaggio, o preparare in gruppi i pezzi composti da più pezzi , e poi assemblari in modo più macro tra loro, come libreria potrei trovare i vari pezzi intermedi già montanti tra loro, devo solo decidere come assemblare nelle maniere diverese per entro un certo range possibile, di tipologia dipendente dai pezzi intermedi assemblati tra loro.

in altre parole , con i pezzi intermedi coerenti rispetto a cosa devo fare, il risultato finale, lo posso fare facilmente in diverse versioni inercabiabili tra loro. 

sembra che a dire cosi , sto citando le funzioni, niente di nuovo sotto il sole, tutti i linguaggi decenti le hanno !! cambia il concetto, ragiono a funzioni che a sua volta chiamano funzioni che vengono passate !!! 

torniamo alla torta scritta in modo funzionale :


```sh
1)  Una torta è una torta calda che è stata raffreddata su un canovaccio umido, dove una torta calda è una torta preparata che è stata cotta in un forno preriscaldato per 30 minuti.
2)  Un forno preriscaldato è un forno che è stato riscaldato a 175 gradi C.
3)  Una torta preparata è una pastella che è stata versata in padelle preparate, dove la pastella è una miscela che ha mescolato le noci tritate. Dove la miscela è burro, zucchero bianco e zucchero di canna che è stato cremato in una grande ciotola fino a quando leggero e soffice.
```

scritta in funzionale "semplice" e nel modo più immediato  viene cosi :

```sh
raffredda(umidisci(canovaccio), prepara(cuoci(30, 175, impasta(crema(burro, zucch_bianco, zucch_canna), trita(noci)) , 
```
la lettura, non è per nulla facile !!!

questo a prima vista, e in prima battuta, si può rispondere nemmeno cosi facile, se la scrivevo in modo dichiarativo, con tante istruzioni, la cosa però che si può notare, dopo averci fatto un po gli occhi , è la linearità della sua espressione, diciamo cosi non spezzo in blocchi con varibili intermedie  !! 

quella ricetta piena di funzioni chiamate dentro se stesse che comportano antipatici annidamento di parentesi , si può scrivere in modo più dichiarativo cosi :

```sh
const cremaMontanta = crema(burro, zucch_bianco, zucch_canna)
const impasto = miscela(cremaMontanta, trita(noci))
const impastoCotto = cuoci((30, 175), impasto)
const torta = raffredda(umidisci(canovaccio), impastoCotto)
```

la lettura parte dall' basso verso l'alto, quindi ci concentriamo su 

raffredda(umidisci(canovaccio), impastoCotto)

se voglio vedere i dettagli dei particolari, come sempre spulcio le funzioni, ma quello che si può notare, che poi risalgo a leggere ancora più dettagli, dal basso verso l'alto mi ritrovo le macro funzioni. 

dico "mi ritrovo", perchè scomponendo in passaggi intermedi, riscrivendo l'espressione un po troppo algebrica e annidata , seguendola, mi ritrovo cosi da solo senza io pensarci , l'ordine che segue il workflow.... annidato, in questo caso le annidazioni sono lineari, una sopra l'altra con valore intermedio.

cosi è tutto molto più facile da leggere, scivere commenti nel codice è fin che superfluo, l'importante è il naming ai valori che ho dato. 

Ma la cosa importante, è che rispettato il naming e il work flow , per capire cosa sta facendo il codice e NON COME LO STA A FARE ESATTAMENTE , mi basta solo leggere l'ultima riga che mi dice :

La torta è un raffrademanto di un impasto cotto. 






con nome sensato ai risultati intermedi pronti da essere passati alla funzione che chiameremo successivamente, 


  In altre parole , passiamo a una programmazione più 



diversamente, dovrei fare tutto l'elenco di metttere a posto i giocatoli e poi l'elenco di vestirsi.... 
cosi però nella lettura i due passaggi chiave legati tra loro : mettere a posto e poi vestirsi, come lettura vengono persi e mescolati nella seqenzialità. 
devo leggermi tutto per capire il mettere a posto e quindi vestirsi banalmente, se codice di altri e non conosco bene il (vestirsi) la mia lettura 


