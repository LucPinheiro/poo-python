## Ejercicio 4: Sistema de Gestión de Comercio Electrónico

Se desea desarrollar un sistema orientado a objetos para la gestión de productos en una plataforma de comercio electrónico.

### Clase Producto
Representa cualquier artículo disponible en la plataforma. Contiene dos atributos públicos: `nombre` y `precio`. Se debe modificar para cumplir con:
* **Atributo privado:** Añadir `referencia`, el cual debe ser tratado como propiedad (`@property`).
* **Atributo de clase:** Añadir un atributo denominado `iva`, cuyo valor sea común a todos los productos creados.
* **Método `modificar_precio`:** Permite actualizar el coste base. Se debe verificar tanto en este método como en el constructor que el valor asignado al precio sea siempre positivo; en caso contrario, debe lanzarse una excepción (`ValueError`).
* **Método estático `calcular_precio_iva`:** Recibe como parámetro el precio base y devuelve el precio final calculado aplicando el IVA correspondiente. Este método no debe acceder a atributos de instancia.

### Clase Inventariable
Su finalidad es proporcionar funcionalidad relacionada con la gestión de stock.
* Almacena el atributo `cantidad` disponible.
* **Método estático:** Debe incluir un método que valide si la cantidad de stock es válida (es decir, que no sea negativa).

### Clase ArticuloBazar (Herencia Múltiple)
Debe heredar simultáneamente de la clase `Producto` y de la clase `Inventariable`.
* **Atributos propios:** Añadir `tamano` y `subcategoria`.
* **Constructor:** Debe inicializar correctamente todos los atributos heredados y los propios utilizando de forma adecuada la herencia múltiple.
* **Constructores alternativos:** Implementar dos formas adicionales de instanciar la clase:
  1. Un constructor por defecto (valores predeterminados).
  2. Un constructor basado en factoría que permita crear una instancia a partir de un diccionario que contenga los datos necesarios.

### Demostración y Pruebas
Se debe demostrar el funcionamiento del sistema creando al menos una instancia válida de `ArticuloBazar` a partir de cada uno de los constructores implementados. Se deben probar los métodos desarrollados y gestionar correctamente los bloques `try-except` en caso de que se produzcan excepciones debido a datos inválidos (como precios negativos).
