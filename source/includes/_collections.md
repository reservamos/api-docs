# Collections

## Obtener un listado de las l&iacute;neas disponibles

```shell
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/lines'
```

> Ejemplo de una respuesta exitosa

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
[
  {
    "name": "Autovías y La Línea",
    "abbr": "autovias-la-linea",
    "human_abbr": "Autovías/La Línea",
    "transporter_name": "Grupo Herradura Occidente",
    "transporter_abbr": "gho",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/1/autovias-la-linea.png"
  },
  {
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
  {
    "name": "Grupo Senda",
    "abbr": "senda-primera",
    "human_abbr": "Senda",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/3/senda-primera.png"
  },
  {
    "name": "Ave",
    "abbr": "ave",
    "human_abbr": "Ave",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/4/ave.png"
  },
  {
    "name": "Tamaulipas",
    "abbr": "tamaulipas",
    "human_abbr": "Tamaulipas",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/5/tamaulipas.png"
  },
  {
    "name": "Turimex Internacional",
    "abbr": "turimex",
    "human_abbr": "Turimex",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/6/turimex.png"
  },
  {
    "name": "Coahuilenses",
    "abbr": "coahuilenses",
    "human_abbr": "Coahuilenses",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/7/coahuilenses.png"
  },
  {
    "name": "Transportes del Norte Diamante",
    "abbr": "tdn-diamante",
    "human_abbr": "TDN Diamante",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/8/tdn-diamante.png"
  },
  {
    "name": "Sendor",
    "abbr": "sendor",
    "human_abbr": "Sendor",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/9/sendor.png"
  },
  {
    "name": "Transportes del Norte",
    "abbr": "tdn",
    "human_abbr": "TDN",
    "transporter_name": "Grupo Senda",
    "transporter_abbr": "senda",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/10/tdn.png"
  },
  {
    "name": "Tufesa Platinum",
    "abbr": "tufesa-platino",
    "human_abbr": "Tufesa Plat.",
    "transporter_name": "Tufesa",
    "transporter_abbr": "tufesa",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/11/tufesa-platino.png"
  },
  {
    "name": "Tufesa Internacional",
    "abbr": "tufesa-internacional",
    "human_abbr": "Tufesa Int.",
    "transporter_name": "Tufesa",
    "transporter_abbr": "tufesa",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/12/tufesa-internacional.png"
  },
  {
    "name": "Tufesa Primera Clase",
    "abbr": "tufesa-primera",
    "human_abbr": "Tufesa P.C.",
    "transporter_name": "Tufesa",
    "transporter_abbr": "tufesa",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/13/tufesa-primera.png"
  },
  {
    "name": "Tufesa Ejecutivo",
    "abbr": "tufesa-ejecutivo",
    "human_abbr": "Tufesa Ejec.",
    "transporter_name": "Tufesa",
    "transporter_abbr": "tufesa",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/14/tufesa-ejecutivo.png"
  },
  {
    "name": "Tufesa High Class",
    "abbr": "tufesa-hc",
    "human_abbr": "Tufesa H.C.",
    "transporter_name": "Tufesa",
    "transporter_abbr": "tufesa",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/15/tufesa-hc.png"
  },
  {
    "name": "Etn",
    "abbr": "etn-lujo",
    "human_abbr": "Etn Lujo",
    "transporter_name": "Grupo Etn-Turistar",
    "transporter_abbr": "etn",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/16/etn-lujo.png"
  },
  {
    "name": "Turistar",
    "abbr": "turistar-lujo",
    "human_abbr": "Turistar Lujo",
    "transporter_name": "Grupo Etn-Turistar",
    "transporter_abbr": "etn",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/17/turistar-lujo.png"
  },
  {
    "name": "Futura Costaline",
    "abbr": "futura",
    "human_abbr": "Futura",
    "transporter_name": "Grupo Aers",
    "transporter_abbr": "aers",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/18/futura.png"
  },
  {
    "name": "Costaline Futura",
    "abbr": "costaline",
    "human_abbr": "Costaline",
    "transporter_name": "Grupo Aers",
    "transporter_abbr": "aers",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/19/costaline.png"
  },
  {
    "name": "Turistar Ejecutivo",
    "abbr": "turistar-ejecutivo",
    "human_abbr": "Turistar Ejecutivo",
    "transporter_name": "Grupo Aers",
    "transporter_abbr": "aers",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/20/turistar-ejecutivo.png"
  },
  {
    "name": "Transpaís",
    "abbr": "transpais",
    "human_abbr": "Transpaís",
    "transporter_name": "Transpaís",
    "transporter_abbr": "trans",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/21/transpais.png"
  },
  {
    "name": "Transpaís Unico",
    "abbr": "unico",
    "human_abbr": "Transpaís Unico",
    "transporter_name": "Transpaís",
    "transporter_abbr": "trans",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/22/unico.png"
  },
  {
    "name": "Transpaís Vista",
    "abbr": "vista",
    "human_abbr": "Transpaís Vista",
    "transporter_name": "Transpaís",
    "transporter_abbr": "trans",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/23/vista.png"
  },
  {
    "name": "Transpaís Mas",
    "abbr": "mas",
    "human_abbr": "Transpaís Mas",
    "transporter_name": "Transpaís",
    "transporter_abbr": "trans",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/24/mas.png"
  },
  {
    "name": "Transpaís Unico Mix",
    "abbr": "unico-mix",
    "human_abbr": "Transpaís Unico Mix",
    "transporter_name": "Transpaís",
    "transporter_abbr": "trans",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/25/unico-mix.png"
  },
  {
    "name": "Autonaves",
    "abbr": "autonaves",
    "human_abbr": "Autonaves",
    "transporter_name": "Grupo Vencedor",
    "transporter_abbr": "vdor",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/26/autonaves.png"
  },
  {
    "name": "Confort",
    "abbr": "confort",
    "human_abbr": "Confort",
    "transporter_name": "Grupo Vencedor",
    "transporter_abbr": "vdor",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/27/confort.png"
  },
  {
    "name": "Norte de Veracruz",
    "abbr": "norte-de-veracruz",
    "human_abbr": "Norte de Veracruz",
    "transporter_name": "Grupo Vencedor",
    "transporter_abbr": "vdor",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/28/norte-de-veracruz.png"
  },
  {
    "name": "Servicio Metropolitano",
    "abbr": "servicio-metropolitano",
    "human_abbr": "Servicio Metropolitano",
    "transporter_name": "Grupo Vencedor",
    "transporter_abbr": "vdor",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/29/servicio-metropolitano.png"
  },
  {
    "name": "Vencedor",
    "abbr": "vencedor",
    "human_abbr": "Vencedor",
    "transporter_name": "Grupo Vencedor",
    "transporter_abbr": "vdor",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/30/vencedor.png"
  },
  {
    "name": "Ovnibus",
    "abbr": "ovnibus",
    "human_abbr": "Ovnibus",
    "transporter_name": "Grupo Valle del Mezquital",
    "transporter_abbr": "gvm",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/31/ovnibus.png"
  },
  {
    "name": "Ovnibus Plus",
    "abbr": "ovnibus-plus",
    "human_abbr": "Ovnibus Plus",
    "transporter_name": "Grupo Valle del Mezquital",
    "transporter_abbr": "gvm",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/32/ovnibus-plus.png"
  },
  {
    "name": "Flecha Roja Zimapan Valles",
    "abbr": "flecha-roja-zimapan-valles",
    "human_abbr": "Flecha",
    "transporter_name": "Grupo Valle del Mezquital",
    "transporter_abbr": "gvm",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/33/flecha-roja-zimapan-valles.png"
  },
  {
    "name": "Tap",
    "abbr": "tap",
    "human_abbr": "Tap",
    "transporter_name": "Grupo Tap",
    "transporter_abbr": "tap",
    "allows_seat_selection": true,
    "volatile_pricing": false,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/34/tap.png"
  },
  {
    "name": "Greyhound",
    "abbr": "greyhound",
    "human_abbr": "Greyhound",
    "transporter_name": "Greyhound",
    "transporter_abbr": "ghound",
    "allows_seat_selection": false,
    "volatile_pricing": true,
    "services": [],
    "commission": 6,
    "logo_url": "https://rsrbs-staging.s3.amazonaws.com/uploads/line/logo/35/greyhound.png"
  }
]
```

### HTTP Request

`GET /lines.json`

## Obtener un listado de ciudades disponibles

```shell
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/cities?q=monterrey&results=1'
```

> Ejemplo de una respuesta exitosa

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
[
   {
      "id":1,
      "name":"Cuatro caminos",
      "slug":"cuatro-caminos",
      "state":"Michoacán",
      "country":"México",
      "to_s":"Cuatro caminos"
   },
   {
      "id":3,
      "name":"Acambaro",
      "slug":"acambaro",
      "state":"Guanajuato",
      "country":"México",
      "to_s":"Acambaro"
   },
   {
      "id":5,
      "name":"Acapulco",
      "slug":"acapulco",
      "state":"Guerrero",
      "country":"México",
      "to_s":"Acapulco"
   }
]
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
      "message": "El formato de 'page' es inválido"
    }
  ]
}
```

### HTTP Request

`GET /cities.json`

### Query Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`q`<br>*opcional* | string | Nombre completo o parcial de la terminal <br>que se quiere buscar.<br>**Ejemplos:** `mon`, `mont`, `monterrey`
`results`<br>*opcional* | entero positivo | Máximo número de resultados a retornar<br>**Ejemplos:** `2`, `3`, `4`
`page`<br>*opcional* | entero positivo | Número de página en base a los resultados <br>solicitados<br>**Ejemplos:** `1`, `2`, `3`
`from`<br>*opcional* | string | Slug de la ciudad o terminal origen para ver <br>sus destinos disponibles. <br>**Ejemplos:** `monterrey`, `guadalajara`,<br> `t-monterrey-central`

## Obtener un listado de terminales disponibles

```shell
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  -H 'Accept: application/json' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/terminals.json?q=monterrey&results=1'
```

> Ejemplo de una respuesta exitosa

```
HTTP/1.1 200 OK
Status: 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
```

```json
[
   {
      "id":2,
      "name":"Terminal de buses",
      "slug":"t-cuatro-caminos",
      "to_s":"Cuatro caminos, Terminal de buses",
      "city":"Cuatro caminos",
      "state":"Michoacán",
      "country":"México"
   },
   {
      "id":4,
      "name":"Terminal de buses",
      "slug":"t-acambaro",
      "to_s":"Acambaro, Terminal de buses",
      "city":"Acambaro",
      "state":"Guanajuato",
      "country":"México"
   },
   {
      "id":6,
      "name":"Terminal de Autobuses Papagayo",
      "slug":"t-acapulco-papagayo",
      "to_s":"Acapulco, Terminal de Autobuses Papagayo",
      "city":"Acapulco",
      "state":"Guerrero",
      "country":"México"
   }
]
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
      "message": "El formato de 'page' es inválido"
    }
  ]
}
```

### HTTP Request

`GET /terminals.json`

### Query Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`q`<br>*opcional* | string | Nombre completo o parcial de la terminal <br>que se quiere buscar.<br>**Ejemplos:** `mon`, `mont`, `monterrey`
`results`<br>*opcional* | entero positivo | Máximo número de resultados a retornar<br>**Ejemplos:** `2`, `3`, `4`
`page`<br>*opcional* | entero positivo | Número de página en base a los resultados <br> solicitados <br>**Ejemplos:** `1`, `2`, `3`
`from`<br>*opcional* | string | Slug de la ciudad o terminal origen para <br>ver sus terminales destino disponibles. <br>**Ejemplos:** `monterrey`, `guadalajara`,<br>`t-monterrey-central`
