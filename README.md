# CalculoFechas
**Ejemplo en *Javascript* para calcular fechas de una manera sencilla**

```javascript
var tiempoCalculado;

var fechaActual = new Date().getTime();
var fecha = fecha.getTime();
var milisTotal = fechaActual - fecha;

var aniosCalculados;
var mesesCalculados;
var diasCalculados;

var aniosCalculados = Math.floor(milisTotal / 1000 / 60 / 60 / 24 / 365.25);

mesesCalculados = Math.floor((milisTotal / 1000 / 60 / 60 / 24) % (365.25/30.42));

diasCalculados = Math.floor(milisTotal / 1000 / 60 / 60 / 24) % (365.25/12);

tiempoCalculado = aniosCalculados + " años, " + mesesCalculados + " meses y " + diasCalculados + " días";

return tiempoCalculado;
```
