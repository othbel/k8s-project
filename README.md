### Le Projet

Notre projet consiste en trois API réalisées avec Node.js et un front React. Ce projet consiste en trois API qui doivent communiquer entre elles pour fonctionner correctement. 

### Comment fonctionne le projet ?

Pour pouvoir tester les endpoints, il est nécessaire, dans notre cas, de faire des appels REST de type POST tel que: 

* Pour tester l'API concernant les utilisateurs, on peut faire une reqête POST à l'endpoint `/signup` pour créer un utilisateur et l'endpoint `/login` pour récupérer le token. Le corps des requêtes doit comporter un JSON de ce type:

```json
{
  "email": "test@example.com",
  "password": "password"
}
```

Dans le cas où l'API fonctionne, on aura une réponse ayant pour code de statut un **2xx** une réponse sous la forme d'un JSON, confirmant le bon fonctionnement de l'API. 

* Pour tester l'API des tâches, il nous faut via le client REST, réaliser un POST vers `/tasks` avec un Bearer token ayant pour valeur `abc` et comme corps de la requête un JSON ayant pour structure: 

```json
{
  "text": "Valeur de text",
  "title": "Valeur de title"
}
```

Le bonfonctionnement de l'API sera confirmé par un code de status **2xx** et une réponse sous la forme d'un JSON comme pour l'API précédente.