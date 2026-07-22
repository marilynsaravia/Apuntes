# 05. Formato

> *"El formato es importante. Es tan importante que no se puede ignorar y debe tomarse en serio. El estilo y la legibilidad del código comunican profesionalismo."* — Robert C. Martin

## Idea Principal
El código que escribimos hoy probablemente será modificado y mantenido por otras personas (o por nosotros mismos en el futuro). Si mantenemos un **formato visual coherente, ordenado y limpio**, facilitamos enormemente la lectura y comprensión de la arquitectura de la aplicación sin necesidad de leer cada línea en detalle.

## Reglas Clave para el Formato
* **Mantener la coherencia visual:** Todo el equipo debe seguir las mismas reglas de estilo y formato para que parezca que el código ha sido escrito por una sola mente.
* **Establecer una longitud de línea razonable:** Evitamos líneas infinitas de código para no tener que hacer desplazamiento horizontal constante en el editor.
* **Organizar el formato vertical:** Separamos los conceptos independientes mediante líneas en blanco y mantenemos juntas las líneas de código que están estrechamente relacionadas (afinidad vertical).
* **Cuidar la indentación:** Usamos bloques correctamente indentados (con espacios o tabulaciones uniformes) para que la jerarquía de bloques y funciones salte a la vista de inmediato.

## Aplicación Práctica en Frontend (React & JavaScript)
Como desarrolladores frontend, podemos estandarizar el formato en nuestros proyectos de la siguiente manera:

1. **Automatizar con Prettier y ESLint:** Configuramos herramientas de formateo automático y linters para que el formato se limpie y ordene solo al guardar el archivo o al hacer un commit.
2. **Ordenar las importaciones (*Imports*):** Mantenemos un orden claro y estructurado en la cabecera de nuestros archivos (primero librerías externas como React, luego componentes internos, hooks, y finalmente estilos o assets).
3. **Estructurar los componentes de React:** Seguimos un orden lógico dentro de la función del componente: primero la declaración de estados (`useState`), luego los efectos (`useEffect`), a continuación las funciones manejadoras de eventos, y por último el bloque de retorno con el JSX.
4. **Respetar el límite de longitud:** Configuramos el editor para que nos avise si una línea o un bloque de JSX se extiende demasiado, dividiendo los componentes complejos en piezas más pequeñas y legibles.