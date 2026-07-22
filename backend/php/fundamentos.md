# ¿Qué es PHP?
PHP es un lenguaje de programación de código abierto, de propósito general y ejecutado en el lado del servidor. Se define técnicamente como un lenguaje de script interpretado, diseñado específicamente para el desarrollo web y capaz de incrustarse directamente dentro del código HTML.

## La esencia
Básicamente, es el puente que conecta el navegador con la base de datos. Mientras el HTML es el esqueleto de una web, PHP es el cerebro que decide qué información mostrar (como tu perfil de Facebook o tu carrito de compras) justo antes de que la página llegue a tu pantalla.

# Origen y Razón de Ser
A mediados de los 90, hacer páginas web dinámicas era un dolor de cabeza: se tenían que escribir programas complejos en C o Perl para que una web hiciera algo más que mostrar texto estático. Era lento y difícil de mantener.

Entonces, en 1994, el programador Rasmus Lerdorf creó unos scripts sencillos en lenguaje C para rastrear las visitas de su currículum en línea. A este paquete de herramientas lo llamó Personal Home Page Tools. Lo que nació como una utilidad personal para simplificar su trabajo, terminó convirtiéndose en un lenguaje global cuando Lerdorf liberó el código y la comunidad empezó a usarlo para conectar sitios web con bases de datos de forma masiva.

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/3a095ca8-ccda-47b2-beaa-0ae20ac5b30e" />


# PHP Hoy: El motor de la Web Moderna

Hoy en día, evolucionado como el acrónimo recursivo PHP: Hypertext Preprocessor, se ha consolidado como el motor esencial de la web moderna, impulsando desde blogs personales hasta gigantes como WordPress y Wikipedia gracias a su capacidad para transformar sitios estáticos en aplicaciones interactivas y escalables.

Aquí tienes toda la sección técnica de los Fundamentos de PHP organizada en formato Markdown profesional, con una estructura clara, bloques de código limpios y resaltado de puntos clave:

# Sintaxis Básica y Variables

PHP se ejecuta en el servidor y se "incrusta" directamente dentro del HTML. Para que el servidor reconozca el código, este debe estar contenido en etiquetas específicas.

Etiquetas: Se delimita con <img width="54" height="26" alt="image" src="https://github.com/user-attachments/assets/d645c54a-26cc-4e62-a33c-dafb571b6d4a" />
 para abrir y <img width="25" height="22" alt="image" src="https://github.com/user-attachments/assets/4ea709cb-414e-463d-b3a0-212768be01d0" />
 para cerrar.

Variables: Siempre comienzan con el signo de dólar <img width="68" height="23" alt="image" src="https://github.com/user-attachments/assets/fa3b6d71-edc1-4dfb-b322-325bd0036f7e" />
. Es un lenguaje de tipado dinámico, por lo que no necesitas declarar qué tipo de dato contiene la variable.

Imprimir datos: Las instrucciones principales son <img width="40" height="20" alt="image" src="https://github.com/user-attachments/assets/b82455e3-1030-4074-bddf-24d5ba5c4d3a" />
 o <img width="51" height="21" alt="image" src="https://github.com/user-attachments/assets/dcbd4f2c-314a-481b-a28d-e296cdf3f1fd" />
.

<img width="674" height="127" alt="image" src="https://github.com/user-attachments/assets/2bab251c-fa9c-4e54-954a-d13a383f1eda" />


# Tipos de Datos
PHP soporta los tipos de datos esenciales para el manejo de información:

Strings: Cadenas de texto.

Integers: Números enteros.

Floats: Números decimales (punto flotante).

Booleans: Valores lógicos (true o false).

Arrays: Colecciones de datos que pueden ser indexados (por número) o asociativos (por clave personalizada).

# Estructuras de Control
Permiten controlar el flujo del programa mediante decisiones o repeticiones.

Condicionales: Determinan si un bloque de código se ejecuta.

if, else, elseif

switch

Bucles (Loops): Repiten tareas eficientemente.

for: Para repeticiones con un número conocido de veces.

while: Repite mientras se cumpla una condición.

foreach: Diseñado específicamente para recorrer arreglos (arrays) de forma sencilla.

# Funciones
Son bloques de código reutilizables que realizan tareas específicas. Pueden recibir parámetros y devolver resultados.

<img width="550" height="118" alt="image" src="https://github.com/user-attachments/assets/d9c2a349-3473-4be8-8568-f153a0815b4d" />

# Manejo de Formularios (GET y POST)
Es la capacidad de PHP para procesar datos enviados por el usuario desde el navegador.

$_GET: Los datos se envían a través de la URL. Es útil para búsquedas o filtros, pero la información es visible.

$_POST: Los datos se envían de forma invisible en el cuerpo de la petición HTTP. Es el método estándar para información sensible (contraseñas) o datos extensos.

# Conexión a Base de Datos
PHP es conocido por su excelente integración con MySQL. Las formas modernas de conexión son:

PDO (PHP Data Objects): La opción más recomendada por ser segura y compatible con múltiples tipos de bases de datos.

MySQLi: Una versión mejorada específica para bases de datos MySQL.

[!IMPORTANT] Nota de seguridad: Nunca insertes variables directamente en una consulta SQL. Usa siempre sentencias preparadas para evitar ataques de Inyección SQL.
