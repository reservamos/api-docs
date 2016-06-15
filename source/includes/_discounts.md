# Discounts

## Aplicar un descuento a una compra

```shell
curl -X POST \
  -H 'Authorization: Token token={api_key}' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -d '{ "code": "TEST" }' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/fVJ9_4XNHQg/discounts.json'
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
  "id": 1,
  "percent": "10.0"
}
```

### HTTP Request

`POST /purchases/{token}/discounts.json`

### Path Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Token identificador de la compra

### Body Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`code`<br>*requerido* | string | Código de descuento.  <br>**Ejemplos:** `VIAJAGUANAJUATO`, <br>`SINFILAS`
