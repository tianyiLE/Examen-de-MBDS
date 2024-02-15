# Corrigé- Microservices & Spring Boot

1. **Vraies affirmations sur les architectures Microservices** :

   - **Vrai** : Elles sont plus flexibles qu'une architecture monolithique, permettant des mises à jour et des modifications plus aisées de parties spécifiques de l'application sans affecter le reste.
   - **Faux** : Elles sont plus rapides à développer en jour/homme total que des architectures monolithiques. En réalité, elles peuvent exiger plus de temps en raison de la complexité liée à la gestion de multiples services distincts.
   - **Vrai** : Elles ont un *time to market* potentiel plus court que dans le cas des architectures monolithiques, grâce à la possibilité de développer, tester et déployer des services de manière indépendante.
   - **Faux** : Le *time to market* sera égal à la somme des temps de développements de tous les services. Ce n'est pas nécessairement vrai, car le développement en parallèle et l'indépendance des services peuvent réduire le temps total de mise sur le marché.

2. **Vraie affirmation sur les architectures Microservices** :

   - **Faux** : Faire évoluer le projet après le développement initial est complexe. Au contraire, l'évolution est généralement plus facile avec les microservices en raison de leur indépendance.
   - **Vrai** : Le coût initial global de développement sera supérieur comparativement aux architectures monolithiques en raison de la nécessité de configurer l'infrastructure de communication entre les services, la gestion des données distribuées, etc.
   - **Faux** : Le coût des tâches d’évolution sera supérieur comparativement aux architectures monolithiques. L'évolution est souvent moins coûteuse sur le long terme avec les microservices.
   - **Faux** : Le coût d’hébergement sera supérieur comparativement aux architectures monolithiques. Cela dépend de l'implémentation et de la gestion des ressources.

3. **Vraies affirmations sur les architectures Microservices** :

   - **Vrai** : Elles supportent mieux les modifications en cours de projet que les architectures monolithiques, offrant une plus grande agilité dans les modifications et les ajouts de fonctionnalités.
   - **Faux** : Elles sont plus résilientes face à la complexité. Elles peuvent gérer la complexité d'une manière différente, mais ne sont pas nécessairement plus résilientes par défaut.
   - **Faux** : Elles sont faites pour être réalisées par une petite équipe de développeur. Bien qu'elles puissent bénéficier de petites équipes travaillant sur des services individuels, les microservices peuvent également être adaptés pour de grandes équipes.
   - **Faux** : Elles vont diminuer la compétitivité de l’entreprise qui la met en oeuvre. Au contraire, elles peuvent augmenter la compétitivité en permettant une innovation et une évolution plus rapides.

4. **Vraies affirmations sur les architectures Microservices** :

   - **Vrai** : Elles sont liées à des thèmes abordés dans les domaines des API REST, les microservices communiquant souvent via des API REST.
   - **Faux** : Échangent principalement via des échanges SOAP. Bien que possible, REST est plus couramment utilisé dans les architectures microservices modernes.
   - **Faux** : Chaque composant a une visibilité sur l’architecture complète. En réalité, chaque service est conçu pour fonctionner de manière indépendante, sans nécessiter une connaissance complète de l'architecture.
   - **Vrai** : Elles sont étroitement liées avec le Single Responsibility Principle, chaque service étant responsable d'une fonctionnalité ou d'un domaine d'affaires spécifique.

5. **Vraies affirmations sur les architectures Microservices** :

   - **Faux** : Elles doivent être développées sur un seul et même environnement technique. L'un des avantages des microservices est la possibilité d'utiliser différentes technologies adaptées à chaque service.
   - **Vrai** : Elles peuvent avoir autant de contexte techniques différentes que de « services », permettant une diversité technologique.
   - **Faux** : Elles doivent partager une même base de données pour tous les « services ». Idéalement, chaque service gère sa propre base de données pour éviter les dépendances.
   - **Faux** : Elles doivent être développées pour fonctionner sur des bases de données relationnelles. Les microservices peuvent utiliser tout type de stockage de données, y compris non relationnel.

      - **Vrai** : Elles peuvent faire cohabiter tous types de base de données simultanément, offrant une flexibilité dans la gestion des données.


6. **Vraies affirmations sur Spring Boot** :

   - **Faux** : C’est l’équivalent de Spring avec d’autres langages. Spring Boot est spécifiquement conçu pour simplifier le développement d'applications Spring en Java.
   - **Vrai** : C’est une surcouche du framework Spring, offrant une configuration par défaut pour démarrer rapidement un projet Spring.
   - **Faux** : Il s’agit uniquement d’une solution pour créer un projet Spring. Spring Boot offre bien plus, y compris l'exécution autonome et la configuration automatique.
   - **Vrai** : S’appuie sur un ensemble de « starters », qui sont des dépendances conçues pour simplifier l'ajout de fonctionnalités à votre application.

7. **Composants impliqués dans la gestion de la persistance via JPA dans Spring Boot** :

   - **Vrai** : Les « Repository ».
   - **Faux** : Les « Controller ». Ils sont utilisés pour gérer les requêtes HTTP, pas directement pour la persistance.
   - **Faux** : Les « RestController ». Comme les « Controller », ils gèrent les requêtes HTTP.
   - **Vrai** : Les « Entity », qui représentent les tables de la base de données dans le code.
   - **Faux** : Les « Service ». Bien qu'ils puissent interagir avec les « Repository », ils ne sont pas spécifiques à JPA.

8. **« Repository » que l'on peut « extends »** :

   - **Faux** : EntityRepository. Ce n'est pas un type de repository standard dans Spring Data.
   - **Vrai** : CrudRepository, fournissant des opérations CRUD pour l'entité.
   - **Vrai** : JpaRepository, offrant des fonctionnalités CRUD et JPA spécifiques.
   - **Faux** : RequestRepository. Ce n'est pas un type de repository standard dans Spring Data.
   - **Vrai** : Repository, l'interface de base pour tous les repositories Spring Data. ==存疑==
   - **Faux** : SimpleRepository. Ce n'est pas un type de repository standard dans Spring Data.

9. **Lors de la création d'un « Repository », on doit préciser** :

   - **Faux** : La cardinalité des relations. Cela est spécifié dans les entités, pas dans les repositories.
   - **Faux** : Les contraintes à appliquer sur le modèle associé à l'entité. Les contraintes sont définies au niveau de l'entité.
   - **Vrai** : Le type de l'identifiant de l'entité désignée, important pour les opérations CRUD.
   - **Vrai** : La classe de l'entité désignée, pour spécifier sur quelle entité le repository opère.

10. **Méthodes exposées par les « Repository »** :

    - **Vrai** : save, pour sauvegarder ou mettre à jour une entité.
    - **Vrai** : findAll, pour récupérer toutes les entités.
    - **Faux** : findAllByName. C'est un exemple de méthode qui pourrait être créée par le développeur en suivant les conventions de nommage de Spring Data, mais ce n'est pas une méthode exposée par défaut.
    - **Faux** : update. Les opérations de mise à jour sont réalisées avec la méthode save.

11. **Conséquences de la déclaration d'une méthode avec « @GetMapping(value = '/products') » dans un « RestController »** :

    - **Vrai** : La méthode sera exécutée lors d'un appel sur l'url « /products » en GET, permettant de récupérer des données.
    - **Faux** : La méthode sera exécutée lors d'un appel sur l'url « /products » en POST. @GetMapping est spécifique aux requêtes GET.
    - **Faux** : La méthode renverra forcément une liste de produits. Le type de retour dépend de l'implémentation de la méthode.
    - **Faux** : La méthode doit renvoyer une réponse à l'utilisateur sans quoi le serveur retournera une erreur 500. Si la méthode ne renvoie pas de réponse, cela ne mène pas nécessairement à une erreur 500; cela dépend de l'implémentation.

12. **Manières de réaliser l'injection de dépendances** :

- **Vrai** : Injection sur les attributs, directement dans les champs de la classe.
- **Vrai** : Injection sur les méthodes, telles que les setters.
- **Faux** : Injection fonctionnelle. Ce n'est pas un terme communément utilisé pour décrire les types d'injection de dépendances.
- **Vrai** : Injection sur les constructeurs, passant les dépendances via les paramètres du constructeur.
- **Faux** : Injection prédictive. Ce n'est pas un concept reconnu dans l'injection de dépendances.
- **Faux** : Injection sur la classe. L'injection se fait sur les membres de la classe, pas sur la classe elle-même.
- **Vrai** : Injection sur les getters / setters, permettant de définir et récupérer des dépendances via des méthodes spécifiques.