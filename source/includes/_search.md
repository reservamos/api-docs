# Search

## Crear una solicitud para b&uacute;squeda de viajes

```shell
   curl -X POST \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -d '{ "origin": "ciudad-de-mexico", "destination": "santiago-de-queretaro", "departs": "05-10-2015"  }' \
  'http://reserbus-sandbox.herokuapp.com/api/v2/search.json'
```

> Ejemplo de una respuesta exitosa

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "search": {
    "id": 9941580,
    "departs": "2016-03-20",
    "origin_id": "monterrey",
    "origin_type": "city",
    "destination_id": "ciudad-de-mexico",
    "destination_type": "city",
    "type_of_transport": {
      "bus": {
        "terminal_ids": [
          "t-ciudad-de-mexico-central-norte",
          "t-monterrey-churubusco",
          "t-monterrey-central"
        ],
        "line_ids": [
          "tdn-diamante",
          "turistar-lujo"
        ]
      },
      "flights": {
        "carrier_ids": [
          "volaris"
        ],
        "airport_ids":[
          "a-acapulco",
          "a-ciudad-juarez"
        ]
      }
    }
  },
  "terminals": {
    "t-ciudad-de-mexico-central-norte": {
      "name": "Terminal Central del Norte",
      "city_id": "Ciudad de México",
      "coordinates": {
        "lat": "19.4794829",
        "long": "-99.13953300000003"
      }
    },
    "t-monterrey-churubusco": {
      "name": "Avenida Churubusco",
      "city_id": "Monterrey",
      "coordinates": {
        "lat": "19.4794829",
        "long": "-99.13953300000003"
      }
    },
    "t-monterrey-central": {
      "name": "Central de Autobuses",
      "city_id": "Monterrey",
      "coordinates": null
    }
  },
  "airports": {
    "a-acapulco": {
      "name": "Acapulco",
      "city_id": "monterrey",
      "coordinates": {
        "lat": "19.4794829",
        "long": "-99.13953300000003"
      }
    },
    "a-ciudad-juarez": {
      "name": "Ciudad Juarez",
      "city_id": "juarez",
      "coordinates": {
        "lat": "19.4794829",
        "long": "-99.13953300000003"
      }
    }
  },
  "carriers": {
    "volaris": {
      "name": "Volaris",
      "human_abbr": "Volaris",
      "average_rating": 4.8,
      "rating_count": 196,
      "last_ratings": [
        {
          "name": "Jose Perez",
          "rating": 3,
          "comment": "Si se compro el boleto pero no se puede imprimir deberia de generar una clave de confirmacion por que aunque este pagado no quiere imprimir el boleto"
        },
        {
          "name": "Elías Ramirez",
          "rating": 4,
          "comment": "En mi último viaje  a Ixmiquilpan de regreso pague por un autobús de primera y nós mandaron uno cualquiera, sin baño. De hecho no era ni de ovnibus, además los boletos tuve que hacer fila por que los que mandaron por Internet  o traía la cadena."
        },
        {
          "name": "Cecilia Alvarez",
          "rating": 5,
          "comment": "El internet no es del todo bueno"
        }
      ],
      "cabin": [
        "bathroom",
        "tv",
        "wifi",
        "coffee"
      ],
      "logo_url": "https://rsrbs-production.s3.amazonaws.com/uploads/airplane/logo/19/volaris.png"
    }
  },
  "lines": {
    "turistar-lujo": {
      "name": "Turistar Lujo",
      "human_abbr": "Turistar Lujo",
      "transporter_name": "Grupo Etn-Turistar",
      "allows_seat_selection": true,
      "volatile_pricing": false,
      "average_ratings": 4.8,
      "last_ratings": [
        {
          "name": "Jose Perez",
          "rating": 3,
          "comment": "Si se compro el boleto pero no se puede imprimir deberia de generar una clave de confirmacion por que aunque este pagado no quiere imprimir el boleto"
        },
        {
          "name": "Elías Ramirez",
          "rating": 4,
          "comment": "En mi último viaje  a Ixmiquilpan de regreso pague por un autobús de primera y nós mandaron uno cualquiera, sin baño. De hecho no era ni de ovnibus, además los boletos tuve que hacer fila por que los que mandaron por Internet  o traía la cadena."
        },
        {
          "name": "Cecilia Alvarez",
          "rating": 5,
          "comment": "El internet no es del todo bueno"
        }
      ],
      "total_ratings": 196,
      "services": [
        "bathroom",
        "tv",
        "wifi",
        "coffee"
      ],
      "logo_url": "https://rsrbs-production.s3.amazonaws.com/uploads/line/logo/19/turistar-lujo.png",
      "ally": false,
      "ticket_counter_exchange":false,
      "redirection_info": {
        "desktop": {
          "url": "https://www.etn.com.mx",
          "mobile_screenshot": "/screenshots/etn-view-mobile.png",
          "desktop_screenshot": "/screenshots/etn-view.png",
          "responsive": true,
          "can_buy_mobile": true,
          "allow_deep_link": true,
          "short_url": "ETN.COM.MX",
          "needs_passengers": false
        },
        "mobile": {
          "url": "https://www.etn.com.mx",
          "mobile_screenshot": "/screenshots/etn-view-mobile.png",
          "desktop_screenshot": "/screenshots/etn-view.png",
          "responsive": true,
          "can_buy_mobile": true,
          "allow_deep_link": true,
          "needs_passengers": true
        }
      }
    },
    "tdn-diamante": {
      "name": "Transportes del Norte Diamante",
      "human_abbr": "Transportes del Norte Diamante",
      "transporter_name": "Grupo Senda",
      "allows_seat_selection": true,
      "volatile_pricing": false,
      "average_ratings": 4.5,
      "last_ratings": [
        {
          "name": "Jose Perez",
          "rating": 3,
          "comment": "Si se compro el boleto pero no se puede imprimir deberia de generar una clave de confirmacion por que aunque este pagado no quiere imprimir el boleto"
        },
        {
          "name": "Elías Ramirez",
          "rating": 4,
          "comment": "En mi último viaje  a Ixmiquilpan de regreso pague por un autobús de primera y nós mandaron uno cualquiera, sin baño. De hecho no era ni de ovnibus, además los boletos tuve que hacer fila por que los que mandaron por Internet  o traía la cadena."
        },
        {
          "name": "Cecilia Alvarez",
          "rating": 5,
          "comment": "El internet no es del todo bueno"
        }
      ],
      "total_ratings": 130,
      "services": [
        "bathroom",
        "tv",
        "wifi"
      ],
      "logo_url": "https://rsrbs-production.s3.amazonaws.com/uploads/line/logo/10/uploads_2F1443811475559-84lbiivvel70hpvi-ac7348993e4a7cda79646cce6101c6c8_2Ftdn-diamante.png",
      "ally": true,
      "ticket_counter_exchange":false,
      "redirection_info": null
    }
  },
  "cities": {
    "monterrey": {
      "name": "Monterrey",
      "state": "Nuevo Leon",
      "state_abbr": "NL",
      "country": "Mexico",
      "country_abbr": "MX"
    },
    "ciudad-de-mexico": {
      "name": "Ciudad de Mexico",
      "state": "Mexico",
      "state_abbr": "CDMX",
      "country": "Mexico",
      "country_abbr": "MX"
    }
  }
}
```

> Ejemplos de errores

```
HTTP/1.1 422 Unprocessable Entity
Status: 422 Unprocessable Entity
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "errors": [
    {
      "code": 3,
      "message": "'origin' es requerido"
    }
  ]
}
```

```
HTTP/1.1 422 Unprocessable Entity
Status: 422 Unprocessable Entity
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "errors": [
    {
      "code": 5,
      "message": "El formato de 'departs' es inválido"
    }
  ]
}
```

```
HTTP/1.1 422 Unprocessable Entity
Status: 422 Unprocessable Entity
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "errors": [
    {
      "code": 7,
      "message": "'departs' no puede ser una fecha en el pasado"
    }
  ]
}
```

### HTTP Request

`POST /search.json`

### Request Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`origin`<br>*requerido* | string | Slug de ciudad de origen.<br>**Ejemplos:** `monterrey`
`destination`<br>*requerido* | string | Slug de ciudad de destino.<br>**Ejemplos:** `ciudad-de-mexico`
`departs`<br>*requerido* | string | Fecha del viaje (formato: `dd-mm-aaaa`).<br>**Ejemplos:** `13-06-2014`
`exclude_carriers`<br>*opcional* | boolean | Decide si enviar detalle de compañía de aviones`
`exclude_lines`<br>*requerido* | boolean | Decide si enviar detalle de líneas de autobuses`

### Response Details

La respuesta contiene los medios de transporte que te llevan a ese destino. Cada medio de transporte, tiene incluido las compañías que ofrecen servicio en esa ruta. Adicionalmente, viene el detalle de todas las ubicaciones(terminales, ciudades y aeropuertos relacionados a los resultados que se van a desplegar)


### Response Body

Nombre | Detalles
--- | ---
`type_of_transport` | Objeto que tiene una llave por cada medio de transporte(bus, ride, airplane) que te lleva a esa ruta
`terminals` | Lista de terminales de autobuses que saldran en los resultados
`airports`  | Lista de aeropuertos que saldran en los resultados
`carriers`  | Lista de aerolineas implicadas en los resultados
`lines`     | Lista de lineas de autobus que saldran en los resultados
`cities`    | Lista de ciudades implicadas en los resultados


### Type of Transports

* Bus

Nombre | Detalles
--- | ---
`terminal_ids` | Una lista de los ids de las terminales de origen/destino de esa ruta
`line_ids` | Una lista de las líneas de autobuses que te llevan a ese destino

* Flights

Nombre | Detalles
--- | ---
`airport_ids` | Una lista de los ids de los aeropuertos de origen/destino de esa ruta
`carrier_ids` | Una lista de las compañías de avión que te llevan a ese destino


* Carriers

Coming soon ...  ;) 

* Lines

Coming soon ... ;)

* Airports

Coming soon ... ;)

* Terminals

Coming soon ... ;)

* Cities

Nombre | Detalles
--- | ---
`name` | 
`state` | 
`state_abbr` | 
`country` | 
`country_abbr` | 

## Consultar estado de la b&uacute;squeda

```bash
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v2/search/84273582?type=trips'
```

> Parametros de búsqueda para autobus

```json
{
  "id": "1casxV2",
  "line_ids": ["tdn" ,"tdn-diamante"],
  "service_ids": ["economy" ,"first_class"],
  "origin_terminal_ids": ["t-monterrey-central"],
  "destination_terminal_ids": ["t-ciudad-de-mexico"],
  "departure_time_min": "4:00",
  "departure_time_max": "23:00",
  "arrival_time_min": "11:00",
  "arrival_time_max": "",
  "price_min": "320",
  "price_max": "555",
  "price_currency": "MXN",
  "duration": 600,
  "stops_count": 2,
  "page": "2",
  "per_page": "10",
  "sort_by": "departure_time",
  "sort_order": "ASC"
}
```

> Parametros de búsqueda para avion (No implementado aun)

```json
{
  "id": "1casxV2",
  "carrier_ids": ["volaris" ,"interjet"],
  "cabin_ids": ["economy" ,"first_class"],
  "origin_airport_ids": ["a-mty"],
  "destination_airport_ids": ["a-mex"],
  "departure_time_min": "4:00",
  "departure_time_max": "23:00",
  "arrival_time_min": "11:00",
  "arrival_time_max": "13:00",
  "price_min": "320",
  "price_max": "555",
  "price_currency": "MXN",
  "duration": 600,
  "stops_count": 2,
  "page": "2",
  "per_page": "10",
  "sort_by": "departure_time",
  "sort_order": "ASC"
}
```

> Parametros de búsqueda para rides (No implementado aun)

```json
{
  "id": "1casxV2",
  "car_comfort": ["economy" ,"first_class"],
  "departure_time_min": "4:00",
  "departure_time_max": "23:00",
  "arrival_time_min": "11:00",
  "arrival_time_max": "13:00",
  "duration": 600,
  "price_min": "320",
  "price_max": "555",
  "price_currency": "MXN",
  "page": "2",
  "per_page": "10",
  "sort_by": "departure_time",
  "sort_order": "ASC"
}
```

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`id`<br>*requerido* | entero positivo | Id de la búsqueda generado por Reserbus
`type` <br>*requerido* | string | Tipo de viaje que desea obtener.  Los valores pueden ser `rides` o `trips`

### HTTP Request

`GET /search/{id}?type={type}`

## Response Details

La respuesta regresa los mismos datos de búsqueda de la creación de una búsqueda. Adicionalmente, vienen todos los viajes pertenecientes a esa búsqueda.

### Response Body

Nombre | Detalles
--- | ---
`search` | 
`trips`/`flights`/`rides` | Lista de viajes de la búsqueda (viajes, vuelos, o aventones)

##  Detalle de viaje en autobus

> Ejemplo de una respuesta exitosa de búsqueda tipo autobús

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "id": 147812808,
  "state": "finished",
  "departs": "2016-03-20",
  "created_at": "2016-03-18T13:17:24.592-06:00",
  "finished_at": "2016-03-18T13:17:26-06:00",
  "origin_id": "monterrey",
  "origin_type": "city",
  "destination_id": "t-ciudad-de-mexico-central-norte",
  "destination_type": "terminal",
  "trips": [
    {
      "id": "mexn-mtyc-20mar161730-980044-19",
      "origin_id": "t-monterrey-churubusco",
      "destination_id": "t-ciudad-de-mexico-central-norte",
      "departure": "2016-03-20T17:30:00",
      "arrival": "2016-03-21T06:00:00",
      "duration": 1345,
      "availability": 6,
      "capacity": 40,
      "pricing": {
        "amount": "1205.0",
        "taxes": "100.0",
        "total": "1305.0"
      },
      "service": "LUJO",
      "line_id": "turistar-lujo",
      "stops": null,
      "passenger_types": [
        {
          "type": "general",
          "availability": 6
        },
        {
          "type": "older",
          "availability": 1
        },
        {
          "type": "minor",
          "availability": 2
        }
      ]
    },
    {
      "id": "mex-mty-20mar162000-8549872-10",
      "origin_id": "t-ciudad-de-mexico-central-norte",
      "destination_id": "t-monterrey-central",
      "departure": "2016-03-20T17:30:00",
      "arrival": "2016-03-21T06:00:00",
      "duration": 1345,
      "availability": 22,
      "capacity": 40,
      "pricing": {
        "amount": "1205.0",
        "taxes": "200.0",
        "total": "2086.0"
      },
      "service": "diamante",
      "line_id": "tdn-diamante",
      "stops": 1,
      "passenger_type": [
        {
          "type": "general",
          "availability": 22
        },
        {
          "type": "older",
          "availability": 8
        },
        {
          "type": "minor",
          "availability": 2
        }
      ]
    }
  ]
}
```

Nombre         | Detalles
---            | ---
`id`           | 
`origin_id`    | 
`destination_id` | 
`departure`    | 
`arrival`      | 
`duration`     | 
`availability` | 
`capacity`     |
`pricing.amount`| 
`pricing.taxes` | 
`pricing.total` | 
`service`      | 
`line_id`      | 
`stops` | 
`passenger_types.type` | 
`passenger_types.availability` | 

##  Detalle de viaje en avion

> Ejemplo de una respuesta exitosa de búsqueda tipo vuelos (No  implementado aun)

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "search": {
    "id": 147812808,
    "state": "finished",
    "departure_date": "2016-03-20",
    "created_at": "2016-03-18T13:17:24.592-06:00",
    "finished_at": "2016-03-18T13:17:26-06:00",
    "origin_id": "ciudad-de-mexico",
    "origin_type": "city",
    "destination_id": "guadalajara",
    "destination_type": "city",
    "flights": [
      {
        "id": "mex-gdl-20mar160509-980044-19",
        "origin_id": "a-MEX",
        "origin_terminal": "B",
        "destination_id": "a-GDL",
        "destination_terminal": "C",
        "distance": 4602,
        "departure": "2016-03-20T05:09:00",
        "arrival": "2016-03-20T12:01:00",
        "flight_duration": 265,
        "connection_duration": 150,
        "duration": 415,
        "availability": 20,
        "pricing": {
          "amount": "363.00",
          "taxes": "557.0",
          "total": "920.00"
        },
        "legs": [
          {
            "origin_id": "a-MEX",
            "origin_terminal": "B",
            "destination_id": "a-MTY",
            "destination_terminal": "C",
            "departure": "2016-03-20T05:09:00",
            "arrival": "2016-03-20T06:59:00",
            "carrier_id": "Y4",
            "flight_number": "756",
            "aircraft": "CVE-6",
            "duration": 118,
            "connection_duration": 145
          },
          {
            "origin_id": "a-MTY",
            "origin_terminal": "B",
            "destination_id": "a-GDL",
            "destination_terminal": "C",
            "departure": "2016-03-20T09:25:00",
            "arrival": "2016-03-20T12:01:00",
            "carrier_id": "Y4",
            "flight_number": "687",
            "aircraft": "CDE-6",
            "duration": 118,
            "connection_duration": 0
          }
        ]
      },
      {
        "id": "mex-gdl-20mar160509-980044-19",
        "origin_id": "a-MEX",
        "origin_terminal": "B",
        "destination_id": "a-GDL",
        "destination_terminal": "C",
        "distance": 4602,
        "departure": "2016-03-20T06:00:00",
        "arrival": "2016-03-20T07:20:00",
        "flight_duration": 80,
        "connection_duration": 0,
        "duration": 80,
        "availability": 20,
        "pricing": {
          "amount": "363.00",
          "taxes": "557.0",
          "total": "920.00"
        },
        "legs": [
          {
            "origin_id": "a-MEX",
            "origin_terminal": "B",
            "destination_id": "a-GDL",
            "destination_terminal": "C",
            "departure": "2016-03-20T06:00:00",
            "arrival": "2016-03-20T07:20:00",
            "carrier_id": "Y4",
            "flight_number": "4734",
            "aircraft": "CVE-2",
            "duration": 118,
            "connection_duration": 0
          }
        ]
      }
    ]
  }
}
```

Nombre | Detalles
--- | ---
`id` | Id de vuelos (Slice)
`origin_id` | Id de aeropuerto de origen
`origin_terminal` | 
`destination_id` | Id de aeropuerto de destino
`destination_terminal` | 
`departure` | 
`arrival` | 
`flight_duration` | 
`connection_duration` | 
`duration` | 
`availability` | 
`price` | Precio de todos los vuelos
`taxes`|
`total`|

* Legs

Nombre | Detalles
--- | ---
`id`|
`origin_id` | Id de aeropuerto de origen
`origin_terminal` | 
`destination_id` | Id de aeropuerto de destino
`destination_terminal` | 
`departure` | 
`arrival` | 
`carrier_id` | Id de compañía de vuelos
`flight_number` | Id de avión
`aircraft` |
`connection_duration` | 

##  Detalle de viaje en carro
> Ejemplos de una respuesta exitosa de búsqueda tipo rides


```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
 "id": 147812808,
 "state": "finished",
 "departure_date": "2016-03-20",
 "created_at": "2016-03-18T13:17:24.592-06:00",
 "finished_at": "2016-03-18T13:17:26-06:00",
 "origin_id": "monterrey",
 "origin_type": "city",
 "destination_id": "guadalajara",
 "destination_type": "city",
 "rides": [
   {
     "id": "12jun160800-504935524-colonia-lazaro-cardenas-villas-del-poniente-bbc",
     "origin": {
       "address": "Monterrey, N.L., Mexico",
       "lat": 25.6866142,
       "long": -100.3161126
     },
     "destination": {
       "address": "Guadalajara, Jal., México",
       "lat": 20.6596988,
       "long": -103.3496092
     },
     "distance": 793,
     "departure": "2016-03-20T07:30:00",
     "arrival": "2016-03-20T16:00:00",
     "duration": 512,
     "availability": 3,
     "capacity": 3,
     "pricing": {
       "amount": "1205.0",
       "taxes": "0.0",
       "total": "1205.0"
     },
     "services": [
       "woman_only",
       "is_comfort",
       "freeway"
     ],
     "car": {
       "model": "CRUZE",
       "make": "CHEVROLET",
       "comfort": "Luxury",
       "comfort_nb_star": 4
     },
     "stop_names": [
       "Monterrey",
       "Guadalajara",
       "Santa María Huatulco"
     ],
     "user": {
       "display_name": "Gisela Garza",
       "gender": "F",
       "age": 30,
       "rating": 4.5,
       "rating_count": 2,
       "experience": "newbie",
       "picture": "https://d2kwny77wxvuie.cloudfront.net/user/p__P0kfROqLAclofvXx8w/thumbnail_72x72.jpeg",
       "smoking": "maybe",
       "music": "yes",
       "pets": "maybe",
       "dialog": "yes"
     },
     "booking": "no_booking_no_mode",
     "redirect_url": "https://www.blablacar.mx/viaje-colonia-lazaro-cardenas-villas-del-poniente-504935524?comuto_cmkt=MX_Reserbus_PSGR_O-Ciudad+de+M%C3%A9xico%2C+M%C3%A9xico-D-Monterrey%2C+M%C3%A9xico_TRIP&utm_source=Reserbus&utm_medium=API&utm_content=RESERBUSSEARCH&utm_campaign=MX_Reserbus_PSGR_O-Ciudad+de+M%C3%A9xico%2C+M%C3%A9xico-D-Monterrey%2C+M%C3%A9xico_TRIP" 
   },
   {
     "id": "mty-gdl-20mar160509-980044-19",
     "origin": {
       "address": "Monterrey, N.L., Mexico",
       "lat": 25.6866142,
       "long": -100.3161126
     },
     "destination": {
       "address": "Guadalajara, Jal., México",
       "lat": 20.6596988,
       "long": -103.3496092
     },
     "distante": 790,
     "departure": "2016-03-20T10:00:00",
     "arrival": "2016-03-20T18:40:00",
     "duration": 518,
     "availability": 3,
     "capacity": 3,
     "pricing": {
       "amount": "1205.0",
       "taxes": "0.0",
       "total": "1205.0"
     },
     "services": [
       "woman_only",
       "is_comfort",
       "freeway"
     ],
     "car": {
       "model": "CRUZE",
       "make": "CHEVROLET",
       "comfort": "Luxury",
       "comfort_nb_star": 4
     },
     "stop_names": [
       "Monterrey",
       "Guadalajara"
     ],
     "user": {
       "display_name": "Jose M G",
       "gender": "M",
       "age": 40,
       "rating": 4.5,
       "rating_count": 4,
       "experience": "experienced",
       "picture": "https://d2kwny77wxvuie.cloudfront.net/user4SVwKRPzRpeNny3OhW0lng/thumbnail_72x72.jpeg",
       "smoking": "no",
       "music": "maybe",
       "pets": "maybe",
       "dialog": "yes"
     }
     "booking": "no_booking_no_mode",
     "redirect_url": "https://www.blablacar.mx/viaje-colonia-lazaro-cardenas-villas-del-poniente-504935524?comuto_cmkt=MX_Reserbus_PSGR_O-Ciudad+de+M%C3%A9xico%2C+M%C3%A9xico-D-Monterrey%2C+M%C3%A9xico_TRIP&utm_source=Reserbus&utm_medium=API&utm_content=RESERBUSSEARCH&utm_campaign=MX_Reserbus_PSGR_O-Ciudad+de+M%C3%A9xico%2C+M%C3%A9xico-D-Monterrey%2C+M%C3%A9xico_TRIP" 
   }
 ]
}
```
Nombres | Detalles
--- | ---

Coming soon ....

> Ejemplos de error

```
HTTP/1.1 404 Not Found
Status: 404 Not Found
Connection: keep-alive
Content-Type: application/json; charset=utf-8
```

```json
{
  "status": "404",
  "error": "Not Found"
}
```
