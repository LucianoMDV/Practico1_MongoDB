# Actividad 2

1. Inicio cmd en windows para usar la consola
2. escribo el comando mongo.
> MongoDB shell version v4.4.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("6c62e653-06d1-4eb7-a5cd-05b43e8b18d6") }
MongoDB server version: 4.4.1
3. me fijo que BD hay actualmente con el comando "show dbs"
> admin       0.000GB  
  config      0.000GB  
  futbolfifa  0.000GB  
  local       0.000GB  
4. creo una nueva BD con el comando "use Netflix"
> switched to db Netflix
5. genero la tabla con el comando "db.createCollection("movies")"
> { "ok" : 1 }  
6. me fijo si esta la tabla con el comando "show collections"
> show collections  
movies  
6. cargo el primer registros con el comando db.movies.insert()  
> db.movies.insert({  
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
7.

