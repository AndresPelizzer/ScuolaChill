# PRD di ScuolaChill · Team Andres.exe

## Informazioni sul documento

| Voce         | Dettaglio                  |
| ------------ | -------------------------- |
| **Prodotto** | ScuolaChill                |
| **Team**     | Andres.exe                 |
| **Autori**   | Andres Pelizzer (1 membro) |
| **Versione** | 1.0                        |
| **Data**     | 08/10/2026                 |
| **Stato**    | Bozza                      |

### Storico delle versioni

| Versione | Data       | Autore          | Cosa è cambiato e perché |
| -------- | ---------- | --------------- | ------------------------ |
| 1.0      | 08/10/2026 | Andres Pelizzer | Prima stesura            |

---

# Prima parte · Il cosa

## Scopo e perimetro

### Perché esiste ScuolaChill

**Dal lato business.** In una scuola il materiale didattico, le verifiche e i voti passano spesso da strumenti diversi, e chi dirige l'istituto fatica ad avere una visione d'insieme. ScuolaChill riunisce tutto in un unico posto: il Direttore controlla l'andamento della scuola, i docenti gestiscono materiale, verifiche e voti e gli studenti trovano ciò che serve per studiare senza chiedere a nessuno.

**Dal lato tecnico.** ScuolaChill è una web app con tre ruoli, ognuno con permessi diversi. Il Direttore crea gli account e le classi e ha visibilità completa su ciò che accade nell'istituto. Il Docente carica il materiale didattico, crea verifiche e compiti e registra le valutazioni. Lo Studente consulta materiali, voti e pagella e svolge le verifiche e i compiti che gli vengono assegnati. Ogni utente accede con le proprie credenziali e può fare solo ciò che il suo ruolo prevede. Il sistema è utilizzabile sia da PC sia da smartphone.

### Cosa è incluso

**Il Direttore**

- crea gli account di docenti e studenti e disattiva l'accesso di un docente quando serve, senza cancellare ciò che ha scritto;
- crea le classi, vi assegna studenti e docenti con le rispettive materie e nomina per ogni classe un docente coordinatore;
- sposta uno studente da una classe a un'altra;
- crea e modifica l'orario dei docenti;
- consulta la vista complessiva della scuola, compresa la media dei voti di ogni classe, e legge in sola lettura le lezioni scritte dai docenti;
- pubblica circolari per studenti e docenti;
- scrive note sugli studenti;
- reimposta la password di un utente quando il recupero via email non funziona.

**Il Docente**

- carica il materiale didattico dei propri corsi;
- crea le proprie verifiche, assegna i voti alle verifiche consegnate e registra le interrogazioni orali;
- assegna compiti per casa con scadenza e allegati, e vede chi ha consegnato e chi in ritardo;
- scrive nell'agenda le lezioni svolte (descrizione e tipo di lezione);
- consulta il proprio orario;
- scrive annotazioni (per esempio compiti non fatti) e note sugli studenti;
- consulta i voti dei propri studenti e inserisce il voto finale intero della propria materia per la pagella;
- se è coordinatore di classe, consulta annotazioni e note degli studenti, inserisce il voto di comportamento e pubblica la pagella della classe.

**Lo Studente**

- vede nella pagina iniziale le lezioni del giorno, i voti ricevuti e le cose da fare, e accede ai propri corsi;
- consulta il materiale didattico dei propri corsi;
- svolge le verifiche assegnate alla propria classe, da computer;
- consulta i compiti e consegna i file richiesti (se la consegna è in ritardo viene segnata come tale);
- consulta i propri voti raggruppati per materia e la propria pagella;
- consulta l'agenda delle lezioni, le circolari e le proprie annotazioni e note.

**Tutti gli utenti**

- accedono con credenziali personali e vedono solo le funzioni del proprio ruolo;
- modificano il proprio profilo e cambiano la password;
- recuperano la password dimenticata tramite email.

### Cosa non è incluso

- **Gestione delle presenze e delle assenze.** Si assume che la scuola la gestisca già con un altro sistema (ASS-02).
- **Comunicazioni con le famiglie.** Servirebbe un quarto ruolo, la Famiglia, con account, collegamento allo studente e permessi propri. Per un progetto sviluppato da una sola persona il costo è troppo alto per la versione 1.0.
- **Valutazione dei compiti.** I compiti servono a esercitarsi e non hanno un voto. La valutazione resta alle verifiche e alle interrogazioni.
- **Modifica da parte del Direttore delle lezioni scritte dai docenti.** Ogni lezione può essere modificata solo da chi l'ha scritta, per mantenere affidabile il registro. Se un docente lascia la scuola, le sue lezioni restano invariate.
- **Minigame e chatbot di navigazione.** Idee per versioni future.

---

## Stakeholder

| Stakeholder                          | Cosa fa                                                                                                  | Cosa gli interessa                                                                                                                                            | Come lo coinvolgete                                                                                  |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Docente del corso                    | Valida il PRD e guida lo studente nello sviluppo di ScuolaChill                                          | Un PRD completo e coerente con la traccia, con ogni scelta motivata; scadenze rispettate; avanzamento regolare; codice di buona qualità                       | Presentazione del PRD e discussione sul progetto                                                     |
| Direttore                            | Usa ScuolaChill per gestire account, classi, orario e circolari, e valuta la qualità del prodotto finale | Avere sotto controllo classi, docenti, orari e andamento dei voti in pochi clic; dati degli studenti protetti; un sistema che non si ferma durante le lezioni | Test periodici dell'applicazione con raccolta di feedback                                            |
| Docenti                              | Usano l'applicativo ogni giorno e ne valutano la praticità                                               | Inserire voti, lezioni e compiti in poco tempo; interfaccia chiara che non richiede formazione lunga; nessun dato perso                                       | Interviste iniziali sul gestionale attualmente in uso e sessioni di test comparativo con ScuolaChill |
| Studenti                             | Usano l'applicativo ogni giorno                                                                          | Trovare subito voti, materiale e compiti; sistema veloce e usabile anche da telefono                                                                          | Test periodici con raccolta di feedback e confronto con il gestionale attualmente in uso             |
| Collaudatori del primo anno          | Testano l'applicazione e ne valutano la riuscita                                                         | Un'applicazione che si capisce senza spiegazioni e che funziona durante una verifica                                                                          | Sessioni di collaudo con raccolta di consigli                                                        |
| Scuola e ente gestore                | Approva l'adozione e sostiene i costi del sistema                                                        | Costi contenuti, dati degli studenti protetti, nessuna interruzione delle lezioni                                                                             | Presentazione dei costi stimati e del piano di deployment                                            |
| Sviluppatore e manutentore           | Costruisce e mantiene ScuolaChill                                                                        | Codice manutenibile, requisiti stabili, tempi realistici                                                                                                      | Revisione del PRD a ogni modifica dei requisiti                                                      |
| Famiglie (fuori perimetro nella 1.0) | Non usano ScuolaChill                                                                                    | Essere informate su voti e circolari                                                                                                                          | Nessuno nella 1.0; da valutare per una versione futura                                               |

---

## Destinatari e contesto d'uso

### La scuola di riferimento

Il CFP Don Bosco di San Donà di Piave, un centro di formazione professionale. I numeri sono stime, non dati ufficiali (ASS-01).

| Voce               | Valore                                                 |
| ------------------ | ------------------------------------------------------ |
| Numero di studenti | 500                                                    |
| Numero di docenti  | 40                                                     |
| Numero di classi   | 20 (circa 25 studenti per classe)                      |
| Orario scolastico  | 8:00 – 13:00, dal lunedì al venerdì                    |
| Connettività       | Wi-Fi scolastico condiviso, rete mobile degli studenti |

### Gli archetipi

| ID      | Archetipo | Contesto d'uso                                                                                                                                                                                                                           | Competenze digitali                                                        | Dispositivo principale                                                          | Frequenza d'uso                 |
| ------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------- |
| ARC-001 | Direttore | Dall'ufficio, con poco tempo a disposizione. Crea account e classi a inizio anno, gestisce l'orario, trasferisce studenti, controlla le medie delle classi e pubblica le circolari.                                                      | Medie: usa il computer ogni giorno, ma è poco esperto di strumenti tecnici | PC                                                                              | Ogni giorno, per brevi sessioni |
| ARC-002 | Docente   | In aula, tra una lezione e l'altra, e a casa per preparare materiali e correggere verifiche. Scrive l'agenda, assegna compiti e voti, annotazioni e voto finale di materia. Se è coordinatore, inserisce anche il voto di comportamento. | Da basse a medie: alcuni molto pratici, altri poco                         | PC in aula e a casa                                                             | Ogni giorno di lezione          |
| ARC-003 | Studente  | In aula e in laboratorio per le verifiche, in corridoio tra una lezione e l'altra, a casa per studiare e consegnare i compiti. Consulta materiale, agenda, voti, note e pagella.                                                         | Alte con lo smartphone, medie con il PC                                    | Smartphone in corridoio e a casa; PC in aula, in laboratorio e per le verifiche | Ogni giorno di lezione          |

---

## Panoramica e casi d'uso

### ScuolaChill in poche righe

ScuolaChill è un gestionale online che permette di gestire tutto ciò che riguarda la vita dell'istituto. Il Direttore controlla le lezioni dei docenti, organizza i loro orari, sposta gli studenti da una classe all'altra quando serve e comunica con tutti attraverso le circolari. I docenti caricano il materiale, creano verifiche e compiti, scrivono le lezioni e danno i voti. Gli studenti studiano, svolgono le verifiche, controllano voti e compiti e, a fine quadrimestre, anche la pagella.

### Come si presenta

Dopo l'accesso lo studente trova una **pagina iniziale** simile a quella di un registro elettronico: le lezioni del giorno in ordine di ora (per esempio _1ª ora · professoressa Bianchi · Scienze · esercizi sulla mole_), con accanto il voto se quel giorno è stato valutato o interrogato. Sotto ci sono le cose da fare entro quel giorno: compiti in scadenza e verifiche in programma. Può spostarsi su altri giorni, anche passati, per recuperare quanto è stato spiegato.

In un'altra sezione ci sono i **corsi**: uno per ogni materia della classe (per esempio _Scienze · 2A_). Entrando nel corso si trovano materiale, verifiche, compiti, voti e lezioni di quella materia. Il docente ha lo stesso schema, con un corso per ogni classe in cui insegna. La pagella e le circolari sono sezioni a parte.

### User flow e scenari

#### Studente

**STU-02 · Svolgere una verifica**

_User flow:_ accesso → pagina iniziale → corso → sezione Verifiche → verifica → risposte → consegna → conferma.

_Scenario principale._ Ambra, del primo anno, ha la verifica di scienze alle 9:00. Dal computer del laboratorio apre ScuolaChill, entra nel corso di Scienze e apre la verifica. Risponde alle domande e consegna prima dello scadere del tempo. Vede la conferma "Verifica consegnata".

_Scenari alternativi._

- La rete della scuola cade a metà verifica: le risposte già scritte restano salvate, Ambra riprende appena torna la connessione, e se il tempo scade prima la verifica si consegna da sola (FR-VER-02).
- Ambra apre la verifica anche in una seconda scheda: la seconda viene bloccata con un avviso (FR-VER-03).
- Ambra prova ad aprire la verifica dal telefono: vede un avviso che la verifica va svolta da computer (FR-VER-04).

**STU-03 · Consultare i propri voti**

_User flow:_ accesso → pagina iniziale con le lezioni del giorno e il voto accanto alla lezione, oppure corso → sezione Voti.

_Scenario principale._ Marco è stato interrogato in inglese. Appena il docente inserisce il voto, Marco lo vede nella pagina iniziale accanto alla lezione di inglese, per esempio "8", e poi nel corso di Inglese, sezione Voti, con l'indicazione di come è stato preso.

_Scenari alternativi._

- Marco non ha ancora nessun voto: vede un messaggio chiaro, non una pagina vuota.

**STU-06 · Consultare la pagella**

_User flow:_ accesso → sezione Pagella → voti finali di tutte le materie e voto di comportamento.

_Scenario principale._ A fine quadrimestre i docenti si riuniscono e inseriscono i voti finali. Il coordinatore pubblica la pagella della classe e Sara la apre dal telefono: vede tutte le materie e il comportamento.

_Scenari alternativi._

- La pagella non è ancora stata pubblicata: Sara vede un messaggio "La pagella non è ancora disponibile".

#### Docente

**DOC-03 · Assegnare i voti**

_User flow:_ accesso → corso della classe → verifica → elenco degli studenti che hanno consegnato → voto per ogni studente → conferma.

_Scenario principale._ Il professor Rossi corregge a casa le verifiche di meccanica. Quando ha finito, apre il corso della classe e per ogni studente sceglie il voto tra quelli disponibili (anche con +, − o ½). Gli studenti lo vedono subito.

_Scenari alternativi._

- Il professore si accorge di aver sbagliato un voto: lo corregge, e il nuovo valore sostituisce il vecchio (FR-VOT-02).
- Uno studente non ha consegnato la verifica: non compare tra quelli a cui assegnare un voto.
- Il professore interroga uno studente a voce: registra l'interrogazione con data e voto, e lo studente lo vede subito nella pagina iniziale (FR-VOT-03).

**DOC-04 · Compilare l'agenda delle lezioni**

_User flow:_ accesso → corso → agenda → descrizione e tipo di lezione → salvataggio.

_Scenario principale._ Al termine della lezione di sistemi, la professoressa Bianchi scrive "Introduzione ai database, spiegazione" nell'agenda del corso. Gli studenti assenti possono leggerla.

_Scenari alternativi._

- La professoressa dimentica di compilarla: può farlo anche dopo, aprendo la lezione di un giorno passato.

**DOC-08 · Inserire il voto di comportamento e pubblicare la pagella (coordinatore)**

_User flow:_ accesso → classe di cui è coordinatore → studente (con le annotazioni e le note, se ce ne sono) → voto di comportamento da 1 a 10 → conferma → pubblicazione della pagella della classe.

_Scenario principale._ Dopo il consiglio di classe, il professor Verdi inserisce il voto di comportamento di ogni studente della sua classe, tenendo conto delle annotazioni dei colleghi e delle note. Quando tutti i voti finali sono presenti, pubblica la pagella.

_Scenari alternativi._

- Uno studente non ha né annotazioni né note: il coordinatore inserisce comunque il voto.
- Manca il voto finale di una materia: il sistema indica quale e non permette di pubblicare.
- Il coordinatore è stato disattivato: la classe risulta senza coordinatore, e finché il Direttore non ne nomina uno nessuno può inserire il comportamento (FR-CLA-02).

#### Direttore

**DIR-03 · Creare classi e comporle**

_User flow:_ accesso → nuova classe → assegnazione degli studenti → assegnazione dei docenti con le materie → nomina del coordinatore.

_Scenario principale._ A settembre il Direttore crea la 2A, vi assegna 20 studenti e i docenti con le materie, e nomina un coordinatore. Per ogni materia si crea il corso, che docente e studenti vedono subito.

_Scenari alternativi._

- Il Direttore aggiunge alla 2A uno studente che è già nella 2B: il sistema mostra la classe attuale e chiede conferma ("Sposto Luca dalla 2B alla 2A? Non sarà più presente nella 2B"). Solo dopo la conferma lo studente passa nella nuova classe (FR-CLA-01).
- Il Direttore nomina coordinatore un docente che lo è già di un'altra classe: l'operazione riesce.

**DIR-05 · Gestire l'orario dei docenti**

_User flow:_ accesso → orario → assegnazione di un docente a una classe in una fascia oraria → salvataggio.

_Scenario principale._ Il Direttore assegna il professor Rossi alla 2A il lunedì dalle 8:00 alle 10:00, e lui lo vede subito nel suo orario.

_Scenari alternativi._

- Il Direttore assegna lo stesso docente a un'altra classe nella stessa fascia: il sistema rifiuta con un messaggio chiaro (FR-ORA-01).

**DIR-06 · Pubblicare circolari**

_User flow:_ accesso → sezione Circolari → titolo e testo → pubblicazione.

_Scenario principale._ La mattina il Direttore pubblica "Oggi alle 11:00 prova di evacuazione". Docenti e studenti la vedono nell'elenco delle circolari.

_Scenari alternativi._

- Il Direttore prova a pubblicare una circolare senza titolo: il sistema segnala il campo mancante e non pubblica.

---

## Requisiti funzionali

### Le user story della traccia

Gli acceptance criteria della traccia valgono tutti. Qui compaiono solo quelli aggiunti dal team, numerati di seguito a quelli della traccia.

| ID     | Storia                            | AC aggiunti dal team                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Note                                                                                    |
| ------ | --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| DIR-01 | Creare account docente            | **AC-04** · Dato che l'email delle credenziali non parte, Quando creo il docente, Allora l'account viene creato e risulta "credenziali non inviate", e posso reinviarle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | FR-UTE-01                                                                               |
| DIR-02 | Creare account studente           | **AC-04** · Dato che l'email delle credenziali non parte, Quando creo lo studente, Allora l'account viene creato e risulta "credenziali non inviate", e posso reinviarle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | FR-UTE-01                                                                               |
| DIR-03 | Creare classi e comporle          | **AC-04** · Dato che compongo una classe, Quando nomino un docente coordinatore, Allora può inserire il voto di comportamento degli studenti di quella classe.<br>**AC-05** · Dato che un docente è già coordinatore di una classe, Quando lo nomino coordinatore di un'altra, Allora l'operazione riesce.<br>**AC-06** · Dato che aggiungo a una classe uno studente già assegnata a un'altra, Quando confermo il trasferimento dopo l'avviso, Allora lo studente passa alla nuova classe, i voti già assegnati restano suoi e vede materiale e agenda della nuova classe.<br>**AC-07** · Dato che assegno un docente a una classe per una materia, Quando confermo, Allora viene creato il corso e docente e studenti lo vedono tra i propri corsi. | FR-CLA-01, FR-CLA-02                                                                    |
| DIR-04 | Vedere tutto                      | **AC-04** · Dato che apro la vista complessiva, Quando seleziono una classe, Allora vedo la media dei voti della classe.<br>**AC-05** · Dato che seleziono una classe, Quando apro l'agenda, Allora vedo in sola lettura le lezioni scritte dai docenti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                                         |
| DOC-01 | Caricare materiale didattico      | **AC-04** · Dato che carico un file, Quando non è di un formato ammesso o supera la dimensione massima, Allora il caricamento viene rifiutato con un messaggio chiaro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Formati e limite da fissare (per esempio PDF, immagini e documenti Office fino a 10 MB) |
| DOC-02 | Creare le proprie verifiche       | **AC-04** · Dato che almeno uno studente ha consegnato la verifica, Quando provo a modificarla, Allora l'operazione viene negata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | FR-VER-01                                                                               |
| DOC-03 | Assegnare i voti                  | **AC-04** · Dato che assegno un voto, Quando scelgo un valore tra quelli disponibili (da 1 a 10, con +, − e ½), Allora viene registrato e lo studente lo vede subito.<br>**AC-05** · Dato che un voto è stato assegnato da me, Quando lo correggo, Allora il nuovo voto sostituisce il precedente.<br>**AC-06** · Dato che il voto è stato assegnato da un altro docente, Quando provo a modificarlo, Allora l'operazione viene negata.<br>**AC-07** · Dato che ho interrogato uno studente a voce, Quando registro l'interrogazione con data e voto, Allora lo studente vede il voto nella pagina iniziale quel giorno e tra i voti della materia.                                                                                                   | FR-VOT-01, FR-VOT-02, FR-VOT-03                                                         |
| STU-01 | Consultare il materiale didattico | **AC-03** · Dato che un materiale è stato caricato da un docente poi disattivato, Quando apro il corso, Allora lo vedo ancora.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | FR-UTE-02                                                                               |
| STU-02 | Svolgere una verifica             | **AC-04** · Dato che sto svolgendo una verifica, Quando la connessione cade, Allora le risposte già scritte restano salvate e posso riprendere.<br>**AC-05** · Dato che il tempo è scaduto, Quando non ho consegnato, Allora la verifica viene consegnata con le risposte presenti.<br>**AC-06** · Dato che ho la verifica aperta in una scheda, Quando la apro in un'altra, Allora la seconda viene bloccata con un avviso.<br>**AC-07** · Dato che accedo da smartphone, Quando apro una verifica da svolgere, Allora vedo un avviso che va svolta da computer.                                                                                                                                                                                     | FR-VER-02, FR-VER-03, FR-VER-04                                                         |
| STU-03 | Consultare i propri voti          | **AC-03** · Dato che non ho ancora voti, Quando apro la pagina dei voti, Allora vedo un messaggio chiaro e non una pagina vuota.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                                                         |

### Le storie aggiunte dal team

**USR-01 · Accedere al sistema**

> Come utente voglio accedere con le mie credenziali così da usare solo le funzioni del mio ruolo.

- AC-01 · Dato che ho un account attivo, Quando inserisco credenziali corrette, Allora accedo e vedo solo le sezioni del mio ruolo.
- AC-02 · Dato che inserisco credenziali errate, Quando confermo, Allora ricevo un errore generico che non rivela se è sbagliata l'email o la password.
- AC-03 · Dato che il mio account è stato disattivato, Quando provo ad accedere, Allora l'accesso viene negato.

**USR-02 · Gestire il proprio profilo e la password**

> Come utente voglio modificare il mio profilo e cambiare la password così da mantenere i miei dati aggiornati e il mio account al sicuro.

- AC-01 · Dato che sono autenticato, Quando cambio la password inserendo quella attuale e una nuova valida, Allora la password è aggiornata e al prossimo accesso vale la nuova.
- AC-02 · Dato che la password attuale inserita è errata, Quando confermo, Allora il cambio viene rifiutato.
- AC-03 · Dato che sono autenticato, Quando provo a modificare il profilo di un altro utente, Allora l'operazione viene negata.

**USR-03 · Recuperare la password**

> Come utente voglio reimpostare la password tramite email così da rientrare nel mio account se la dimentico.

- AC-01 · Dato che non ricordo la password, Quando richiedo il recupero con la mia email, Allora ricevo un link per scegliere una nuova password.
- AC-02 · Dato che inserisco un'email non registrata, Quando richiedo il recupero, Allora vedo lo stesso messaggio di conferma (il sistema non rivela se l'email esiste).
- AC-03 · Dato che il link è scaduto o già usato, Quando lo apro, Allora la reimpostazione viene rifiutata e posso richiederne un altro.
- AC-04 · Dato che l'email non parte, Quando richiedo il recupero, Allora la richiesta non va persa e il Direttore può reimpostare la password dell'utente (FR-UTE-03).

**DIR-05 · Gestire l'orario dei docenti**

> Come Direttore voglio creare e modificare l'orario dei docenti così da sapere chi insegna in quale classe e in quale fascia oraria.

- AC-01 · Dato che sono autenticato come Direttore, Quando assegno un docente a una classe in una fascia oraria libera, Allora l'orario viene salvato e il docente lo vede.
- AC-02 · Dato che il docente ha già una lezione in quella fascia, Quando provo ad assegnarlo a un'altra classe, Allora l'operazione viene rifiutata con un messaggio chiaro.
- AC-03 · Dato che sono autenticato come Docente o Studente, Quando provo a modificare l'orario, Allora l'operazione viene negata.

**DIR-06 · Pubblicare circolari**

> Come Direttore voglio pubblicare circolari così da comunicare avvisi a studenti e docenti.

- AC-01 · Dato che sono autenticato come Direttore, Quando pubblico una circolare, Allora docenti e studenti la vedono nell'elenco.
- AC-02 · Dato che sono autenticato come Docente o Studente, Quando provo a pubblicare una circolare, Allora l'operazione viene negata.

**DIR-07 · Disattivare un docente**

> Come Direttore voglio disattivare l'accesso di un docente così da sostituirlo quando necessario, senza perdere ciò che ha scritto.

- AC-01 · Dato che disattivo un docente, Quando lui prova ad accedere, Allora l'accesso viene negato.
- AC-02 · Dato che un docente è stato disattivato, Quando consulto lezioni, voti e materiali che ha scritto, Allora sono ancora presenti e invariati.
- AC-03 · Dato che disattivo un docente coordinatore, Quando confermo, Allora il sistema segnala che la classe è senza coordinatore e il Direttore deve nominarne un altro.
- AC-04 · Dato che consulto l'elenco dei docenti, Quando non applico filtri, Allora vedo solo i docenti attivi, con un filtro per vedere anche i disattivati.

**DIR-08 · Scrivere note sugli studenti**

> Come Direttore voglio scrivere note sugli studenti così da segnalare comportamenti che osservo direttamente.

- AC-01 · Dato che sono autenticato come Direttore, Quando scrivo una nota su uno studente, Allora lo studente la vede tra le sue note.
- AC-02 · Dato che la nota è di un altro autore, Quando provo a modificarla o a cancellarla, Allora l'operazione viene negata.

**DOC-04 · Compilare l'agenda delle lezioni**

> Come Docente voglio scrivere la descrizione e il tipo di ogni lezione così da lasciare agli studenti un riferimento chiaro di quanto svolto.

- AC-01 · Dato che sono assegnato a una classe, Quando inserisco una lezione con descrizione e tipo, Allora gli studenti della classe la vedono nell'agenda.
- AC-02 · Dato che una lezione è di un altro docente, Quando provo a modificarla, Allora l'operazione viene negata.

**DOC-05 · Consultare il proprio orario**

> Come Docente voglio consultare il mio orario settimanale così da sapere in quale classe fare lezione.

- AC-01 · Dato che sono autenticato come Docente, Quando apro l'orario, Allora vedo le mie classi e le fasce orarie assegnate dal Direttore.
- AC-02 · Dato che apro l'orario, Quando provo a modificarlo, Allora l'operazione viene negata.
- AC-03 · Dato che apro la pagina iniziale in un giorno di lezione, Quando guardo le lezioni di oggi del mio orario, Allora posso scriverne la descrizione e il tipo direttamente da lì.

**DOC-06 · Scrivere annotazioni e note sugli studenti**

> Come Docente voglio scrivere annotazioni e note sugli studenti dei miei corsi così da tenere traccia di compiti non fatti e di comportamenti che influiscono sul voto di comportamento.

- AC-01 · Dato che insegno in una classe, Quando scrivo un'annotazione su uno studente di quella classe, Allora lo studente la vede.
- AC-02 · Dato che insegno in una classe, Quando scrivo una nota su uno studente di quella classe, Allora lo studente la vede.
- AC-03 · Dato che l'annotazione o la nota è mia, Quando la modifico o la cancello, Allora l'operazione riesce.
- AC-04 · Dato che l'annotazione o la nota è di un altro autore, Quando provo a modificarla o a cancellarla, Allora l'operazione viene negata.

**DOC-07 · Consultare i voti di uno studente**

> Come Docente voglio consultare i voti precedenti di uno studente nella mia materia così da calcolarne la media e capire se serve un'ulteriore valutazione.

- AC-01 · Dato che insegno una materia a una classe, Quando apro uno studente, Allora vedo i suoi voti nella mia materia e la media.
- AC-02 · Dato che lo studente non è della mia classe, Quando consulto i suoi voti, Allora l'operazione viene negata.

**DOC-08 · Inserire il voto di comportamento e pubblicare la pagella (coordinatore)**

> Come docente coordinatore voglio vedere annotazioni e note degli studenti della mia classe, inserire il voto di comportamento e pubblicare la pagella così da registrare la decisione presa con gli altri docenti.

- AC-01 · Dato che sono coordinatore della classe, Quando apro uno studente, Allora vedo le sue annotazioni e le sue note e posso inserire il voto di comportamento (intero da 1 a 10).
- AC-02 · Dato che non sono coordinatore di quella classe, Quando provo a inserire il voto di comportamento, Allora l'operazione viene negata.
- AC-03 · Dato che tutte le materie hanno il voto finale e il comportamento è inserito, Quando pubblico la pagella della classe, Allora gli studenti la vedono.
- AC-04 · Dato che manca almeno un voto finale o un voto di comportamento, Quando provo a pubblicare la pagella, Allora il sistema indica cosa manca e non pubblica.

**DOC-09 · Inserire il voto finale di materia in pagella**

> Come Docente voglio vedere la media di uno studente nella mia materia e inserire il voto finale intero così da registrare in pagella la decisione presa con gli altri docenti.

- AC-01 · Dato che insegno la materia a quella classe, Quando apro lo studente, Allora vedo la media (anche decimale) e posso inserire il voto finale da 1 a 10.
- AC-02 · Dato che non insegno quella materia a quella classe, Quando provo a inserire il voto finale, Allora l'operazione viene negata.

**DOC-10 · Assegnare compiti per casa**

> Come Docente voglio assegnare compiti con una scadenza e, se serve, degli allegati così da far esercitare gli studenti tra una lezione e l'altra.

- AC-01 · Dato che insegno in un corso, Quando creo un compito con titolo, descrizione e scadenza (e allegati facoltativi), Allora gli studenti del corso lo vedono con la scadenza.
- AC-02 · Dato che gli studenti hanno consegnato, Quando apro il compito, Allora vedo chi ha consegnato, chi ha consegnato in ritardo, chi no e i file consegnati.
- AC-03 · Dato che il compito è di un altro docente, Quando provo a modificarlo, Allora l'operazione viene negata.

**STU-04 · Consultare la pagina iniziale e l'agenda**

> Come Studente voglio vedere le lezioni del giorno, i voti ricevuti e le cose da fare così da sapere subito cosa è successo e cosa devo preparare, anche se ero assente.

- AC-01 · Dato che sono autenticato come Studente, Quando apro la pagina iniziale in un giorno di lezione, Allora vedo le lezioni di oggi in ordine di ora, con materia, docente e descrizione della lezione se già scritta.
- AC-02 · Dato che oggi sono stato valutato o interrogato, Quando apro la pagina iniziale, Allora vedo il voto accanto alla lezione.
- AC-03 · Dato che ho compiti in scadenza o verifiche in programma quel giorno, Quando apro la pagina iniziale, Allora li vedo sotto le lezioni.
- AC-04 · Dato che scelgo un altro giorno, anche passato, Quando lo apro, Allora vedo le lezioni, i voti e le scadenze di quel giorno.
- AC-05 · Dato che in quel giorno non ci sono lezioni, Quando apro la pagina, Allora vedo un messaggio chiaro.
- AC-06 · Dato che l'agenda è di un'altra classe, Quando provo ad aprirla, Allora l'operazione viene negata.

**STU-05 · Consultare le circolari**

> Come Studente voglio consultare le circolari del Direttore così da essere informato su avvisi e cambiamenti.

- AC-01 · Dato che il Direttore ha pubblicato una circolare, Quando apro le circolari, Allora la vedo.
- AC-02 · Dato che sono autenticato come Studente, Quando provo a pubblicare una circolare, Allora l'operazione viene negata.

**STU-06 · Consultare la pagella**

> Come Studente voglio consultare la mia pagella con i voti delle materie e il voto di comportamento così da avere il quadro completo.

- AC-01 · Dato che la pagella è stata pubblicata, Quando la apro, Allora vedo i voti finali di tutte le materie e il voto di comportamento.
- AC-02 · Dato che la pagella non è ancora stata pubblicata, Quando apro la sezione, Allora vedo un messaggio che non è ancora disponibile.
- AC-03 · Dato che provo ad aprire la pagella di un altro studente, Quando confermo, Allora l'operazione viene negata.

**STU-07 · Consultare le proprie annotazioni e note**

> Come Studente voglio consultare le annotazioni e le note che mi riguardano così da sapere come vengono valutati i miei comportamenti.

- AC-01 · Dato che ho annotazioni o note, Quando apro la sezione, Allora vedo solo le mie.
- AC-02 · Dato che provo a vedere quelle di un altro studente, Quando confermo, Allora l'operazione viene negata.

**STU-08 · Consultare e consegnare i compiti**

> Come Studente voglio vedere i compiti assegnati e consegnare i file richiesti così da svolgerli entro la scadenza.

- AC-01 · Dato che il docente ha assegnato un compito al mio corso, Quando lo apro, Allora vedo descrizione, scadenza e allegati e posso consegnare uno o più file.
- AC-02 · Dato che ho già consegnato, Quando consegno di nuovo prima della scadenza, Allora la nuova consegna sostituisce la precedente.
- AC-03 · Dato che la scadenza è passata, Quando consegno, Allora la consegna viene accettata e segnata come in ritardo.
- AC-04 · Dato che il file non è di un formato ammesso o supera la dimensione massima, Quando lo carico, Allora il caricamento viene rifiutato con un messaggio chiaro.
- AC-05 · Dato che il compito appartiene a un'altra classe, Quando provo ad aprirlo, Allora l'operazione viene negata.

### Le decisioni lasciate aperte dalla traccia

**FR-VOT-01 · Scala dei voti** (collegato a DOC-03, DOC-09)
Per le verifiche il docente sceglie tra i voti da 1 a 10, ognuno con le varianti "+", "−" e "½". Per la media si usa questa convenzione: + = +0,25, ½ = +0,5, − = −0,25. I voti in pagella (voto finale di materia e voto di comportamento) sono interi da 1 a 10, senza segni.
_Motivazione:_ i docenti valutano le verifiche con sfumature, mentre la pagella ufficiale usa solo interi.

**FR-VOT-02 · Correzione dei voti** (collegato a DOC-03)
Un docente può correggere solo i voti che ha assegnato lui. Il nuovo voto sostituisce il precedente e lo studente lo vede subito.
_Motivazione:_ ogni valutazione ha un solo responsabile, e lo studente non deve aspettare per vedere un voto.

**FR-VOT-03 · Interrogazioni orali** (collegato a DOC-03, STU-04)
Il docente può registrare un'interrogazione a voce indicando studente, data e voto, senza che esista una verifica svolta nell'applicazione. Il voto compare allo studente nella pagina iniziale del giorno e tra i voti della materia.
_Motivazione:_ nella scuola reale molti voti nascono da interrogazioni e non da verifiche scritte.

**FR-CLA-01 · Trasferimento di uno studente fra classi** (collegato a DIR-03)
Solo il Direttore può spostare uno studente in un'altra classe. Quando aggiunge a una classe uno studente già assegnato a un'altra, il sistema mostra la classe attuale e chiede conferma, spiegando che lo studente non sarà più presente nella vecchia classe. Dopo la conferma i voti già assegnati restano allo studente, che vede materiale e agenda della nuova classe.
_Motivazione:_ i voti appartengono allo studente e non devono andare persi, e l'avviso evita spostamenti fatti per errore.

**FR-CLA-02 · Coordinatore di classe** (collegato a DIR-03, DIR-07)
Ogni classe ha un solo coordinatore, e un docente può coordinare più classi. Se il coordinatore viene disattivato, il Direttore ne nomina un altro.
_Motivazione:_ riproduce la scuola reale e tiene semplice il modello dei permessi.

**FR-ORA-01 · Orario senza sovrapposizioni** (collegato a DIR-05)
Un docente non può essere assegnato a due classi nella stessa fascia oraria, e una classe non può avere due docenti nella stessa fascia. Il sistema rifiuta l'assegnazione con un messaggio chiaro.
_Motivazione:_ nella scuola reale una persona non può essere in due luoghi nello stesso momento e una classe segue una lezione alla volta.

**FR-VER-01 · Modifica di una verifica dopo lo svolgimento** (collegato a DOC-02)
Una verifica non può più essere modificata quando almeno uno studente l'ha consegnata.
_Motivazione:_ gli studenti devono essere valutati sulle stesse domande.

**FR-VER-02 · Connessione che cade durante una verifica** (collegato a STU-02)
Le risposte vengono salvate mentre lo studente le scrive. Se la connessione cade, può riprendere dal punto in cui era, finché dura il tempo. Allo scadere del tempo la verifica si consegna da sola con le risposte presenti.
_Motivazione:_ lo studente non deve perdere il lavoro per un problema di rete, e le verifiche devono finire comunque.

**FR-VER-03 · Verifica aperta su due schede** (collegato a STU-02)
Se lo studente apre la stessa verifica in una seconda scheda, la seconda viene bloccata con un avviso.
_Motivazione:_ evita risposte che si sovrascrivono a vicenda e consegne duplicate.

**FR-VER-04 · Verifiche solo da computer** (collegato a STU-02)
Le verifiche si svolgono solo da computer. Da smartphone lo studente vede un avviso e può comunque usare tutte le altre funzioni.
_Motivazione:_ scrivere le risposte e rivedere il proprio lavoro su uno schermo piccolo è scomodo e aumenta gli errori.

**FR-COM-01 · Compiti per casa** (collegato a DOC-10, STU-08)
Il docente assegna un compito con titolo, descrizione, scadenza e allegati facoltativi. Lo studente consegna uno o più file e può sostituire la consegna. Se consegna dopo la scadenza, la consegna viene accettata e segnata come in ritardo. Il docente vede chi ha consegnato, chi in ritardo e chi no. I compiti non hanno un voto.
_Motivazione:_ i compiti servono a esercitarsi; la valutazione resta alle verifiche, e un compito non fatto può essere segnalato con un'annotazione. Accettare la consegna in ritardo evita che un problema di tempo faccia perdere il lavoro svolto.

**FR-UTE-01 · Email delle credenziali non inviata** (collegato a DIR-01, DIR-02)
L'account viene creato comunque e risulta "credenziali non inviate". Il Direttore può reinviarle.
_Motivazione:_ un servizio esterno che fallisce non deve bloccare il lavoro del Direttore.

**FR-UTE-02 · Docente disattivato** (collegato a DIR-07)
Disattivare un docente blocca il suo accesso ma non cancella nulla di ciò che ha scritto. Le sue lezioni, i suoi voti e i suoi materiali restano invariati e nessun altro li modifica.
_Motivazione:_ l'integrità del registro e dello storico degli studenti.

**FR-UTE-03 · Recupero password con email non funzionante** (collegato a USR-03)
Se l'email di recupero non parte, il Direttore può reimpostare la password dell'utente.
_Motivazione:_ nessun utente resta bloccato per un problema del servizio email.

**FR-NOT-01 · Annotazioni e note** (collegato a DIR-08, DOC-06, DOC-08)
Le annotazioni riguardano l'attività scolastica (per esempio compiti non fatti) e le scrivono solo i docenti. Le note riguardano il comportamento (per esempio lanciare una sedia, copiare in una verifica, rompere una finestra) e le possono scrivere sia i docenti sia il Direttore. Ognuno modifica e cancella solo ciò che ha scritto. Annotazioni e note contano nel voto di comportamento.
_Motivazione:_ il Direttore non segue le lezioni e non controlla i compiti, quindi scrive solo note su ciò che osserva direttamente; i docenti vedono entrambe le situazioni in aula.

**FR-PAG-01 · Pagella** (collegato a DOC-08, DOC-09, STU-06)
Il voto finale di ogni materia lo inserisce il docente di quella materia, il voto di comportamento il coordinatore. La media dei voti è il riferimento principale per il voto finale, ma la decisione resta ai docenti, che possono arrotondarla in eccesso o in difetto. Il coordinatore pubblica la pagella della classe solo quando tutte le materie e il comportamento sono presenti, e solo da quel momento gli studenti la vedono.
_Motivazione:_ la media è la base oggettiva, l'arrotondamento è una valutazione dei docenti, e gli studenti non devono mai vedere una pagella incompleta.

---

## Requisiti non funzionali

| ID     | Famiglia      | Requisito                            | Soglia e condizione                                                                                                                                                                                                                                                           | Come si verifica                                           | Storie collegate               |
| ------ | ------------- | ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------ |
| NFR-01 | Prestazioni   | Apertura della verifica nel picco    | Meno di 2 s per il 95% delle richieste, con 75 studenti che aprono la verifica nello stesso minuto                                                                                                                                                                            | Test di carico con utenti simulati                         | STU-02                         |
| NFR-02 | Prestazioni   | Consegna della verifica nel picco    | Meno di 3 s per il 95% delle consegne, con 75 studenti che consegnano nello stesso minuto                                                                                                                                                                                     | Test di carico con utenti simulati                         | STU-02                         |
| NFR-03 | Prestazioni   | Registrazione di un voto             | Meno di 3 s tra la conferma del docente e la visibilità allo studente                                                                                                                                                                                                         | Test di carico con utenti simulati                         | DOC-03                         |
| NFR-04 | Prestazioni   | Vista complessiva del Direttore      | Meno di 3 s con tutte le 20 classi e 500 studenti                                                                                                                                                                                                                             | Test di carico con utenti simulati                         | DIR-04                         |
| NFR-05 | Sicurezza     | Password protette                    | Nessuna password è salvata in chiaro e nessuno, nemmeno il Direttore, può leggerla                                                                                                                                                                                            | Revisione del codice e controllo dei dati salvati          | USR-01, USR-02                 |
| NFR-06 | Sicurezza     | Controllo dei ruoli                  | Se un utente prova a fare qualcosa che il suo ruolo non permette, anche in un modo non previsto dall'interfaccia (per esempio scrivendo a mano un indirizzo), il sistema rifiuta sempre l'operazione. Si verifica un caso per ogni AC con "operazione negata": 100% rifiutati | Test automatici con un utente per ruolo                    | DIR-01, DIR-05, DOC-03, STU-06 |
| NFR-07 | Sicurezza     | Link di recupero password            | Valido 60 minuti e utilizzabile una sola volta                                                                                                                                                                                                                                | Test manuale e automatico                                  | USR-03                         |
| NFR-08 | Usabilità     | Accesso rapido ai contenuti          | Materiale, voti e compiti raggiungibili in al massimo due clic dalla pagina iniziale                                                                                                                                                                                          | Osservazione dei collaudatori                              | STU-01, STU-03, STU-08         |
| NFR-09 | Usabilità     | Uso da smartphone                    | Tutte le funzioni dello studente, tranne lo svolgimento delle verifiche, sono usabili su uno schermo largo 360 px senza scorrimento orizzontale                                                                                                                               | Prova su due dispositivi diversi                           | STU-01, STU-03, STU-06, STU-08 |
| NFR-10 | Usabilità     | Primo utilizzo senza aiuto           | Almeno il 90% dei collaudatori del primo anno svolge una verifica senza chiedere aiuto                                                                                                                                                                                        | Osservazione durante il collaudo                           | STU-02                         |
| NFR-11 | Usabilità     | Compilazione dell'agenda             | Un docente inserisce descrizione e tipo di una lezione in meno di 1 minuto, al primo utilizzo                                                                                                                                                                                 | Osservazione di un docente                                 | DOC-04                         |
| NFR-12 | Disponibilità | Raggiungibilità in orario scolastico | 99% di disponibilità dalle 8:00 alle 13:00 nei giorni di lezione (circa 1 ora di fermo al mese); gli aggiornamenti si fanno fuori orario scolastico                                                                                                                           | Monitoraggio mensile                                       | STU-02, DOC-03                 |
| NFR-13 | Disponibilità | Nessuna perdita di dati              | Zero voti persi; in caso di guasto si perdono al massimo 24 ore di dati                                                                                                                                                                                                       | Confronto tra voti inseriti e salvati; ripristino di prova | DOC-03, DOC-09                 |
| NFR-14 | Scalabilità   | Crescita della scuola                | Con la scuola raddoppiata (1.000 studenti, circa 270 utenti contemporanei nel picco massimo) il sistema regge aumentando solo le risorse, senza riscrivere il codice                                                                                                          | Test di carico con 270 utenti simulati                     | STU-02                         |
| NFR-15 | Ambientale    | Rete e dispositivi                   | Funziona dalla rete Wi-Fi della scuola e da rete mobile, e sulle ultime due versioni di Chrome, Edge, Firefox e Safari                                                                                                                                                        | Prova manuale su rete scolastica e 4G                      | STU-02, DOC-04                 |
| NFR-16 | Supporto      | Aiuto per chi non riesce ad accedere | Il Direttore risolve il problema di accesso di un utente entro un giorno lavorativo; i problemi tecnici segnalati sono presi in carico dallo sviluppatore entro il giorno lavorativo successivo                                                                               | Registro delle richieste di aiuto                          | USR-01, USR-03                 |
| NFR-17 | Supporto      | Diagnosi dei problemi                | Ogni errore del sistema viene registrato con data, ora e utente, e si può consultare per 30 giorni                                                                                                                                                                            | Controllo dei registri dopo un errore provocato            | DOC-03, STU-02                 |
| NFR-18 | Interazione   | Servizio email esterno               | Le credenziali e i link di recupero partono entro 1 minuto per il 95% degli invii; se l'invio fallisce non si perde nulla (FR-UTE-01)                                                                                                                                         | Prova con servizio email disattivato                       | DIR-01, DIR-02, USR-03         |
| NFR-19 | Conformità    | Protezione dei dati personali        | I dati degli studenti (in gran parte minorenni) sono accessibili solo ai ruoli autorizzati e ospitati nell'Unione Europea                                                                                                                                                     | Checklist GDPR e controllo dei permessi                    | Tutte                          |
| NFR-20 | Prestazioni   | Caricamento di file                  | Un file fino a 10 MB (materiale o consegna di un compito) si carica in meno di 30 s dalla rete scolastica                                                                                                                                                                     | Prova con file di dimensione massima                       | DOC-01, STU-08                 |

### Requisiti trasversali della traccia

| ID      | Requisito                                                                                  | Come si verifica                                             |
| ------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| NFR-T01 | Tutto il traffico fra frontend e backend viaggia su HTTPS                                  | Controllo del certificato e blocco delle richieste in chiaro |
| NFR-T02 | Gli elenchi di studenti, materiali e voti sono paginati                                    | Test con più elementi della dimensione di una pagina         |
| NFR-T03 | Le API principali sono documentate con OpenAPI/Swagger e coperte da una collezione Postman | Esecuzione della collezione                                  |
| NFR-T04 | Gli errori hanno un formato uniforme e codici HTTP coerenti                                | Confronto delle risposte di errore                           |
| NFR-T05 | L'applicazione ha due configurazioni, Development e Production, senza segreti nel codice   | Revisione del repository                                     |
| NFR-T06 | Il sistema è raggiungibile pubblicamente per il collaudo                                   | Accesso da una rete esterna                                  |

### Requisiti impliciti

Sezione da completare dopo un'intervista a uno studente del primo anno (DIP-05), con la domanda "Cosa daresti per scontato che un'app di questo tipo faccia sempre, o non faccia mai?".

---

## Assunzioni, vincoli e dipendenze

### Assunzioni

| ID     | Assunzione                                                                                                                                                                                                   | Cosa succede se è falsa                                                                                          |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| ASS-01 | La scuola ha circa 500 studenti, 20 classi (circa 25 studenti per classe) e 40 docenti                                                                                                                       | Il dimensionamento e le soglie degli NFR vanno rifatti                                                           |
| ASS-02 | Le presenze e le assenze sono già gestite con un altro sistema della scuola                                                                                                                                  | Va aggiunta una funzione di gestione delle presenze e il perimetro cambia                                        |
| ASS-03 | La scuola usa già un gestionale per voti e lezioni, e docenti e studenti lo conoscono                                                                                                                        | Il confronto con il sistema attuale previsto nei test non è possibile e docenti e studenti vanno formati da zero |
| ASS-04 | Le lezioni vanno dalle 8:00 alle 13:00, dal lunedì al venerdì, e il picco di una verifica è di tre classi (circa 75 studenti) che iniziano nello stesso minuto                                               | I requisiti di prestazioni e di disponibilità vanno rivisti                                                      |
| ASS-05 | Il Wi-Fi della scuola è stabile e non blocca l'accesso al sistema, e la scuola ha computer a sufficienza (aula informatica o portatili) per far svolgere una verifica a una classe                           | I requisiti ambientali vanno rivisti e le verifiche da computer (FR-VER-04) non sono praticabili                 |
| ASS-06 | Il voto di comportamento viene registrato dal coordinatore di classe, dopo una discussione tra i docenti fuori dal sistema                                                                                   | Il ruolo del coordinatore e i permessi di DOC-08 vanno rivisti                                                   |
| ASS-07 | Un docente può coordinare più classi                                                                                                                                                                         | FR-CLA-02 va cambiato in una sola classe per docente                                                             |
| ASS-08 | Gli studenti sono in gran parte minorenni, e le famiglie ricevono le informazioni dalla scuola o dagli studenti, non da ScuolaChill                                                                          | Serve il ruolo Famiglia e il perimetro cambia                                                                    |
| ASS-09 | In media il 5% degli studenti e il 25% dei docenti sono connessi nello stesso momento; all'inizio della giornata e alla pubblicazione delle pagelle si connette circa il 25% degli studenti nei primi minuti | La stima del carico va rifatta                                                                                   |

### Vincoli

| ID     | Vincolo                                                                                                                    | Da dove viene        |
| ------ | -------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| VIN-01 | Il PRD va validato prima di scrivere il codice                                                                             | Traccia del progetto |
| VIN-02 | Gli acceptance criteria della traccia sono il minimo: si possono aggiungere, non togliere                                  | Traccia del progetto |
| VIN-03 | Il sistema deve essere raggiungibile pubblicamente su un'infrastruttura cloud per il collaudo con i ragazzi del primo anno | Traccia del progetto |
| VIN-04 | Il controllo dei ruoli deve stare nel backend, e non solo nell'interfaccia                                                 | Traccia del progetto |
| VIN-05 | I dati degli studenti minorenni vanno trattati secondo il GDPR                                                             | Normativa            |
| VIN-06 | Il progetto è sviluppato da una sola persona, nel tempo del corso e in parallelo con lo stage                              | Contesto del corso   |

### Dipendenze

| ID     | Dipendenza                                                                                                        | Serve entro                         | Chi se ne occupa           |
| ------ | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------- | -------------------------- |
| DIP-01 | Servizio email esterno attivo e configurato per credenziali e recupero password                                   | Prima del collaudo                  | Andres                     |
| DIP-02 | Account sul provider cloud con credito o budget sufficiente                                                       | Prima della prima versione in cloud | Andres                     |
| DIP-03 | Disponibilità dei ragazzi del primo anno per il collaudo, del Direttore e di un docente                           | Collaudo                            | Docente del corso e Andres |
| DIP-04 | Conferme del docente sui punti incerti (presenze, gestionale in uso, comportamento, pagella, numeri della scuola) | Validazione del PRD                 | Andres                     |
| DIP-05 | Intervista a uno studente del primo anno per i requisiti impliciti                                                | Prima della validazione del PRD     | Andres                     |

---

# Seconda parte · Il come

## Stima del carico

### Utenti concorrenti

| Situazione                      | Utenti concorrenti | Da dove viene il numero                                                              |
| ------------------------------- | ------------------ | ------------------------------------------------------------------------------------ |
| Uso normale durante la giornata | circa 35           | 5% dei 500 studenti (25) più 25% dei 40 docenti (10), ASS-09                         |
| Inizio giornata (8:00-8:15)     | circa 135          | 25% degli studenti apre la pagina iniziale nei primi 10 minuti (125), più 10 docenti |
| Picco delle 9:00 (verifiche)    | circa 78           | 3 classi da 25 studenti (75) più 3 docenti                                           |
| Fine quadrimestre, voti finali  | circa 40           | I 40 docenti inseriscono i voti nella stessa sessione                                |
| Pubblicazione delle pagelle     | circa 125          | 25% degli studenti apre la pagella nei primi minuti                                  |
| Scuola raddoppiata (NFR-14)     | circa 270          | Il doppio del picco massimo (135)                                                    |

### Profilo di carico

| Operazione                                      | Frequente?                | Pesante? | Critica? | Note                                                                                                                         |
| ----------------------------------------------- | ------------------------- | -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Login                                           | Sì, soprattutto alle 8:00 | No       | Sì       | Senza accesso nessuna funzione è utilizzabile                                                                                |
| Pagina iniziale (lezioni del giorno)            | Sì                        | No       | No       | È la pagina più visitata, riassume pochi dati                                                                                |
| Apertura della verifica                         | Solo durante le verifiche | Media    | Sì       | 75 studenti nello stesso minuto (NFR-01)                                                                                     |
| Salvataggio delle risposte                      | Sì, durante le verifiche  | No       | Sì       | Con un salvataggio ogni 30 secondi per studente sono circa 2,5 salvataggi al secondo; lo studente non deve perdere il lavoro |
| Consegna della verifica                         | No                        | Media    | Sì       | 75 consegne vicine alla scadenza (NFR-02)                                                                                    |
| Consultazione dei voti                          | Sì                        | No       | No       | Letture semplici                                                                                                             |
| Inserimento di un voto                          | Sì, dopo le verifiche     | No       | Sì       | Nessun voto deve andare perso (NFR-13)                                                                                       |
| Dashboard del Direttore                         | No, poche volte al giorno | Sì       | No       | Aggrega i voti di 500 studenti (NFR-04)                                                                                      |
| Caricamento di materiale e consegna dei compiti | Media                     | Sì       | No       | File fino a 10 MB (NFR-20)                                                                                                   |
| Pubblicazione e consultazione della pagella     | Rara, a fine quadrimestre | No       | Sì       | Circa 125 aperture nei primi minuti                                                                                          |

### Volumi di dati (stima per anno scolastico)

| Dato                        | Stima        | Da dove viene il numero                                       |
| --------------------------- | ------------ | ------------------------------------------------------------- |
| Voti                        | circa 50.000 | 500 studenti, 10 materie, circa 10 voti all'anno per materia  |
| Lezioni scritte nell'agenda | circa 20.000 | 20 classi, circa 5 ore al giorno, circa 200 giorni di scuola  |
| Materiale didattico (file)  | circa 2 GB   | 40 docenti, circa 50 MB ciascuno                              |
| Consegne dei compiti (file) | circa 25 GB  | 500 studenti, circa 50 consegne all'anno, circa 1 MB ciascuna |

I dati di testo (voti, lezioni, annotazioni) occupano poche decine di MB, mentre quasi tutto lo spazio è dei file. Questa stima serve per il dimensionamento e per i costi.
