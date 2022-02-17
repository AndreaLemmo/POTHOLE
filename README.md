# POTHOLE

[Board Jira](https://natour21.atlassian.net/jira/software/projects/POT/boards/5)

## Descrizione sintetica
Realizzare un sistema client-server che consenta la racconta e l’interrogazione di informazioni riguardanti la presenza di irregolarità (buche) su di una superficie.

## Descrizione dettagliata
Il sistema deve memorizzare e rendere disponibile una lista di eventi generati dai clients riguardanti la rilevazione di una un repentino cambiamento dell’accelerazione lungo l’asse verticale che superi una soglia comunicata dal server in fase di connessione. Ciascun client è identificato da un nickname, scelto dall’utente.

Il sistema tramite il client deve offrire agli utenti i seguenti servizi:
- Permettere all’utente di avviare una sessione di registrazione eventi durante la quale il client si connette al server, riceve i parametri di soglia e comunica al server la posizione e il valore del cambiamento ogni volta che registra un nuovo evento.
- Mostrare all’utente la lista di tutti gli eventi registrati dal server in un certo raggio dalla propria posizione.

## Regole generali
Il server va realizzato in linguaggio C su piattaforma UNIX/Linux e deve essere ospitato online su Microsoft Azure. Il client va realizzato in linguaggio Java su piattaforma Android e deve fare utilizzo dei sensori di accelerazione. Client e server devono comunicare tramite socket TCP o UDP. Oltre alle system call UNIX, il server può̀ utilizzare solo la libreria standard del C. Il server deve essere di tipo concorrente, ed in grado di gestire un numero arbitrario di client contemporaneamente. Il server effettua il log delle principali operazioni (nuove connessioni, sconnessioni, richieste da parte dei client) su standard output.

## Richieste nella documentazione
- Guida alla compilazione e all'uso per il server e per il client.
- Sezione che illustri il protocollo al livello di applicazione utilizzato nelle comunicazioni tra client e server (non il protocollo TCP/IP).
- Sezione che descriva i dettagli implementativi giudicati più interessanti (con particolare riferimento alle system call del corso), eventualmente corredati dai corrispondenti frammenti di codice.
- Sezione che descriva i dettagli implementativi del client e che mostri le classi realizzate per implementare la comunicazione client-server, eventualmente usando degli artefatti.
