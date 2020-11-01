#Actividad 4
```
db.movies.insert([
    {
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
        "nInserted" : 15,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
```
