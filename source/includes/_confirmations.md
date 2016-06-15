# Confirmation Requests

## Generar una petici&oacute;n para confirmar la compra y generar los boletos

```shell
curl -X POST \
  -H 'Authorization: Token token={api_key}' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8/confirmation_requests.json'
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
  "id": 70,
  "created_at": "2015-09-28T17:19:26.684-05:00"
}
```

### HTTP Request

`POST /purchases/{token}/confirmation_requests.json`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Token identificador de la compra

## Consultar estado de la petici&oacute;n de confirmaci&oacute;n

```shell
curl -X GET \
  -H 'Authorization: Token token={api_key}' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8/confirmation_requests/70.json'
```

```json
{
   "id":1,
   "created_at":"2014-10-17T12:22:52.250-05:00",
   "purchase":{
      "token":"4016e4e0f75f36e3129ea7b3062de69b",
      "state":"completed",
      "departs":{
         "state":"completed",
         "trip_slug":"mty-gdl-18oct2300",
         "amount":0,
         "taxes":0,
         "total":0,
         "ticket_pdf_url":"https://rsrbs-staging.s3.amazonaws.com/tickets/4016e4e0f75f36e3129ea7b3062de69b/66/tickets.pdf",
         "tickets":[
            {
               "state":"payed",
               "first_name":"Adrian",
               "last_name":"Cuadros",
               "gender":"m",
               "category":"general",
               "seat":"11",
               "amount":"875.0",
               "taxes":"0.0",
               "total":"875.0"
            }
         ],
         "line":{
            "name":"Omnibus de México Servicio Plus",
            "abbr":"odm-plus",
            "human_abbr":"ODM Plus",
            "transporter_name":"Omnibus de Mexico",
            "transporter_abbr":"odm"
         }
      },
      "amount":0,
      "taxes":0,
      "total":0,
      "expires_at":"2014-10-17 12:08:19 -0500"
   },
   "state":"finished"
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
  "id": 70,
  "created_at": "2015-09-28T17:19:26.684-05:00",
  "state": "failed_reservation"
}
```

### HTTP Request

`GET /purchases/{token}/confirmation_requests/{id}`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Token identificador de la compra
`id`<br>*requerido* | integer | Id de la petición de confirmación generado por Reserbus
