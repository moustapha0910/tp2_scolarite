# Compte Rendu - TP 2 : Dart en pratique

- **Étudiants :** Diarrassouba Moustaphe Abdala et Dozounon Marie Ange Christelle
- **Lien du dépôt GitHub :** https://github.com/moustapha0910/tp2_scolarite
- **Identifiant du dernier commit (Hash) :** c1d2ebf

---

## 1. Réponses aux questions [Q]

- **[Q1] Quel est l'intérêt d'utiliser l'opérateur de coalescence null `??` dans le décodage JSON des étudiants ?**
  L'opérateur `??` permet de fournir une valeur par défaut (par exemple, une map vide ou une chaîne spécifique) si la valeur lue dans le JSON est `null`, évitant ainsi les erreurs de type `NullPointerException` lors du parsing des données optionnelles comme l'e-mail ou les notes.

- **[Q2] Pourquoi les fonctions de statistiques (`moyenne`, `classement`, etc.) ont-elles été conçues sans utiliser de boucles `for` traditionnelles ?**
  L'utilisation de méthodes fonctionnelles (`fold`, `reduce`, `where`, `map`) favorise un code plus déclaratif, plus lisible et plus immunisé contre les erreurs d'indices ou de mutation d'état, ce qui s'aligne avec les paradigmes modernes gérés par Dart.

- **[Q3] Quel est l'avantage des classes scellées (`sealed class`) associées à une expression `switch` pour la gestion des résultats de délibération ?**
  Les classes scellées garantissent l'exhaustivité des cas possibles au moment de la compilation. Le compilateur Dart s'assure ainsi que tous les cas de résultats (Admis, Rattrapage, Ajourné) sont explicitement traités dans le `switch`, rendant le code plus sûr et facilitant l'évolutivité en cas d'ajout de nouveaux statuts.

---

## 2. Difficultés rencontrées et solutions
- **Manipulation des types dans les collections :** Le cast explicite des types dynamiques vers des structures typées (comme `Map<String, double>`) a été résolu grâce à l'application rigoureuse des méthodes de transformation fonctionnelle.
- **Asynchronisme :** La coordination des flux (`Stream`) et des requêtes asynchrones en parallèle (`Future.wait`) a nécessité une structuration précise des services de test dans `service.dart`.
