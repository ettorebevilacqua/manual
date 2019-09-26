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
Alice togliti il pigiama, prendi la prima gonna a destra nel armadio e infilatela e allacciala, prendi la maglietta nel secondo cassetto e infilatela alzando le braccia, prendi le calze nel terzo cassetto, e mettile , prendi le scarpe sotto il letto e allacciale.
```
Mettere a posto i giocattoli :
```sh
Alice, dal cesto vai dritto e  prendi il trenino che incontri con la mano destra lo prendi torni indietro e lo butto nel cesto, poi fai un passo avanti ti giri di 90 vai avanti e con la mano destra prendi la bambola prosegui e con la mano sinistra prendi la corda , girati e vai verso la cesta , butta dentro quello che hai nella mano sinistra e destra. 
```

anche qui abbiamo un elenco di azioni sequenziali imperative, ma il concetto è questo, io ad alice mi devo limitare a dire :
```sh
Alice , metti a posto i giocatolli e quando hai finito vestiti . 
```
leggo la frase , e chiamo ... le funzioni metti_a_posto, e vestiti come scrivere come nome, con condizione di sequenza, si preferisce fa mettere a posto prima i giocatolli , magari cosi si trovano in meno disordine i vestiti (in programmazione potrebe essere una lista con meno elementi da ciclare per ottimizzare). 

il nome delle funzioni e la conoscenza anche solo di cosa servono senza guardare il come, mi bastano e avanzano per capire tutto. 
nel mondo reale significa che alice, una volta che ha imparato a vestirsi e mettere a posto i giocattoli (funzioni di libreria), io mi limiterò a dirgli COSA deve fare e non COME deve farlo, che è quello che mi interessa, domani insegnerò nuove "tecniche" per mettere a posto i giocattoli, quindi estenderò quella funzione, ma per mettere a posto sempre allo stesso modo dirò. 

questo è l'esempio più facile per comprendere il cambio di paradgma concetualle con la programmazione funzionale, fare esempi di questo tipo, sui piccoli problemi , limita però il far notare i vantaggi.
per intenderci alla fine dei giochi, se proseguiamo l'esempio, arrivamo a :

Alice : svegliati, metti a posto, lavati, vestiti, prepara la cartella, vai a scuola , torna da scuola, mangia , riposa, fai i compiti, gioca, ecc ecc 
estendendo ancora e seguendo il concetto di prima funzionale rispetto al imperativo , inizierò a leggere su un programma per alice più esteso :

preparati per andare a scuola , mangia e preparati a fare i compiti e fai i compiti (che siginifica preparati = riposati e finitio di riposare fai i compiti) , per poter giocare (fare i compiti implica farli tutti, come specificato "dentro" la funzione fare_compiti, e dove come farli di specifico non rientra nel problema più generale di azioni da fare.

elencare minuziosamente invece , passaggio dopo passaggio, comportava di dover leggere una sorta di libro per capire cosa deve fare in generale alice , i commenti possono aiutare , ma nel caso più funzionale , non cè bisogno dei commenti, la giista nomenclatore da sola fa anche da commento se vogliamo.

  In altre parole , passiamo a una programmazione più 



diversamente, dovrei fare tutto l'elenco di metttere a posto i giocatoli e poi l'elenco di vestirsi.... 
cosi però nella lettura i due passaggi chiave legati tra loro : mettere a posto e poi vestirsi, come lettura vengono persi e mescolati nella seqenzialità. 
devo leggermi tutto per capire il mettere a posto e quindi vestirsi banalmente, se codice di altri e non conosco bene il (vestirsi) la mia lettura 


