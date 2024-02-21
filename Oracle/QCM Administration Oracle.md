# QCM Administration Oracle

Cochez la ou les bonnes réponses ou répondre, note SGIDB et au moins Oracle 12c

## Question 1 :

- [ ] Vous souhaitez créer une base de données appelée DBHQ.UNICE.FR (DB1 Head Quarter) avec deux bases de données enfichables (pluggable) : PDBVENTES et PDBCOMPTA. Cochez ce qui est juste <<
  - [ ] Avec le DBCA (Database Configurations Assistant) je peux créer en un seul trait les 3 bases

  - [ ] Avec le DBCA je peux créer PDBVENTES ou PDBCOMPTA
  - [ ] Avec le DBCA je peux ajouter au moment PDBVENTES ou PDBCOMPTA
  - [ ] L'ajout d'une nouvelle pluggable database n'est possible que par commande. Pas via l'interface graphique

## Question 2 :

- Supposons une container database appelée DBHQ.UNICE.FR. Elle contient au moins. <<
- [ ] Les tablespaces SYSTEM, SYSAUX, TEMP, UNDOTBS.- 
- [ ] Les fichiers de contrôles
- [ ] Les fichiers redolog
- [ ] Il est impossible d'y ajouter de nouveaux tablespaces

## Question 3 :

- Supposons une pluggable database PDBVENTES créée dans la container database appelée DBHQ.UNICE.FR. Elle contient au moins <<
- [ ] Les tablespaces SYSTEM, SYSAUX, TEMP, UNDOTBS.
- [ ] Les fichiers de contrôles
- [ ] Les fichiers redolog
- [ ] Il est impossible d'y ajouter de nouveaux tablespaces

## Question 4 :

- L'architecture de la CDB container Database DB1HQ.UNICE.FR permet <<
- [ ] D’économiser des ressources mémoires
- [ ] D’économiser l’espace disque
- [ ] D’augmenter la sécurité autour d’une base de données
- [ ] Un utilisateur connecté sur une base de données pluggable de cette CDB peut interroger sans problèmes les données contenues dans la CDB .

## Question 5 :

- Un checkpoint Oracle intervient dans les conditions suivantes <<
- [ ] Toutes les 3 secondes et Oracle vide le buffer de données et le buffer redolog
- [ ] Tous les matins à 9h les lrs de l'UW du DBA à son bureau
- [ ] A chaque fois que l'ordre SQL ROLLBACK est lancé
- [ ] A chaque fois que l'ordre SQL COMMIT est exécuté pour valider une transaction

## Question 6 :

- En cas de COMMIT <<
- [ ] Oracle sauvegarde dans le fichier REDOLOG le contenu du buffer REDOLOG. Transactions validées ou non validées
- [ ] Oracle sauvegarde uniquement les mises à jour de la transaction committée
- [ ] Oracle sauvegarde uniquement les mises à jour des transactions non committée
- [ ] Oracle Sauvegarde le contenu entier du buffer de données vers les fichiers de données



## Question 7 :

- Le buffer de données <<
- [ ] Contient les blocks des segments de données (table, cluster) et d’index les plus souvent sollicités
- [ ] Contient les blocks des segments rollback les plus souvent sollicités
- [ ] Contient les blocks des fichiers redolog courant les plus souvent sollicités
- [ ] Contient uniquement les blocks des fichiers données du tablespace SYSTEM

## Question 8 :

- Le processus DBW est responsable <<
- [ ] D’écrire les blocks de données modifiés dans les fichiers de contrôles 
- [ ] D’écrire les blocks de données modifiés dans les fichiers de données
- [ ] De lire les blocks de données depuis les fichiers de données
- [ ] D’échanger des messages pour se synchroniser avec LOGWRITER et ARCH

## Question 9 :

- Après avoir exécuté une requête en mode server partagé <<
- [ ] Le processus server partagé dépose le résultat dans la RESPONSE QUEUE du dispatcher concerné
- [ ] Le processus server partagé envoi le résultat au LISTENER
- [ ] Le processus server partagé envoie directement le résultat au processus client
- [ ] Le processus server partagé envoie le résultat indirectement au processus DISPATCHER

## Question 10 :

- Cochez ce qui est bon pour la pluggable PDBVENTES de la CDB DBHQ.UNICE.FR qui a aussi une pluggable appelée PDBCOMPTA <<
- [ ] Si le service de la CDB s’appelle DBHQ.UNICE.FR le service de PDBVENTES s’appelle PDBVENTES.UNICE.FR
- [ ] Le dictionnaire de PDBVENTES contient aussi les informations sur les métadonnées de DBHQ et PDBCOMPTA
- [ ] Le dictionnaire de PDBVENTES contient uniquement les informations sur ses propres métadonnées (tables, indexes, …)
- [ ] La pluggable PDBVENTES est toujours démarrée automatiquement

## Question 11 :

- Le traitement des requêtes sql se fait dans les caches Oracle appellés SGA et PGA. Nous avons une base Oracle 12c. Cochez ce qui est bon <<
- [ ] Un bon dimensionnement de ces zones est essentiel pour le traitement rapide des requêtes
- [ ] Les dimensionnements recommandés se fait automatiquement en fixant les paramètres memory_max_size et memory_target
- [ ] Les dimensionnements recommandés se fait en fixant les paramètres pga_aggregate_target, db_cache_size, log_buffer, shared_pool_size, java_pool_size
- [ ] Les dimensionnements recommandés se fait aussi automatiquement en fixant les paramètres sga_target, sga_max_size et pga_aggregate_target

## Question 12 :

- Le traitement des requêtes sql qui seront lancées se fait dans le cache Oracle appelé SGA. Cochez ce qui compose au mieux la SGA <<
- [ ] Elle comprend : un buffer de données, un buffer redolog, une zone des requêtes partagées, un buffer java, ...
- [ ] Elle comprend : un buffer de données, un buffer redolog, une zone des requêtes partagées, un buffer python, ...
- [ ] Elle comprend : uniquement un buffer redolog
- [ ] Elle comprend : une zone des requêtes partagées et un buffer java

## Question 13 :

- Vous avez lancé un client SQLPLUS, vous êtes connectés et travaillez. Vous lancez les actions suivantes : `update emp set sal=12000 where empno=7777; COMMIT ;` Cochez ce qui est juste <<
- [ ] DBW vide les blocks modifiés dans le buffer de données vers les fichiers de données
- [ ] RECO envoie un message à une base distante et se met en attente
- [ ] LGWR recopile le contenu du buffer redolog vers le groupe de log courant
- [ ] Un erreur de mise à jour est signalée car le ma a jour est effectué sur l’employé numéro 7777

## Question 14 :

- Supposons la commande sql (users est un tablespace en autoallocate) suivante : 

  - ```sql
    create table employe (
      empno number(4) constraint pk_emp_empno primary key,
      ename varchar2(30) constraint pk_emp_ename unique)
    tablespace users
    storage (initial 1M minextents 2 pctincrease 0)
    segment creation defferred;
    ```

  A l'issue de l'exécution de cette commande, un segment appelé EMPLOYE va être créé. Cochez l'espace correcte qui sera alloué a ce segment à l'issue de la commande<<

  - [ ] une extension de 2 Mo sera allouée
  - [ ] Deux extensions de 1 Mo chacune seront allouée
  - [ ] 32 extensions de 64 Ko  seront allouées
  - [ ] Aucune extension n’est créé à l’issue de la commande

## Question 15 :

- Un segment créé dans un tablespace appelé NomTS géré localement (il y a suffisamment d'espaces disques)

  ```sql
  Create table nomTable(...) 
  tablespace NomTS storage (initial val1, next val1, minextents 1 pctincrease 0 maxextents 100)
  ```

  La commande se créée <<

  - [ ] 1. Le nombre maximum d'extensions allouable pour ce segment est limité à 100
  - [ ] 2. Le nombre maximum d'extensions allouable pour ce segment est illimité
  - [ ] 3. Dans le cas ou le tablespace avait été créé avec l'option UNIFORM SIZE, toutes les extensions de tous les segments dudit tablespace ont la même taille
  - [ ] L'affirmation faite en 3) est des plus grotesque

## Question 16 :

- Cochez les bonnes tailles possibles de blocks de fichiers de données Oracle :
- [ ] 64 K
- [ ] 32K
- [ ] 8K
- [ ] 128K

## Question 17 :

- Considérons le tablespace System. Cochez ce qui est juste pour ce tablespace <<
- [ ] Il contient le dictionnaire de données Oracle
- [ ] Il peut être réparé en cas de panne base ouverte (base avec le status OPEN)
- [ ] Y sont stockées les informations sur les tables, les colonnes, les indexes, les utilisateurs, les procédures stockées, ...
- [ ] Les données qui s'y trouvent ne sont jamais mises à jour

## Question 18 :

- Les fichiers redolog <<
- [ ] Sont modifiés par les process serveurs
- [ ] Sont modifiés par le process LGWR
- [ ] Sont modifiés par le process ARCH
- [ ] Contiennent des données validées ou non validées

## Question 19 :

- A l'issue de la création d'une base et par défaut, des tablespaces sont créés. Cochez la ou les lignes correspondants aux tablespaces créés : <<
  - [ ] Sysjava, system, sysaux
  - [ ] system, sysaux, temp, undo_tbs, users
  - [ ] users, ts_tab_airbase, system, sysaux, ts_index_airbase
  - [ ] System, sysaux, temp, undofbs, users, ts_tab_airbase. ts_index_airbase, sysjava

## Question 20 :

Considérons la requête présentée dans la question ci-dessous. L'utilisateur est connecté sur une base 12c.

```
CREATE TABLE employe
(
  empno NUMBER(4) CONSTRAINT pk_emp_empno PRIMARY KEY,
  ename VARCHAR2(30) CONSTRAINT pk_emp_ename UNIQUE
)
TABLESPACE users
STORAGE (
  INITIAL 1M
  MINEXTENT 2
  PCTINCREASE 0
);
```

À l'issue de l'exécution de la requête, vous recevez le message « Table créée ». Cochez ce qui est vrai.

- [ ] Les espaces allouables au segment table et index sont alloués.
- [ ] Les espaces allouables au segment table et index seront alloués après le premier INSERT dans la table.
- [ ] Les espaces allouables au segment table et index seront alloués après le deuxième INSERT dans la table.
- [ ] La clause `SEGMENT CREATION IMMEDIATE` est nécessaire pour que l'espace soit immédiatement alloué.

