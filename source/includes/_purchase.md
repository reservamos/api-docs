# Purchases

## Crear un intento de compra

```shell
curl -X POST \
  -H 'Authorization: Token token={api_key}' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -d '{ "departs": "mex-qro-30sep150715-239-2", "returns": "qro-mex-1oct150400-395-2"}' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases.json'
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
  "token": "aCoGqGyiJt8",
  "state": "attempt",
  "expires_at": "2015-09-28 15:00:22 -0500",
  "purchaser_first_name": null,
  "purchaser_last_name": null,
  "email": null,
  "phone": null,
  "wants_insurance": true,
  "available_payments": [
    "credit_card",
    "paypal"
  ],
  "departs": {
    "id": 539,
    "state": "attempt",
    "trip_slug": "mex-qro-30sep150715-239-2",
    "discounts": [],
    "tickets": [],
    "trip": {
      "id": 3592,
      "slug": "mex-qro-30sep150715-239-2",
      "key": "239",
      "price": 173,
      "regular_price": 173,
      "open": true,
      "service": "Primera",
      "capacity": 32,
      "created_at": "2015-09-15T15:26:49.840-05:00",
      "updated_at": "2015-09-28T11:05:52.026-05:00",
      "departure": {
        "to_s": "2015-09-30T07:15:00",
        "date": "Miércoles, 30 de Septiembre",
        "hours": "07:15 AM",
        "uts": 1443615300
      },
      "arrival": {
        "to_s": "2015-09-30T10:10:00",
        "date": "Miércoles, 30 de Septiembre",
        "hours": "10:10 AM",
        "uts": 1443625800
      },
      "discounts": [],
      "available_all": 30,
      "stopovers": "0",
      "origin": {
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
      "destination": {
        "id": 31,
        "terminal": "Terminal de Autobuses",
        "city": "Santiago de Querétaro",
        "code": "QRO",
        "slug": "t-santiago-de-queretaro-terminal",
        "coordinates": null
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
          "category": "general",
          "amount": "173.0",
          "taxes": "0.0",
          "total": "173.0",
          "availability": 30
        },
        {
          "category": "minor",
          "amount": "87.0",
          "taxes": "0.0",
          "total": "87.0",
          "availability": 12
        },
        {
          "category": "special",
          "amount": "87.0",
          "taxes": "0.0",
          "total": "87.0",
          "availability": 2
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
  },
  "returns": {
    "id": 540,
    "state": "attempt",
    "trip_slug": "qro-mex-1oct150400-395-2",
    "discounts": [],
    "tickets": [],
    "trip": {
      "id": 4430,
      "slug": "qro-mex-1oct150400-395-2",
      "key": "395",
      "price": 173,
      "regular_price": 173,
      "open": true,
      "service": "Primera",
      "capacity": 30,
      "created_at": "2015-09-28T11:05:49.900-05:00",
      "updated_at": "2015-09-28T11:05:49.900-05:00",
      "departure": {
        "to_s": "2015-10-01T04:00:00",
        "date": "Jueves, 01 de Octubre",
        "hours": "04:00 AM",
        "uts": 1443690000
      },
      "arrival": {
        "to_s": "2015-10-01T06:55:00",
        "date": "Jueves, 01 de Octubre",
        "hours": "06:55 AM",
        "uts": 1443700500
      },
      "discounts": [],
      "available_all": 30,
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
            "logo":"https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/4/primera-plus.png",
            "url":"https://www.primeraplus.com.mx",
            "mobile_screenshot":"https://www.reserbus.mx/screenshots/gfa-view-mobile.png",
            "desktop_screenshot":"https://www.reserbus.mx/screenshots/gfa-view.png",
            "responsive":true,
            "can_buy_mobile":true,
            "allow_deep_link":false,
            "short_url":"PRIMERAPLUS.com.mx"
          },
          "desktop": {
            "logo":"https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/4/primera-plus.png",
            "url":"https://www.primeraplus.com.mx",
            "mobile_screenshot":"https://www.reserbus.mx/screenshots/gfa-view-mobile.png",
            "desktop_screenshot":"https://www.reserbus.mx/screenshots/gfa-view.png",
            "responsive":true,
            "can_buy_mobile":true,
            "allow_deep_link":false,
            "short_url":"PRIMERAPLUS.com.mx"
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
          "category": "special",
          "amount": "87.0",
          "taxes": "0.0",
          "total": "87.0",
          "availability": 0
        },
        {
          "category": "general",
          "amount": "173.0",
          "taxes": "0.0",
          "total": "173.0",
          "availability": 30
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
  },
  "passengers": []
}
```

> Ejemplo de error

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
      "message": "Tu viaje de vuelta no puede ser antes de tu viaje de ida"
    }
  ]
}
```

### HTTP Request

`POST /purchases.json`

### Body Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`departs`<br>*requerido* | string | Identificador (slug) del viaje de salida.  <br>**Ejemplos:** `mty-gdl-9sep0700`, <br>`mex-gdl-9sep2320`
`returns`<br>*opcional* | string | Identificador (slug) del viaje de regreso.  <br>**Ejemplos:** `gdl-mty-16sep0700`, <br> `gdl-mex-17sep2200`
`client_key`<br>*opcional* | string | Código con el que identifiques esta compra<br> en tu sistema. <br>**Ejemplos:** `31000`, `I898723ZQ3`

<aside class="notice">
    En esta estructura se encuentra, dentro de <strong>line</strong>, un 
    <a href="#nested-complex-types">Nested Complex Type</a> 
    llamado <strong>Site</strong>. 
<p> 
    Los detalles de esta estructura estan 
    <a href="#site-redirecciones">aquí</a>.
</p>
</aside>
## Ver detalle de una compra

```shell
curl -X GET \
  -H 'Authorization: Token token={api_key}' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8.json'
```

> Ejemplo de respuesta

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "token": "fVJ9_4XNHQg",
  "state": "attempt",
  "expires_at": "2015-12-15 17:34:54 -0600",
  "purchaser_first_name": "Adrian",
  "purchaser_last_name": "Cuadros",
  "email": "adrian@reserbus.com",
  "phone": "8114175678",
  "wants_insurance": true,
  "available_payments": [
    "credit_card",
    "paypal",
    "store",
    "deposit"
  ],
  "qualifies_for_insurance": true,
  "amount": "280.0",
  "taxes": "0.0",
  "extras": "9.28",
  "total": "289.28",
  "discount_amount": 0,
  "departs": {
    "id": 1914,
    "state": "locked_seats",
    "trip_slug": "mex-qro-18dic150450-935-2",
    "amount": "280.0",
    "taxes": "0.0",
    "service_fees": "0.0",
    "total": "280.0",
    "tickets": [
      {
        "id": 3390,
        "state": "locked",
        "first_name": "Adrian",
        "last_name": "Cuadros",
        "gender": "m",
        "category": "general",
        "seat": "1",
        "amount": "280.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "total": "280.0"
      }
    ],
    "trip": {
      "id": 11292,
      "slug": "mex-qro-18dic150450-935-2",
      "key": "935",
      "price": 280,
      "regular_price": 280,
      "open": true,
      "service": "Primera",
      "capacity": 34,
      "created_at": "2015-12-08T12:31:09.110-06:00",
      "updated_at": "2015-12-15T17:20:57.313-06:00",
      "departure": {
        "to_s": "2015-12-18T04:50:00",
        "date": "Viernes, 18 de Diciembre",
        "hours": "04:50 AM",
        "uts": 1450435800
      },
      "arrival": {
        "to_s": "2015-12-18T07:45:00",
        "date": "Viernes, 18 de Diciembre",
        "hours": "07:45 AM",
        "uts": 1450446300
      },
      "discounts": [],
      "available_all": 34,
      "stopovers": "0",
      "product_id": "ciudad-de-mexico_santiago-de-queretaro",
      "origin": {
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
      "destination": {
        "id": 31,
        "terminal": "Terminal de Autobuses",
        "city": "Santiago de Querétaro",
        "code": "QRO",
        "slug": "t-santiago-de-queretaro-terminal",
        "coordinates": null
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
        "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/2/primera-plus.png"
      },
      "categories": [
        {
          "category": "minor",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 12
        },
        {
          "category": "special",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 2
        },
        {
          "category": "general",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 34
        },
        {
          "category": "older",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 2
        },
        {
          "category": "teacher",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 0
        },
        {
          "category": "student",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 0
        }
      ]
    }
  },
  "passengers": [
    {
      "id": 1397,
      "name": "Adrian Cuadros",
      "first_name": "Adrian",
      "last_name": "Cuadros",
      "category": "general",
      "gender": "m"
    }
  ],
  "discount": null
}
```

> Ejemplo de respuesta con descuento

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "token": "fVJ9_4XNHQg",
  "state": "attempt",
  "expires_at": "2015-12-15 17:34:54 -0600",
  "purchaser_first_name": "Adrian",
  "purchaser_last_name": "Cuadros",
  "email": "adrian@reserbus.com",
  "phone": "8114175678",
  "wants_insurance": true,
  "available_payments": [
    "credit_card",
    "paypal",
    "store",
    "deposit"
  ],
  "qualifies_for_insurance": true,
  "amount": "280.0",
  "taxes": "0.0",
  "extras": "9.28",
  "total": "260.352",
  "discount_amount": "28.928",
  "departs": {
    "id": 1914,
    "state": "locked_seats",
    "trip_slug": "mex-qro-18dic150450-935-2",
    "amount": "280.0",
    "taxes": "0.0",
    "service_fees": "0.0",
    "total": "280.0",
    "tickets": [
      {
        "id": 3390,
        "state": "locked",
        "first_name": "Adrian",
        "last_name": "Cuadros",
        "gender": "m",
        "category": "general",
        "seat": "1",
        "amount": "280.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "total": "280.0"
      }
    ],
    "trip": {
      "id": 11292,
      "slug": "mex-qro-18dic150450-935-2",
      "key": "935",
      "price": 280,
      "regular_price": 280,
      "open": true,
      "service": "Primera",
      "capacity": 34,
      "created_at": "2015-12-08T12:31:09.110-06:00",
      "updated_at": "2015-12-15T17:20:57.313-06:00",
      "departure": {
        "to_s": "2015-12-18T04:50:00",
        "date": "Viernes, 18 de Diciembre",
        "hours": "04:50 AM",
        "uts": 1450435800
      },
      "arrival": {
        "to_s": "2015-12-18T07:45:00",
        "date": "Viernes, 18 de Diciembre",
        "hours": "07:45 AM",
        "uts": 1450446300
      },
      "discounts": [],
      "available_all": 34,
      "stopovers": "0",
      "product_id": "ciudad-de-mexico_santiago-de-queretaro",
      "origin": {
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
      "destination": {
        "id": 31,
        "terminal": "Terminal de Autobuses",
        "city": "Santiago de Querétaro",
        "code": "QRO",
        "slug": "t-santiago-de-queretaro-terminal",
        "coordinates": null
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
        "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/2/primera-plus.png"
      },
      "categories": [
        {
          "category": "minor",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 12
        },
        {
          "category": "special",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 2
        },
        {
          "category": "general",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 34
        },
        {
          "category": "older",
          "amount": "140.0",
          "taxes": "0.0",
          "total": "140.0",
          "availability": 2
        },
        {
          "category": "teacher",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 0
        },
        {
          "category": "student",
          "amount": "280.0",
          "taxes": "0.0",
          "total": "280.0",
          "availability": 0
        }
      ]
    }
  },
  "passengers": [
    {
      "id": 1397,
      "name": "Adrian Cuadros",
      "first_name": "Adrian",
      "last_name": "Cuadros",
      "category": "general",
      "gender": "m"
    }
  ],
  "discount": {
    "id": 1,
    "percent": "10.0"
  }
}
```

> Ejemplo de error

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

`GET /purchases/{token}.json`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Token identificador de la compra

