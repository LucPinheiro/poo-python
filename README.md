# POO: Programación Orientada a Objectos
Este repositorio está diseñado para recopilar y resolver ejercicios avanzados de **Programación Orientada a Objetos (POO)** en Python, basados en supuestos y exámenes oficiales de desarrollo de software.

## 🛠️ Estructura del Proyecto

Para mantener el código limpio, desacoplado y seguir las mejores prácticas de control de versiones con Git, **cada ejercicio se encuentra desarrollado en su propia rama independiente**. 

Puedes explorar las soluciones completas cambiando a las siguientes ramas:

*   **`ejercicio_1_taller`**: Modelado de un sistema de reparaciones y tareas para un taller mecánico (conceptos de composición y relaciones estructurales).
*   **`ejercicio_2_hotel`**: Gestión de estancias y reservas hoteleras con implementación de constructores alternativos (`@classmethod`) mediante diccionarios de datos.
*   **`ejercicio_3_alquiler`**: Sistema de alquiler de vehículos enfocado en encapsulamiento estricto (`@property`), validación de datos y sobrecarga de operadores nativos (`__add__`, `__gt__`).
*   **`ejercicio_4_comercio_electronico`**: Plataforma de e-commerce que implementa herencia múltiple, atributos de clase, métodos estáticos y control robusto de excepciones.
*   **`ejercicio_5_parque_tematico_ficheros`**: Aplicación integral con clases abstractas (`abc.ABC`), validación avanzada de datos y persistencia en múltiples formatos de disco planos y estructurados (`.txt`, `.json`, `.xml`).

---
## 📁 Vista de Archivos por Rama

Cada rama contiene una estructura de archivos limpia enfocada en su lógica de negocio:

* **[poo-python/ (Rama: main)](../../tree/main)**
  * `README.md` # Enunciado general y guía del repositorio

* **[poo-python/ (Rama: ejercicio_1_taller)](../../tree/ejercicio_1_taller)**
  * `taller_mechanico.py` # Clases Cliente, Reparacion y TareaReparacion

* **[poo-python/ (Rama: ejercicio_2_hotel)](../../tree/ejercicio_2_hotel)**
  * `gestion_hotel.py` # Factoría de reservas desde diccionarios

* **[poo-python/ (Rama: ejercicio_3_alquiler)](../../tree/ejercicio_3_alquiler)**
  * `alquiler_vehiculos.py` # Propiedades encapsuladas y sobrecarga de operadores

* **[poo-python/ (Rama: ejercicio_4_comercio_electronico)](../../tree/ejercicio_4_comercio_electronico)**
  * `comercio_electronico.py` # Herencia múltiple y métodos estáticos

* **[poo-python/ (Rama: ejercicio_5_parque_tematico_ficheros)](../../tree/ejercicio_5_parque_tematico_ficheros)**
  * `parque_tematico.py` # Clases abstractas y lógica del sistema principal
  * `jornada.txt` # Informe diario de ingresos en texto plano
  * `atracciones.json` # Serialización estructurada de datos del parque
  * `atracciones.xml` # Volcado jerárquico del estado de las atracciones

```


## 🚀 Cómo Clonar y Navegar por el Repositorio

1. **Clona el repositorio** localmente en tu máquina:
   ```bash
   git clone https://github.com
   cd poo-python
   ```

2. **Lista todas las ramas** disponibles para verificar las soluciones:
   ```bash
   git branch -a
   ```

3. **Salta a la rama del ejercicio** que desees revisar o ejecutar (por ejemplo, el ejercicio 5):
   ```bash
   git checkout ejercicio_5_parque_tematico_ficheros
   ```

