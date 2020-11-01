#Actividad 4
1. En base a la BD que ya tenia agrego 20 peliculas mas para llegar a completar la minima cantidad de 30 peliculas que pide el ejercicio.
> 1. Utilizar la misma base de datos de películas e insertar varias películas (al menos 30) con distinto contenido.
```
db.movies.insert([
    {
        title: "Animales fantásticos: los crímenes de Grindelwald",
        year: 2018,
        rating: 2.0,
        genre: "Gánsteres",
        description: "Grindewald ha logrado escapar y pretende encabezar una revuelta de los magos purasangre para dominar el mundo. Dumbledore, acompañado por su antiguo estudiante Scamander, tratará de evitar que quien fuera su gran amigo cumpla su siniestro propósito.",
        actors: ["Eddie Redmayne", "Johnny Depp", "Jude Law"],
        country: "Hollywood",
        income: 654900000,
        duration: 209
    }, {
        title: "Angry Birds 2: la película",
        year: 2019,
        rating: 3.8,
        genre: "Animación",
        description: "Los amigos emplumados deben unirse a los cerdos verdes cuando las agresivas aves planean destruirlos a ambos.",
        actors: ["Jason Sudeikis", "Josh Gad", "Peter Dinklage"],
        country: "Hollywood",
        income: 65000000,
        duration: 97
    }, {
        title: "¿Quién @#*%$ es papá?",
        year: 2017,
        rating: 4.4,
        genre: "Comedia",
        description: "Dos hermanos mellizos crecieron pensando que su padre había muerto, pero descubren que está vivo y emprenden un viaje para encontrarlo. Pese al entusiasmo que ponen en localizarlo, no será sencillo, ya que su madre se acostó con muchos hombres poderosos y famosos en la década de 1970.",
        actors: ["Ed Helms", "Owen Wilson", "Glenn Close"],
        country: "EEUU",
        income: 25600000,
        duration: 125
    }, {
        title: "Batman: la máscara del fantasma",
        year: 1993,
        rating: 3.5,
        genre: "Animación",
        description: "La exnovia de Bruce Wayne es implicada en la misteriosa y letal campaña de un villano contra criminales.",
        actors: ["Dana Delany", "Mark Hamill", "Kevin Conroy"],
        country: "EEUU",
        income: 1000000,
        duration: 77
    }, {
        title: "Un jefe en pañales",
        year: 2017,
        rating: 4.3,
        genre: "",
        description: "Tim, de 7 años, tiene celos de su hermano, un bebé que viste traje y corbata, hasta que descubre que el bebé puede hablar. Los hermanos protagonizan una misión secreta contra un villano que pretende acabar con el amor de los niños por las mascotas.",
        actors: ["David Soren", "Tobey <agiore", "James McGranth"],
        country: "Argentina",
        income: 2000000,
        duration: 97
    }, {
        title: "Furia de Dragones",
        year: 2007,
        rating: 2.5,
        genre: "Accion",
        description: "Ethan Kendrick (Jason Behr) descubre que unas criaturas antiguas llamadas Imoogi han regresado a la Tierra, y la única forma de detenerlas es con la ayuda de Sarah (Amanda Brooks). Basada en una leyenda coreana.",
        actors: ["Jason Behr", "Amanda Brooks", "Robert Forster", "Chris Mulkey", "Elizabeth Pena"],
        country: "EEUU",
        income: 70000000,
        duration: 107
    }, {
        title: "Holidate",
        year: 2020,
        rating: 3.6,
        genre: "Navidad",
        description: "Holidate es una comedia romántica, dirigida por John Whitesell, con guion de Tiffany Paulsen. Está protagonizada por Emma Roberts, Luke Bracey, Jake Manley, Jessica Capshaw, Andrew Bachelor, Frances Fisher, Manish Dayal y Kristin Chenoweth. La película se estrenó en Netflix el 28 de octubre de 2020.",
        actors: ["Emma Roberts", "Luke Bracey", "Jake Manley", "Jessica Capshaw", "Andrew Bachelor"],
        country: "EEUU",
        income: 1000000,
        duration: 103
    }, {
        title: "¿Qué le pasó a Lunes?",
        year: 2017,
        rating: 4.5,
        genre: "Accion",
        description: "En un futuro en el que está prohibido tener más de un hijo, seis hermanas que fingen ser la misma para pasar inadvertidas tratan de escapar del control opresivo del Gobierno mientras buscan a la séptima hermana, que ha desaparecido.",
        actors: ["Noomi Rapace", "Willem Dafoe", "Glenn Close", "Marwan Kenzari"],
        country: "EEUU",
        income: 9115000,
        duration: 124
    }, {
        title: "Los cazafantasmas II",
        year: 1989,
        rating: 4.4,
        genre: "Fantasia",
        description: "Los cazafantasmas persiguen a una nueva ola de fantasmas, conjurados por el renovado espíritu de un viejo brujo cárpato.",
        actors: ["Bill Murray", "Dan Aykroyd", "Sigourney Weaver", "Peter MacNicol"],
        country: "EEUU",
        income: 215394738,
        duration: 110
    }, {
        title: "Mi villano favorito 3",
        year: 2017,
        rating: 4.3,
        genre: "Animacion",
        description: "Gru trabaja ahora capturando villanos pero fracasa y es despedido. Poco después descubre que tiene un hermano, Dru, y juntos se enfrentan a un villano que pretende robar un diamante y destruir Hollywood. Sin embargo, Dru quiere convencer a Gru para que además retome su carrera como villano, ya que su padre lo fue también.",
        actors: ["Steve Carell", "Kristen Wiig", "Trey Parker", "Miranda Cosgrove"],
        country: "EEUU",
        income: 80000000,
        duration: 96
    }, {
        title: "Safe House",
        year: 2012,
        rating: 3.8,
        genre: "Accion",
        description: "Después de apenas escapar del ataque de unos mercenarios, un agente novato y un policía renegado deben unir fuerzas y descubrir quién los quiere muertos.",
        actors: ["Denzel Washington", "Ryan Reynolds", "Vera Farmiga", "Brendan Gleeson", "Sam Shepard"],
        country: "EEUU",
        income: 85000000,
        duration: 115
    }, {
        title: "Kicking & Screaming",
        year: 2005,
        rating: 4.2,
        genre: "Comedia",
        description: "Un vendedor de vitaminas y su competitivo padre se enfrentan como entrenadores de equipos de fútbol infantil.",
        actors: ["Will Ferrell", "Robert Duvall", "Mike Ditka", "Kate Walsh", "Musetta Vander"],
        country: "EEUU",
        income: 91000000,
        duration: 95
    }, {
        title: "El hombre que conocía el infinito",
        year: 2015,
        rating: 4.8,
        genre: "Drama",
        description: "La historia del profesor de matemáticas de origen indio Srinivasa Ramanujan, que rompió estereotipos y barreras socioculturales cuando en 1913 consiguió ingresar en la Universidad de Cambridge para colaborar con el prestigioso académico G. H. Hardy. Esto lo consiguió pese a la tara que en la época conllevaba su procedencia.",
        actors: ["Dev Patel", "Jeremy Irons", "Devika Bhise", "Toby Jones", "Stephen Fry"],
        country: "EEUU",
        income: 75000000,
        duration: 114
    }, {
        title: "Cuestión de tiempo",
        year: 2013,
        rating: 4.8,
        genre: "Romance",
        description: "Cuando Tim Lake cumple 21 años, su padre le dice un secreto: los hombres de su familia pueden viajar por el tiempo. A pesar de que él no puede cambiar la historia, Tim decide mejorar su vida buscando una novia. Él conoce a Mary, se enamora y finalmente se gana su corazón con los viajes en el tiempo …",
        actors: ["Domhnall Gleeson", "Rachel McAdams", "Bill Nighy", "Margot Robbie", "Lindsay Duncan"],
        country: "EEUU",
        income: 100000000,
        duration: 124
    }, {
        title: "Robots",
        year: 2005,
        rating: 3.3,
        genre: "Animacion",
        description: "Un robot encabeza una revolución en contra de un directivo corporativo que desea destruir a los modelos antiguos.",
        actors: ["Ewan McGregor", "Halle Berry", "Greg Kinnear", "Mel Brooks", "Drew Carey"],
        country: "EEUU",
        income: 75000000,
        duration: 91
    }, {
        title: "Cómo entrenar a tu dragón 3",
        year: 2019,
        rating: 4.5,
        genre: "Animacion",
        description: "Hipo descubre que Chimuelo no es el único Furia Nocturna y debe buscar el Mundo Oculto, una utopía secreta para descubrir finalmente sus destinos como dragón y jinete.",
        actors: ["Jay Baruchel", "America Ferrera", "F. Murray Abraham", "Cate Blanchett"],
        country: "EEUU",
        income: 129000000,
        duration: 105
    }, {
        title: "Un juego vs. el destino",
        year: 2006,
        rating: 4.2,
        genre: "Drama",
        description: "En un centro de detención juvenil, un consejero decide transformar a los prisioneros a su cargo en un equipo de fútbol americano para enseñarles sobre el autoestima y la responsabilidad social, pero se enfrenta a la oposición de los entrenadores de las preparatorias que no quieren que sus jugadores se enfrenten a los criminales en el campo de juego.",
        actors: ["Dwayne The Rock Johnson", "Xzibit", "L. Scott Caldwell", "Kevin Dunn"],
        country: "EEUU",
        income: 74000000,
        duration: 126
    }, {
        title: "Olé: El viaje de Ferdinand",
        year: 2017,
        rating: 4.7,
        genre: "Animacion",
        description: "En España, un toro grande y amable llamado Ferdinand, a quien los demás toros ridiculizan porque no le gusta pelear, escapa un día y acaba siendo adoptado por un cultivador de flores, su hija, Nina, de quien se hace muy amigo, y su perro, Paco. Sin embargo, lo atrapan de nuevo, pero Ferdinand intent…",
        actors: ["Bobby Cannavale", "Karla Martínez", "David Tennant", "Gabriel Iglesias", "Boris Kodjoe"],
        country: "EEUU",
        income: 111000000,
        duration: 108
    }, {
        title: "El Hobbit: la batalla de los cinco ejércitos",
        year: 2014,
        rating: 4.6,
        genre: "Aventuras",
        description: "Mientras Smaug lanza su ira ardiente contra los ciudadanos de la Ciudad del Lago, Sauron envía legiones de orcos a atacar la Montaña Solitaria. La Tierra está en peligro cuando hombres, enanos y elfos deben decidir si se unen o son destruidos.",
        actors: ["Ian Mckellen", "Martin Freeman", "Richard Armitage", "Evangeline Lilly"],
        country: "Nueva Zelanda",
        income: 250000000,
        duration: 164
    }, {
        title: "Buenos muchachos",
        year: 1990,
        rating: 4.8,
        genre: "Drama",
        description: "Henry, un niño de trece años de Brooklyn, vive fascinado con el mundo de los gánsters. Su sueño se hace realidad cuando entra en la familia Pauline.",
        actors: ["Robert De Niro", "Joe Pesci", "Ray Liotta", "Lorraine Bracco", "Paul Sorvino"],
        country: "EEUU",
        income: 25000000,
        duration: 148
    }
])
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 20,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```
> 2. Crear índice en field rating y luego hacer búsquedas usando este campo.

```
> db.movies.createIndex({ rating: 1})
{
        "createdCollectionAutomatically" : false,
        "numIndexesBefore" : 1,
        "numIndexesAfter" : 2,
        "ok" : 1
}
```
 - Un ejemplo de busqueda con respecto al campo rating:
```
> db.movies.find({rating: {$gte: 1} }, {_id:0, rating: 1})
{ "rating" : 2 }
{ "rating" : 2.5 }
{ "rating" : 3 }
{ "rating" : 3.3 }
{ "rating" : 3.5 }
{ "rating" : 3.5 }
{ "rating" : 3.6 }
{ "rating" : 3.8 }
{ "rating" : 3.8 }
{ "rating" : 4 }
{ "rating" : 4 }
{ "rating" : 4.2 }
{ "rating" : 4.2 }
{ "rating" : 4.3 }
{ "rating" : 4.3 }
{ "rating" : 4.4 }
{ "rating" : 4.4 }
{ "rating" : 4.5 }
{ "rating" : 4.5 }
{ "rating" : 4.5 }
Type "it" for more
```
> 3. Crear índice en title y description, y después hacer búsquedas de texto en estos campos.
```
> db.movies.createIndex({title: "text", description: "text"})
{
        "createdCollectionAutomatically" : false,
        "numIndexesBefore" : 1,
        "numIndexesAfter" : 3,
        "ok" : 1
}
>
```
 - Un ejemplo de busqueda con respecto al campo description:
 ```
 > db.movies.find({ $text: { $search: "juvenil" } })
{ "_id" : ObjectId("5f9f1eb319d04033a0647021"), "title" : "Un juego vs. el destino", "year" : 2006, "rating" : 4.2, "genre" : "Drama", "description" : "En un centro de detención juvenil, un consejero decide transformar a los prisioneros a su cargo en un equipo de fútbol americano para enseñarles sobre el autoestima y la responsabilidad social, pero se enfrenta a la oposición de los entrenadores de las preparatorias que no quieren que sus jugadores se enfrenten a los criminales en el campo de juego.", "actors" : [ "Dwayne The Rock Johnson", "Xzibit", "L. Scott Caldwell", "Kevin Dunn" ], "country" : "EEUU", "income" : 74000000, "duration" : 126 }
>
 ```
 - otro ejemplo de busqueda con respecto al campo title:
 ```
 > db.movies.find({ $text: { $search: "Harry Potter" } })
{ "_id" : ObjectId("5f9b1d9baceaef14fe88c645"), "title" : "Harry Potter y la cámara secreta", "year" : 2002, "rating" : 4, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Toby Jones", "Kenneth Branagh" ], "country" : "EEUU", "income" : 3500000, "duration" : 161 }
{ "_id" : ObjectId("5f9b1d9baceaef14fe88c644"), "title" : "Harry Potter y la piedra filosofal", "year" : 2001, "rating" : 5, "genre" : "Fantasía", "description" : "serie de Fantasía", "actors" : [ "Daniel Radcliffe", "Rupert Grint", "Emma Watson", "Robbie Coltrane", "Richard Harris", "Alan Rickman", "Maggie Smith" ], "country" : "EEUU", "income" : 5000000, "duration" : 152, "highlighted" : true }
>
 ```
