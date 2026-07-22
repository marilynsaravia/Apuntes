# 03. Funciones

> *"Las funciones son las primeras líneas de organización de cualquier lenguaje de programación."* — Robert C. Martin

## Idea Principal
Si queremos escribir código limpio, **nuestras funciones deben ser pequeñas, hacer una sola cosa y hacerla bien**. Cuando acumulamos múltiples responsabilidades en una sola función, el código se vuelve rígido, difícil de leer e imposible de probar de forma aislada.

## Reglas Clave para Funciones
* **Reducir el tamaño:** Las funciones deben ocupar pocas líneas de código. Idealmente, no deberían sobrepasar las 20 o 30 líneas. Si crecemos demasiado, es una señal clara de que estamos intentando hacer demasiadas cosas.
* **Hacer una sola cosa (SRP):** Una función debe realizar una única tarea dentro de su nivel de abstracción. Si podemos extraer otra función de ella cuyo nombre sea simplemente una reafirmación de su implementación, es que hace de más.
* **Mantener un nivel único de abstracción:** Las sentencias dentro de una función deben estar en el mismo nivel de abstracción. No debemos mezclar lógica de negocio de alto nivel con detalles de bajo nivel o manipulación directa del DOM en la misma función.
* **Reducir los argumentos (¡Cero o uno idealmente!):** Cuantos menos parámetros reciba una función, más fácil será entenderla y probarla. 
    * **0 argumentos (Niládica):** La opción más limpia.
    * **1 o 2 argumentos (Monádica / Diádica):** Bastante aceptables y naturales.
    * **3 argumentos (Triádica):** Requieren justificación y deberíamos evitarlas siempre que podamos.
    * **Más de 3 argumentos (Polinádica):** ¡Prohibidas! Debemos agruparlos en un objeto o estructura de datos.

## Aplicación Práctica en Frontend (React & JavaScript)
Como equipo de desarrollo frontend, podemos aplicar estas reglas en nuestros componentes y hooks:

1. **Evitar funciones monstruo en nuestros componentes:** No debemos mezclar llamadas a APIs (`fetch`), lógica de estado (`useState`) y transformaciones complejas de datos dentro de una misma función manejadora de eventos. Separamos responsabilidades en funciones auxiliares o hooks personalizados.
2. **Limitar los parámetros en nuestros componentes y props:** Si un componente de React o una función de utilidad recibe una larga lista de parámetros sueltos, refactorizamos para pasar un único objeto de opciones o un objeto de `props` bien estructurado.
3. **Nombrar las funciones según lo que hacen (con verbos):** Nos aseguramos de que el nombre refleje exactamente su única acción, por ejemplo: `calcularTotalCarrito()` o `filtrarProductosPorCategoria()`, evitando nombres vagos como `procesarDatos()`.
4. **Evitar banderas de control (*Flags* como argumentos):** Si pasamos un booleano (por ejemplo, `actualizar(datos, true)`) para que la función haga dos cosas distintas según el valor, preferimos dividirla en dos funciones separadas: `crearRegistro(datos)` y `modificarRegistro(datos)`.