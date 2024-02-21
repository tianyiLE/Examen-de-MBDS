# QCM Administration Oracle

Cochez la ou les bonnes réponses ou répondre, note SGDB et au moins Oracle 12c

## Question 1 :

Vous souhaitez créer une base de données appelée DBHQ.UNICE.FR (DB1 Head Quarter) avec deux bases de données enfichables (pluggable) : PDBVENTES et PDBCOMPTA. Cochez ce qui est juste 
- [ ] Avec le DBCA (Database Configurations Assistant) je peux créer en un seul trait les 3 bases

- [x] Avec le DBCA je peux creer en un seul trait DBHQ et PDBVENTES ou DBHQ et PDBCOMPTA
- [x] Avec le DBCA je peux ajouter a tout moment PDBVENTES ou PDBCOMPTA.
- [ ] L'ajout d'une nouvelle pluggable database n'est possible que par commande. Pas via l'interface graphique

## Question 2 :

Supposons une container database appelée DBHQ.UNICE.FR. Elle contient au moins. 

- [x] Les tablespaces SYSTEM, SYSAUX, TEMP, UNDOTBS.- 
- [x] Les fichiers de contrôles
- [x] Les fichiers redolog
- [ ] Il est impossible d'y ajouter de nouveaux tablespaces

## Question 3 :

Supposons une pluggable database PDBVENTES créée dans la container database appelée DBHQ.UNICE.FR. Elle contient au moins 

- [x] Les tablespaces SYSTEM, SYSAUX, TEMP, UNDOTBS.
- [ ] Les fichiers de contrôles
- [ ] Les fichiers redolog
- [ ] Il est impossible d'y ajouter de nouveaux tablespaces

## Question 4 :

L'architecture de la CDB container Database DB1HQ.UNICE.FR permet 

- [x] D’économiser des ressources mémoires
- [x] D’économiser l’espace disque
- [x] D’augmenter la sécurité autour d’une base de données
- [ ] Un utilisateur connecté sur une base de données pluggable de cette CDB peut interroger sans problèmes les données contenues dans la CDB .

## Question 5 :

Un checkpoint Oracle intervient dans les conditions suivantes 

- [ ] Toutes les 3 secondes et Oracle vide le buffer de données et le buffer redolog
- [ ] Tous les matins à 9h lors de l'arrivé du DBA à son bureau
- [ ] A chaque fois que l'ordre SQL ROLLBACK est lancé
- [x] A chaque fois que l'ordre SQL COMMIT est exécuté pour valider une transaction

## Question 6 :

En cas de COMMIT 

- [ ] Oracle sauvegarde dans le fichier REDOLOG le contenu du buffer REDOLOG. Transactions validées ou non validées
- [x] Oracle sauvegarde uniquement les mises à jour de la transaction committée
- [ ] Oracle sauvegarde uniquement les mises à jour des transactions non committée
- [ ] Oracle Sauvegarde le contenu entier du buffer de données vers les fichiers de données



## Question 7 :

Le buffer de données 

- [x] Contient les blocks des segments de données (table, cluster) et d’index les plus souvent sollicités
- [ ] Contient les blocks des segments rollback les plus souvent sollicités
- [ ] Contient les blocks des fichiers redolog courant les plus souvent sollicités
- [ ] Contient uniquement les blocks des fichiers données du tablespace SYSTEM

## Question 8 :

Le processus DBW est responsable 

- [ ] D’écrire les blocks de données modifiés dans les fichiers de contrôles 
- [x] D’écrire les blocks de données modifiés dans les fichiers de données
- [ ] De lire les blocks de données depuis les fichiers de données
- [ ] D’échanger des messages pour se synchroniser avec LOGWRITER et ARCH

## Question 9 :

Après avoir exécuté une requête en mode server partagé 

- [x] Le processus server partagé dépose le résultat dans la RESPONSE QUEUE du dispatcher concerné
- [ ] Le processus server partagé envoi le résultat au LISTENER
- [ ] Le processus server partagé envoie directement le résultat au processus client
- [ ] Le processus server partagé envoie le résultat indirectement au processus DISPATCHER

## Question 10 :

Cochez ce qui est bon pour la pluggable PDBVENTES de la CDB DBHQ.UNICE.FR qui a aussi une pluggable appelée PDBCOMPTA <<

- [ ] Si le service de la CDB s’appelle DBHQ.UNICE.FR le service de PDBVENTES s’appelle PDBVENTES.UNICE.FR
- [ ] Le dictionnaire de PDBVENTES contient aussi les informations sur les métadonnées de DBHQ et PDBCOMPTA
- [x] Le dictionnaire de PDBVENTES contient uniquement les informations sur ses propres métadonnées (tables, indexes, …)
- [ ] La pluggable PDBVENTES est toujours démarrée automatiquement

## Question 11 :

Le traitement des requêtes sql se fait dans les caches Oracle appellés SGA et PGA. Nous avons une base Oracle 12c. Cochez ce qui est bon 

- [x] Un bon dimensionnement de ces zones est essentiel pour le traitement rapide des requêtes
- [x]  Leurs dimensionnements recommandés se fait automatiquement en fixant les paramètres memory_max_size et memory_target
- [x]  Leurs  dimensionnements recommandés se fait en fixant les paramètres pga_aggregate_target, db_cache_size, log_buffer, shared_pool_size, java_pool_size
- [x]  Leurs dimensionnements recommandés se fait aussi automatiquement en fixant les paramètres sga_target, sga_max_size et pga_aggregate_target

## Question 12 :

Le traitement des requêtes sql qui seront lancées se fait dans le cache Oracle appelé SGA. Cochez ce qui compose au mieux la SGA 

- [x] Elle comprend : un buffer de données, un buffer redolog, une zone des requêtes partagées, un buffer java, ...
- [ ] Elle comprend : un buffer de données, un buffer redolog, une zone des requêtes partagées, un buffer python, ...
- [ ] Elle comprend : uniquement un buffer redolog
- [ ] Elle comprend : une zone des requêtes partagées et un buffer java

## Question 13 :

Vous avez lancé un client SQLPLUS, vous êtes connectés et travaillez. Vous lancez les actions suivantes : `update emp set sal=12000 where empno=7777; COMMIT ;` Cochez ce qui est juste <<

- [ ] DBW vide les blocks modifiés dans le buffer de données vers les fichiers de données
- [ ] RECO envoie un message à une base distante et se met en attente
- [x] LGWR recopile le contenu du buffer redolog vers le groupe de log courant
- [ ] Un erreur de mise à jour est signalée car la mise a jour est effectué sur l’employé numéro 7777

## Question 14 :

Supposons la commande sql (users est un tablespace en autoallocate) suivante : 

- ```sql
  create table employe (
    empno number(4) constraint pk_emp_empno primary key,
    ename varchar2(30) constraint pk_emp_ename unique)
  tablespace users
  storage (initial 1M minextents 2 pctincrease 0)
  segment creation defferred;
  ```

A l'issue de l'exécution de cette commande, un segment appelé EMPLOYE va être créé. Cochez l'espace correcte qui sera alloué a ce segment à l'issue de la commande

- [ ] une extension de 2 Mo sera allouée
- [ ] Deux extensions de 1 Mo chacune seront allouée
- [ ] 32 extensions de 64 Ko  seront allouées
- [x] Aucune extension n’est créé à l’issue de la commande

## Question 15 :

Un segment créé dans un tablespace appelé NomTS géré localement (il y a suffisamment d'espaces disques)

```sql
Create table nomTable(...) 
tablespace NomTS storage (initial val1, next val1, minextents 1 pctincrease 0 maxextents 100)
```

La commande se créée <<

- [x] 1. Le nombre maximum d'extensions allouable pour ce segment est limité à 100
- [ ] 2. Le nombre maximum d'extensions allouable pour ce segment est illimité
- [x] 3. Dans le cas ou le tablespace avait été créé avec l'option UNIFORM SIZE, toutes les extensions de tous les segments dudit tablespace ont la même taille
- [ ] 4. L'affirmation faite en 3 est des plus grotesque

## Question 16 :

Cochez les bonnes tailles possibles de blocks de fichiers de données Oracle :

- [ ] 64 K
- [x] 32K
- [x] 8K
- [ ] 128K

## Question 17 :

Considérons le tablespace System. Cochez ce qui est juste pour ce tablespace 

- [x] Il contient le dictionnaire de données Oracle
- [ ] Il peut être réparé en cas de panne base ouverte (base avec le status OPEN)
- [x] Y sont stockées les informations sur les tables, les colonnes, les indexes, les utilisateurs, les procédures stockées, ...
- [ ] Les données qui s'y trouvent ne sont jamais mises à jour

## Question 18 :

Les fichiers redolog 

- [ ] Sont modifiés par les process serveurs
- [x] Sont modifiés par le process LGWR
- [ ] Sont modifiés par le process ARCH
- [ ] Contiennent des données validées ou non validées

## Question 19 :

A l'issue de la création d'une base et par défaut, des tablespaces sont créés. Cochez la ou les lignes correspondants aux tablespaces créés : 
- [ ] Sysjava, system, sysaux
- [x] system, sysaux, temp, undo_tbs, users
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
- [x] Les espaces allouables au segment table et index seront alloués après le premier INSERT dans la table.
- [ ] Les espaces allouables au segment table et index seront alloués après le deuxième INSERT dans la table.
- [ ] La clause `SEGMENT CREATION IMMEDIATE` est nécessaire pour que l'espace soit immédiatement alloué.



****

# répondre et expliquer

Pour répondre et expliquer chaque question dans le contexte de l'administration d'une base de données Oracle, en particulier Oracle 12c, voici le détail des réponses justes selon les connaissances d'Oracle Database :

### Question 1
- Avec Oracle Database 12c et versions ultérieures, il est possible de créer une base de données conteneur (CDB) et des bases de données pluggables (PDB) en utilisant le Database Configuration Assistant (DBCA). Il est possible de créer la CDB et une ou plusieurs PDBs dans une seule opération, mais les options peuvent varier en fonction de l'interface et des versions spécifiques d'Oracle. En pratique, on crée généralement la CDB et peut-être une PDB initiale, puis on ajoute d'autres PDBs selon les besoins.
- **Réponse 1**: Incorrecte, car selon les versions et les interfaces du DBCA, il pourrait être possible de créer la CDB et plusieurs PDBs en une seule opération.
- **Réponse 2 et 3**: Correctes. Le DBCA permet la création de la CDB avec une PDB initiale et autorise l'ajout ultérieur de nouvelles PDBs.
- **Réponse 4**: Incorrecte. L'interface graphique du DBCA et les commandes SQL (via SQL*Plus ou autres interfaces) permettent d'ajouter des PDBs.

### Question 2
- Une CDB contient effectivement les tablespaces SYSTEM, SYSAUX, TEMP, et UNDO, ainsi que des fichiers de contrôle et des fichiers redolog. De nouveaux tablespaces peuvent être ajoutés à une CDB pour répondre à des besoins spécifiques.
- **Réponses**: Toutes les options mentionnées sont vraies pour une CDB, sauf la dernière qui est incorrecte car il est possible d'ajouter de nouveaux tablespaces.

### Question 3
- Une PDB contient ses propres tablespaces SYSTEM, SYSAUX, TEMP, mais elle n'a pas ses propres fichiers de contrôle ou fichiers redolog, car ceux-ci sont partagés au niveau de la CDB. Il est possible d'ajouter de nouveaux tablespaces dans une PDB.
- **Réponse 1**: Correcte pour les tablespaces.
- **Réponses 2 et 3**: Incorrectes, car les PDBs utilisent les fichiers de contrôle et les fichiers redolog de la CDB.
- **Réponse 4**: Incorrecte, car il est possible d'ajouter de nouveaux tablespaces dans une PDB.

### Question 4
- L'architecture multitenant introduite avec Oracle 12c, permettant de disposer de CDBs et de PDBs, offre plusieurs avantages, dont l'économie de ressources mémoire et d'espace disque grâce au partage de certaines structures entre les PDBs. Elle augmente également la sécurité et l'isolation entre les bases de données. Cependant, l'accès direct d'une PDB à une autre ou à la CDB pour des requêtes transverses nécessite une configuration spécifique.
- **Réponses**: Toutes sont vraies à l'exception de la dernière qui est conditionnelle et nécessite une clarification.

### Question 5
- Un checkpoint Oracle est un mécanisme qui synchronise l'état du cache en mémoire avec les fichiers de données sur disque. Il ne se produit pas à des intervalles de temps fixes comme toutes les 3 secondes ou à un moment précis de la journée, mais plutôt lors d'événements spécifiques tels que le commit d'une transaction, lors de checkpoints programmés, etc.
- **Réponse 4**: Correcte, car un checkpoint peut se produire lors d'un COMMIT.

### Question 6
- Lors d'un COMMIT, Oracle écrit les enregistrements redo générés par les transactions validées dans les fichiers redolog pour garantir la durabilité des données. Il ne sauvegarde pas le contenu entier du buffer de données ni les transactions non validées.
- **Réponse 2**: Correcte.

### Question 7
- Le buffer de données (database buffer cache) contient les blocs de données les plus fréquemment accédés, y compris les données des tables et des index, mais pas spécifiquement les blocs des fichiers redolog ou uniquement les blocs du tablespace SYSTEM.
- **Réponse 1**: Correcte.

### Question 8
- Le processus DBWn (Database Writer) est responsable de l'écriture des blocs de données modifiés du
- cache de la base de données vers les fichiers de données sur le disque. Il ne s'occupe pas des fichiers de contrôle, de la lecture des blocs de données, ni de la synchronisation directe avec les processus LGWR (Log Writer) et ARCH (Archiver).
  - **Réponse 2**: Correcte. DBWn écrit les blocs de données modifiés dans les fichiers de données pour assurer la persistance des modifications.


### Question 9
- Dans un mode de serveur partagé (Shared Server Mode), le processus serveur partagé gère les requêtes des utilisateurs et place les résultats dans une queue de réponse spécifique d'où le dispatcher les récupère pour les envoyer au client. Il ne communique pas directement avec le listener ni ne renvoie directement les résultats au processus client.
- **Réponse 1**: Correcte. Le processus serveur partagé dépose le résultat dans la queue de réponse du dispatcher concerné.

### Question 10
- Dans l'architecture multitenant, chaque PDB a son propre dictionnaire de données contenant les métadonnées relatives à ses objets. Les services sont nommés spécifiquement pour chaque PDB, et les métadonnées de chaque PDB sont isolées des autres.
- **Réponse 3**: Correcte. Le dictionnaire de données de PDBVENTES contient uniquement les informations sur ses propres métadonnées.

### Question 11
- Un bon dimensionnement de la SGA (System Global Area) et de la PGA (Program Global Area) est crucial pour les performances de la base de données. Oracle fournit des mécanismes de gestion automatique et manuelle pour le dimensionnement de ces composants.
- **Réponses**: Toutes sont correctes, car elles soulignent l'importance du dimensionnement approprié et des mécanismes pour y parvenir.

### Question 12
- La SGA comprend plusieurs structures, dont le buffer de données (Database Buffer Cache), la zone des requêtes partagées (Shared Pool), mais pas un buffer redolog qui est séparé de la SGA, ni un buffer python qui n'existe pas dans ce contexte.
- **Réponse 1**: Correcte, en excluant la mention du buffer redolog comme partie de la SGA.

### Question 13
- Lorsqu'une transaction est validée (commit), LGWR écrit les informations de redo log dans le groupe de logs actuel pour garantir la durabilité des transactions. DBWn peut écrire les blocs modifiés dans les fichiers de données mais pas immédiatement après chaque commit.
- **Réponse 3**: Correcte. LGWR écrit le contenu du buffer redolog vers le groupe de log courant lors d'un COMMIT.

### Question 14
- La commande SQL fournie diffère de l'usage habituel d'Oracle car elle spécifie `SEGMENT CREATION DEFERRED`, ce qui signifie qu'aucun espace n'est immédiatement alloué pour le segment de la table. L'espace est alloué lors de la première insertion de données.
- **Réponse 4**: Correcte. Aucune extension n'est créée immédiatement à l'issue de la commande due à la directive `SEGMENT CREATION DEFERRED`.

### Question 15
- La commande spécifie les paramètres de stockage pour un segment. Dans un tablespace géré localement, le nombre maximum d'extensions est déterminé par les paramètres de la commande, et l'option UNIFORM SIZE affecte la taille de toutes les extensions dans le tablespace s'il est spécifié.
- **Réponses 1 et 3**: Correctes. Le nombre maximum d'extensions est limité à 100, et l'affirmation 3 est vraie pour un tablespace avec l'option UNIFORM SIZE.

### Question 16
- Oracle Database supporte différentes tailles de blocs pour les fichiers de données, mais 128K n'est typiquement pas une taille de bloc standard.
- **Réponses 2 et 3**: Correctes. 32K et 8K sont des tailles de blocs possibles pour les fichiers de données Oracle.

### Question 17
- Le tablespace SYSTEM contient le dictionnaire de données Oracle et d'autres structures importantes. Il est mis à jour régulièrement, et certaines réparations peuvent être effectuées, mais avec précaution et dans des cas spécifiques.
- **Réponses 1 et 3**: Correctes. Il contient le dictionnaire de données et des informations sur les objets de la base.

### Question 18
-

- Les fichiers redo log sont essentiels pour la récupération de la base de données et le processus LGWR est responsable de leur écriture. Ils contiennent les informations nécessaires pour reproduire les transactions, permettant ainsi la restauration de l'état de la base de données en cas de panne.
- **Réponse 2**: Correcte. Le processus LGWR est chargé de modifier les fichiers redo log en y écrivant les informations de redo des transactions validées.

### Question 19
- Par défaut, lors de la création d'une nouvelle base de données Oracle, un certain nombre de tablespaces sont automatiquement créés pour supporter différentes fonctions et stockages de la base de données, incluant le tablespace SYSTEM, SYSAUX, TEMP, et souvent un tablespace pour les undo data et un tablespace par défaut pour les objets utilisateur (comme USERS).
- **Réponse 2**: Correcte. Les tablespaces SYSTEM, SYSAUX, TEMP, UNDO_TBS, et USERS sont typiquement créés par défaut lors de l'initialisation d'une nouvelle base de données Oracle.

### Question 20
- La commande SQL fournie crée une table dans le tablespace USERS avec un espace initial spécifié. La création de segment est différée jusqu'à ce que des données soient effectivement insérées dans la table, à moins que la clause `SEGMENT CREATION IMMEDIATE` ne soit spécifiée.
- **Réponse 2**: Correcte. L'espace alloué au segment de table et d'index sera effectivement alloué après le premier INSERT dans la table, en raison de la politique de création de segment différée par défaut dans Oracle 12c et versions ultérieures (si `SEGMENT CREATION DEFERRED` est actif ou par défaut sans spécification contraire).

Ces réponses et explications couvrent un large éventail de fonctionnalités et de concepts clés d'Oracle Database, en particulier dans le contexte de la version 12c et au-delà, y compris l'architecture multitenant, la gestion des tablespaces, les mécanismes de récupération et de sauvegarde, ainsi que la configuration et l'optimisation de la performance.
