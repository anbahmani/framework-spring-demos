# Démo — Cours 09 : Exposer un service Spring avec MCP

Expose un outil en lecture seule avec un serveur MCP Streamable HTTP. MCP Inspector permet de découvrir l’outil et de l’appeler sans configurer de modèle d’IA.

**Cours associé :** [ouvrir le support](https://anbahmani.github.io/framework-spring-course/cours/09-mcp.html).

## Lancer la démonstration

Prérequis : Java 25 et Maven 3.9. Depuis ce dossier :

```bash
mvn spring-boot:run
```

Le serveur MCP écoute à `http://localhost:8080/mcp`. Pour l’explorer, lancer `npx -y @modelcontextprotocol/inspector`, choisir le transport Streamable HTTP et se connecter à cette adresse. L’outil `findUserById` accepte un identifiant ; les fiches `1` et `2` sont présentes.

## Ce que montre le projet

`DirectoryTools` expose une méthode annotée avec `@McpTool`. Spring AI détecte le bean, publie la description et le schéma du paramètre, puis transmet les appels à `DirectoryService`. L’application ne dépend d’aucun modèle ni d’aucune clé d’API.

Le projet utilise Spring Boot 4.1.1 et Spring AI 2.0.1. Le transport HTTP n’applique pas à lui seul une politique d’authentification ; cette démonstration reste locale et en lecture seule.

## Collection Bruno et Postman

MCP utilise un cycle JSON-RPC et une session Streamable HTTP, pas une API REST classique. Les clients HTTP génériques ne remplacent pas l’inspecteur MCP pour cette découverte guidée ; consulter les notes dans `bruno/` et `postman/`.
