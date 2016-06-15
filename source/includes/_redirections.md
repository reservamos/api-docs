# Redirections

## Redirigir a proveedor

Un url el cual puedas visitar y te redirija automáticamente a la página de proveedor

```bash
curl -X GET \
  -H 'Authorization: Token token=f986373f694ffdf9cfbae45ba23f3d8c' \
  'http://reserbus-sandbox.herokuapp.com/api/v1/redirect?
     departure=men-aca-20mar161800-50443-20
     &return=aca-men-21mar161800-50443-20
     &type=desktop
     &general=1
     &student=3'
```

### Query Parameters

Nombre | Tipo | Descripción
--- | --- | ---
`departure`<br> | String | Slug del viaje de vuelta
`return`<br>*opcional* | String | Slug del viaje de vuelta
`type`<br> | String | Tipo de sitio al cual redigirir. Puede ser desktop o mobile
`general`<br>*opcional* | entero positivo | Cantidad de pasajeros adultos
`student`<br>*opcional* | entero positivo | Cantidad de pasajeros estudiantes
`minor`<br>*opcional* | entero positivo | Cantidad de pasajeros menores
`older`<br>*opcional* | entero positivo | Cantidad de pasajeros mayores
`teacher`<br>*opcional* | entero positivo | Cantidad de pasajeros profesores
