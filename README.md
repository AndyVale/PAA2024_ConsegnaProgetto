Andrea Valentino Ricotti 5306194
Progetto "Scacchi in Unreal Engine 5.2" per il corso di Progettazione e Analisi di Algoritmi nell'anno accademico 2023/2024. 

Note riguardanti il progetto:

Sono state implementate le funzionalità di arrocco e cattura enpassant.

Le immagini utilizzate per i pezzi sono state quelle fornite su aulaweb.

La notazione delle mosse utilizzata per lo storyboard è quella estesa.

Il progetto deve avere come livello iniziale "MainMenu" (settato di default), così da poter selezionare il nemico contro il quale giocare (random o minimax).
Se non si dovesse passare da "MainMenu" ma si cariccasse direttamente il livello "BaseMap" verrà scelto in automatico il nemico random.
Durante il gioco è comunque possibile, solo durante il proprio turno o a fine partita, cambiare nemico.
Se si sceglie di farlo la partita attuale verrà persa (stato della scacchiera e storyboard), i punti verranno però mantenuti.

È possibile selezionare la pedina da muovere cliccando su essa.
Una volta selezionato verranno mostrate le mosse legali che la pedina può compiere.
Per annullare la selezione della pedina è sufficiente cliccare una qualsiasi casa non evidenziata della scacchiera.

È possibile utilizzare, durante il proprio turno, la funzione replay cliccando sulla mossa voluta nello storyboard.
Se la mossa in esame è una mossa avversaria è possibile a quel punto cambiare la propria mossa successiva (cancellando tutte le mosse successive ovviamente).
Così facendo eventuali punti acquisiti da mosse successive (vittoria di uno dei due giocatori) verranno mantenuti.

Al momento della promozione del pedone il pedone verrà promosso in automatico in un pezzo (regina ad esempio), comparirà però un widget accanto lo storyboard che deve essere cliccato per selezionare (o confermare) il pezzo desiderato.
Durante la promozione del pedone non è possibile nè utilizzare il replay nè cambiare nemico, va prima scelto il pezzo della promozione.

L'euristica utilizzata per il minimax è stata: materiale bianco - materiale nero.
Con questa scelta ho notato che il player si comporta piuttosto bene in middlegame mentre in apertura e quando i pezzi sono pochi non sempre effettua mosse soddisfacenti.
Per sopperire a questo problema ho iniziato a implementare delle evaluation board, matrici che forniscano un punteggio in base alla posizione di un pezzo nella scacchiera, per ragioni di tempistiche non sono riuscito a terminare lo sviluppo pertanto il codice sarà commentato.