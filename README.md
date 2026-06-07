## Ejercicio 2: Sistema de Reservas de un Hotel

Un hotel necesita estructurar la información de sus habitaciones y reservas. 

### Clase Habitacion
* **Atributos:** 
  * `numero_habitacion`
  * `capacidad`
  * `precio_noche_persona`

### Clase Reserva
* **Atributos:** 
  * `habitacion` (objeto de tipo Habitacion)
  * `nombre_huesped`
  * `numero_noches`
  * `numero_huespedes`
  * `coste_estancia`
* **Cálculo de coste:** La propiedad `coste_estancia` debe ser calculada de manera dinámica como:
  `coste_estancia = (habitacion.precio_noche_persona * numero_huespedes) * numero_noches`


### Requerimientos de diseño:
Además del constructor normal, se debe implementar un constructor alternativo: `Reserva.crear_desde_dict(data_dict)`, que permita instanciar una reserva a partir de un diccionario con la siguiente estructura:

```json
{ 
  "numero_habitacion": 423, 
  "capacidad_personas": 2, 
  "precio_noche_persona": 50, 
  "nombre_huesped": "Ana Gómez", 
  "numero_noches": 4, 
  "numero_huespedes": 2 
} 
```
Este método de clase debe encargarse de crear el objeto `Habitacion` pertinente y, posteriormente, crear y retornar el nuevo objeto `Reserva` asociado a dicha habitación.

---
