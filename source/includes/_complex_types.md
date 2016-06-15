# Nested Complex types

Un *Nested Complex Type* es una entidad que encuentra anidada en diferentes respuestas del API.


## Site (Redirecciones)

```json
{
  "mobile": {
    "allow_deep_link": false,
    "can_buy_mobile": false,
    "desktop_screenshot":"https://www.reserbus.mx/screenshots/geb-futura-view.png",
    "mobile_screenshot":"https://www.reserbus.mx/screenshots/geb-futura-view-mobile.png",
    "responsive": false,
    "short_url": "FUTURA.com.mx",
    "url": "https://www.futura.com.mx",
    "needs_passenger": false
  },
  "desktop": {
    "allow_deep_link": false,
    "can_buy_mobile": false,
    "desktop_screenshot":"https://www.reserbus.mx/screenshots/geb-view.png",
    "mobile_screenshot":"https://www.reserbus.mx/screenshots/geb-view-mobile.png",
    "responsive": false,
    "short_url": "ESTRELLABLANCA.com.mx",
    "url": "https://www.estrellablanca.com.mx",
    "needs_passenger": false
  }
}
```

Un *Site* representa los sitios Web de una l&iacute;nea externa a los que se redirige al usuario cuando desea comprar.  

Un usuario puede ser redireccionado a distintos sitios dependiendo de si esta en *desktop* o en *mobile*.

Cuando una l&iacute;nea es aliada, el site es `null` ya que no hace falta realizar redireccip&oacute;n.

### Atributos

Dentro de cada tipo de sitio, se pueden encontrar los siguentes atributos: 

Nombre | Tipo | Descripcion 
-------|------|-------------
`allow_deep_link` |  Booleano | Permite saber si la redireccion va a ser hacia la p&aacute;gina de resultado.
`can_buy_mobile` | Booleano | Muestra si es posible realizar compras desde m&oacute;vil en ese sitio.
`desktop_screenshot` | String | Url con la imagen que representa el sitio en desktop 
`mobile_screenshot` | String | Url con la imagen que representa el sitio desde m&oacute;vil
`responsive` | Booleano | Permite saber si el sitio se adapta a distintos dispositivos de manera cómoda
`short_url` | String | Representa la abreviaci&oacute;n del sitio que se debe colocar en caso que no se pueda usar el logo de la l&iacute;nea.
`url` | String | La url del sitio
`needs_passengers` |  Booleano | Permite saber si, para realizar la redirecci&oacute;n, el sitio necesita tener informaci&oacute;n del n&uacute;mero de pasajeros del viaje.

