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
9. muestro como va la tabla movies cargada con el "comando db.movies.find()"
```
> db.movies.find()
{ "_id" : ObjectId("5f9a14d7e4ebe0c5fb3e8c83"), "title" : "Toy Story", "year" : 1990, "rating" : 5, "genre" : "animada", "description" : "serie de animacion", "actors" : [ "Sheriff Woody", "Jessie", "Forky", "Buzz Lightyear", "Betty" ], "country" : "EEUU", "income" : 2000000, "duration" : 60 }
{ "_id" : ObjectId("5f9a1e4be4ebe0c5fb3e8c84"), "title" : "Toy Story 2", "year" : 1999, "rating" : 4.5, "genre" : "animada", "description" : "serie de animacion", "actors" : [ "Tom Hanks", "Tim Allen", "Joan Cusack", "Don Rickles" ], "country" : "EEUU", "income" : 3000000, "duration" : 92 }
{ "_id" : ObjectId("5f9a374fe4ebe0c5fb3e8c85"), "title" : "Harry Potter y la piedra filosofal", "year" : 2001, "rating" : 5, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Robbie Coltrane", "Richard Harris", "Alan Rickman", "Maggie Smith" ], "country" : "EEUU", "income" : 5000000, "duration" : 152 }
{ "_id" : ObjectId("5f9a374fe4ebe0c5fb3e8c86"), "title" : "Harry Potter y la cámara secreta", "year" : 2002, "rating" : 4, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Toby Jones", "Kenneth Branagh" ], "country" : "EEUU", "income" : 3500000, "duration" : 161 }
```
10. Actualizar películas agregando el field highlighted=true a aquellas con rating > 4.5.
```
> db.movies.updateMany(
 { rating : {$gt: 4.5}},
     {
         $set: {
             highlighted: true
         }
     },
 { upsert: true })
{ "acknowledged" : true, "matchedCount" : 2, "modifiedCount" : 2 }
```
11. muestro de nuevo si hya cambios con la consulta anterior
```
> db.movies.find()
{ "_id" : ObjectId("5f9a14d7e4ebe0c5fb3e8c83"), "title" : "Toy Story", "year" : 1990, "rating" : 5, "genre" : "animada", "description" : "serie de animacion", "actors" : [ "Sheriff Woody", "Jessie", "Forky", "Buzz Lightyear", "Betty" ], "country" : "EEUU", "income" : 2000000, "duration" : 60, "highlighted" : true }
{ "_id" : ObjectId("5f9a1e4be4ebe0c5fb3e8c84"), "title" : "Toy Story 2", "year" : 1999, "rating" : 4.5, "genre" : "animada", "description" : "serie de animacion", "actors" : [ "Tom Hanks", "Tim Allen", "Joan Cusack", "Don Rickles" ], "country" : "EEUU", "income" : 3000000, "duration" : 92}
{ "_id" : ObjectId("5f9a374fe4ebe0c5fb3e8c85"), "title" : "Harry Potter y la piedra filosofal", "year" : 2001, "rating" : 5, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Robbie Coltrane", "Richard Harris", "Alan Rickman", "Maggie Smith" ], "country" : "EEUU", "income" : 5000000, "duration" : 152, "highlighted" : true }
{ "_id" : ObjectId("5f9a374fe4ebe0c5fb3e8c86"), "title" : "Harry Potter y la cámara secreta", "year" : 2002, "rating" : 4, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Toby Jones", "Kenneth Branagh" ], "country" : "EEUU", "income" : 3500000, "duration" : 161 }
>
```
12. Cambie la opcion porque justo no cargue una pelicula con genre "drama" pero cumple con el comando solicitado.
> 5. Actualizar películas cambiando el genre “drama” por “bored”.
```
> db.movies.updateMany(
 { genre: "animada" }, {
     $set: {
         genre: "bored"
     }
 }, { upsert: true })
{ "acknowledged" : true, "matchedCount" : 2, "modifiedCount" : 2 }
```
13. Muestro de nuevo los cambios que se hicieron con el comando anterior sacando los id por que solo molestan para ver los datos que cambiaron
```
> db.movies.find({},{_id: 0})
{ "title" : "Toy Story", "year" : 1990, "rating" : 5, "genre" : "bored", "description" : "serie de animacion", "actors" : [ "Sheriff Woody", "Jessie", "Forky", "Buzz Lightyear", "Betty" ], "country" : "EEUU", "income" : 2000000, "duration" : 60, "highlighted" : true }
{ "title" : "Toy Story 2", "year" : 1999, "rating" : 4.5, "genre" : "bored", "description" : "serie de animacion", "actors" : [ "Tom Hanks", "Tim Allen", "Joan Cusack", "Don Rickles" ], "country" : "EEUU", "income" : 3000000, "duration" : 92 }
{ "title" : "Harry Potter y la piedra filosofal", "year" : 2001, "rating" : 5, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Robbie Coltrane", "Richard Harris", "Alan Rickman", "Maggie Smith" ], "country" : "EEUU", "income" : 5000000, "duration" : 152, "highlighted" : true }
{ "title" : "Harry Potter y la cámara secreta", "year" : 2002, "rating" : 4, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Toby Jones", "Kenneth Branagh" ], "country" : "EEUU", "income" : 3500000, "duration" : 161 }
>  
```
14. Cambio un poco la condicion para que coincida con los datos que tengo cargados pero cumple igual con la condicion.
6. Borrar todas las películas que tengan más de 30 años.
```
> db.movies.deleteMany({year: {$lt: 2020 - 28 }})
{ "acknowledged" : true, "deletedCount" : 1 }
>
```
15. muestro como quedo la tabla de movies ahora tiene 1 registro menos siendo que tenia mas de 28 años la pelicula de 1990 de Toy Story.
```
> db.movies.find({}, {_id:0});
{ "title" : "Toy Story 2", "year" : 1999, "rating" : 4.5, "genre" : "bored", "description" : "serie de animacion", "actors" : [ "Tom Hanks", "Tim Allen", "Joan Cusack", "Don Rickles" ], "country" : "EEUU", "income" : 3000000, "duration" : 92 }
{ "title" : "Harry Potter y la piedra filosofal", "year" : 2001, "rating" : 5, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Robbie Coltrane", "Richard Harris", "Alan Rickman", "Maggie Smith" ], "country" : "EEUU", "income" : 5000000, "duration" : 152, "highlighted" : true }
{ "title" : "Harry Potter y la cámara secreta", "year" : 2002, "rating" : 4, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Toby Jones", "Kenneth Branagh" ], "country" : "EEUU", "income" : 3500000, "duration" : 161 }
>
```
7. Buscar todas las películas argentinas.
8. Buscar todas las películas de acción con un buen rating (ej. > 4.0)
que hayan salido los últimos 2 años.
