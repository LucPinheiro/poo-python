## Ejercicio 3: Empresa de Alquiler de Vehículos

Implementar un sistema de gestión de datos para una empresa de alquiler. El sistema almacenará información sobre `Cliente`, `Vehiculo` y `Alquiler`.

### Requisitos de la clase Cliente
* **Atributos:** `nombre`, `dni`, `telefono`.
* El `dni` de los clientes debe ser de uso interno. Todas las consultas y modificaciones desde el exterior deben realizarse tratándolo como una propiedad (`@property`).
* Debe existir un método que devuelva una cadena de texto con la representación completa de los datos del cliente.
* Se deben poder comparar clientes utilizando operadores lógicos, considerándose iguales (`==`) si comparten el mismo `dni`.

### Requisitos de la Clase Vehiculo
* **Atributos:** `marca`, `modelo`, `matricula`, `precio_por_dia`.
* Al crear el vehículo o modificar su precio, no se permitirá un valor negativo. En caso de que se introduzca un número menor que 0, se almacenará automáticamente un `0`.
* Debe existir un método que devuelva la información del vehículo formateada de la siguiente forma exacta:  
  `"Vehículo(Seat Ibiza, 1111AAA, 25€)"`
* Implementar un método que determine mediante operadores lógicos si un vehículo es mayor que otro (`>`) basándose en si su precio por día es superior.

### Requisitos de la Clase Alquiler
* **Atributos:** `cliente`, `vehiculo`, `dias_alquiler`, `coste_total`.
* El `coste_total` será una propiedad calculada automáticamente a partir de los atributos `precio_por_dia` del vehículo y `dias_alquiler`.
* No se permitirán alquileres con días menores que 0. En caso de introducir un número negativo, se almacenará un `0`.
* Un método debe devolver una cadena de texto que unifique los datos del cliente, del vehículo y el coste total del alquiler.
* Sobrecargar el operador suma (`+`). Al sumar dos alquileres que pertenezcan al **mismo cliente** y al **mismo vehículo**, debe retornar un objeto `Alquiler` nuevo con los costes totales y los días de alquiler sumados. Este método debe lanzar una validación y solo funcionar si se cumple la condición del mismo cliente.
