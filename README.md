## Ejercicio 1: Sistema de Gestión de un Taller Mecánico

Se requiere modelar un sistema para gestionar las reparaciones de vehículos de un taller mecánico. El sistema debe incluir las siguientes entidades:

### Clase Cliente
* **Atributos:**
  * `dni`
  * `nombre`
  * `telefono`
* **Métodos:**
  * `crear_reparacion()`: inicia una nueva reparación asociada al cliente.

### Clase Reparacion
* **Atributos:**
  * `id_reparacion`
  * `dni_cliente`
  * `fecha`
  * `tareas` (lista de objetos `TareaReparacion`)
* **Métodos:**
  * `agregar_tarea(tarea)`: agrega una tarea a la reparación.
  * `calcular_coste_total()`: suma los costes de todas las tareas.

### Clase TareaReparacion
* **Atributos:**
  * `id_tarea`
  * `descripcion`
  * `coste`
* **Métodos:**
  * `mostrar_info()`: retorna la descripción y el costo.

### Requerimientos de diseño:
* Una `Reparacion` consta de varias `TareaReparacion`.
* Las tareas están asociadas estrictamente a una `Reparacion`. Si esta se elimina, sus tareas deben desaparecer (relación de composición).

---
