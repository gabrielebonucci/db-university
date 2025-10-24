Entità        |  Relazione        |  Tipo                              |  Spiegazione                                                                                      
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Dipartimenti  |  → Corsi Laurea   |  1 : N                             |  Un dipartimento offre più corsi di laurea                                                        
Corsi Laurea  |  → Corsi          |  1 : N                             |  Un corso di laurea prevede più corsi                                                             
Corsi         |  → Insegnanti     |  N : M tramite CORSI_INSEGNANTI    |  Ogni corso può essere tenuto da molteplici insegnanti, e viceversa                               
Corsi         |  → Appelli Esame  |  1 : N                             |  Un corso prevede più appelli d'esame                                                             
Corsi Laurea  |  → Studenti       |  1 : N                             |  Ogni studente è iscritto a un solo corso di laurea                                               
Studenti      |  → Appelli Esame  |  N : M tramite ISCRIZIONE_APPELLO  |  Ogni studente può iscriversi a diversi appelli d’esame e per ogni iscrizione è registrato il voto