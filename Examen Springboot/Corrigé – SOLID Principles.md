# Corrigé – SOLID Principles

1. Les principes SOLID sont des directives conçues pour développer des logiciels de manière à ce qu'ils soient faciles à maintenir et à étendre au fil du temps. Parmi les affirmations données :
   - **Vrai** : Ils vous aident à concevoir et produire des architectures flexibles, scalables et faciles à maintenir.
   - **Faux** : L'ensemble de principes est voué à produire des architectures avec comme soucis principal la robustesse. Bien que la robustesse puisse être un effet secondaire, ce n'est pas le souci principal.
   - **Faux** : Les principes sont un ensemble de règles à respecter qui décrivent la manière d'implémenter vos architectures dans différents langages. Les principes SOLID sont plutôt des concepts de haut niveau et ne dépendent pas d'un langage spécifique.
   - **Vrai** : Les principes sont un ensemble des règles et bonnes pratiques de haut niveau sans lien avec une implémentation particulière.

2. Le Single Responsibility Principle (SRP) stipule qu'une classe doit avoir une seule raison de changer, ce qui signifie :

   - **Vrai** : Dit qu'une classe doit avoir une seule raison de changer.
   - **Faux** : Dit qu'une classe ne doit avoir qu'une seule interface. Ce n'est pas ce que le SRP indique.
   - **Faux** : Dit qu'une classe ne doit être parent que d'un seul héritage. Ce n'est pas lié au SRP.
   - **Vrai** : Fait un parallèle entre la "responsabilité" et les "raisons de changer".

3. La mise en œuvre du Single Responsibility Principle aide à obtenir des architectures :

   - **Faux** : Robustes. Bien que la robustesse puisse être améliorée, ce n'est pas l'objectif principal du SRP.
   - **Faux** : Véloces. La vitesse n'est pas le focus direct du SRP.
   - **Vrai** : Avec des éléments réutilisables. Le SRP favorise la réutilisabilité en minimisant les responsabilités de chaque classe.
   - **Faux** : Résistantes aux intrusions. Ceci est plus lié à la sécurité et n'est pas le focus du SRP.

4. Le niveau de segmentation dans la mise en œuvre du Single Responsibility Principle dépend de :

   - **Faux** : Le langage utilisé pour le développement de l'architecture. Le choix du langage n'affecte pas directement le niveau de segmentation.
   - **Vrai** : La taille de l'équipe de développement. Une grande équipe peut gérer plus de segmentation.
   - **Vrai** : Les compétences de l'équipe de développement. Les équipes plus compétentes peuvent gérer des architectures plus segmentées efficacement.
   - **Vrai** : Du type de gestion de projet utilisé. Différentes méthodologies peuvent influencer le degré de segmentation.
   - **Vrai** : Des contraintes de temps. Les délais peuvent limiter la capacité à segmenter finement.

5. L’Open / Closed Principle stipule que les entités logicielles (classes, modules, fonctions, etc.) doivent être ouvertes à l'extension, mais fermées à la modification :

   - **Faux** : La visibilité de vos attributs doit être précise et adaptée. Ceci est plus lié à l'encapsulation.
   - **Faux** : Vos classes doivent être ouvertes aux modifications. Cela va à l'encontre de l'Open/Closed Principle.
   - **Faux** : Les classes ouvertes doivent être ouvertes aux modifications. Encore une fois, ceci contredit le principe.
   - **Vrai** : Vos classes doivent être ouvertes aux extensions.
   - **Vrai** : Vos classes doivent être fermées aux modifications.
   - **Faux** : Vos classes doivent être fermées aux extensions. Le principe encourage les extensions.

6. Pour mettre en œuvre l'Open / Closed Principle, on peut utiliser :

   - **Vrai** : L’héritage.
   - **Vrai** : Les interfaces.
   - **Faux** : L’association. Bien qu'utile dans certains contextes, ce n'est pas un moyen direct d'appliquer ce principe.
   - **Vrai** : La composition.
   - **Faux** : La relation. Ce terme est trop général et ne spécifie pas une technique directe d'application de ce principe

.

7. En Java, S est considéré comme un sous-type de T :

   - **Faux** : Lorsque S est T. Cela indique l'identité plutôt que la sous-typification.
   - **Faux** : Lorsque S est composé de T. La composition ne fait pas de S un sous-type de T.
   - **Vrai** : Lorsque S hérite de T.
   - **Vrai** : Lorsque S implémente T.
   - **Faux** : Lorsque T est composé de S. Ceci indique une composition inverse et non une relation de sous-typage.

8.  Le Principe de Substitution de Liskov (LSP) stipule qu'un objet d'un certain type doit être remplaçable par des objets de types dérivés sans altérer la correction du programme. Cela implique :

   - **Vrai** pour 8 : Un sous-type doit pouvoir être remplacé par son type de base. 
   - **Faux** pour 8 : Un type de base doit pouvoir être remplacé par son sous-type. LSP est souvent formulé en termes de sous-types remplaçant les types de base.
   - **Vrai** pour 8 : Si S est un type dérivé de T, les objets de type S doivent se comporter comme les objets de type T sont censés se comporter s'ils sont traités comme des objets de type T.
   - **Faux** pour 8 : Une classe et son sous type doivent toujours hériter d'une superclasse. Ce n'est pas spécifique au LSP.

9. Pour 9, Liskov parle de covariance et de contravariance dans le contexte des types de retour et des arguments de méthode, mais dans un sens qui favorise la substituabilité :
    - **Faux** : Il doit y avoir contra variance des arguments. LSP ne stipule pas cela; il s'agit de la covariance des arguments.
    - **Faux** : Il doit y avoir contra variance des types de retour. LSP favorise la covariance des types de retour.
    - **Faux** : Il doit y avoir covariance des arguments. C'est le contraire; LSP s'occupe de la covariance des types de retour.
    - **Vrai** : Il doit y avoir covariance des types de retour. Cela permet la substituabilité sans erreur.

10. Le Principe de Ségrégation des Interfaces (ISP) recommande de ne pas forcer les clients à dépendre d'interfaces qu'ils n'utilisent pas :

   - **Faux** : Il vaut mieux créer des interfaces génériques. ISP favorise des interfaces plus petites et spécifiques.
   - **Vrai** : Il vaut mieux créer des interfaces spécifiques.
   - **Faux** : Il faut créer une interface par méthode « générique ». Ce serait une interprétation extrême et pas toujours pratique.
   - **Vrai** : Il faut faire en sorte d'avoir des interfaces qui font sens.

11. Le Principe d’Inversion des Dépendances (DIP) concerne la manière dont les dépendances sont structurées dans un programme :

    - **Faux** : Les modules de haut niveau doivent dépendre des modules de bas niveau. DIP stipule le contraire.
    - **Faux** : Les modules de bas niveau doivent dépendre des modules de haut niveau. Encore une fois, DIP prône l'inverse.
    - **Vrai** : Les modules de haut et bas niveau doivent dépendre d'abstractions.
    - **Faux** : Les abstractions doivent dépendre des modules de haut niveau. C'est l'inverse qui est vrai dans DIP.
    - **Faux** : Les abstractions doivent dépendre des modules de bas niveau. DIP indique que les dépendances doivent être sur les abstractions et non l'inverse.
    - **Faux** : Est une conséquence naturelle de l'application du 2^ème et 3^ème principe. Bien que lié, c'est indépendant dans son application.

12. Les objectifs des principes SOLID incluent :

    - **Faux** : Être capable de briller en société. Bien que connaître SOLID puisse impressionner dans certains milieux, ce n'est pas l'objectif principal.
    - **Vrai** : Être capable de concevoir des systèmes flexibles, tolérants aux pannes, scalable avec des composants hautement interopérants (Stateless) qui vous permettront facilement de mettre en œuvre des architectures type « Micro-services ».

        - **Vrai** : Donner un ensemble de guidelines qui vont vous mener vers un ensemble de bonnes pratiques qui vous permettront de vous adapter à n'importe quelle équipe de développement.
