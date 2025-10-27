Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

-----Ragionamento logico-----

Entità        |  Relazione        |  Tipo                              |  Spiegazione                                                                                      
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Dipartimenti  |  → Corsi Laurea   |  1 : N                             |  Un dipartimento offre più corsi di laurea                                                        
Corsi Laurea  |  → Corsi          |  1 : N                             |  Un corso di laurea prevede più corsi                                                             
Corsi         |  → Insegnanti     |  N : M tramite CORSI_INSEGNANTI    |  Ogni corso può essere tenuto da molteplici insegnanti, e viceversa                               
Corsi         |  → Appelli Esame  |  1 : N                             |  Un corso prevede più appelli d'esame                                                             
Corsi Laurea  |  → Studenti       |  1 : N                             |  Ogni studente è iscritto a un solo corso di laurea                                               
Studenti      |  → Appelli Esame  |  N : M tramite ISCRIZIONE_APPELLO  |  Ogni studente può iscriversi a diversi appelli d’esame e per ogni iscrizione è registrato il voto