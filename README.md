## Ejercicio 5: Sistema de Gestión de un Parque Temático (Objetos, Ficheros y XML)

Un parque temático desea desarrollar una aplicación para gestionar sus atracciones, controlar la actividad diaria del parque y almacenar la información generada en distintos formatos (.txt, .json, .xml).

### Apartado A: Clase Abstracta Base
Crear una clase abstracta denominada **Atraccion**.

* **Atributos de clase:**
  * `iva`
  * `total_atracciones`
* **Atributos de instancia:**
  * `cod_id`, `nombre`, `ubicacion`, `capacidad_maxima`, `visit_jornada`, `precio_medio`, `estado`

El constructor debe inicializar todos los atributos y actualizar automáticamente el número total de atracciones creadas. 

**Métodos abstractos obligatorios:**
* `calcular_ingreso()`
* `mostrar_resumen()`

**Método de clase:** Implementar un `@classmethod` que permita modificar el IVA aplicado de forma global a todas las atracciones.

### Apartado B: Clases Derivadas
Crear las siguientes clases que hereden de `Atraccion` e implementen sus métodos abstractos:

1. **MontañaRusa:** Atributos específicos `velocidad_max`, `altura_max`, `num_vagones`.
2. **CasaDelTerror:** Atributos específicos `nivel_susto`, `inten_sonora`, `duracion_recorrido`.
3. **SimuladorVR:** Atributos específicos `tipo_experiencia`, `num_cab`, `duracion_sesion`.

### Apartado C: Validaciones con Propiedades
Implementar filtros de encapsulamiento mediante `@property` y `@setter`. Debe lanzarse una excepción `ValueError` si:
* `capacidad_maxima` es menor o igual a cero.
* `precio_medio` es menor o igual a cero.
* `num_cab` es menor o igual a cero.
* `inten_sonora` no está comprendida de forma inclusiva entre 1 y 5.

### Apartado D: Cálculo de Ingresos Diarios
El ingreso de una atracción se calculará mediante la fórmula: 
\[\text{ingresos} = \text{visit\_jornada} \times \text{precio\_medio}\]
Las clases hijas deberán reutilizar el comportamiento común de la clase padre mediante el uso de `super()`.

### Apartado E: Exportación a Texto Plano (.txt)
Utilizando la librería `pathlib` y el módulo `datetime`, generar el fichero `jornada.txt`. 
* La primera línea contendrá la fecha actual del sistema.
* Las siguientes líneas listarán el código, nombre, visitantes e ingresos de cada atracción.
* La última línea mostrará el sumatorio de ingresos totales del parque.

*Ejemplo de salida:*
```text
Fecha: 07/06/2026
MR01 - Montaña Rusa - 150 visitantes - 1200 €
CT01 - Casa del Terror - 90 visitantes - 675 €
VR01 - Simulador VR - 120 visitantes - 1380 €
Ingresos Totales del Parque: 3255 €
```

### Apartado F: Exportación a JSON (.json)
Generar un fichero estructurado denominado `atracciones.json` que almacene de forma serializada toda la información y estado de las atracciones usando el módulo nativo `json`.

### Apartado G: Exportación a XML (.xml)
Generar un archivo estructurado denominado `atracciones.xml` utilizando la librería estándar `xml.etree.ElementTree` para volcar de forma jerárquica las propiedades del parque.

### Apartado H: Programa Principal
Desarrollar un flujo de ejecución (`__main__`) que:
1. Instancie al menos un objeto válido de cada tipo de atracción.
2. Almacene todas las instancias en una lista común.
3. Imprima por consola el resumen de cada atracción.
4. Calcule y muestre los ingresos parciales y totales.
5. Automatice la creación simultánea de los tres ficheros (`jornada.txt`, `atracciones.json` y `atracciones.xml`).

