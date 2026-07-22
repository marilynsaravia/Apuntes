# 07. Gestión de Errores

> *"Los errores ocurren, por lo que como desarrolladores somos responsables de asegurarnos de que nuestro código haga lo que debe cuando las cosas fallan."* — Robert C. Martin

## Idea Principal
Una mala gestión de errores puede oscurecer por completo la lógica principal de nuestra aplicación. Si ensuciamos todo el código con comprobaciones constantes de códigos de retorno o valores nulos, el flujo real del negocio se vuelve ilegible. Debemos usar **excepciones en lugar de códigos de error** y diseñar flujos limpios ante los fallos.

## Reglas Clave para la Gestión de Errores
* **Lanzar excepciones en lugar de retornar códigos:** Evitamos devolver un código de error numérico o un booleano falso que obligue al código llamante a comprobarlo inmediatamente; preferimos lanzar una excepción para separar la lógica de éxito de la de error.
* **Proporcionar contexto con las excepciones:** Cada excepción que lanzamos debe incluir suficiente información descriptiva (como el mensaje o la traza) para poder rastrear el origen exacto del fallo.
* **Definir clases de excepciones según las necesidades del llamante:** Agrupamos y estructuramos las excepciones basándonos en cómo van a ser capturadas por el resto del sistema, evitando saturar con bloques `try-catch` excesivos.
* **Evitar retornar nulos (*Null*):** En la medida de lo posible, evitamos que nuestras funciones devuelvan `null`, ya que esto obliga a escribir constantes y tediosas comprobaciones de nulidad en cada rincón del código.

## Aplicación Práctica en Frontend (React & JavaScript)
Como desarrolladores frontend, podemos aplicar estas directrices en el manejo de errores de nuestras interfaces:

1. **Utilizar bloques `try-catch` limpios en llamadas asíncronas:** Al consumir APIs con `async/await`, envolvemos las peticiones en bloques estructurados para capturar los errores de red de forma centralizada y predecible.
2. **Implementar *Error Boundaries* en React:** En lugar de dejar que toda la aplicación colapse si un componente falla, utilizamos límites de errores (*Error Boundaries*) para aislar el fallo y mostrar una interfaz de respaldo amigable al usuario.
3. **Evitar devolver `null` silenciosamente en componentes:** Si un componente no recibe datos o está cargando, preferimos retornar estados de carga (`Skeleton` o *spinners*) o mensajes claros en lugar de devolver `null` de forma ambigua.
4. **Manejar estados de error en los formularios:** Centralizamos la gestión de errores de validación de entradas en nuestros formularios mediante estados limpios (`hasError`, `errorMessage`), separando claramente el flujo correcto de los datos del flujo de alerta al usuario.