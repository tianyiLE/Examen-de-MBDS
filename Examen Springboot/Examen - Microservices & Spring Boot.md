# Examen - Microservices & Spring Boot

1. Quelles affirmations sont vraies à propos des **architectures Microservices ?**
   - [x] Elles sont plus flexibles qu'une architecture monolithique
   
   - [ ] Elles sont plus rapides à développer en jour/homme total que des architectures monolithiques
   
   - [x] Elles ont un *time to market* potentiel plus court que dans le cas des architectures monolithiques
   
   - [ ] Le *time to market* sera égal à la somme des temps de développements de tous les services
   
2. Quelle affirmation est vraie à propos des **architectures Microservices ?**
   - [ ] Faire évoluer le projet après le développement initial est complexe
   
   - [x] Le coût initial global de développement sera supérieur comparativement aux architectures monolithiques
   
   - [ ] Le coût des tâches d’évolution sera supérieur comparativement aux architectures monolithiques
   
   - [ ] Le coût d’hébergement sera supérieur comparativement aux architectures monolithiques
   
3. Quelles affirmations sont vraies à propos des **architectures Microservices ?**
   
   - [x] Elles supportent mieux les modifications en cours de projet que les architectures monolithiques
   
   - [ ] Elles sont plus résilientes face à la complexité

   - [ ] Elles sont faites pour être réalisées par une petite équipe de développeur
   
   - [ ] Elles vont diminuer la compétitivité de l’entreprise qui la mettent en oeuvre
   
4. Quelles affirmations sont vraies à propos des **architectures Microservices** ?
   
   - [x] Elles sont liées à des thèmes abordés dans les domaines des API REST
   
   - [ ] Échangent principalement via des échanges SOAP

   - [ ] Chaque composant a une visibilité sur l’architecture complète
   
   - [x] Elles sont étroitement liées avec le Single Responsibility Principle
   
5. Quelles affirmations sont vraies à propos des architectures Microservices ?
   - [ ] Elles doivent être développées sur un seul et même environnement technique (tout en Spring ou tout en Python par exemple)
   
   - [x] Elles peuvent avoir autant de contexte techniques différentes de que « services »
   
   - [ ] Elles doivent partager une même base de données pour tous les « services »

   - [ ] Elles doivent être développées pour fonctionner sur des bases de données relationnelles
   
   - [x] Elles peuvent faire cohabiter tous types de base de données simultanément
   
6. Quelles affirmations sont vraies à propos de Spring Boot ?
   
   - [ ] C’est l’équivalent de Spring avec d’autres langages
   
   - [x] C’est une surcouche du framework Spring
   
   - [ ] Il s’agit uniquement d’une solution pour créer un projet Spring
   
   - [x] S’appuie sur un ensemble de « starters »

7. La gestion de la persistance dans Spring Boot via JPA implique plusieurs composants, quels sont-ils ?
   - [x] Les « Repository »
   
   - [ ] Les « Controller »
   
   - [ ] Les « RestController »

   - [x] Les « Entity »
   
   - [ ] Les « Service »
   
8. Quels sont les « Repository » dont on peut « extends » ?
   
   - [ ] EntityRepository
   
   - [x] CrudRepository
   
   - [x] JpaRepository

   - [ ] RequestRepository
   
   - [ ] Repository
   
   - [ ] SimpleRepository
   
9. Lors de la création d'un « Repository », on doit « extends » le « Repository » souhaité et préciser ces éléments ...
   - [ ] La cardinalité des relations
   
   - [ ] Les contraintes à appliquer sur le modèle associé à l'entité
   
   - [x] Le type de l'identifiant de l'entité désignée
   
   - [ ] La classe de l'entité désignée
   
10. Les « Repository » exposent un certain nombre de méthodes, quelles sont-elles ?
   - [x] save
   
   - [x] findAll
   
   - [ ] findAllByName
   
   - [ ] update
   
11. Quelles seront les conséquences de la déclaration dans un « RestController » d'une méthode précédée de l'annotation « @GetMapping(value = '/products') » ?
   - [x] La méthode sera exécutée lors d'un appel sur l'url « /products » en GET
   
   - [ ] La méthode sera exécutée lors d'un appel sur l'url « /products » en POST
   
   - [ ] La méthode renverra forcément une liste de produits
   
   - [ ] La méthode doit renvoyer une réponse à l'utilisateur sans quoi le serveur retournera une erreur 500
   
12. L'injection de dépendances peut se faire de plusieurs manières, quelles sont-elles ?
   
   - [x] Injection sur les attributs
   
   - [x] Injection sur les méthodes
   
   - [ ] Injection fonctionnelle
   
   - [x] Injection sur les constructeurs
   
   - [ ] Injection prédictive
   
   - [ ] Injection sur la classe
   
   - [x] Injection sur les getters / setters