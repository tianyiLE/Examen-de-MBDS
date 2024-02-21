# MBDS TUNING ORACLE. Tune 2

durée 1h. 1 points/question. pas de docs autorisés.

Des points sont enlevés au prorata des mauvaises réponses cochées 1, 2 ou 3 réponses peuvent être correctes.

1) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. Les données collectées sont :
   - [x] Les temps CPU. Elapsed, le nombre de blocs lus dans les fichiers et/ou en mémoire pour chaque requête
   - [ ] Les erreurs de compilations de vos requêtes
   - [x] Les informations sur les paramètres d'initialisation
   - [x] Les événements et temps d'attentes pour chaque requête

2) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. Les données collectées sont cumulées par :
   - [ ] Par tablespace
   - [x] Par requêtes SQL
   - [x] Par session utilisateur (en se connectant l'utilisateur créé une session)
   - [x] Pour toutes les requêtes de la base depuis le démarrage d'une instance

3) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. Les données collectées qui forment le repository AWR (Automatic Workload Repository) y sont stockées dans le ou les tablespaces suivants :
   - [ ] System
   - [ ] Undotbs1
   - [x] Sysaux
   - [ ] Temp

4) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. La collecte des données suit la ou les règles suivantes :
   - [ ] Toutes les 3 secondes ou qu'un checkpoint a passé
   - [ ] A chaque fois qu'un COMMIT OU ROLLBACK est passé
   - [x] Toutes les heures par défaut
   - [x] La rythme de la collecte peut être adapté par l'administrateur

5) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. La collecte des données n'est possible que si le ou les paramètres d'initialisation suivants sont posés :
   - [ ] Memory_max_size et memory_target valent chacun 10G
   - [ ] Statistic_level valut BASIC
   - [x] Statistic_level valut TYPICAL ou ALL
   - [ ] Pga_aggregate_target valut 10G

6) Depuis la version 10g Oracle a développé un optimiseur automatique pour aider le DBA. Oracle collecte des données pour son fonctionnement. Les données collectées sont conservées dans le dictionnaire. La durée de conservation est :
   - [ ] Illimitée, en effet, oracle conserve bien les utilisateurs créés de façon illimitée
   - [ ] De 1 mois c'est la valeur par défaut
   - [x] De 1 semaine c'est la valeur défaut
   - [ ] De 1 an c'est la valeur par défaut

7) Depuis la version 10g l'optimiseur automatique d'Oracle s'appuie sur un certain nombre de conseillers. Cochez ce qui vous paraît caractériser le conseiller ADDM (Automatic Database Diagnostic Monitor):

   - [x] Ce conseiller peut être invoqué automatiquement ou manuellement
   - [ ] Il peut recommander d'arrêter et redémarrer de temps en temps l'instance pour tout réinitialiser (vitesse oblige)
   - [x] Il peut recommander de mieux régler les requêtes gourmandes
   - [x] Il peut recommander d'augmenter le nombre de CPU

8)  Depuis la version 10g l'optimiseur automatique d'Oracle s'appuie sur un certain nombre de conseillers. Cochez ce qui vous paraît caractériser le conseiller ADDM (Automatic Database Diagnostic Monitor):

   - [ ] Il peut recommander d'utiliser le conseiller Sql Tuning Advisor pour récupérer l'espace dans un segment
   - [ ] Il peut recommander d'utiliser le conseiller Sql Tuning Advisor pour augmenter la taille de la SGA et la PGA
   - [x] Il peut recommander d'utiliser le conseiller Sql Tuning Advisor pour régler un programme PL/SQL consommateur
   - [ ] Il peut recommander d'utiliser le conseiller Sql Tuning Advisor augmenter un programme java consommateur

9) **Depuis la version 10g l'optimiseur automatique d'Oracle s'appuie sur un certain nombre de conseillers. Cochez ce qui vous paraît caractériser le conseiller ADDM (Automatic Database Diagnostic Monitor):**

   - [x] Il peut recommander d'utiliser le conseiller Sql Access Advisor pour créer des vues matérialisées

   - [x] Il peut recommander d'utiliser le conseiller Sql Access Advisor pour investiguer la création d'indexes

   - [ ] Il peut recommander d'utiliser le conseiller Sal Access Advisor pour restructurer les requêtes mal écrites

   - [ ] Il peut recommander d'utiliser le conseiller Sal Access Advisor pour créer des profiles

10) Lors de la lecture d'un rapport ADDM, le développeur ou l'administrateur trouve le message suivant : le buffer Redolog est sous dimensionné. Valer actualisée 5 Mo. Pour traiter ce problème cocher la ou les bonnes actions correctives pouvant être proposées par ADDM :

   - [ ] Fixer la valeur de MEMORY_MAX_TARGET et MEMORY_TARGET à 10G

   - [x] Fixer la valeur de LOG_BUFFER à 500Mo

   - [ ] Fixer la valeur de LOG_BUFFER à 25Mo

   - [ ] Fixer la valeur de SGA_MAX_SIZE et SGA_TARGET à 5G

11) Lors de la lecture d'un rapport ADDM, le développeur ou l'administrateur trouve le message suivant : « La SGA et PGA sont sous dimensionnés, taille actuelle 1G, nous sommes en Oracle 11g ». Pour traiter ce problème, le DBA fixe MEMORY_MAX_TARGET à 3G, MEMORY TARGET à 3G. Cochez la ou les affirmations valides :

    - [ ] Il faut plutôt mettre SGA_MAX_SIZE et SGA_TARGET à 3G
    - [ ] Il faut plutôt mettre DB_CACHE_SIZE à 3G
    - [x] La configuration posée est bonne
    - [ ] Il faut plutôt mettre DB_recovery_file_dest à 100G

12) Lorsque l'administrateur sollicite le conseiller SQL Access Advisor, les requêtes à traiter lui sont fournies à travers :

    - [ ] Une charge définit par l'utilisateur dans une table appelée user_workload
    - [x] Une charge venant du cache des curseurs (sql area)
    - [ ] Une charge venant de la table Plan_table
    - [ ] Une charge venant d'un SQL Tuning Set

13) Lorsque l'administrateur sollicite le conseiller SQL Tuning Advisor, les requêtes à traiter peuvent provenir de:

    - [ ] Une charge définit par l'utilisateur dans une table appelée user_workload
    - [x] Une charge venant du cache des curseurs (sql area)
    - [ ] Une charge venant de la table v$session
    - [ ] Une charge venant du repository AWR (entre deux cliqués AWR)


14. Vous êtes en phase de développement d'une application de gestion des placements en bourse. Vous avez écrit un millier de requêtes. Vous souhaitez les optimiser. Choisir la ou les meilleures approches:
    - [ ] J'insère des lignes dans mes tables puis j'invoque le conseiller SQL Tuning Advisor
    - [ ] J'insère des lignes dans mes tables puis j'invoque le conseiller SQL Access Advisor 
    - [ ] J'insère des lignes dans mes tables puis j'invoque le conseiller segment Advisor
    - [x] J'insère des lignes dans mes tables puis je procède dans un premier temps au réglage manuel de chaque requête. C'est important pour comprendre les processus.

15. ADDM vous signale des ralentissements lors de l'accès à certains fichiers de données de votre base de données appelée DBCOURS. Quel est le ou les bons conseillers à utiliser pour Investiguer plus:
    - [ ] SQL Tuning Advisor
    - [x] SQL Access Advisor
    - [x] Segment Advisor
    - [ ] Undo Advisor

16.  Lorsque je veux générer un rapport ADDM en invoquant ce conseiller explicitement :

    - [ ] N'importe quel cliché AWR apparaissant dans la liste (indépendamment des instances) est utilisable

    - [x] Seuls les clichés issus d'une même instance sont utilisables

    - [ ] Les clichés générés manuellement dans une même instance par l'appel de la méthode dbms_workload_repository.create_snapshot sont utilisables

    - [ ] Les clichés générés manuellement dans une même instance par l'appel de la méthode dbms_workload_repository.create_snapshot ne sont utilisables

17. L'administrateur de base Oracle d'une banque bien connue souhaite lancer une activité de suppression / recréation des index d'une application. En effet, les indexs ne sont bon pour les performances. Au même moment les utilisateurs lancent des requêtes de consultation, à quelle classe d'événements d'attentes peuvent-ils à coût sûr être confrontés par rapport à cette activité.

    - [ ] À la classe d'événements User i/o
    - [ ] À la classe d'événements system i/o
    - [ ] À la classe d'événements commit
    - [x] À la classe d'événements administrative

18. L'activité du conseiller ADDM consiste à

    - [ ] Collecter les statistiques toutes heures et les stocker dans le repository AWR

    - [x] Analyser les statistiques de l'activité entre deux clichés AWR et proposer des recommandations de réglage

    - [ ] À ne pas détecter les requêtes SQL, les programmes PL/SQL, les programmes Java qui consomment le plus

    - [ ] Analyser les statistiques de l'activité entre deux clichés Statspack et proposer des recommandations de réglage

19.  Le conseiller sql tuning advisor est capable de recommander la génération d'un profil pour une requête. Cochez dans quel(s) cas les profils sont intéressants

    - [ ] Lorsque le dba souhaite éviter la génération des plans d'exécution dans la table plan_table

    - [ ] Lorsque le dba souhaite éviter sql access advisor

    - [x] Lorsque le dba ne peut accéder à la requête de régler que dans le cache des curseurs

    - [ ] Lorsque le dba peut accéder au code source de l'application qui contient cette requête

20. Vous avez la requête suivante que vous fait grincer les cheveux. Select ename, sal from emp, dept where emp.deptno=dept.deptno and ename="KING" and sal<3000, ADDM suggère qu'elle est très lente. Vous décidez d'utiliser le conseiller sql access advisor. Quelle peuvent être les recommandations les plus efficaces de ce conseiller :

    - [ ] De créer un index sur la colonne JOB de la table EMP
    - [x] De créer un index sur la colonne ENAME de la table EMP
    - [ ] De créer un index sur la colonne EMPNO et SAL de la table EMP
    - [x] De créer un index concaténé sur les colonnes ENAME et SAL de la table EMP

