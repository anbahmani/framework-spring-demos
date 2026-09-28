# Démonstrations des huit cours Spring

Ce dépôt contient les applications de démonstration exécutables du cours d’architecture et framework Spring. La démonstration fait partie de chaque séance : elle présente le comportement général et les composants essentiels du projet avant le TP, qui demande aux étudiants de modifier le code. Prérequis : Java 25, Maven 3.9 et Spring Boot 3.5.16.

| Cours | Démo | Support |
| --- | --- | --- |
| 1 | [Démarrer Spring Boot et répondre à une requête HTTP](course-01-premiers-pas/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/01-premiers-pas.html) |
| 2 | [Observer méthode HTTP, paramètres et conversion JSON](course-02-http-json/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/02-http-json.html) |
| 3 | [Suivre l’injection entre contrôleur et service](course-03-injection-couches/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/03-injection-couches.html) |
| 4 | [Observer le cycle CRUD et les réponses HTTP](course-04-api-crud/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/04-api-crud.html) |
| 5 | [Comparer collection en mémoire et stockage H2](course-05-persistance/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/05-persistance.html) |
| 6 | [Lire les tests qui vérifient HTTP et rollback](course-06-tests-transactions/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/06-tests-transactions.html) |
| 7 | [Faire un appel HTTP depuis une seconde application Spring](course-07-client-http/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/07-client-http.html) |
| 8 | [Observer l’envoi et la réception asynchrones](course-08-messages/README.md) | [Cours associé](https://anbahmani.github.io/framework-spring-course/cours/08-messages.html) |

Chaque projet dispose de son propre `pom.xml` et README. Depuis le dossier choisi, lancer `mvn spring-boot:run` ou `mvn test` selon la séance. À la racine, `mvn test` vérifie les huit démos de cours. Les deux exemples complémentaires `rest-users` et `jms-orders` ne font pas partie de cette progression ; ils se vérifient séparément avec `mvn -f rest-users/pom.xml test` et `mvn -f jms-orders/pom.xml test`.
