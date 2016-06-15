# Trip Details

## Crear una petici&oacute;n para obtener detalles de un viaje

```shell
curl -X POST \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/trips/qro-mex-1oct151920-577-2/details_requests'
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
  "id": 3076,
  "state": "pending",
  "poll_to": "/api/v1/trips/qro-mex-1oct151920-577-2/details_requests/3076",
  "error_code": null,
  "error_message": null,
  "created_at": "2015-09-28T13:11:59.546-05:00",
  "updated_at": "2015-09-28T13:11:59.546-05:00"
}
```

> Ejemplo de un error

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

### HTTP Request

`POST /trips/{slug}/details_requests`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`slug`<br>*requerido* | string | Cadena de caracteres que identifica el viaje<br>**Ejemplos:** `qro-mex-1oct151920-577-2`

## Consultar estatus de los detalles del viaje

```shell
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/trips/qro-mex-1oct151920-577-2/details_requests/3076'
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
  "id": 3076,
  "state": "finished",
  "poll_to": null,
  "error_code": null,
  "error_message": null,
  "created_at": "2015-09-28T13:11:59.546-05:00",
  "updated_at": "2015-09-28T13:12:05.077-05:00",
  "bus": [
    [
      [
        {
          "category": "seat_tv",
          "number": "1",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "2",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "4",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "5",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "6",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "8",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "9",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "10",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat_tv",
          "number": "11",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "12",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat_tv",
          "number": "13",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "14",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "15",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "16",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "17",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "18",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "19",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "20",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "21",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "22",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat_tv",
          "number": "23",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "24",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "25",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "26",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "27",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "28",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat_tv",
          "number": "29",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "30",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "31",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "32",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "33",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "34",
          "occupied": false
        }
      ],
      [
        {
          "category": "bathroom_women"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "kitchen"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "bathroom_men"
        }
      ],
      [
        {
          "category": "seat_tv",
          "number": "1",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "2",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "3",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "4",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "5",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "6",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "7",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "8",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "9",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "10",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat_tv",
          "number": "11",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "12",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat_tv",
          "number": "13",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "14",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "15",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "16",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "17",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "18",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "19",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "20",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "21",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "22",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat_tv",
          "number": "23",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "24",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "25",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "26",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "27",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "28",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat_tv",
          "number": "29",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "30",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "31",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "32",
          "occupied": false
        }
      ],
      [
        {
          "category": "seat",
          "number": "33",
          "occupied": false
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "seat",
          "number": "34",
          "occupied": false
        }
      ],
      [
        {
          "category": "bathroom_women"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "kitchen"
        },
        {
          "category": "hallway"
        },
        {
          "category": "hallway"
        },
        {
          "category": "bathroom_men"
        }
      ]
    ]
  ],
  "trip": {
    "id": 4431,
    "slug": "qro-mex-1oct151920-577-2",
    "key": "577",
    "price": 173,
    "regular_price": 173,
    "open": true,
    "service": "Primera",
    "capacity": 35,
    "created_at": "2015-09-28T11:05:49.919-05:00",
    "updated_at": "2015-09-28T11:05:49.919-05:00",
    "departure": {
      "to_s": "2015-10-01T19:20:00",
      "date": "Jueves, 01 de Octubre",
      "hours": "07:20 PM",
      "uts": 1443745200
    },
    "arrival": {
      "to_s": "2015-10-01T22:15:00",
      "date": "Jueves, 01 de Octubre",
      "hours": "10:15 PM",
      "uts": 1443755700
    },
    "discounts": [],
    "available_all": 35,
    "stopovers": "0",
    "origin": {
      "id": 31,
      "terminal": "Terminal de Autobuses",
      "city": "Santiago de Querétaro",
      "code": "QRO",
      "slug": "t-santiago-de-queretaro-terminal",
      "coordinates": null
    },
    "destination": {
      "id": 22,
      "terminal": "Terminal Central del Norte",
      "city": "Ciudad de México",
      "code": "MEX",
      "slug": "t-ciudad-de-mexico-central-norte",
      "coordinates": {
        "lat": 16.18,
        "long": -95.19
      }
    },
    "line": {
      "name": "Primera Plus",
      "abbr": "primera-plus",
      "human_abbr": "Primera Plus",
      "transporter_name": "Grupo Flecha Amarilla",
      "transporter_abbr": "gfa",
      "allows_seat_selection": true,
      "volatile_pricing": false,
      "services": [],
      "commission": 6,
      "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/2/primera-plus.png",
      "ally":false,
      "copyright_protected":false,
      "site": {
        "mobile": {
          "url":"https://www.primeraplus.com.mx",
          "mobile_screenshot":"https://www.reserbus.mx/screenshots/gfa-view-mobile.png",
          "desktop_screenshot":"https://www.reserbus.mx/screenshots/gfa-view.png",
          "responsive":true,
          "can_buy_mobile":true,
          "allow_deep_link":false,
          "short_url":"PRIMERAPLUS.com.mx",
          "needs_passenger": false
        },
        "desktop": {
          "url":"https://www.primeraplus.com.mx",
          "mobile_screenshot":"https://www.reserbus.mx/screenshots/gfa-view-mobile.png",
          "desktop_screenshot":"https://www.reserbus.mx/screenshots/gfa-view.png",
          "responsive":true,
          "can_buy_mobile":true,
          "allow_deep_link":false,
          "short_url":"PRIMERAPLUS.com.mx",
          "needs_passenger": false
        }
      }
    },
    "categories": [
      {
        "category": "minor",
        "amount": "87.0",
        "taxes": "0.0",
        "total": "87.0",
        "availability": 2
      },
      {
        "category": "general",
        "amount": "173.0",
        "taxes": "0.0",
        "total": "173.0",
        "availability": 35
      },
      {
        "category": "older",
        "amount": "87.0",
        "taxes": "0.0",
        "total": "87.0",
        "availability": 2
      },
      {
        "category": "teacher",
        "amount": "173.0",
        "taxes": "0.0",
        "total": "173.0",
        "availability": 0
      },
      {
        "category": "student",
        "amount": "173.0",
        "taxes": "0.0",
        "total": "173.0",
        "availability": 0
      }
    ]
  }
}
```

> Ejemplo de un error

```
HTTP/1.1 404 Not Found
Status: 404 Not Found
Connection: keep-alive
Content-Type: application/json; charset=utf-8
```

### HTTP Request

`GET /trips/{slug}/details_requests/{id}`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`slug`<br>*requerido* | string | Cadena de caracteres que identifica el viaje<br>**Ejemplos:** `mty-gdl-1sep1900`
`id`<br>*requerido* | entero positivo | Id de la petición de detalles generado por Reserbus
<aside class="notice">
    En esta estructura se encuentra, dentro de <strong>line</strong>, un 
    <a href="#nested-complex-types">Nested Complex Type</a> 
    llamado <strong>Site</strong>. 
<p> 
    Los detalles de esta estructura estan 
    <a href="#site-redirecciones">aquí</a>.
</p>
</aside>
