## Ejercicios

### Test de inicios 

*`pytestes`*
![](img/act8-inicio1.png)

*`cov`*
![](img/act8-inicio2.png)

### Ejercicio 1: Método para vaciar el carrito

**Objetivo:**  
Implementa en la clase `Carrito` un método llamado `vaciar()` que elimine todos los items del carrito. Luego, escribe pruebas siguiendo el patrón AAA para verificar que, al vaciar el carrito, la lista de items quede vacía y el total sea 0.

**Pistas:**
- Agrega el método `vaciar` en `src/carrito.py` que realice `self.items = []`.
- Crea pruebas en `tests/test_carrito.py` que agreguen varios productos, invoquen `vaciar()` y verifiquen que `obtener_items()` retorne una lista vacía y `calcular_total()` retorne 0.

 **Metodo `vaciar`**

 ![](img/act8-ejc1-1.png)

**Pruebas - `test_vaciar_carrito()`**

![](img/act8-ejc1-2.png)

**Pruebas - `test_vaciar_carrito_total_cero()`**

![](img/act8-ejc1-3.png)

**`pytest`**

![](img/act8-ejc1-4.png)