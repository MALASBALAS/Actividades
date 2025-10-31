# Comunicación entre Actividades – Android



Proyecto que muestra cómo enviar datos entre dos actividades mediante Intent y putExtra().



## Funcionamiento



### MainActivity



Solicita nombre, edad y localidad al usuario.



Valida los campos y muestra un aviso si hay alguno vacío.



Envía los datos a SegundaActivity:

```kotlin

val intent = Intent(this, SegundaActivity::class.java)

intent.putExtra("id", nombre)

intent.putExtra("edad", edad)

intent.putExtra("localidad", localidad)

startActivity(intent)

```



Muestra un Toast con la información introducida.



### SegundaActivity



Recibe los valores con intent.extras y los muestra en tres TextView.



Muestra también un Toast con los datos recibidos.



Incluye un botón para volver a la primera actividad.



## Conceptos usados



Intent explícitos



putExtra() y getExtras()



Toast.makeText()



OnFocusChangeListener



Validación de campos

