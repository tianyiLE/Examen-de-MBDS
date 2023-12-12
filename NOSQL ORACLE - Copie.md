NOSQL ORACLE, Mars 2020, durée 1h, 1 points/question, 
Des points sont enlevés au prorata des mauvaises réponses cochées, 1, 2 ou 3 réponses peuvent être correctes.  Pas de document autorisé.

# Les questions

**Considérons l'architecture et les données de l'application exemple (à lire avant de commencer) :**

## Question01

Nous souhaitons charger les données dans la base Oracle NoSQL. Il faut pour cela :

- [ ] 1/ Si on le souhaite Utiliser l'utilitaire SQLLOADER Oracle
- [ ] 2/ Si on le souhaite Utiliser l'utilitaire ODI (Oracle Data Integrator)
- [ ] 3/ Si on le souhaite écrire un programme dans un langage de haut niveau tel que Java ou C/C++
- [ ] 4/ Si on le souhaite utiliser scoop

## Question02

Nous souhaitons charger les données dans la base Oracle SQL. Il faut pour cela :

- [ ] 1/ Si on le souhaite Utiliser l'utilitaire SQLLOADER Oracle
- [ ] 2/ Si on le souhaite écrire une table externe Oracle qui pointe vers le fichier puis insérer les EMPLOYE à partir de cette table
- [ ] 3/ Si on le souhaite écrire un programme dans un langage de haut niveau tel que Java ou C/C++
- [ ] 4/ Si on le souhaite utiliser à tous les coût un driver C++

## Question03

Nous souhaitons charger les données dans la base Oracle SQL. Il faut pour cela :

- [ ] 1/ Si on le souhaite Utiliser l'utilitaire ODI (Oracle Data Integrator)
- [ ] 2/ Si on le souhaite utiliser le driver ORACLE_HDFS
- [ ] 3/ Si on le souhaite le driver ORACLE_HIVE
- [ ] 4/ SQLLOADER reste tout de même une bonne option

## Question04

Nous souhaitons charger les données dans le SGF distribué HADOOP HDFS il faut pour cela :

- [ ] 1/ Si on le souhaite Utiliser l'utilitaire SQLLOADER Oracle
- [ ] 2/ Si on le souhaite Utiliser l'utilitaire ODI (Oracle Data Integrator)
- [ ] 3/ Si on le souhaite nous devons créer un dossier Hadoop HDFS puis déplacer le fichier de produit dans ce dossier
- [ ] 4/ Si on le souhaite utiliser scoop Hadoop

## Question05

Considérons l'architecture définie ci-dessous :

- [ ] 1/ Elle permet de mettre à jour les données des bases impliquées à partir d'une base Oracle SQL
- [ ] 2/ Elle permet de mettre à jour les données des bases impliquées à partir de HADOOP HIVE
- [ ] 3/ Elle permet de consulter les données stockées dans des bases hétérogènes depuis Oracle SQL
- [ ] 4/ Elle permet de consulter les données stockées dans des bases hétérogènes depuis Hadoop HIVE

## Question06

Considérons l'architecture définie ci-dessous :

- [ ] 1/ Elle permet de construire un DWH centralisé comme dans les années 90.
- [ ] 2/ Elle permet d'accéder depuis une base SQL à des données hétérogènes
- [ ] 3/ Elle permet de connecter un DW virtual et de temps réel
- [ ] 4/ On parle aussi de la gestion de lacs de données

## Question07

Considérons l'architecture définie ci-dessous :

- [ ] 1/ Cette architecture permet aux utilisateurs d’outils OLAP de manipuler des données hétérogènes.
- [ ] 2/ Cette architecture permet de manipuler les données dans le CLOUD uniquement
- [ ] 3/ Cette architecture permet d’utiliser des outils de deep learning pour manipuler des données hétérogènes
- [ ] 4/ Cette architecture permet d’utiliser des outils de machine learning pour manipuler des données hétérogènes**

## Question08

Le langage Big Data SQL au niveau d'Oracle SQL se caractérise par :

- [ ] 1/ L’absence de la possibilité d’effectuer des opérations de groupe
- [ ] 2/ Tout ce qu'il y a dans l’ordre SQL SELECT peut être utilisé dans Big Data SQL
- [ ] 3/ Un des éléments caractéristiques de Big Data SQL est la notion de tables externes
- [ ] 4/ Un des éléments caractéristiques de Big Data SQL est le traitement parallèle des requêtes

## Question09

Supposons une requête mêlant des tables internes et des tables externes au niveau de la base Oracle SQL :

- [ ] 1/ L'optimiseur rapatrie toutes les lignes venant d’Oracle NoSQL et Hadoop vers la base SQL sans traiter de WHERE
- [ ] 2/ L'optimiseur Oracle rapatrie les lignes vers la base SQL uniquement les lignes utiles. Les clauses Where sont appliquées dans les SGBD ou SGF sources
- [ ] 3/ Les traitements impliquant les tables externes sont rapides à l’image des SGBD NoSQL impliqués
- [ ] 4/ L’algorithme HADOOP MAP REDUCE peut s’appliquer dans la chaine des tables externes

## Question10

Nous souhaitons ajouter une nouvelle commande. Cochez ce qui est syntaxiquement juste

- [ ] 1/ put table -name commande -json '{"commid": "20001", "commandate" :"12-11-2019", "prodid":"1000", "clientid":"1", "quantite":"9, "prixunitaire":"2.0", "vendeurid" : "7370"}';
  2/ put table -name commande -json '{"commid": "20002", "commandate" :"12-11-2019", "prodid":"1000", "clientid":"1", "quantite":"9, "prixunitaire":"2.0", "vendeurid" : "7370"}';
- [ ] 3/ get table -name commande -json '{"commid": "20001", "commandate" :"12-11-2019", "prodid":"1000", "clientid":"1", "quantite":"9, "prixunitaire":"2.0", "vendeurid" : "7370"}';
- [ ] 4/ put kv -name commande -json '{"commid": "20003", "commandate" :"12-11-2019", "prodid":"1000", "clientid":"1", "quantite":"9, "prixunitaire":"2.0", "vendeurid" : "7370"}';

## Question11

Nous souhaitons créer une table appelée ligne de commande (LignesDeCommande), cochez ce qui est possible

- [ ] 1/ execute 'create table as select * from lignesDeCommande@CDB';
- [ ] 2/ KVStore store=...; TableAPI tableAPI = store.getTableAPI(); stmt="create table lignesDeCommande(...);"; store.executeSync(stmt);
- [ ] 3/ execute 'create table lignesDeCommande(...)';
- [ ] 4/ execute 'create table lignesDeCommande(...)' in kvstore ;

## Question12

Nous souhaitons rechercher des commandes sur la ligne de commande kv->. Cochez ce qui est juste

- [ ] 1/ get table -name commande -field commid -value 1
- [ ] 2/ get table -name commande -field prodid -value 1000
- [ ] 3/ get table -name commande -field prodid -value 1000 -field clientid -value 1
- [ ] 4/ get table -name commande -field prodid -value 1000 -field commid -field 1

## Question13

Le moteur NOSQL Oracle est un SGBD partitionné (distribué) et répliqué

- [ ] 1/ Le partition chez Oracle NoSql correspond à un SHARD
- [ ] 2/ Un SHARD comprend un nœud de réplication maître et plusieurs nœuds de réplications esclave
- [ ] 3/ Une base de données Oracle NoSQL peut comprendre plusieurs SHARD
- [ ] 4/ Une base de données Oracle NoSQL comprend un et un seul SHARD

## Question14

Dans la théorie les SGBD NOSQL sont caractérisés par le théorème CAP (Constance, Availability Partitionning)

- [ ] 1/ Oracle NoSQL supporte le C, A et P
- [ ] 2/ Oracle NoSQL supporte le C et A
- [ ] 3/ Oracle NoSQL supporte le A et P
- [ ] 4/ Oracle NoSQL supporte le C et P

## Question15

Considérons la PK et la clause SHARD(PRODID) dans la requête de création de la table COMMANDE plus bas. Cochez ce qui est juste

- [ ] 1/ PROID c'est l'équivalent la majeur KEY dans le modèle KEY/VALUE
- [ ] 2/ ClientID est command indiquent une mineure key composée
- [ ] 3/ SHARD(PRODID) indique que toutes commandes d'un même produit sont stockées dans un même SHARD
- [ ] 4/ Aucune des affirmations précédentes n'est juste

## Question16

Nous souhaitons effectuer une lecture constante d'une commande connaissant sa PK complète. Supposons la clé key
Cochez ce qui est juste

- [ ] 1/ store.get(key, Consistency.ABSOLUTE, 0, ...);
- [ ] 2/ store.get(key, Consistency.NONE_REQUIRED, 0, ...);
- [ ] 3/ store.get(key);
- [ ] 4/ La réponse en 3/ est fausse

## Question17

Avec le modèle clé/Valeur, une clé peut être composée d'une partie Major Key et d'une partie Minor KEY

- [ ] 1/ La partie Major Key peut être composée de une ou plusieurs majeurs keys
- [ ] 2/ La partie Minor Key peut être composée de une ou plusieurs minors keys
- [ ] 3/ La partie Major Key doit être composée d'une seule major key
- [ ] 4/ Il n'est pas obligatoire d'avoir une minor key

## Question18

La structuration en major et minor key permet

- [ ] 1/ D'optimiser l'accès aux enregistrements
- [ ] 2/ De mieux partitionner les données
- [ ] 3/ De réduire le coût d'accès
- [ ] 4/ D'éloudir inutilement la programmation

## Question19

Supposons que vous souhaitez accéder aux données de votre table COMMANDE depuis une base Oracle SQL
- [ ] Vous devez créer une table externe Hive qui pointe vers la table Commande, puis une table externe oracle sql qui pointe vers la table externe Hive
- [ ] Vous devez créer une table externe oracle Sql qui pointe directement vers la table Oracle nosql
- [ ] Le plus rapide c'est de coder son propre access driver
- [ ] Le mieux c'est d'utiliser l'access driver HDFS proposé par Oracle nommé ORACLE_HDFS

## Question20

Dans l'hypothèse ou une table externe appelée COMMANDE_EXT existe dans la base oracle SQL. Cette table pointe au final vers la table COMMANDE dabs la base Nosql. Cochez le ou les ordres SQL qui fonctionnent. Une commande Nr 1 existe:
- [ ] Update COMMANDE_EXT set quantite =10 where commid=1;
- [ ] Insert into COMMANDE_EXT values (...);
- [ ] Delete from COMMANDE_EXT where commid=1;
- [ ] Select * from COMMANDE_EXT where commid=1;

## Question21

Vous souhaitez accéder aux données du fichier HADOOP HDFS appelé PRODUITS.TXT depuis une base Oracle SQL. Cochez ce qui est juste
- [ ] Vous pouvez créer une table externe Hive qui pointe vers le fichier produits.txt, puis une table externe oracle sql qui pointe vers la table externe Hive
- [ ] Vous pouvez créer une table externe oracle Sql qui pointe directement vers le fichier produits.txt
- [ ] La solutions en 2) est fausse
- [ ] Les drivers Oracle ORACLE_HDFS ou ORACLE_HIVE peuvent être l'un ou l'autre utilisé selon les cas

## Question22

Supposons que la table COMMANDE résidait physiquement dans une autre BD NOSQL autre que Oracle NoSQL
- [ ] Vous devez créer une table externe Hive qui pointe vers la table Commande, puis une table externe oracle sql qui pointe vers la table externe Hive
- [ ] Vous devez créer une table externe oracle Sql qui pointe directement vers la table Oracle nosql
- [ ] Le plus rapide c'est de coder son propre access driver
- [ ] Le mieux c'est d'utiliser l'access driver HDFS proposé par Oracle nommé ORACLE_HDFS



# Application example

### Considérons l'architecture Big Data ci-dessous

![image-20231212153200677](C:\Users\t.le\AppData\Roaming\Typora\typora-user-images\image-20231212153200677.png)



### Ci-dessous la répartition des données :

#### Sur Oracle NoSQL

Execute '`CREATE TABLE CLIENT(clientId Integer, , clientnom string, clientdnais string, clientadr string, primary key (clientId))`';
Il y a plus de 10000 clients avec les infos suivantes dans l'ordre des champs dans un fichier TXT (ci-dessous les 2 premiers):

1. ```
   1. "Akim", "12-DEC-1927", "Washington";
   2. "Erzulie", "12-DEC-1942", "Arbonite";
      ...
   ```

   

Execute '`create table commande(commid Integer, commandate string, prodid integer, clientid integer, quantite Integer, prixunitaire integer, vendeurid integer, primary key(shard(prodid), clientid, commid))`'
Il y a plus de 20000 commandes par mois avec les infos suivantes dans l'ordre des champs dans un fichier TXT (ci-dessous les 3 premières):

1. ```
   1. "11-11-2019", 10001, 4, 2, 7369 ;
   2. "11-11-2019", 10001, 10, 2, 7369 ;
   3. "12-11-2019", 10001, 1, 9, 7369;
      ...
   ```

   

#### Sur Hadoop HDFS

S'y trouve un fichier de produits (produits.txt)
Produid, prodnom, proddescription, prodprixunitaire

```
1000, "Coca cola 2 litres", "Coca cola 2 litres saveur caféine", 2"
1001, "orangina pack de 6 bouteilles de 1,5 litres", "orangina pack de 6 bouteilles de 1,5 litres", 6;
```



#### Sur Oracle SQL DB

```sql
CREATE TABLE EMP(EMPNO NUMBER(4) NOT NULL primary key,
    ENAME VARCHAR2(10),
    JOB VARCHAR2(9),
    MGR NUMBER(4),
    HIREDATE DATE,
    SAL NUMBER(7, 2),
    COMM NUMBER(7, 2),
    DEPTNO NUMBER(2));
```

Il y a plus de 1000 employés avec les infos suivantes dans l'ordre des champs dans un fichier txt.

```
7369, 'SMITH', 'CLERK', 7902, '17-DEC-1980', 800, NULL, 20;
7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-1981', 1600, 300, 30;
7521, 'WARD', 'SALESMAN', 7698, '22-FEB-1981', 1250, 500, 30;
7566, 'JONES', 'MANAGER', 7839, '2-APR-1981', 2975, NULL, 20;
7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-1981', 1250, 1400, 30;
7698, 'BLAKE', 'MANAGER', 7839, '1-MAY-1981', 2850, NULL, 30;
7782, 'CLARK', 'MANAGER', 7839, '9-JUN-1981', 2450, NULL, 10;
7788, 'SCOTT', 'ANALYST', 7566, '09-DEC-1982', 3000, NULL, 20;
7839, 'KING', 'PRESIDENT', NULL, '17-NOV-1981', 5000, NULL, 10;
7844, 'TURNER', 'SALESMAN', 7698, '8-SEP-1981', 1500, 0, 30;
7876, 'ADAMS', 'CLERK', 7788, '12-JAN-1983', 1100, NULL, 20;
7900, 'JAMES', 'CLERK', 7698, '3-DEC-1981', 950, NULL, 30;
7902, 'FORD', 'ANALYST', 7566, '3-DEC-1981', 3000, NULL, 20;
7934, 'MILLER', 'CLERK', 7782, '23-JAN-1982', 1300, NULL, 10;
```



#  Refer to the answer第一版

Voici les réponses et les explications pour chaque question de votre examen sur Oracle NoSQL et les technologies associées :

## Question 01
**Réponse :** 2, 3
**Explication :** ODI (Oracle Data Integrator) est souvent utilisé pour l'intégration de données dans Oracle NoSQL. Écrire un programme dans un langage de haut niveau comme Java ou C/C++ est également une méthode courante pour charger des données.

## Question 02
**Réponse :** 1, 2, 3
**Explication :** SQLLOADER est un outil classique pour charger des données dans Oracle SQL. La création d'une table externe pour pointer vers un fichier suivi d'insertions dans la table EMPLOYE est une autre approche valide. L'écriture d'un programme personnalisé est également une option viable.

## Question 03
**Réponse :** 1, 4
**Explication :** ODI peut être utilisé pour l'intégration de données dans Oracle SQL. SQLLOADER reste une bonne option pour charger des données directement.

## Question 04
**Réponse :** 3, 4
**Explication :** Pour charger des données dans Hadoop HDFS, il est courant de créer un dossier Hadoop HDFS et d'y déplacer les fichiers. L'utilisation de Sqoop Hadoop est également une méthode efficace pour transférer des données entre Hadoop et les bases de données relationnelles.

## Question 05
**Réponse :** 3, 4
**Explication :** L'architecture en question permet probablement la consultation des données stockées dans des bases hétérogènes depuis Oracle SQL et depuis Hadoop HIVE.

## Question 06
**Réponse :** 2, 3, 4
**Explication :** Cette architecture semble permettre l'accès à des données hétérogènes depuis une base SQL, la connexion à un DW virtuel et en temps réel, et gérer des lacs de données.

## Question 07
**Réponse :** 1, 4
**Explication :** Cette architecture permet aux utilisateurs d’outils OLAP de manipuler des données hétérogènes et l'utilisation d'outils de machine learning pour manipuler ces données.

## Question 08
**Réponse :** 2, 3, 4
**Explication :** Big Data SQL chez Oracle permet l'utilisation de la plupart des opérations SQL SELECT, y compris les tables externes et le traitement parallèle des requêtes.

## Question 09
**Réponse :** 2
**Explication :** L'optimiseur Oracle est conçu pour rapatrier uniquement les lignes nécessaires, appliquant les clauses WHERE dans les SGBD ou SGF sources.

## Question 10
**Réponse :** 1
**Explication :** La syntaxe 'put table -name commande -json' est correcte pour ajouter une nouvelle commande dans le modèle clé/valeur.

## Question 11
**Réponse :** 2, 3
**Explication :** Pour créer une table 'lignesDeCommande', on peut utiliser l'API TableAPI d'Oracle NoSQL ou exécuter une instruction 'create table' directement dans un environnement SQL.

## Question 12
**Réponse :** 1, 2, 3
**Explication :** Les commandes 'get table -name' avec différentes spécifications de champs et valeurs sont correctes pour rechercher des commandes.

## Question 13
**Réponse :** 1, 2, 3
**Explication :** Dans Oracle NoSQL, un SHARD correspond à un partitionnement, et une base de données peut comprendre plusieurs SHARDs. Chaque SHARD inclut un nœud de réplication maître et plusieurs nœuds esclaves.

## Question 14
**Réponse :** 3
**Explication :** Selon le théorème CAP, un système peut supporter deux des trois propriétés suivantes : cohérence, disponibilité et tolérance au partitionnement. Oracle NoSQL privilégie la disponibilité (A) et la tolérance au partitionnement (P).

## Question 15
**Réponse :** 3
**Explication :** La clause SHARD(PRODID) indique que toutes les commandes d'un même produit sont stockées dans un même SHARD, ce qui optimise les requêtes et les performances.

## Question 16
**Réponse :** 1, 3
**Explication :** La méthode 'store.get(key)' avec différentes spécifications de cohérence est correcte pour lire une valeur connaissant sa clé primaire complète.

## Question 17
**Réponse :** 1, 2, 4
**Explication :** Dans le modèle clé/valeur, une clé peut être composée d'une partie Major Key et d'une partie Minor Key, avec diverses combinaisons possibles de ces éléments.

## Question 18
**Réponse :** 1, 2, 3
**Explication :** La structuration en major et minor keys aide à optimiser l'accès aux enregistrements, à mieux partitionner les données et à réduire le coût d'accès.

## Question 19
**Réponse :** 2
**Explication :** Pour accéder aux données d'une table Oracle NoSQL depuis une base Oracle SQL, il est préférable de créer une table externe Oracle SQL qui pointe directement vers la table Oracle NoSQL.

## Question 20
**Réponse :** 4
**Explication :** Avec une table externe, généralement seul un ordre SELECT est possible. Les opérations de mise à jour, d'insertion ou de suppression ne sont généralement pas réalisables directement sur des tables externes.

## Question 21
**Réponse :** 1, 4
**Explication :** Pour accéder aux données d'un fichier Hadoop HDFS depuis une base Oracle SQL, on peut créer une table externe Hive qui pointe vers le fichier, puis une table externe Oracle SQL qui pointe vers la table Hive. Les drivers Oracle ORACLE_HDFS ou ORACLE_HIVE peuvent être utilisés selon les cas.

## Question 22
**Réponse :** 1, 4
**Explication :** Si la table COMMANDE se trouve dans une autre base NoSQL que Oracle NoSQL, il serait approprié de créer une table externe Hive qui pointe vers cette table, puis une table externe Oracle SQL qui pointe vers la table Hive. Utiliser l'access driver HDFS proposé par Oracle nommé ORACLE_HDFS peut également être une bonne option.

### Concernant l'application exemple :

Pour répondre précisément aux questions en relation avec l'application exemple, il serait nécessaire d'avoir plus de détails sur l'architecture Big Data mentionnée et les données spécifiques impliquées. Cependant, en général :

- L'architecture Big Data pourrait inclure l'intégration de données hétérogènes provenant de sources comme Oracle NoSQL et Hadoop HDFS, ce qui pourrait influencer les réponses aux questions 5, 6, et 7.
- La structure des tables `CLIENT` et `COMMANDE` dans Oracle NoSQL et les données dans Hadoop HDFS doivent être considérées lors de l'élaboration des stratégies de requête et d'intégration de données, ce qui est pertinent pour les questions 19 à 22.

Sans une vue complète de l'image et des détails spécifiques, il est difficile de fournir des réponses plus précises pour ces questions.



# Refer to the answer第二版

Pour répondre à ces questions, il faut comprendre l’architecture Big Data proposée ainsi que les différentes technologies et utilitaires mentionnés. Voici les réponses et explications pour chaque question basées sur les informations fournies :

## Question01
- [x] 3/ Si on le souhaite écrire un programme dans un langage de haut niveau tel que Java ou C/C++
  - **Explication** : Oracle NoSQL est une base de données NoSQL qui offre des interfaces de programmation Java et d’autres langages pour interagir avec la base de données. SQLLoader et ODI sont principalement utilisés pour les bases de données relationnelles Oracle.

## Question02
- [x] 1/ Si on le souhaite Utiliser l'utilitaire SQLLOADER Oracle
- [x] 2/ Si on le souhaite écrire une table externe Oracle qui pointe vers le fichier puis insérer les EMPLOYE à partir de cette table
  - **Explication** : SQLLoader est un utilitaire pour charger des données dans les tables Oracle SQL. Les tables externes sont aussi une méthode pour charger des données à partir de fichiers dans Oracle SQL.

## Question03
- [x] 4/ SQLLOADER reste tout de même une bonne option
  - **Explication** : Bien que ODI, et les drivers Oracle_HDFS et Oracle_HIVE puissent être utilisés dans certains contextes, SQLLoader est un choix valide pour charger des données dans Oracle SQL.

## Question04
- [x] 4/ Si on le souhaite utiliser scoop Hadoop
  - **Explication** : Sqoop est un outil conçu pour transférer des données entre Hadoop et des bases de données relationnelles. Il n'est pas prévu d'utiliser SQLLoader ou ODI pour Hadoop HDFS.

## Question05
- [x] 3/ Elle permet de consulter les données stockées dans des bases hétérogènes depuis Oracle SQL
  - **Explication** : L'architecture permet l'intégration de différentes bases de données, permettant les consultations croisées depuis Oracle SQL.

## Question06
- [x] 2/ Elle permet d'accéder depuis une base SQL à des données hétérogènes
  - **Explication** : L'architecture décrite permet d'accéder à des données de différents types de bases de données à partir d'une base de données Oracle SQL.

## Question07
- [x] 1/ Cette architecture permet aux utilisateurs d’outils OLAP de manipuler des données hétérogènes.
  - **Explication** : En ayant des connecteurs et des interfaces appropriés, les données hétérogènes peuvent être utilisées pour l'analyse OLAP.

## Question08
- [x] 3/ Un des éléments caractéristiques de Big Data SQL est la notion de tables externes
- [x] 4/ Un des éléments caractéristiques de Big Data SQL est le traitement parallèle des requêtes
  - **Explication** : Big Data SQL intègre des tables externes pour accéder à des données stockées en dehors de la base de données Oracle et utilise le traitement parallèle pour optimiser les requêtes.

## Question09
- [x] 2/ L'optimiseur Oracle rapatrie les lignes vers la base SQL uniquement les lignes utiles. Les clauses Where sont appliquées dans les SGBD ou SGF sources
  - **Explication** : L'optimiseur Oracle essaie de pousser l'exécution de la clause WHERE au plus près de la source de données pour minimiser le transfert de données inutiles.

## Question10
- [ ] Aucune des options n'est syntaxiquement juste; elles contiennent toutes des erreurs de syntaxe, comme des virgules et guillemets	 manquants.

## Question11
- [x] 2/ KVStore store=...; TableAPI tableAPI = store.getTableAPI(); stmt="create table lignesDeCommande(...);"; store.executeSync(stmt);
  - **Explication** : Cela semble être un exemple de code pour créer une table dans une base de données NoSQL en utilisant son API Java.

## Question12
- [x] 3/ get table -name commande -field prodid -value 1000 -field clientid -value 1
  - **Explication** : Cette commande recherche dans la table 'commande' pour un 'prodid' spécifique et 'clientid'.

## Question13
- [x] 1/ Le partition chez Oracle NoSql correspond à un SHARD
- [x] 2/ Un SHARD comprend un nœud de réplication maître et plusieurs nœuds de réplications esclave
- [x] 3/ Une base de données Oracle NoSQL peut comprendre plusieurs SHARD
  - **Explication** : Cela décrit correctement la structure d'un environnement Oracle NoSQL distribué et répliqué.

## Question14
- [ ] Selon le théorème CAP, un système distribué ne peut garantir que deux des trois propriétés suivantes à tout moment : Consistence (C), Availability (A), Partition Tolerance (P). Les options ne reflètent pas cette compréhension. 

## Question15
- [x] 3/ SHARD(PRODID) indique que toutes commandes d'un même produit sont stockées dans un même SHARD
  - **Explication** : La clause SHARD est utilisée pour déterminer la distribution des données sur différents SHARDs.

## Question16
- [x] 3/ store.get(key);
  - **Explication** : Cette commande semble être une façon de récupérer une entrée dans une base de données NoSQL Oracle en utilisant une clé primaire complète.

## Question17
- [x] 1/ La partie Major Key peut être composée de une ou plusieurs majeurs keys
- [x] 2/ La partie Minor Key peut être composée de une ou plusieurs minors keys
- [x] 4/ Il n'est pas obligatoire d'avoir une minor key
  - **Explication** : Cela reflète la flexibilité des clés dans le modèle clé/valeur.

## Question18
- [x] 1/ D'optimiser l'accès aux enregistrements
- [x] 2/ De mieux partitionner les données
- [x] 3/ De réduire le coût d'accès
  - **Explication** : La structuration en major et minor keys aide à l'organisation et l'accès efficace aux données.

## Question19
- [x] Vous devez créer une table externe Hive qui pointe vers la table Commande, puis une table externe oracle sql qui pointe vers la table externe Hive
  - **Explication** : Cela permettrait d'accéder à la table NoSQL à partir d'Oracle SQL via Hive.

## Question20
- [x] 4/ Select * from COMMANDE_EXT where commid=1;
  - **Explication** : Les tables externes en Oracle sont généralement en lecture seule, donc un SELECT serait possible, mais pas les opérations d'insertion, de mise à jour ou de suppression.

## Question21
- [x] 1/ Vous pouvez créer une table externe Hive qui pointe vers le fichier produits.txt, puis une table externe oracle sql qui pointe vers la table externe Hive
  - **Explication** : Cette approche est standard pour accéder aux fichiers HDFS via une base de données Oracle SQL, en utilisant Hive comme intermédiaire.

## Question22
- [x] 1/ Vous devez créer une table externe Hive qui pointe vers la table Commande, puis une table externe oracle sql qui pointe vers la table externe Hive
  - **Explication** : Si la table COMMANDE résidait dans une autre BD NoSQL, une table externe Hive pourrait servir de pont pour accéder à ces données depuis Oracle SQL.

En résumé, les questions de cet examen couvrent les stratégies de gestion des données entre différentes bases de données et systèmes de fichiers dans un écosystème Big Data. Elles touchent à des concepts tels que les tables externes, les utilitaires de chargement de données, les API de programmation, et les principes de conception des bases de données NoSQL.
