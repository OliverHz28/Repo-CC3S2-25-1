### Actividad: Ejecutar pruebas con pytest

**Paso 1: Instalando pytest y pytest-cov**

Inicio de nuestro workspace

![](img/act10-paso1-1.png)

*Ejecutamos el siguiente comando.*

```bash
python3 -m pip install pytest pytest-cov
```

Este comando nos descargará e instalará las últimas versiones de pytest y pytest-cov en nuestro entorno de Python. 

![](img/act10-paso1-2.png)

**Paso 2: Escribiendo y ejecutando pruebas con pytest**

*Ejecutamos el siguiente comando.*

```
pytest -v
```

La opción -v activa el modo detallado, mostrando qué pruebas se ejecutaron y sus resultados. Si las pruebas pasan, verás una salida con texto en verde. Si alguna prueba falla, el texto será rojo.

![](img/act10-paso2-1.png)

* Pytest comenzó la ejecución.
* Mostró detalles del entorno (SO, Python, pytest, plugins).
* Indica dónde guarda la caché (`.pytest_cache`) para acelerar futuras ejecuciones y la raíz del proyecto.
* Listó plugins activos incluyendo `cov`que corresponde al `pytest-cov` que instalamos previamente.
* Encuentra 11 pruebas.
* Ejecuta cada prueba mostrando su nombre y el resultado (`PASSED`).
* Muestra una barra de avance hasta el 100%.
* Reportó que las 11 pruebas pasaron en 0.88 segundos.

> `pytest` ejecutó exitosamente las 11 pruebas unitarias, mostrando un resultado detallado de cada una.

**Paso 3: Añadiendo cobertura de pruebas con pytest-cov**

*Ejecutamos el siguiente comando.*

```
pytest --cov`
```

Para ejecutar las pruebas y obtener un informe de cobertura de todo los archivos del directorio.

![](img/act10-paso2-2.png)


* Pytest comienza la ejecución con la intención de medir la cobertura.
* Se encuentran 11 pruebas en `test_triangle.py`.
* Las 11 pruebas en `test_triangle.py` se ejecutaron y pasaron.
* `pytest-cov` analizó la cobertura de los archivos `.py` encontrados en el directorio actual (`pruebas_pytest`) y sus subdirectorios.
* Se genera un reporte en la terminal mostrando la cobertura por archivo:
    * `test_triangle.py`: 30 declaraciones, 0 perdidas, 100% de cobertura.
    * `triangle.py`: 10 declaraciones, 0 perdidas, 100% de cobertura.
* Se reporta una cobertura total del 100% para las 40 declaraciones combinadas.

> `pytest` ejecutó exitosamente todas las pruebas y `pytest-cov` generó un informe de cobertura que indica que el 100% del código ejecutable en `test_triangle.py` y `triangle.py` fue cubierto por las pruebas.


*Ejecutamos el siguiente comando.*

```
pytest --cov --cov-report=html`
```

Si también deseas generar un informe de cobertura en HTML para visualizarlo.

![](img/act10-paso2-3.png)

* De manera similar al ejecutar `pytest --cov` 
* La línea `Coverage HTML written to dir htmlcov` indica que `pytest-cov` generó un informe de cobertura detallado en formato HTML y lo guardó en un nuevo directorio llamado `htmlcov` dentro del proyecto.

> `pytest` ejecuta las pruebas, mide la cobertura del código en el proyecto y genera un informe HTML completo.


*Ejecutamos el siguiente comando.*

```
pytest -v --cov=triangle`
```

Si solo deseas medir la cobertura de un módulo  o directorio específico, en nuestro caso `triangle.py`.

![](img/act10-paso2-4.png)


* `pytest` comienza la ejecución en modo detallado (`-v`) y con la intención de medir la cobertura del módulo `triangle`.
* Se encontraron 11 pruebas en `test_triangle.py`.
* Se ejecutaron las 11 pruebas, mostrando el nombre de cada prueba y su estado (`PASSED`).
* `pytest-cov` analizó la cobertura del módulo `triangle.py` durante la ejecución de las pruebas.
* Genera un reporte en la terminal mostrando la cobertura del módulo `triangle`:
    * `triangle.py`: 10 declaraciones, 0 perdidas, 100% de cobertura.
* Reporta una cobertura total del 100% para el módulo `triangle.py`.

> `pytest` ejecutó exitosamente todas las pruebas en modo detallado y `pytest-cov` generó un informe de cobertura que indica que el 100% del código ejecutable en el módulo `triangle.py` fue cubierto por las pruebas.


*Ejecutamos el siguiente comando.*

```
pytest --cov=triangle --cov-report=term-missing`
```

Si deseas un informe más detallado que muestre las líneas que no están cubiertas,

![](img/act10-paso2-5.png)


* Pytest comienza la ejecución con la intención de medir la cobertura del módulo `triangle` y mostrar las líneas no cubiertas en la terminal.
* Se encuentran 11 pruebas en `test_triangle.py`.
* Las 11 pruebas en `test_triangle.py` se ejecutaron y pasaron.
* `pytest-cov` analiza la cobertura del módulo `triangle.py`.
* Se genera un reporte en la terminal mostrando:
    * `triangle.py`: 10 declaraciones, 0 perdidas, 100% de cobertura. La columna "Missing" estaría vacía o indicaría que no hay líneas faltantes.
* Se reportó una cobertura total del 100% para el módulo `triangle.py`.

> `pytest` ejecuta exitosamente todas las pruebas y `pytest-cov` generó un informe de cobertura detallado en la terminal para el módulo `triangle.py`, indicando que todas las líneas ejecutables fueron cubiertas por las pruebas. La opción `--cov-report=term-missing` mostraría las líneas faltantes si hubiera alguna.

*Ejecutamos el siguiente comando.*

```
pytest --cov=triangle --cov-report=term-missing --cov-report=html`
```

Si deseas un informe más detallado que muestre las líneas que no están cubiertas,

![](img/act10-paso2-6.png)

Ejecución de `pytest --cov=triangle --cov-report=term-missing --cov-report=html`:

* De manera similar al ejecutar `pytest --cov=triangle --cov-report=term-missing` 
* La línea `Coverage HTML written to dir htmlcov` indica que `pytest-cov` también generó un informe de cobertura detallado en formato HTML y lo guardó en el directorio `htmlcov`.

`pytest` ejecuta exitosamente todas las pruebas y `pytest-cov` generó dos tipos de informes de cobertura para el módulo `triangle.py`: uno detallado en la terminal y otro completo en formato HTML para una visualización más interactiva. Ambos indican una cobertura del 100%.

**Paso 4: Añadiendo colores automáticamente**

*Ejecutamos el siguiente comando.*

```
pytest --color=yes
```

Si por alguna razón los colores no se muestran.

![](img/act10-paso4.png)

**Paso 5: Automatizando la configuración de pytest**
En lugar de escribir todos los parámetros de configuración cada vez que ejecutes pytest, puedes guardarlos en un archivo pytest.ini o como se ha realizado aqui setup.cfg. 

* **Elegir el archivo con sabiduría:**
    * **`pytest.ini` para lo esencial de testing:** Si nuestro foco es la configuración *únicamente* de pytest (opciones de ejecución, plugins principales como `cov`), este es el ideal. Simple y directo.
    * **`setup.cfg` para el ecosistema del proyecto:** Si ya contamos con un `setup.cfg` gestionando otras herramientas (linters, formatters, empaquetado), centralizar la configuración de pytest bajo `[tool:pytest]` mantiene todo organizado.
* **`addopts`:** Definimos aquí las opciones que siempre queremos activas (`-v`, `--tb=short`, `--cov=.`, `--cov-report=term-missing`, etc.). Esto evita repeticiones tediosas en la terminal.
* **Secciones de plugins:** No dudar en configurar plugins directamente en estos archivos (`[coverage:run]`, `[flake8]`, etc.). Simplifica la invocación de herramientas.
* **Consistencia en el equipo:** Asegura que todo el equipo utilice la misma configuración (commit estos archivos al repositorio). Evita sorpresas y "en mi máquina funciona".


**setup.cfg**


La configuración de setup.cfg está configurada de la siguiente manera:

```
[tool:pytest]
addopts = -v --tb=short --cov=. --cov-report=term-missing

[coverage:run]
branch = True

[coverage:report]
show_missing = True
```

Este archivo te permitirá automatizar la configuración de las pruebas.

[tool:pytest]es una sección específica para configurar pytest.
- addopts: Opciones adicionales para pytest (en este caso, activa la salida detallada -v, el tipo de rastro corto para errores --tb=short, y la cobertura con informe de líneas faltantes --cov-report=term-missing).
- [coverage:run] y [coverage:report]: Configuración para la herramienta de cobertura, en este caso, para medir la cobertura de ramas (branch=True) y mostrar qué líneas faltan (show_missing=True).

**pytest.ini**

Es un archivo de configuración específico para pytest. Solo contiene configuraciones que pytest usa directamente.

Si quieres configurar solo pytest sin agregar configuraciones de otras herramientas o mantener la configuración más organizada para esta herramienta en particular, pytest.ini es una opción preferida.

Sigue una estructura más simple y directa que se parece a lo siguiente:

```
[pytest]
addopts = -v --tb=short --cov=. --cov-report=term-missing

[coverage:run]
branch = True

[coverage:report]
show_missing = True
```

**Paso 6: Ejecutando pruebas con la configuración automatizada**
Una vez que hayas creado el archivo o setup.cfg pytest.ini, simplemente ejecuta pytest sin ningún parámetro adicional:

```
pytest
```

Esto ejecutará las pruebas con los parámetros definidos en el archivo de configuración, ahorrándote la necesidad de escribirlos cada vez.

![](img/act10-paso6.png)