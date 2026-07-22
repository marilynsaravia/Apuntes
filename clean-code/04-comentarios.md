# 04. Comentarios

> *"No comentes un código malo, reescríbelo."* — Brian Kernighan

## Idea Principal
Los comentarios son, en el mejor de los casos, un mal necesario. Si nuestro código estuviera lo suficientemente limpio, expresivo y bien estructurado, apenas necesitaríamos comentarios. Cuando vemos un comentario, debemos recordar que **cada comentario miente un poco**, ya que con el tiempo el código cambia, pero los desarrolladores suelen olvidar actualizar el texto que lo acompaña.

## Reglas Clave para Comentarios
* **Justificar las intenciones:** Explicar el *por qué* detrás de una decisión técnica compleja o poco intuitiva que no sea evidente a simple vista en el código.
* **Aclarar información:** Traducir o explicar de forma concisa algún parámetro o valor que resulte confuso por sí mismo (por ejemplo, expresiones regulares complejas).
* **Advertir consecuencias:** Avisar al resto del equipo sobre posibles efectos secundarios, como el uso de una función bloqueante o la necesidad de respetar un orden específico de ejecución.
* **Evitar comentarios redundantes:** No escribir comentarios que repitan exactamente lo que el código ya dice de forma obvia.
* **Prohibir código comentado ("Código Zombi"):** No debemos dejar bloques enteros de código antiguo o anulado comentados "por si acaso". Para eso usamos el control de versiones de Git.

## Aplicación Práctica en Frontend (React & JavaScript)
Como equipo de desarrollo frontend, podemos gestionar los comentarios en nuestros proyectos de la siguiente manera:

1. **Eliminar comentarios redundantes:** Evitamos añadir explicaciones innecesarias en componentes simples, por ejemplo, no escribimos un comentario como `// Este componente renderiza el botón de enviar` justo encima de `<SubmitButton />`.
2. **Utilizar JSDoc para documentar utilidades:** Escribimos bloques JSDoc limpios únicamente en funciones complejas o de utilidad general que se consumen en varias partes de la aplicación, detallando los parámetros y el valor de retorno esperados.
3. **Evitar marcas de autor o fechas:** No dejamos firmas personales, correos ni registros de fecha en los comentarios del código fuente, ya que Git se encarga perfectamente de rastrear el historial de cambios y autoría de cada línea.
4. **Transformar comentarios en nombres claros:** Si sentimos la necesidad de explicar con un comentario qué hace un bloque largo de código dentro de un componente, preferimos extraer ese bloque a una función o variable bien nombrada que hable por sí misma.