# Ticket Requests

## Crear boletos bloqueados asociados a una compra

```shell
curl -X POST \
  -H 'Authorization: Token token={api_key}' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -d '{
  "trip_slug": "mex-qro-30sep150715-239-2",
  "tickets": [
    {
      "first_name": "Adrian",
      "last_name": "Cuadros",
      "gender": "m",
      "category": "general",
      "seat": "17"
     },
     {
       "first_name": "Erika",
       "last_name": "Cuadros",
       "gender": "f",
       "category": "general",
       "seat": "18"
      },
      {
        "first_name": "Luciana",
        "last_name": "Cuadros",
        "gender": "f",
        "category": "minor",
        "seat": "19"
       }
    ]
}' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8/ticket_requests.json'
```

> Ejemplo de una respuesta

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "id": 993,
  "state": "pending_lock",
  "created_at": "2015-09-28 16:39:37 -0500",
  "errors": {},
  "poll_to": "/api/v1/purchases/aCoGqGyiJt8/ticket_requests/991"
}
```

> Ejemplo de un error

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
      "message": "Asiento no puede estar en blanco"
    }
  ]
}
```

### HTTP Request

`POST /purchases/{token}/ticket_requests`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Identificador de la intención de compra <br>**Ejemplos:** `1200a1f06f52441eae140f9264bf4614`, `8199bd21be565cc99ad12ef4f132f739`

### Body Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`trip_slug`<br>*requerido* | string | Identificador (slug) del viaje de salida.  <br>**Ejemplos:** `mty-gdl-9sep0700`,<br>`mex-gdl-9sep2320`
`tickets`<br>*requerido*<br>*(al menos 1)* | array | Boletos a bloquear

Nombre | Tipo | Descripción
--- | --- | ---
`first_name`<br>*requerido* | string | Primer nombre del pasajero <br>**Ejemplos:** `Andres`, `Elias`
`last_name`<br>*requerido* | string | Apellido del pasajero<br>**Ejemplos:** `Sucre`, `Matheus`
`category`<br>*requerido* | string | Categoría del pasajero<br>(De las disponibles en el viaje) <br>**Ejemplos:** `general`, `minor`, `student`
`gender`<br>*opcional* | string | Género del pasajero en código de un caracter<br>(`m` o `f`)
`seat`<br>*requerido* | string | Identificador de asiento elegido para el pasajero <br>**Ejemplos:** `20`, `10`, `6`

## Consultar estado de una petici&oacute;n de bloqueo de asientos

```shell
curl -X GET \
  -H 'Authorization: Token token={api_key}' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8/ticket_requests/990.json'
```

> Ejemplo de una respuesta

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "id": 993,
  "state": "finished",
  "created_at": "2015-09-28 17:08:41 -0500",
  "errors": {},
  "tickets": [
    {
      "id": 1216,
      "state": "locked",
      "first_name": "Adrian",
      "last_name": "Cuadros",
      "gender": "m",
      "category": "general",
      "seat": "17",
      "amount": "173.0",
      "taxes": "0.0",
      "total": "173.0"
    },
    {
      "id": 1217,
      "state": "locked",
      "first_name": "Erika",
      "last_name": "Cuadros",
      "gender": "f",
      "category": "general",
      "seat": "18",
      "amount": "173.0",
      "taxes": "0.0",
      "total": "173.0"
    },
    {
      "id": 1218,
      "state": "locked",
      "first_name": "Luciana",
      "last_name": "Cuadros",
      "gender": "f",
      "category": "minor",
      "seat": "19",
      "amount": "87.0",
      "taxes": "0.0",
      "total": "87.0"
    }
  ]
}
```

> Ejemplo de un error

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
{
  "id": 990,
  "state": "failed",
  "created_at": "2015-09-28 16:21:56 -0500",
  "errors": {
    "state": [
      "occupied:El asiento que elegiste está ocupado. Por favor elige un asiento diferente"
    ]
  }
}
```

### HTTP Request

`GET /purchases/{token}/ticket_requests/{id}`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Identificador de la intención de compra <br>**Ejemplos:** `1200a1f06f52441eae140f9264bf4614`, `8199bd21be565cc99ad12ef4f132f739`
`id`<br>*requerido* | entero positivo | Identificador de la petición de bloqueo de asientos <br> generado por Reserbus <br>**Ejemplos:** `1`, `2`
