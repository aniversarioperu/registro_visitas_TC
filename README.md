# Registro de visita del Tribunal Consitucional peruano

Este repositorio contiene las páginas HTML del registro de visitas.
El objetivo es parsear todos los campos a un archivo JSON (de preferencia
        JSONLINES) para ser incorporados en <http://manolo.rocks>

**Problemas**:

* Si bien el parse puede ser sencillo ya que cada registro está en filas de
tablas HTML, el problema es la falta de consistencia entre la mayoría de
páginas.
* Un set de reglas para parsear ciertas páginas no necesariamente servirán para
parsear otras.
* Los patrones del registro se mantienen constantes en fechas cercanas entre
sí. Pero pueden ser radicalmente diferentes en ciertas páginas para un mismo
año, o un mismo mes.
* Para asegurarse que todos los registros son parseados con un mínimo margen de
error será necesario avanzar de a pocos hasta terminar de parsear todas las
hojas HTML.

## JSON
La idea es que se generen un archivo JSON con estos mismos campos:

```javascript
{
  "date" : "2005-07-15",
  "time_end" : "17:13",
  "time_start" : "16:17",
  "full_name" : "Carlos  Rocha",
  "id_document" : "DNI",
  "id_number" : "07556056",
  "host_name" : "Silsa",
  "reason" : "",
  "entity" : "",
  "location" : "",
  "institution" : "Tribunal Constitucional"
}
```

