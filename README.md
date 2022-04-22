# Craps Game in C
*Questo esercizio è tratto dal Capitolo 9 di "Programmazione in C" di Kim N. King.*

Scrivete un programma che simuli il gioco *craps* che viene fatto con due dadi. Al primo lancio il giocatore vince se la somma dei dadi è 7 o 11. Il giocatore
perde se la somma è 2, 3 oppure 12. Qualsiasi altra uscita viene chiamata il "punto" e il gioco continua. Su tutte le giocate seguenti il giocatore vince se realizza 
nuovamente il "punto". Perde invece se ottiene un 7. Qualsiasi altro valore viene ignorato e il gioco continua. Alla fine di ogni partita il programma dovrà chiedere
all''utente se vuole giocare ancora. Nel caso in cui l'utente risponda diversamente da `y` o `Y`, il programma, prima di terminarsi, dovrà visualizzare il numero di 
vittorie e di perdite.

*Esempio*
```
You rolled: 8
Your point is 8
You rolled 3
You rolled 10
You rolled 8
You win!

Play again? n

Wins: 1 Losses: 0
```

Scrivete il vostro programma in modo che sia costituito da 3 funzioni: main, roll_dice e play_game. Questi sono i prototipi per le ultime due funzioni:
```C
int roll_dice(void);
bool play_game(void);
```
`roll_dice` dovrà generare due numeri casuali, ognuno compreso tra 1 e 6 e poi restituirne la somma. La funzione `play_game` invece dovrà giocare una partita di craps
(ovvero chiamare `roll_dice` per determinare l'esito di ogni lancio di dadi). La funzione dovrà restituire `true` se il giocatore vince, `false` se il giocatore perde. 
La funzione `play_game` dovrà anche essere responsabile della visualizzazione dei messaggi che mostrano gli esiti dei vari lanci. Il `main` dovrà chiamare ripetutamente
la funzione `play_game` tenendo traccia del numero di vittorie e del numero di sconfitte. Dovrà anche visualizzare i messaggi "you win" e "you lose". 

*Suggerimento*: usate la funzione rand per generare i numeri casuali.
