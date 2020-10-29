# Actividad 1
1. Veo que estoy conectado y que BD hay.
> show dbs  
admin   0.000GB  
config  0.000GB  
local   0.000GB  

2. Crear una nueva base de datos llamada futbolfifa.
> use futbolfifa  
switched to db futbolfifa

3. Crear una nueva collection llamada players.  
> db.createCollection("players")  
{ "ok" : 1 }

4. Insertar 5 documentos en la collection players con datos básicos (nombre, apellido, posición, fecha de nacimiento, etc).  
> db.players.insert(  
                    { "nombre" : "Luciano",  
                      "apellido" : "D'Agata",  
                      "posición" : "delantero",  
                      "fechaNacimiento" : "08/10/1991"  
                      })  
WriteResult({ "nInserted" : 1 })  

5. me fijo si lo cargo bien  
> db.players.find()  
{ "_id" : ObjectId("5f7f5d28a01cfdca9d5664bb"),  
  "nombre" : "Luciano",  
  "apellido" : "D'Agata",  
  "posición" : "delantero",  
  "fechaNacimiento" : "08/10/1991" }  
  
6. busque como insertar mas de uno registro a la vez  
> db.players.insertMany(  
[  
    {  
        "nombre" : "Manuel",  
        "apellido" : "Rivas" ,  
        "posición" : "defensor",  
        "fechaNacimiento" : "28/06/1999"  
    },  
    {  
        "nombre" : "Roberto",  
        "apellido" : "Garcia" ,  
        "posición" : "defensor",  
        "fechaNacimiento" : "11/01/1965"  
    },  
    {  
        "nombre" : "Sebastian",  
        "apellido" : "Saavedra" ,  
        "posición" : "medioCampo",  
        "fechaNacimiento" : "25/04/1985"  
    },  
    {  
        "nombre" : "Manuel",  
        "apellido" : "Garcia",  
        "posición" : "delantero",  
        "fechaNacimiento" : "07/08/1998"  
    }  
]  
{  
  "acknowledged" : true,  
  "insertedIds" : [  
          ObjectId("5f7f5de0a01cfdca9d5664bc"),  
          ObjectId("5f7f5de0a01cfdca9d5664bd"),  
          ObjectId("5f7f5de0a01cfdca9d5664be"),  
          ObjectId("5f7f5de0a01cfdca9d5664bf")  
  ]  
}  
7. Listar todos los documentos de la collection players.  
> db.players.find()  
{ "_id" : ObjectId("5f7f5d28a01cfdca9d5664bb"), "nombre" : "Luciano", "apellido" : "D'Agata", "posición" : "delantero", "fechaNacimiento" : "08/10/1991" }  
{ "_id" : ObjectId("5f7f5de0a01cfdca9d5664bc"), "nombre" : "Manuel", "apellido" : "Rivas", "posición" : "defensor", "fechaNacimiento" : "28/06/1999" }  
{ "_id" : ObjectId("5f7f5de0a01cfdca9d5664bd"), "nombre" : "Roberto", "apellido" : "Garcia", "posición" : "defensor", "fechaNacimiento" : "11/01/1965" }  
{ "_id" : ObjectId("5f7f5de0a01cfdca9d5664be"), "nombre" : "Sebastian", "apellido" : "Saavedra", "posición" : "medioCampo", "fechaNacimiento" : "25/04/1985" }  
{ "_id" : ObjectId("5f7f5de0a01cfdca9d5664bf"), "nombre" : "Manuel", "apellido" : "Garcia", "posición" : "delantero", "fechaNacimiento" : "07/08/1998" }  
