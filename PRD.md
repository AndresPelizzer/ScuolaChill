# PRD di ScuolaChill · Team Andres.exe

## Informazioni sul documento

|              | Valore                     |
| ------------ | -------------------------- |
| **Prodotto** | ScuolaChill                |
| **Team**     | Andres.exe                 |
| **Autori**   | Andres Pelizzer (1 membro) |
| **Versione** | 1.0                        |
| **Data**     | 23/09/2026                 |
| **Stato**    | Bozza                      |

### Storico delle versioni

| Versione | Data       | Autore          | Cosa è cambiato e perché |
| -------- | ---------- | --------------- | ------------------------ |
| 1.0      | 23/09/2026 | Andres Pelizzer | Prima stesura            |

## Scopo e perimetro

### Perché esiste ScuolaChill

**Dal lato business.** In una scuola il materiale didattico, le verifiche e i voti
passano spesso da strumenti diversi, e chi dirige l'istituto fatica ad avere una
visione d'insieme. ScuolaChill riunisce tutto in un unico posto: il Direttore
controlla l'andamento della scuola, i docenti gestiscono materiale, verifiche e voti
senza lavoro doppio, gli studenti trovano ciò che serve per studiare senza chiedere
a nessuno.

**Dal lato tecnico.** ScuolaChill è un sistema web con tre ruoli, ognuno con permessi
diversi. Il Direttore crea gli account e le classi e ha visibilità completa su ciò
che accade nell'istituto. Il Docente carica il materiale didattico, crea le verifiche
e registra le valutazioni. Lo Studente consulta materiali e voti e svolge le verifiche
che gli vengono assegnate. Ogni utente accede con le proprie credenziali e può fare
solo ciò che il suo ruolo prevede. Il sistema è utilizzabile sia da PC sia da
smartphone.

### Cosa è incluso

**Il Direttore**

- crea gli account di docenti e studenti e disattiva l'accesso di un docente quando serve, senza cancellare ciò che ha scritto;
- crea le classi, vi assegna gli studenti e i docenti con le rispettive materie, e nomina per ogni classe un docente coordinatore;
- crea e modifica l'orario dei docenti;
- consulta la vista complessiva della scuola, compresa la media dei voti di ogni classe;
- pubblica le circolari per studenti e docenti, e può scrivere annotazioni sugli studenti.

**Il Docente**

- carica il materiale didattico per le proprie classi e materie;
- crea le proprie verifiche e assegna i voti agli studenti (numeri interi da 1 a 10);
- scrive nell'agenda le lezioni svolte (descrizione e tipo di lezione) e rivede quelle passate;
- scrive annotazioni sugli studenti;
- se è coordinatore di classe, consulta le annotazioni degli studenti della classe e inserisce il voto di comportamento per la pagella.

**Lo Studente**

- consulta il materiale didattico dei docenti della propria classe;
- svolge le verifiche assegnate alla propria classe;
- consulta i propri voti raggruppati per materia, la propria pagella e le proprie annotazioni;
- consulta l'agenda delle lezioni e le circolari.

**Per tutti**

- l'accesso avviene con credenziali personali, e ogni utente può fare solo ciò che il suo ruolo prevede.

### Cosa non è incluso

- **Gestione delle presenze e delle assenze.** Si assume che la scuola la gestisca già con un altro sistema (vedi Assunzioni).
- **Comunicazioni con le famiglie.** Servirebbe un quarto ruolo, la Famiglia, con account, collegamento allo studente e permessi propri. Per un progetto sviluppato da una sola persona il costo è troppo alto per la versione 1.0.
- **Modifica da parte del Direttore delle lezioni scritte dai docenti.** Ogni lezione può essere modificata solo da chi l'ha scritta, per mantenere affidabile il registro. Se un docente lascia la scuola, le sue lezioni restano invariate.
- **Minigame e chatbot di navigazione.** Idee per versioni future.

# STAKEHOLDER

# Stakeholder - Cosa fa - Cosa gli interessa - Come lo coinvolgete

Docente del corso - Valida PRD, aiuta studente con il progetto ScuolaChill - PRD efficiente, impegno costante durante realizzazione dell'applicazione, rispetto delle scadenze , buone pratiche nell'uso del codice - Presentazione PRD, discussione sul progetto ScuolaChill

Direttore - Valuta qualità prodotto finale - Applicativo efficiente,funzionale,sicuro e facilmente adoperabile da studenti e docenti - Test periodici dell'applicazione con aggiunta di feedback

Docenti - Utilizzano l'applicativo quotidianamente e ne valutano la praticità - Interfaccia intuitiva, assenza di bug , riduzione tempi di compilazione - Interviste iniziali sul vecchio gestionale e sessioni test comparativi con ScuolaChill

Studenti - Utilizzano l'applicativo quotidianamente - Applicativo performante , fruibile e interattivo - Test periodici del gestionale con raccolta feedback e confronto con il vecchio applicativo

Collaudatori del primo anno - Testano l'applicazione e ne valutano la buona riuscita - Applicativo finale efficiente e semplice da utilizzare - Facendo testare l'applicativo e dando dei consigli sulla buona riuscita

# DESTINATARI E CONTESTI D'USO

# La scuola che avete immaginato

Numero studenti - 500
Numero docenti - 20
Numero classi - 20
Orario - 8:00 - 13:00 , lunedi - venerdi
Connettività - Wifi scolastico condiviso, rete mobile degli studenti

# Gli archetipi

# ID - Archetipo - Contesto d'uso - Competenze digitali - Dispositivo principale - Frequenza

ARC001 - Direttore - Trasferimento studente da una classe ad un altra - ... - PC - ...
ARC002 - Studente - Visualizzazione materiale didattico - ... - PC in aula / Telefono in corridoio - ...
ARC003 - Docente - Inserimento valutazioni - ... - PC in aula/PC a casa - ...

# Panoramica e casi d'uso

# Scuola Chill in poche righe

ScuolaChill è un gestionale scolastico utilizzabile da direttore,docenti e studenti. Questo applicativo permette di gestire a 360° la vita quotidiana dell'istituto con valutazione degli studenti, inserimento e visualizzazione di circolari , solo per citarne alcune.

# USER STORY

# STU-001

- Come studente, voglio consultare il materiale messo a disposizione dai docenti, così da poter seguire le lezioni dal mio dispositivo personale

User Flow
SCENARIO POSITIVO
Faccio Login - entro all'interno del corso - visualizzo materiale
SCENARIO NEGATIVO
Faccio Login - entro all'interno del corso - non sono iscritto al corso! -> visualizzazione form - iscriviti per accedere

# STU-002

- Come studente, voglio visualizzare le valutazioni di una materia, così da verificare la mia conoscenza di un determinato argomento
  SCENARIO POSITIVO
  Faccio Login - entro all'interno del corso -> clicco sulla sezione Valutazioni - Visualizzo voti
  SCENARIO NEGATIVO
  Faccio Login - entro all'interno del corso -> clicco sulla sezione Valutazioni -> Connessione persa... - Rifare login

# STU-003

- Come studente, voglio poter consultare la bacheca della mia scuola, così da poter vedere le circolari
  SCENARIO POSITIVO
  Faccio Login - entro all'interno della bacheca cliccando sulla sezione "bacheca" - vedo circolari
  SCENARIO NEGATIVO
  Faccio Login - entro all'interno del corso -> clicco sulla sezione bacheca

# DIR-001

- Come direttore, voglio consultare il numero di studenti in una classe, così da poter sapere dove aggiungere o spostare un alunno

# DIR-002

- Come direttore, voglio poter licenziare un docente, così da poterlo sostituire nel caso fosse necessario

# DIR-003

- Come direttore, voglio poter inserire le circolari in bacheca, così da essere visualizzate da studenti e docenti

# DOC-001

- Come docente, voglio poter assegnare voti alle verifiche consegnate dai miei studenti, cosi dà poter valutare la loro conoscenza

# DOC-002

- Come docente, voglio poter visualizzare i voti precedenti di un determinato studente, cosi dà calcolarne la media e capire se è necessaria un ulteriore valutazione

# DOC-003

- Come docente, voglio poter visualizzare l'orario settimanale con le classe assegnatomi, cosi dà sapere in che classe fare lezione

# DOC-004

- Come docente, voglio poter inserire la descrizione e il tipo di lezione (spiegazione,interrogazione,ecc) così che i miei studenti abbiano un riferimento chiaro di quanto visto a lezione

# DOC-005

- Come docente, voglio poter visualizzare le lezioni passate , così dà avere un riepilogo chiaro di quanto svolto in classe

# DOC-006

- Come docente, voglio poter inserire delle annotazioni , così da punire lo studente abbassandogli il voto di comportamento

# Requisiti non funzionali

# ID - Famiglia - Requisito - Soglia e condizione - Come si verifica - Storie collegate

NFR-01 - Prestazioni - Aggiornamento voti - Meno di 3 secondi per aggiornare il voto - Test di carico - DOC-001

NFR-02 - Prestazioni - Apertura dell'orario nel picco - Almeno 5 docenti nello stesso minuto -
Test di carico - DOC-003

NFR-03 - Usabilità - Accesso veloce alla bacheca - Due tasti per accedere - Consulto con studente - STU-003

NFR-04 - Usabilità - Accesso veloce al registro studenti - Due tasti per accedere - Consulto con studente - DOC-002

NFR-05 - Usabilità - Accesso veloce al materiale dei docenti - Due tasti per accedere - Consulto con studente
