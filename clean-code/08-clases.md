# 08. Clases

> *"Las clases deben ser pequeñas."* — Robert C. Martin

## Idea Principal
Al igual que ocurre con las funciones, **la primera regla de las clases es que deben ser pequeñas**. No medimos su tamaño por el recuento de líneas, sino por la cantidad de **responsabilidades** que asumen. Si una clase tiene demasiadas razones para cambiar, significa que estamos acumulando demasiadas tareas en un solo lugar.

## Reglas Clave para Clases
* **Respetar el Principio de Responsabilidad Única (SRP):** Una clase o módulo debe tener una, y solo una, razón para cambiar. Separamos las responsabilidades para que el sistema sea más fácil de mantener y modificar.
* **Mantener la cohesión alta:** Las clases deben tener un número pequeño de variables de instancia, y cada método de la clase debe manipular una o varias de esas variables, asegurando que guarden una estrecha relación lógica.
* **Organizar verticalmente el código:** Estructuramos el contenido de la clase siguiendo un orden lógico y legible: primero las constantes públicas, luego las variables estáticas y privadas, y finalmente los métodos públicos y auxiliares.
* **Programar orientados a interfaces:** Dependemos de abstracciones y contratos en lugar de implementaciones concretas, lo que nos permite desacoplar los componentes y facilitar las pruebas unitarias.

## Aplicación Práctica en Frontend (React & JavaScript)
Podemos aplicar estos conceptos en la arquitectura de nuestros componentes y módulos:

1. **Evitar componentes de React gigantescos:** Dividimos los componentes grandes en subcomponentes más pequeños y especializados, separando la estructura visual de la lógica compleja de negocio.
2. **Modularir la lógica con servicios y utilidades:** Sacamos la lógica que no pinta elementos visuales (como llamadas a APIs, formateo de fechas o validaciones) fuera de los componentes, ubicándola en archivos de clases o módulos independientes (*services* o *helpers*).
3. **Encapsular el estado local y global:** Mantenemos la lógica de estado contenida y coherente, utilizando custom hooks o gestores de estado bien acotados que manejen una única porción de los datos de la aplicación.
4. **Separar la presentación de los contenedores:** Distinguimos entre componentes puramente visuales (que solo reciben props y renderizan UI) y componentes contenedores (que gestionan datos y efectos), manteniendo cada uno con una única responsabilidad clara.