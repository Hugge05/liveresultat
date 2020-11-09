# Liveresultat

## API
All API requests should be made via HTTPS GET reqests, content returned is returned as JSON.
While there are no limit on how much or how often you can request, try to go easy on the servers if possible.

### ``getallcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions``

Returns a list of all events and their: ``id``, ``name``, ``organizerId``, ``dateTime`` (when the event will be hosted) and ``createdTime`` (when the event was created on Liveresultat), ``icon``, ``eventorId``, ``organizerIcon``,``hasData``.
The following may be null: ``icon``, ``organizerIcon``, ``eventorId``.

### ``getcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions&page=0&results=15``
Like ``getallcompetitions`` but starts from the given number, defaults to 0.

### ``getuserinfo``
``https://pallhed.se/api.php?method=getuserinfo&id=1``
Returns the users details: ``id``, ``username``, ``rank`` (superadmin = Administrator, admin = Organizer), ``icon``.

### ``getcompetitioninfo``
``https://pallhed.se/api.php?method=getcompetitioninfo&id=14``

Returns the competitions details, runners and organisations.
Example:
```json
{
   "competition":{
      "name":"Exempelt\u00e4vling",
      "organizerId":"8",
      "dateTime":"2020-11-25",
      "createdTime":"2020-10-24 19:36:57",
      "icon":null,
      "eventorId":"33192",
      "organizerIcon":"https:\/\/pallhed.se\/img\/users\/gifPfp.png"
   },
   "runners":[
      {
         "id":"193584",
         "name":"Adelina Bergmann",
         "orgId":"509",
         "stat":"1",
         "st":"670240",
         "rt":"13640",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"193583",
         "name":"Jesca Bergman",
         "orgId":"509",
         "stat":"5",
         "st":"672630",
         "rt":"14070",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"193582",
         "name":"Christina Sj\u00f6str\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"657660",
         "rt":"8910",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"193581",
         "name":"Fardhe Lindgren",
         "orgId":"509",
         "stat":"1",
         "st":"672040",
         "rt":"12100",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"193580",
         "name":"Zakarias Norstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"648680",
         "rt":"13170",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"192059",
         "name":"Tommy Sundstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"559230",
         "rt":"11860",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"192058",
         "name":"Yvonne \u00d6stberg",
         "orgId":"509",
         "stat":"1",
         "st":"556840",
         "rt":"9900",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"190003",
         "name":"Lykke Ohlson",
         "orgId":"509",
         "stat":"1",
         "st":"611440",
         "rt":"11580",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"187990",
         "name":"Alf Lund",
         "orgId":"509",
         "stat":"1",
         "st":"547250",
         "rt":"17310",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"187989",
         "name":"Jens Ohly",
         "orgId":"509",
         "stat":"1",
         "st":"544260",
         "rt":"16040",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"181958",
         "name":"Torsten Cederblom",
         "orgId":"509",
         "stat":"1",
         "st":"609640",
         "rt":"12480",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"172967",
         "name":"Hebbla J\u00e4rnefelt",
         "orgId":"509",
         "stat":"1",
         "st":"592230",
         "rt":"14270",
         "tstat":"1",
         "it":"0",
         "classId":"80"
      },
      {
         "id":"170833",
         "name":"Nicole Backstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"591640",
         "rt":"13140",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"170551",
         "name":"Georg Petersson",
         "orgId":"509",
         "stat":"1",
         "st":"652230",
         "rt":"5360",
         "tstat":"1",
         "it":"0",
         "classId":"90"
      },
      {
         "id":"170549",
         "name":"Vollrat Lagerkvist",
         "orgId":"509",
         "stat":"1",
         "st":"658830",
         "rt":"13970",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"94698",
         "name":"Edith Sv\u00e4rd",
         "orgId":"509",
         "stat":"1",
         "st":"649230",
         "rt":"15340",
         "tstat":"1",
         "it":"0",
         "classId":"60"
      },
      {
         "id":"94699",
         "name":"Tone Ekbom",
         "orgId":"509",
         "stat":"1",
         "st":"657050",
         "rt":"8410",
         "tstat":"1",
         "it":"0",
         "classId":"100"
      },
      {
         "id":"98364",
         "name":"Anton \u00c5gren",
         "orgId":"509",
         "stat":"1",
         "st":"525650",
         "rt":"18080",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"100131",
         "name":"Edit Dalin",
         "orgId":"509",
         "stat":"1",
         "st":"610800",
         "rt":"16530",
         "tstat":"1",
         "it":"0",
         "classId":"60"
      },
      {
         "id":"101838",
         "name":"Joakim Widforss",
         "orgId":"509",
         "stat":"1",
         "st":"523230",
         "rt":"11690",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"102209",
         "name":"Majken Hjortsberg",
         "orgId":"509",
         "stat":"3",
         "st":"589230",
         "rt":"11870",
         "tstat":"1",
         "it":"0",
         "classId":"70"
      },
      {
         "id":"103158",
         "name":"Gyrid Lindblad",
         "orgId":"509",
         "stat":"1",
         "st":"661840",
         "rt":"15160",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"105101",
         "name":"Josefina Ekbom",
         "orgId":"509",
         "stat":"1",
         "st":"656430",
         "rt":"17670",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"106382",
         "name":"Sture Fagerudd",
         "orgId":"509",
         "stat":"1",
         "st":"568820",
         "rt":"10500",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"108851",
         "name":"Richard Malmsten",
         "orgId":"509",
         "stat":"20",
         "st":"-1",
         "rt":"0",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"110625",
         "name":"Elvin Crusenstolpe",
         "orgId":"509",
         "stat":"1",
         "st":"613230",
         "rt":"13840",
         "tstat":"1",
         "it":"0",
         "classId":"60"
      },
      {
         "id":"117826",
         "name":"Marcus Ohlson",
         "orgId":"509",
         "stat":"1",
         "st":"609040",
         "rt":"21300",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"117925",
         "name":"Alina Bjorkman",
         "orgId":"509",
         "stat":"1",
         "st":"666960",
         "rt":"13530",
         "tstat":"1",
         "it":"0",
         "classId":"120"
      },
      {
         "id":"117926",
         "name":"B\u00f6rje Lindblom",
         "orgId":"509",
         "stat":"1",
         "st":"653050",
         "rt":"11070",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"118418",
         "name":"Arendt Carlsson",
         "orgId":"509",
         "stat":"1",
         "st":"547840",
         "rt":"16650",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"119543",
         "name":"G\u00e4rdar Cederblom",
         "orgId":"509",
         "stat":"1",
         "st":"544880",
         "rt":"14440",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"120947",
         "name":"Ludvig Laxman",
         "orgId":"509",
         "stat":"1",
         "st":"614430",
         "rt":"9160",
         "tstat":"1",
         "it":"0",
         "classId":"70"
      },
      {
         "id":"121016",
         "name":"Ellen Granqvist",
         "orgId":"509",
         "stat":"5",
         "st":"543660",
         "rt":"11430",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"121062",
         "name":"Victoria Lagerfeld",
         "orgId":"509",
         "stat":"1",
         "st":"543040",
         "rt":"17120",
         "tstat":"1",
         "it":"0",
         "classId":"100"
      },
      {
         "id":"121417",
         "name":"Ivar Hedman",
         "orgId":"509",
         "stat":"1",
         "st":"607830",
         "rt":"6870",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"121750",
         "name":"Elton Lundstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"546030",
         "rt":"12280",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"122230",
         "name":"Alvin Edlund",
         "orgId":"509",
         "stat":"1",
         "st":"604310",
         "rt":"7460",
         "tstat":"1",
         "it":"0",
         "classId":"100"
      },
      {
         "id":"128972",
         "name":"Anja Ostr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"606040",
         "rt":"9610",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"129258",
         "name":"Filip Tegn\u00e9r",
         "orgId":"509",
         "stat":"1",
         "st":"593420",
         "rt":"18820",
         "tstat":"1",
         "it":"0",
         "classId":"60"
      },
      {
         "id":"129259",
         "name":"Ingvar Bergstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"586220",
         "rt":"11380",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"129619",
         "name":"Hannes Skoog",
         "orgId":"509",
         "stat":"1",
         "st":"546620",
         "rt":"11830",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"136583",
         "name":"Mats Sj\u00f6str\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"585030",
         "rt":"13180",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"144447",
         "name":"Britta Friberg",
         "orgId":"509",
         "stat":"5",
         "st":"651030",
         "rt":"13210",
         "tstat":"1",
         "it":"0",
         "classId":"120"
      },
      {
         "id":"160221",
         "name":"Maj-Britt Palmstruch",
         "orgId":"509",
         "stat":"3",
         "st":"654650",
         "rt":"8800",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"161704",
         "name":"Alice Fornberg",
         "orgId":"509",
         "stat":"20",
         "st":"-1",
         "rt":"0",
         "tstat":"1",
         "it":"0",
         "classId":"100"
      },
      {
         "id":"94692",
         "name":"Henry Hagerstr\u00f6m",
         "orgId":"509",
         "stat":"3",
         "st":"651630",
         "rt":"16880",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"88627",
         "name":"Emelie Adelsk\u00f6ld",
         "orgId":"509",
         "stat":"1",
         "st":"657630",
         "rt":"14570",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      },
      {
         "id":"87505",
         "name":"Edvard Henriksson",
         "orgId":"509",
         "stat":"1",
         "st":"667810",
         "rt":"10910",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"87500",
         "name":"Johannes Bystr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"661200",
         "rt":"5760",
         "tstat":"1",
         "it":"0",
         "classId":"90"
      },
      {
         "id":"87499",
         "name":"Christin Liljestr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"664840",
         "rt":"6360",
         "tstat":"1",
         "it":"0",
         "classId":"110"
      },
      {
         "id":"74525",
         "name":"Julie Holmstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"588020",
         "rt":"10150",
         "tstat":"1",
         "it":"0",
         "classId":"80"
      },
      {
         "id":"67968",
         "name":"Emil Skarsg\u00e5rd",
         "orgId":"509",
         "stat":"1",
         "st":"612620",
         "rt":"9890",
         "tstat":"1",
         "it":"0",
         "classId":"80"
      },
      {
         "id":"73385",
         "name":"Melina Nordlund",
         "orgId":"509",
         "stat":"1",
         "st":"666040",
         "rt":"20120",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"61541",
         "name":"Nichole Lagerl\u00f6f",
         "orgId":"509",
         "stat":"1",
         "st":"652830",
         "rt":"15380",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      },
      {
         "id":"59973",
         "name":"Isabella Paulsson",
         "orgId":"509",
         "stat":"1",
         "st":"546020",
         "rt":"10860",
         "tstat":"1",
         "it":"0",
         "classId":"80"
      },
      {
         "id":"54917",
         "name":"Alexander Wallin",
         "orgId":"509",
         "stat":"20",
         "st":"-1",
         "rt":"0",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"56587",
         "name":"Jan Malmstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"654020",
         "rt":"11010",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"54916",
         "name":"Camilla Gylling",
         "orgId":"509",
         "stat":"1",
         "st":"588620",
         "rt":"46400",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"54788",
         "name":"\u00d6rjan Norberg",
         "orgId":"509",
         "stat":"1",
         "st":"589820",
         "rt":"9720",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"49842",
         "name":"Britt-Louise Paulsson",
         "orgId":"509",
         "stat":"20",
         "st":"-1",
         "rt":"0",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"49615",
         "name":"Ebbe Malmsten",
         "orgId":"509",
         "stat":"1",
         "st":"655230",
         "rt":"13450",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      },
      {
         "id":"49510",
         "name":"Hildr S\u00f6dergren",
         "orgId":"509",
         "stat":"1",
         "st":"567030",
         "rt":"12760",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"49509",
         "name":"William Heidenstam",
         "orgId":"509",
         "stat":"1",
         "st":"565220",
         "rt":"15020",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"41977",
         "name":"Vidar K\u00e4llstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"591630",
         "rt":"14360",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"42759",
         "name":"Zacharias Hagstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"585630",
         "rt":"13510",
         "tstat":"1",
         "it":"0",
         "classId":"70"
      },
      {
         "id":"48481",
         "name":"Frida Stenbock",
         "orgId":"509",
         "stat":"1",
         "st":"648030",
         "rt":"16670",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"38898",
         "name":"Noah Schauman",
         "orgId":"509",
         "stat":"1",
         "st":"671420",
         "rt":"11530",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      },
      {
         "id":"38445",
         "name":"Holvaster Degermark",
         "orgId":"509",
         "stat":"1",
         "st":"526830",
         "rt":"12770",
         "tstat":"1",
         "it":"0",
         "classId":"30"
      },
      {
         "id":"30846",
         "name":"Segol Augustsson",
         "orgId":"509",
         "stat":"1",
         "st":"589220",
         "rt":"12420",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"31850",
         "name":"Frank Heidenstam",
         "orgId":"509",
         "stat":"1",
         "st":"608420",
         "rt":"10130",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"32510",
         "name":"Herse Lagerkvist",
         "orgId":"509",
         "stat":"5",
         "st":"665430",
         "rt":"9110",
         "tstat":"1",
         "it":"0",
         "classId":"120"
      },
      {
         "id":"34694",
         "name":"Charlotta Posse",
         "orgId":"509",
         "stat":"1",
         "st":"586820",
         "rt":"9610",
         "tstat":"1",
         "it":"0",
         "classId":"70"
      },
      {
         "id":"35969",
         "name":"Katarina Lindholm",
         "orgId":"509",
         "stat":"1",
         "st":"678030",
         "rt":"12410",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"38443",
         "name":"Ulla Bloch",
         "orgId":"509",
         "stat":"1",
         "st":"522030",
         "rt":"15660",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"38444",
         "name":"Anna-Lena Bruun",
         "orgId":"509",
         "stat":"20",
         "st":"-1",
         "rt":"0",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"26446",
         "name":"Zacharias Dalin",
         "orgId":"509",
         "stat":"1",
         "st":"658230",
         "rt":"15320",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"22405",
         "name":"Ronja Bj\u00f6rk",
         "orgId":"509",
         "stat":"1",
         "st":"545430",
         "rt":"15910",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"21273",
         "name":"Janina H\u00e4gglund",
         "orgId":"509",
         "stat":"1",
         "st":"587420",
         "rt":"13790",
         "tstat":"1",
         "it":"0",
         "classId":"40"
      },
      {
         "id":"20592",
         "name":"Ebbe Ekdal",
         "orgId":"509",
         "stat":"1",
         "st":"660640",
         "rt":"13500",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"20637",
         "name":"Barbro Degermark",
         "orgId":"509",
         "stat":"1",
         "st":"543630",
         "rt":"14000",
         "tstat":"1",
         "it":"0",
         "classId":"50"
      },
      {
         "id":"18802",
         "name":"Kent Lundholm",
         "orgId":"509",
         "stat":"1",
         "st":"670220",
         "rt":"11200",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      },
      {
         "id":"18096",
         "name":"Patrick Lundquist",
         "orgId":"509",
         "stat":"1",
         "st":"667230",
         "rt":"15400",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"15400",
         "name":"Ingemar Almqvist",
         "orgId":"509",
         "stat":"1",
         "st":"577550",
         "rt":"14890",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"10638",
         "name":"Veronica Hopp",
         "orgId":"509",
         "stat":"1",
         "st":"613850",
         "rt":"15140",
         "tstat":"1",
         "it":"0",
         "classId":"140"
      },
      {
         "id":"2886",
         "name":"Leona Sohlmann",
         "orgId":"509",
         "stat":"1",
         "st":"664230",
         "rt":"16620",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"2826",
         "name":"Gj\u00f6l Hedman",
         "orgId":"509",
         "stat":"1",
         "st":"650430",
         "rt":"18060",
         "tstat":"1",
         "it":"0",
         "classId":"20"
      },
      {
         "id":"2203",
         "name":"Allan Sundqvist",
         "orgId":"509",
         "stat":"1",
         "st":"585640",
         "rt":"15360",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"2202",
         "name":"Simon Bergstr\u00f6m",
         "orgId":"509",
         "stat":"1",
         "st":"590430",
         "rt":"12440",
         "tstat":"1",
         "it":"0",
         "classId":"130"
      },
      {
         "id":"1355",
         "name":"Catarina Ulf",
         "orgId":"509",
         "stat":"1",
         "st":"669030",
         "rt":"13420",
         "tstat":"1",
         "it":"0",
         "classId":"10"
      }
   ],
   "organisations":[
      {
         "id":"241",
         "name":"Lindebygdens OK"
      },
      {
         "id":"375",
         "name":"Surahammars SOK"
      },
      {
         "id":"32",
         "name":"Almby IK"
      },
      {
         "id":"74",
         "name":"OK Djerf"
      },
      {
         "id":"95",
         "name":"Garphyttans IF"
      },
      {
         "id":"123",
         "name":"Hagaby GoIF \u00d6rebro"
      },
      {
         "id":"485",
         "name":"OK Tyl\u00f6skog"
      },
      {
         "id":"501",
         "name":"KFUM \u00d6rebro OK"
      },
      {
         "id":"502",
         "name":"OK Tisaren"
      },
      {
         "id":"508",
         "name":"OK Milan"
      },
      {
         "id":"509",
         "name":"Exempelklubb"
      }
   ],
   "classes":[
      {
         "id":"10",
         "name":"H21 E",
         "order":"100"
      },
      {
         "id":"20",
         "name":"D21 E",
         "order":"200"
      },
      {
         "id":"30",
         "name":"H 16-18 E",
         "order":"300"
      },
      {
         "id":"40",
         "name":"D 16-18 E",
         "order":"400"
      },
      {
         "id":"50",
         "name":"H14 E",
         "order":"500"
      },
      {
         "id":"60",
         "name":"D14 E",
         "order":"600"
      },
      {
         "id":"70",
         "name":"H12 E",
         "order":"700"
      },
      {
         "id":"80",
         "name":"D12 E",
         "order":"800"
      },
      {
         "id":"90",
         "name":"H10 E",
         "order":"900"
      },
      {
         "id":"100",
         "name":"D10 E",
         "order":"1000"
      },
      {
         "id":"110",
         "name":"Gr\u00f6n-Vit E",
         "order":"1100"
      },
      {
         "id":"120",
         "name":"Gul E",
         "order":"1200"
      },
      {
         "id":"130",
         "name":"Orange E",
         "order":"1300"
      },
      {
         "id":"140",
         "name":"Violett E",
         "order":"1400"
      }
   ]
}
```
