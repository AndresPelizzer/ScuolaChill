# PRD di ScuolaChill · Team [Andres.exe]

Prodotto | ScuolaChill
Team | Andres.exe
Autori | Andres Pelizzer (Numero membri : 1)
Versione | 1.0
Data | 23/09/2026
Stato | Bozza

# Storico delle versioni

Versione | 1.0
Data | 23/09/2026
Autore | Andres
Cambiamenti | Nessuno (Prima stesura)

# Prima parte · Il cosa

# Scopo e perimetro

# Perché esiste ScuolaChill

# Dal lato business

L'applicazione ScuolaChill è un gestionale scolastico utilizzabile da studenti, docenti e direttore. Questo software permette di dirigere le attività principali dell'istituto come inserimento e visualizzazione delle valutazioni o come la gestione delle presenze in aula. É disponibile anche la versione mobile di ScuolaChill.

# Dal lato tecnico

Dal punto di vista tecnico, si tratta di un applicazione fullstack costituita da 3 ruoli: direttore, che possiede controllo completo su ciò che accade all'interno dell'istituto, docente , che oltre a creare materiale didattico e verifiche può registrare le valutazioni , e studente. Quest'ultimo potrà svolgere le verifiche assegnatogli e consultare materiali e voti.

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
