# Actividad 3
1. Utilizar la misma base de datos de películas e insertar varias películas con distinto contenido.
2. Listar todas las películas del año 2018.
```
> db.movies.find({year: 2018})
```
3. Listar las 10 primeras películas de Hollywood.
> db.movies.find({country: "Hollywood"}).limit(10)

 cambie la consulta para mostrar un ejemplo pero es lo mismo pero con menos cantidad de resultados y  no proyecte los id que son innecesarios para mostrar este ejemplo.
```
> db.movies.find({country: "Hollywood"}, {_id:0}).limit(5)
{ "title" : "El irlandés", "year" : 2019, "rating" : 4, "genre" : "Gánsteres", "description" : "serie de Gánsteres", "actors" : [ "Robert De Niro", "Al Pacino", "Joe Pesci" ], "country" : "Hollywood", "income" : 8000000, "duration" : 209 }
{ "title" : "The Trial of the Chicago 7", "year" : 2020, "rating" : 4.5, "genre" : "Soundtrack", "description" : "serie de Soundtrack", "actors" : [ "Yahya Abdul-Mateen II", "Sacha Baron Cohen", "Daniel Flaherty", "Joseph Gordon-Levitt", "Michael Keaton" ], "country" : "Hollywood", "income" : 35000000, "duration" : 130 }
{ "title" : "Focus", "year" : 2015, "rating" : 4.5, "genre" : "Comedia dramática", "description" : "serie de Comedia dramática", "actors" : [ "Will Smith", "Margot Robbie" ], "country" : "Hollywood", "income" : 50100000, "duration" : 104 }
{ "title" : "American Sniper", "year" : 2014, "rating" : 5, "genre" : "Drama", "description" : "serie de Drama", "actors" : [ "Bradley Cooper", "Sienna Miller" ], "country" : "Hollywood", "income" : 58800000, "duration" : 132 }
{ "title" : "The Lego Movie", "year" : 2014, "rating" : 3, "genre" : "Animación", "description" : "serie de Animación", "actors" : [ "Chris Pratt", "Elizabeth Banks", "Will Ferrell", "Will Arnett" ], "country" : "Hollywood", "income" : 60000000, "duration" : 100 }
>
```
 - muestro como esta cargada la tambla movies para corroborrar que si funciona las siguientes dos consultas
```
> db.movies.find({},{income: 1, _id:0}).sort({income: -1})
{ "income" : 160000000 }
{ "income" : 60000000 }
{ "income" : 58800000 }
{ "income" : 50100000 }
{ "income" : 35000000 }
{ "income" : 8000000 }
{ "income" : 6000000 }
{ "income" : 5000000 }
{ "income" : 3500000 }
{ "income" : 3000000 }
>
```
4. Listar las 5 películas más taquilleras.
```
> db.movies.find({},{income: 1, _id:0}).sort({income: -1}).limit(5)
{ "income" : 160000000 }
{ "income" : 60000000 }
{ "income" : 58800000 }
{ "income" : 50100000 }
{ "income" : 35000000 }
```
5. Listar el 2do conjunto de 5 películas más taquilleras.
```
> db.movies.find({},{income: 1, _id:0}).sort({income: -1}).skip(5).limit(5)
{ "income" : 8000000 }
{ "income" : 6000000 }
{ "income" : 5000000 }
{ "income" : 3500000 }
{ "income" : 3000000 }
>
```
6. Repetir query 3 y 4 pero retornando sólo el título y genre.
7. Mostrar los distintos países que existen en la base de datos.

