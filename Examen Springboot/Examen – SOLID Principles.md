# Examen – SOLID Principles

1. Quelles affirmations sont vraies à propos des principes SOLID ?

   - [x] Ils vous aident à concevoir et produire des architectures flexibles, scalables et faciles à maintenir.

   - [ ] L'ensemble de principes est voué à produire des architectures avec comme soucis principal la robustesse

   - [ ] Les principes sont un ensemble de règles à respecter qui décrivent la manière d'implémenter vos architectures dans differents langages

   - [x] Les principes sont un ensemble des règles et bonnes pratiques de haut niveau sans lien avec une implémentation particulière.

2. Quelles affirmations sont vraies à propos du **Single Responsibility Principle** ?

   - [x] Dit qu'une classe doit avoir une seule raison de changer

   - [ ] Dit qu'une classe ne doit avoir qu'une seule interface

   - [ ] Dit qu'une lasse ne doit être parent que d'un seul héritage

   - [x] Fait un parallèle entre la "responsablité" et les "raisons de changer"

3. La mise en œuvre du **Single Responsibility Principle** va aider à obtenir des architectures...
   - [ ] Robustes

   - [ ] Véloces

   - [x] Avec des éléments réutilisables

   - [ ] Résistantes aux intrusions

4. Dans la mise en œuvre du **Single Responsibility Principle** on peut segmenter plus ou moins une architecture le niveau de segmentation dépendra de plusieurs critères, lesquels ?

   - [ ] Le langage utilsé pour le développement de l'architecture

   - [x] Le taille de l'équipe de développement

   - [x] Les compétences de l'équipe de développement

   - [x] Du type de gestion de projet utilsé

   - [x] Des contraintes de temps

5. Quelles affirmations sont vraies à propos de l’Open / Closed Principle ?

   - [ ] La visibilité de vos attributs doit être précise et adaptée

   - [ ] Vos classes doivent être ouvertes aux modifications

   - [ ] Les classes ouvertes doivent être ouvertes aux modifications

   - [x] Vos classes doivent être ouvertes aux extensions

   - [x] Vos classes doivent être fermées aux modifications

   - [ ] Vos classes doivent être fermées aux extensions

6. Par quels moyens peut-on mettre en œuvre ce principe ? ==存疑==

   - [x] L’héritage

   - [x] Les interfaces

   - [ ] L’association

   - [x] La composition

   - [ ] La relation

7. En Java, dans quels cas considère-t-on que S est un sous type de T ?

   - [ ] Lorsque S est T

   - [ ] Lorsque S est composé de T

   - [x] Lorsque S hérite de T

   - [x] Lorsque S implémente T

   - [ ] Lorsque T est composé de S

8. Quelles affirmations sont vraies à propos du **Principe de Substitution de Liskov ?**

   - [x] Un sous-type doit pouvoir être remplacé par son type de base

   - [ ] Un type de base doit pouvoir être remplacé par son sous-type

   - [x] Si S est un type de type déclaré de T, les objets de type S doivent se comporter comme les objets de type T sont censés se comporter s'ils sont traités comme des objets de type T

   - [ ] Une classe et son sous type doivent toujours hériter d'une superclasse

9. Quelles affirmations sont vraies à propos du **Principe de Substitution de Liskov ?**

   - [ ] Il doit y avoir contra variance des arguments

   - [ ] Il doit y avoir contra variance des types de retour

   - [ ] Il doit y avoir covariance des arguments

   - [x] Il doit y avoir covariance des types de retour

10. Quelles affirmations sont vraies à propos du **Principe de Ségrégation des Interfaces ?**

  - [ ] Il vaut mieux créer des interfaces génériques

  - [x] Il vaut mieux créer des interfaces spécifiques

  - [ ] Il faut créer une interface par méthode « générique »

  - [x] Il faut faire en sorte d'avoir des interfaces qui font sens

11. Quelles affirmations sont vraies à propos du **Principe d’Inversion des Dépendances ?**

   - [ ] Les modules de haut niveau doivent dépendre des modules de bas niveau

   - [ ] Les modules de bas niveau doivent dépendre des modules de haut niveau

   - [x] Les modules de haut et bas niveau doivent dépendre d'abstractions

   - [ ] Les abstractions doivent dépendre des modules de haut niveau

   - [ ] Les abstractions doivent dépendre des modules de bas niveau

   - [ ] Est une conséquence naturelle de l'application du 2^ème et 3^ème principe

12. Quels sont les objectifs de ces principes (Celle-là c'est pour moi.) ?

   - [ ] Être capable de briller en société

   - [x] Être capable de concevoir des systèmes flexibles, tolérants aux pannes, scalable avec des composants hautement interopérants (Stateless) qui vous permettront facilement de mettre en œuvre des architectures type « Micro-services »

   - [x] Donner un ensemble de guidelines qui vont vous mener vers un ensemble de bonnes pratiques qui vous permettront de vous adapter à n'importe quelle équipe de développement