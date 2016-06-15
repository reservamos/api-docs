# Price Quote

## Consultar precio que cobrar&aacute; el operador para una compra

```shell
curl -X GET \
  -H 'Authorization: Token token={api_key}' \
  -H 'Content-Type: application/form-data' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/purchases/aCoGqGyiJt8/pricing_quotes.json?general=1&student=2'
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
  "amount": "1038.0",
  "taxes": "0.0",
  "service_fees": "0.0",
  "discounts": "0.0",
  "total": "1038.0",
  "departs": {
    "amount": "519.0",
    "taxes": "0.0",
    "service_fees": "0.0",
    "discount": "0.0",
    "total": "519.0",
    "categories": [
      {
        "category": "general",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      },
      {
        "category": "student",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      },
      {
        "category": "student",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      }
    ]
  },
  "returns": {
    "amount": "519.0",
    "taxes": "0.0",
    "service_fees": "0.0",
    "discount": "0.0",
    "total": "519.0",
    "categories": [
      {
        "category": "general",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      },
      {
        "category": "student",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      },
      {
        "category": "student",
        "amount": "173.0",
        "taxes": "0.0",
        "service_fee": "0.0",
        "discount": "0.0",
        "total": "173.0"
      }
    ]
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
`POST /purchases/{token}/pricing_quotes.json`

### Path Parameters
Nombre | Tipo | Descripción
--- | --- | ---
`token`<br>*requerido* | string | Identificador de la intención de compra <br>**Ejemplos:** `1200a1f06f52441eae140f9264bf4614`, `8199bd21be565cc99ad12ef4f132f739`

### Query Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`general`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
`student`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
`minor`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
`older`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
`teacher`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
`wheelchair_handicap`<br>*opcional* | entero positivo | Categoría usada para consultar su precio tanto en viaje de ida como de vuelta
