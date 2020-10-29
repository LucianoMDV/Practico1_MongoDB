# Actividad 2

1. Inicio cmd en windows para usar la consola
2. escribo el comando "mongo".
> mongo
```
MongoDB shell version v4.4.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("6c62e653-06d1-4eb7-a5cd-05b43e8b18d6") }
MongoDB server version: 4.4.1
```
3. me fijo que BD hay actualmente con el comando "show dbs"
> show dbs
```
admin       0.000GB
config      0.000GB
futbolfifa  0.000GB
local       0.000GB
```
4. creo una nueva BD con el comando "use Netflix"
> use Netflix
```
> switched to db Netflix
```
5. genero la tabla con el comando "db.createCollection("movies")"
> db.createCollection("movies")
```
{ "ok" : 1 }  
```
6. me fijo si esta la tabla con el comando "show collections"
> show collections
```
movies
```
6. cargo el primer registro con el comando db.movies.insert()  
```
db.movies.insert({  
             title : "Toy Story",  
             year : 1990,  
             rating : 5.0,  
             genre : "animada",  
             description: "serie de animacion",  
             actors : [  
                 "Sheriff Woody",  
                 "Jessie", "Forky",  
                 "Buzz Lightyear",  
                 "Betty"  
             ],  
             country : "EEUU",  
             income : 2000000,  
             duration : 60  
 })
WriteResult({ "nInserted" : 1 })
```

7. cargo el siguiente registro con el comando db.movies.insertOne()

```
> db.movies.insertOne(
     {
         title : "Toy Story 2",
         year : 1999,
         rating : 4.5,
         genre : "animada",
         description: "serie de animacion",
         actors : [
             "Tom Hanks",
             "Tim Allen",
             "Joan Cusack",
             "Don Rickles"
         ],
         country : "EEUU",
         income : 3000000,
         duration : 92
     }
 )
{
        "acknowledged" : true,
        "insertedId" : ObjectId("5f9a1e4be4ebe0c5fb3e8c84")
}
```
8.
```
> db.movies.insertMany(
     [
         {
             title : "Harry Potter y la piedra filosofal",
             year : 2001,
             rating : 5.0,
             genre : "Fantasía",
             description: "serie de Fantasía",
             actors : [
                 "Daniel Radcliffe",
                 "Rupert Grint",
                 "Emma Watson",
                 "Robbie Coltrane",
                 "Richard Harris",
                 "Alan Rickman",
                 "Maggie Smith"
             ],
             country : "EEUU",
             income : 5000000,
             duration : 152
         },
         {
             title : "Harry Potter y la cámara secreta",
             year : 2002,
             rating : 4.0,
             genre : "Fantasía",
             description: "serie de Fantasía",
             actors : [
                 "Daniel Radcliffe",
                 "Rupert Grint",
                 "Emma Watson",
                 "Toby Jones",
                 "Kenneth Branagh"
             ],
             country : "EEUU",
             income : 3500000,
             duration : 161
         },
     ]
 )
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("5f9a374fe4ebe0c5fb3e8c85"),
                ObjectId("5f9a374fe4ebe0c5fb3e8c86")
        ]
}
```
