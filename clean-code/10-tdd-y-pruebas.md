# 10. Las Leyes del TDD y Pruebas

> *"El código limpio sin pruebas es, simplemente, un código inseguro. Por muy elegante que sea, si no podemos demostrar que funciona, no podemos confiar en él."* — Robert C. Martin

## Idea Principal
El **TDD (Desarrollo Guiado por Pruebas)** no es solo una técnica de testing, sino una disciplina de diseño de código. Nos obliga a pensar en la interfaz y los requisitos antes de escribir la implementación, lo que da como resultado componentes desacoplados, pequeños y altamente testeables.

## 🔑 Las Tres Leyes del TDD
Si decidimos aplicar TDD en nuestro flujo de trabajo diario, debemos seguir estrictamente estas tres reglas:

1. **Primera Ley:** **No debemos escribir ningún código de producción** hasta que hayamos escrito una prueba unitaria que falle.
2. **Segunda Ley:** **No debemos escribir más de una prueba unitaria de lo suficiente para que falle** (y fallar en compilación o ejecución ya cuenta como fallo).
3. **Tercera Ley:** **No debemos escribir más código del necesario para hacer pasar la prueba unitaria actual.**

Seguir este ciclo (*Red -> Green -> Refactor*) de forma constante nos impide acumular código innecesario o sobreingeniería.

## Aplicación Práctica en Frontend (React & JavaScript)
Pdemos integrar el TDD y las pruebas en nuestras aplicaciones de la siguiente manera:

1. **Escribir la prueba antes del componente o hook:** Antes de construir un hook personalizado de React (por ejemplo, para gestionar un carrito de compras), escribimos una prueba con herramientas como *Jest* o *Vitest* que espere el comportamiento deseado y la veamos fallar.
2. **Probar el comportamiento, no la implementación:** En lugar de comprobar cada línea interna de un componente, diseñamos las pruebas (con *React Testing Library*) simulando lo que haría el usuario (hacer clic en un botón, rellenar un input) y verificando qué se muestra en pantalla.
3. **Mantener las pruebas limpias y legibles:** El código de nuestras pruebas es tan importante como el de producción. Aplicamos las mismas reglas de nombres claros, funciones pequeñas y cero duplicación en nuestros archivos de test (*.test.js* / *.spec.jsx*).
4. **Refactorizar sin miedo:** Una vez que la prueba pasa a verde (*Green*), refactorizamos nuestro código frontend sabiendo que la red de seguridad de las pruebas nos avisará inmediatamente si rompemos algo.