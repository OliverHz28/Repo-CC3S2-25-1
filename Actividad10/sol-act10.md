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

![](img/act10-paso2-1.png)

* Pytest comenzó la ejecución.
* Mostró detalles del entorno (SO, Python, pytest, plugins).
* Indica dónde guarda la caché (`.pytest_cache`) para acelerar futuras ejecuciones y la raíz del proyecto.
* Listó plugins activos incluyendo `cov`que corresponde al `pytest-cov` que instalamos previamente.
* Encontró 11 pruebas.
* Ejecutó cada prueba mostrando su nombre y el resultado (`PASSED`).
* Mostró una barra de avance hasta el 100%.
* Reportó que las 11 pruebas pasaron en 0.88 segundos.

> `pytest` ejecutó exitosamente las 11 pruebas unitarias, mostrando un resultado detallado de cada una.

