# CalculoFechas
**Ejemplo en *Javascript* para calcular edades de una manera sencilla**

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

**Ejemplo en *Java* para calcular edades. *¡OJO! Es necesario tener Java8* **
```java
public String calcularEdad(String fechaDeNacimiento){
  
  LocalDate today = LocalDate.now();

  LocalDate birthday = LocalDate.parse(fechaDeNacimiento);
  Period age = Period.between(birthday, today);

  /*Optional format*/
  DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd/LLLL/yy");
  String formattedBirthday = birthday.format(formatter);
  /****************/
  
  String message = "Tu fecha de nacimiento es" + formattedBirthday + " y tienes " + age + "años";
  
  return message;
}
````
