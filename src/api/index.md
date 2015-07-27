---
title: Overview
sectionName: API Reference
template: api.jade
menuIndex: 2
---

Cette page contient la documentation générale sur l'API. Utilisez les liens à la droite pour naviguer aux ressources voulues.

### Content-type

L'API utilise le format JSON. A moins que spécifié autrement, toutes les requêtes et 
réponses doivent avoir le header suivant :

	Content-Type: application/json

### verbes HTTP 

L'API utilise les verbes HTTP standard pour réaliser des opréations CRUD (**C**reate,
**R**etrieve, **U**pdate, **D**elete) sur les ressources.

Ci-dessous un bref résumé de comment les verbes HTTP sont utilisés dans l'API :

| Verbes   | Description |
|----------|--------
| `GET`    | Utilisé pour retrouver une ressource ou une collection de ressources.
| `POST`   | Utilisé pour créer une nouvelle ressource ou faire une opération de recherche avec paramètres.
| `PUT`    | Utilisé pour faire une mise à jours complête de la ressource (remplacera la ressource par les données JSON provenant de la requête).
| `DELETE` | Utilisé pour supprimer des ressources.

`HEAD` et `PATCH` ne sont actuellement pas utilisés.

### Authentification

Pour intéragir avec l'API, votre client devra être authentifié pour certaines ressources. Ceci est fait par l'utilisation de l'entête "Authorization" avec un token obtenu une fois connecté et retransmit dans chaque requête. Cela donnera un entête comme cela :

	Authorization: Bearer <token>

### Autorisation

| Role      | Description |
|-----------|--------
| `user` 	| Tout utilisateur avec le rôle user.
| `staff`   | Tuot utilisateur avec le rôle staff.
| `manager` | Tuot utilisateur avec le rôle manager.

### Errors

<p>401/403 - Accès à cette ressource non autorisé car n'a pas les droits, ou n'est pas connecté.</p>
<p>404 - Lorsqu'une ressource n'est pas trouvée ou existante, un status 404 est envoyé au client.</p>
<p>500 - Une erreur du serveur.</p>
