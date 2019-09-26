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

Ho messo in luce , il problema della sequenzialità delle azioni che chiamamo il work flow del programma, cosa può cambiare pur avendo lo stesso esatto risultato, giusto per citare il problema delle prestazioni, dove cè chi storce il naso per un abbassamento di prestazioni, cosa che dipende dal linguaggio, e come volevo far mettere in luce, dalla stessa organizzazione del codice, dove la posizione inifluente per il risultato può incidere per le prestazioni. 

Vedremo poi come la programmazione funzionale ci può molto aiutare nella programmazione parallela sopratutto per organizzare diciamo cosi le prestazioni e sfruttarle meglio, per non dilunguarmi, in generale permettendoci di scrivere codice più ottimizzato e facilmente modificabile, si è più portati a scrivere codice più performante, quanto è facile scrivere codice poi lento per quanto veloce il linguaggio. 

Il problema delle prestazioni spesso è un non problema, se la programmazione funzionale non è cosi performante, allora non si dovrebbe usare java e il le pagine web con il suo pesante dom.

Sfato subito questo mito, perchè il discorso delle prestazioni, partendo dal fatto che un linguaggi tipo il java , può fare operazioni molto performanti perchè per esempio si limita a chiamare funzioni più pesanti scrite in linguaggio più performante, se non direttamente richiami a funzioni hardware come l'accelerazione grafica, le mie performance dipendono dal lavoro interno della mia funzione. 

La programmazzione funzionale, storicamente ha sofferto di perfomance rispetto sopratutto a un c++, contribuendo in questo a limitare il suo sviluppo, ma oggi partendo in realtà già da ieri dopo i primi sviluppi, molti linguaggi funzionali scrivono codice molto perfomante , e nei casi di programmazzione a task complessa e parallela, è molto più facile scrivere codice perfomante , semplice e senza problemi di eventuali e rognosi bug rispetto alla programmazione imperativa, potrei far capire questo concetto cosi : 

uno mi chiede , devo scrivere tal programma che sfrutta l' elaborazione parallela, che devo fare CIRCA  una certa cosa....  (attenzione al "circa", che ci comporterà modifiche delicate e  importanti poi al codice), e il programma è complesso e deve gestire molti input diversi.

posso scrivere anche con il c, ma quanto ci metto ?? ma ancor più importante , quanti bug e difficoltù dovrò affrontare ?? quanto è mission critical l'applicazione ?? quanto dovrò poi modificarla e ampliarla ??

insomma , come sempore la programmazione funzionale è migliore ?? dipende !!! 
nel caso esposto , è facile che senza ammattirmi e concentrandomi sul COSA DEVO FARE rispetto al come farlo, stando attento a tante cose, posso produrre anche in perfomance in prodotto migliore con la programmazione funzionale, rispetto a dover metterci 10 volte il lavoro (se non di più. più è grande il progetto) con maggiori probabilità di bug.

è un problema di costi, che alla fine si riduce in nei casi peggiori, mi costa più il software o l'hardware ?? quasi sempre più il sontware specie rispetto al passato o applicazioni per determinata famiglia di dispositivi.

in altre parole facilissimo che poi uno che si è ammazzato per guadagnare quel 20% o 30% che fosse, gli costa decine di volte , quanto invece raddoppiare l' hardware e quindi raddoppiare direttamente le prestazione , rispetto a 10 , magari viene a costare 0.5, non solo difficile discrepanze tali.

Aggiungiamo inoltre per finire il discorso, che molte applicazioni specie moderne, specie quelle legate d azioni utente, il vantaggio di prestazioni in genere non si sente, causa le lente azioni del utente su molte tipiche applicazioni che in genere utilizza, come per esempio i gestionali. 

Se sviluppo un gestionale, le prestazioni le troverò sulle librerie per l'output grafico, che di certo non andrò io a scrivere, i vantaggi li ho sulla logica della applicazione e le sempre più funzionalità , rispetto che l'utente vede quella appena più fluidità in più nel passare da schermata all'altra.

in pratica estendo il concetto di gestionali, le appliccazioni che prendono molto input diverso dal utente che poi verrà eleborato per essere visualizzato nei richiesti modi, stiamo parlando del più tipico grosso sviluppo che viene fatto oggi, considerando che anche un videogioco ha la sua parte "gestionale", nel suo sviluppo , per esempio a differenza del discorso fatto, si concentra il codice sulle prestazioni grafiche ed eleborative dei dati (es inteliggenza artificiale), ma nelle schermate di impostazioni, scelta missioni , magazzino ecc , che non precludono forte azione e variazione gradica continua, farle anche 10 di volte più lente rispetto alla azione di gioco, l' utente non nota nessuna differenza, non perderò certo tempo li a far notare agli occhi più fini , la fluidità della schermata delle impostazioni, l' utente la cercherà e apprezzarà sul gaming andasse pure molte lenta e bruttina ma funzionante, semmai migliorero nelle versioni successive , visto le lamentele sul gaming  !!

Tutto questo per dire , prestazioni ?? valuta bene se il caso di ammattirti, dove piuttosto concentrarti, quanto ti conviene in costi ecc ecc, in genere oggi per quello che tendenzialmente si sviluppa, ti cambia molto poco ed è meglio che investi in funzionalità e codice più facile da scrivere e mantenere, diversamente sei fortemente fuori mercato !! 










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

