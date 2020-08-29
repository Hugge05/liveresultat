# Liveresultat

## API
All API requests should be made via HTTPS GET reqests, content returned is returned as JSON.

### ``getallcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions``

Returns a list of all events and their: ``id``, ``name``, ``organizerId``, ``dateTime`` (when the event will be hosted) and ``createdTime`` (when the event was created on Liveresultat).

### ``getcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions&page=0&results=15``

Like ``getallcompetitions`` but divided into pages, starting at 0. Results defaults to 15.


### ``getcompetitions2``
``https://pallhed.se/api.php?method=getallcompetitions&page=0&results=15``

Like ``getcompetitions`` but starts from the given number, defaults to 0.

### ``getuserinfo``
``https://pallhed.se/api.php?method=getuserinfo&id=1``

Returns the users details.

### ``getcompetitioninfo``
``https://pallhed.se/api.php?method=getcompetitioninfo&id=14``

Returns the competitions details, runners and organisations.
Return example:

```json
{
    "competition": {
        "name": "GIF-Ringen Etapp 5",
        "organizerId": "1",
        "dateTime": "2020-07-24",
        "createdTime": "2020-07-24 17:28:17"
    },
    "runners": [
        {
            "id": "193504",
            "name": "Bertil Jansson",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "193503",
            "name": "Lukas Pallhed",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "193502",
            "name": "Jonas Janegren",
            "orgId": "501",
            "classId": "120"
        },
        {
            "id": "193500",
            "name": "Maja Oskarsson",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "193497",
            "name": "Matilda Gustafsson",
            "orgId": "74",
            "classId": "110"
        },
        {
            "id": "192058",
            "name": "Max Hane",
            "orgId": "74",
            "classId": "110"
        },
        {
            "id": "192059",
            "name": "Lykke Hane",
            "orgId": "74",
            "classId": "110"
        },
        {
            "id": "190003",
            "name": "Jonathan Wikström Örlén",
            "orgId": "241",
            "classId": "110"
        },
        {
            "id": "182260",
            "name": "Jonas Robertsson",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "181958",
            "name": "Tuva Hedmark",
            "orgId": "241",
            "classId": "110"
        },
        {
            "id": "170833",
            "name": "Rihards Darzins",
            "orgId": "32",
            "classId": "130"
        },
        {
            "id": "170551",
            "name": "Arne Lagerqvist",
            "orgId": "95",
            "classId": "90"
        },
        {
            "id": "161704",
            "name": "Matilda Henriksson Ribeiro",
            "orgId": "74",
            "classId": "100"
        },
        {
            "id": "160221",
            "name": "Nellie Holmquist Pahlm",
            "orgId": "95",
            "classId": "110"
        },
        {
            "id": "158169",
            "name": "Tova Edgren",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "148526",
            "name": "Robin Persson",
            "orgId": "74",
            "classId": "90"
        },
        {
            "id": "144447",
            "name": "Saara Nummelin",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "136583",
            "name": "Arvid Andersson",
            "orgId": "32",
            "classId": "50"
        },
        {
            "id": "129619",
            "name": "Viggo Holmberg",
            "orgId": "485",
            "classId": "50"
        },
        {
            "id": "128972",
            "name": "Klara Thybeck",
            "orgId": "241",
            "classId": "110"
        },
        {
            "id": "122230",
            "name": "Lin Pelander",
            "orgId": "74",
            "classId": "110"
        },
        {
            "id": "121750",
            "name": "Tony Holmberg",
            "orgId": "485",
            "classId": "130"
        },
        {
            "id": "121417",
            "name": "Ingrid Arnesson",
            "orgId": "241",
            "classId": "110"
        },
        {
            "id": "121062",
            "name": "Sigrid Janegren",
            "orgId": "501",
            "classId": "100"
        },
        {
            "id": "120947",
            "name": "Oliver Arnesson",
            "orgId": "241",
            "classId": "70"
        },
        {
            "id": "119543",
            "name": "Henning Janegren",
            "orgId": "501",
            "classId": "50"
        },
        {
            "id": "117826",
            "name": "Åsa Wikström",
            "orgId": "508",
            "classId": "130"
        },
        {
            "id": "117925",
            "name": "Elin Djerf",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "117926",
            "name": "Hanna Djerf",
            "orgId": "95",
            "classId": "110"
        },
        {
            "id": "115604",
            "name": "Henrik Nettelmark",
            "orgId": "375",
            "classId": "140"
        },
        {
            "id": "106794",
            "name": "Julia Gustafsson",
            "orgId": "501",
            "classId": "60"
        },
        {
            "id": "110625",
            "name": "Wilma Wikström",
            "orgId": "508",
            "classId": "60"
        },
        {
            "id": "106382",
            "name": "Rasmus Pettersson",
            "orgId": "74",
            "classId": "30"
        },
        {
            "id": "105101",
            "name": "Kia Lagerqvist",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "103158",
            "name": "Karuna Dahlberg",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "102209",
            "name": "Edwin Säker",
            "orgId": "123",
            "classId": "70"
        },
        {
            "id": "101838",
            "name": "Vidar Nettelmark",
            "orgId": "375",
            "classId": "30"
        },
        {
            "id": "98365",
            "name": "Peter Österberg",
            "orgId": "375",
            "classId": "140"
        },
        {
            "id": "94698",
            "name": "Elin Doering",
            "orgId": "95",
            "classId": "60"
        },
        {
            "id": "94699",
            "name": "Jonna Doering",
            "orgId": "95",
            "classId": "100"
        },
        {
            "id": "98364",
            "name": "Beatrice Österberg",
            "orgId": "375",
            "classId": "40"
        },
        {
            "id": "94692",
            "name": "Ylva Doering",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "88627",
            "name": "Niklas Doering",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "87505",
            "name": "Fabian Bergqvist",
            "orgId": "95",
            "classId": "50"
        },
        {
            "id": "87500",
            "name": "Petter Bergqvist",
            "orgId": "95",
            "classId": "90"
        },
        {
            "id": "87499",
            "name": "Mona Bergqvist",
            "orgId": "95",
            "classId": "110"
        },
        {
            "id": "83449",
            "name": "Agnes Johansson",
            "orgId": "375",
            "classId": "40"
        },
        {
            "id": "83216",
            "name": "Fabian Larsson",
            "orgId": "508",
            "classId": "50"
        },
        {
            "id": "81211",
            "name": "Yvonne Franzén",
            "orgId": "32",
            "classId": "130"
        },
        {
            "id": "74052",
            "name": "Hugo Örn",
            "orgId": "501",
            "classId": "30"
        },
        {
            "id": "75175",
            "name": "Vilma Larsson",
            "orgId": "508",
            "classId": "40"
        },
        {
            "id": "79974",
            "name": "Sofie Franzén",
            "orgId": "32",
            "classId": "40"
        },
        {
            "id": "73385",
            "name": "Kaisa Mårtensson",
            "orgId": "95",
            "classId": "20"
        },
        {
            "id": "73282",
            "name": "Peter Mårtensson",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "73280",
            "name": "David Mårtensson",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "61541",
            "name": "Daniel Stunz",
            "orgId": "501",
            "classId": "10"
        },
        {
            "id": "64879",
            "name": "Ulf Johansson",
            "orgId": "375",
            "classId": "140"
        },
        {
            "id": "67968",
            "name": "Lovisa Thybeck",
            "orgId": "241",
            "classId": "80"
        },
        {
            "id": "58323",
            "name": "Joakim Dahlberg",
            "orgId": "32",
            "classId": "140"
        },
        {
            "id": "59973",
            "name": "Sofia Halldin",
            "orgId": "501",
            "classId": "80"
        },
        {
            "id": "56587",
            "name": "Axel Nilsson",
            "orgId": "95",
            "classId": "50"
        },
        {
            "id": "54917",
            "name": "Noel Helmersson",
            "orgId": "502",
            "classId": "30"
        },
        {
            "id": "54788",
            "name": "Valter Pettersson",
            "orgId": "502",
            "classId": "30"
        },
        {
            "id": "54916",
            "name": "Robin Helmersson",
            "orgId": "502",
            "classId": "50"
        },
        {
            "id": "52276",
            "name": "Lovisa Gustafsson",
            "orgId": "501",
            "classId": "40"
        },
        {
            "id": "54113",
            "name": "Niclas Risberg",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "52274",
            "name": "Anna Gustafsson",
            "orgId": "501",
            "classId": "140"
        },
        {
            "id": "52273",
            "name": "Mats Gustafsson",
            "orgId": "501",
            "classId": "140"
        },
        {
            "id": "49842",
            "name": "Elin Sundvall Krüger",
            "orgId": "95",
            "classId": "40"
        },
        {
            "id": "49615",
            "name": "Leif Krüger",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "49510",
            "name": "Edvard Pelander",
            "orgId": "74",
            "classId": "50"
        },
        {
            "id": "48481",
            "name": "Sara Garpenlund",
            "orgId": "501",
            "classId": "20"
        },
        {
            "id": "49509",
            "name": "Ellen Pelander",
            "orgId": "74",
            "classId": "40"
        },
        {
            "id": "41275",
            "name": "Lars-Erik Hasler",
            "orgId": "375",
            "classId": "140"
        },
        {
            "id": "42759",
            "name": "Oscar Kristoffersson",
            "orgId": "32",
            "classId": "70"
        },
        {
            "id": "38445",
            "name": "Ludvig Hasler",
            "orgId": "375",
            "classId": "30"
        },
        {
            "id": "34694",
            "name": "Måns Dahlberg",
            "orgId": "32",
            "classId": "70"
        },
        {
            "id": "32510",
            "name": "Helmina Pallhed",
            "orgId": "95",
            "classId": "120"
        },
        {
            "id": "32504",
            "name": "Christer Persson",
            "orgId": "74",
            "classId": "130"
        },
        {
            "id": "31850",
            "name": "Axel Thybeck",
            "orgId": "241",
            "classId": "50"
        },
        {
            "id": "26446",
            "name": "Erik Nilsson",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "22536",
            "name": "Martin Risberg",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "21273",
            "name": "Sofie Bodin",
            "orgId": "32",
            "classId": "40"
        },
        {
            "id": "20637",
            "name": "Edvin Halldin",
            "orgId": "501",
            "classId": "50"
        },
        {
            "id": "20592",
            "name": "Lars Walldoff",
            "orgId": "95",
            "classId": "130"
        },
        {
            "id": "2886",
            "name": "Karin Nilsson",
            "orgId": "95",
            "classId": "20"
        },
        {
            "id": "10638",
            "name": "Sofia Carlsson",
            "orgId": "241",
            "classId": "140"
        },
        {
            "id": "15400",
            "name": "Lena Westerlund",
            "orgId": "74",
            "classId": "140"
        },
        {
            "id": "18096",
            "name": "Torun Pahlm",
            "orgId": "95",
            "classId": "20"
        },
        {
            "id": "18802",
            "name": "Jesper Melin",
            "orgId": "95",
            "classId": "10"
        },
        {
            "id": "2826",
            "name": "Lena Jansson",
            "orgId": "95",
            "classId": "20"
        },
        {
            "id": "2203",
            "name": "Annica Kristoffersson",
            "orgId": "32",
            "classId": "130"
        },
        {
            "id": "2202",
            "name": "Nils-Olof Bodin",
            "orgId": "32",
            "classId": "120"
        },
        {
            "id": "1355",
            "name": "Torben Malm",
            "orgId": "95",
            "classId": "10"
        }
    ],
    "organisations": [
        {
            "id": "508",
            "name": "OK Milan"
        },
        {
            "id": "502",
            "name": "OK Tisaren"
        },
        {
            "id": "501",
            "name": "KFUM Örebro OK"
        },
        {
            "id": "485",
            "name": "OK Tylöskog"
        },
        {
            "id": "375",
            "name": "Surahammars SOK"
        },
        {
            "id": "241",
            "name": "Lindebygdens OK"
        },
        {
            "id": "123",
            "name": "Hagaby GoIF Örebro"
        },
        {
            "id": "95",
            "name": "Garphyttans IF"
        },
        {
            "id": "32",
            "name": "Almby IK"
        },
        {
            "id": "74",
            "name": "OK Djerf"
        }
    ],
    "classes": [
        {
            "id": "140",
            "name": "Violett E",
            "order": "1400"
        },
        {
            "id": "130",
            "name": "Orange E",
            "order": "1300"
        },
        {
            "id": "120",
            "name": "Gul E",
            "order": "1200"
        },
        {
            "id": "110",
            "name": "Grön-Vit E",
            "order": "1100"
        },
        {
            "id": "100",
            "name": "D10 E",
            "order": "1000"
        },
        {
            "id": "90",
            "name": "H10 E",
            "order": "900"
        },
        {
            "id": "80",
            "name": "D12 E",
            "order": "800"
        },
        {
            "id": "70",
            "name": "H12 E",
            "order": "700"
        },
        {
            "id": "60",
            "name": "D14 E",
            "order": "600"
        },
        {
            "id": "50",
            "name": "H14 E",
            "order": "500"
        },
        {
            "id": "40",
            "name": "D 16-18 E",
            "order": "400"
        },
        {
            "id": "30",
            "name": "H 16-18 E",
            "order": "300"
        },
        {
            "id": "10",
            "name": "H21 E",
            "order": "100"
        },
        {
            "id": "20",
            "name": "D21 E",
            "order": "200"
        }
    ]
}
```
