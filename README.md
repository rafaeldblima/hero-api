### Rodar aplicação
```bash
$ mvn clean install
$ cd infra
$ docker-compose up -d
```
### Endpoints
- GET http://localhost/api/v1/hero?name=<name>
- POST http://localhost:8080/api/v1/hero
  
  Body: 
  ```json
  {
      "name": "Super-man",
      "race": "HUMAN",
      "power_stats": {
        "strength": 100,
        "agility": 100,
        "dexterity": 100,
        "intelligence": 100,
      },
      "enabled": true,
  }
  ```
- GET http://localhost:8080/api/v1/hero/<id>
- PUT http://localhost:8080/api/v1/hero/<id>

  Body:
  ```json
  {
      "id": "6b3c84e6-bf4d-4bb0-b4a4-db1ed06b2a80",
      "name": "Super-man",
      "race": "HUMAN",
      "power_stats": {
        "id": "6b3c84e6-bf4d-4bb0-b4a4-db1ed06b2a80",
        "strength": 100,
        "agility": 100,
        "dexterity": 100,
        "intelligence": 100,
        "created_at": "2021-03-20T23:02:24.384Z",
        "updated_at": "2021-03-20T23:02:24.384Z"
      },
      "enabled": true,
      "created_at": "2021-03-20T23:02:24.384Z",
      "updated_at": "2021-03-20T23:02:24.384Z"
    }
    ```
- DELETE http://localhost:8080/api/v1/hero/<id>
- POST http://localhost:8080/api/v1/hero/compare

    Body:
    ```json
      {
      "hero1":     {
        "id": "652e9328-4998-4014-a399-1108c6d45608",
        "name": "Spider-man",
        "race": "ALIEN",
        "enabled": true,
        "powerStats": {
          "id": "d5ca5f98-f9b2-4073-b8fb-598a773c82b8",
          "strength": 100,
          "agility": 100,
          "dexterity": 100,
          "intelligence": 100,
          "createdAt": "2021-03-22T02:11:30Z",
          "updatedAt": "2021-03-22T02:11:30Z"
        },
        "createdAt": "2021-03-22T02:11:30Z",
        "updatedAt": "2021-03-22T02:11:30Z"
      },
      "hero2":{
        "id": "cc69191d-7210-4c03-b68e-a3340d6df6a6",
        "name": "Birdwoman",
        "race": "ALIEN",
        "enabled": true,
        "powerStats": {
          "id": "040326dd-64f2-450b-b6c4-70be95748e27",
          "strength": 100,
          "agility": 100,
          "dexterity": 100,
          "intelligence": 100,
          "createdAt": "2021-03-22T02:11:30Z",
          "updatedAt": "2021-03-22T02:11:30Z"
        },
        "createdAt": "2021-03-22T02:11:30Z",
        "updatedAt": "2021-03-22T02:11:30Z"
      }
    }
    ```