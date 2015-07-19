---
title: Overview
sectionName: API Reference
template: api.jade
menuIndex: 3
---

This pages contains general documentation about the API. Use the links on the
right to navigate to specific resources.

### Content-type

The API uses the JSON format. Unless specified otherwise, all requests and
response should have the `Content-Type: application/json` header.

### HTTP verbs

The API uses the standard HTTP verbs to perform CRUD operations (**C**reate,
**R**etrieve, **U**pdate, **D**elete) on resources, following standard RESTful
API practices.

Find below a quick summary of how HTTP verbs are used in the API:

| Verb     | Description |
|----------|--------
| `GET`    | Used for retrieving a resource or a collection of resources.
| `POST`   | Used for creating a new resource or performing a non-CRUD operation on a resource.
| `PUT`    | Used to perform a full update of a resource (replacing the resource by the JSON data provided in the request).
| `DELETE` | Used for deleting resources.

`HEAD` et `PATCH` ne sont actuellement pas utilisés.

### Authentication

To interact with the API, your client will need to be authenticated for few resources. This is done by using the **x-user-id** header with the user id of the client and gives something that looks like:

	x-user-id: <id>

### Authorizations

| Role      | Description |
|-----------|--------
| `any`     | Authenticated user is enough.
| `various` | Complex authorization scheme detailed directly in the resource.
| `citizen` | Any user with citizen role.
| `staff`   | Any user with staff role.

### Errors

401/403 - Accès à cette ressource non autorisé car n'a pas les droits, ou n'est pas connecté.
404 - Lorsqu'une ressource n'est pas trouvée ou existante, un status 404 est envoyé au client.
500 - Une erreur du serveur.
