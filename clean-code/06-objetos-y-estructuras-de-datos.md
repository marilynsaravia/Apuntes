# 06. Objetos y Estructuras de Datos

> *"Los objetos ocultan sus datos detrás de abstracciones y exponen funciones que operan sobre esos datos. Las estructuras de datos exponen sus datos y no tienen funciones significativas."* — Robert C. Martin

## Idea Principal
Entender la diferencia entre **objetos** y **estructuras de datos** es fundamental para diseñar arquitecturas flexibles. Mientras que los objetos ocultan su estructura interna y exponen comportamiento (métodos), las estructuras de datos exponen simplemente sus datos sin comportamiento asociado. Saber cuándo usar cada uno evita acoplamientos innecesarios en nuestro código.

## Reglas Clave para Datos y Objetos
* **Ocultar la estructura (El principio de ocultación):** No debemos exponer los detalles internos de nuestros objetos; en su lugar, proporcionamos métodos de alto nivel para interactuar con ellos.
* **Respetar la Ley de Demeter:** Un módulo no debe conocer los detalles internos de los objetos que manipula. Evitamos las cadenas largas de llamadas (como `a.getB().getC().doSomething()`), ya que acoplan demasiado el código a la estructura interna.
* **Evitar estructuras híbridas:** No debemos crear entidades que sean mitad objeto y mitad estructura de datos, ya que combinan lo peor de ambos mundos (dificultan añadir nuevas funciones y también añadir nuevos tipos de datos).
* **Preferir objetos para encapsular comportamiento:** Usamos objetos cuando necesitamos proteger el estado interno y obligar a que las operaciones pasen a través de reglas de negocio definidas.

## Aplicación Práctica en Frontend (React & JavaScript)
Como desarrolladoress frontend, podemos aplicar estos conceptos en el manejo de nuestros estados y componentes:

1. **Encapsular la lógica en Custom Hooks:** En lugar de dejar que nuestros componentes manipulen directamente estructuras de datos complejas o llamadas a APIs dispersas, agrupamos el estado y su comportamiento en un *Custom Hook* que actúa como un objeto bien encapsulado.
2. **Evitar la acumulación de puntos (*Prop Drilling* excesivo o encadenamiento):** No accedemos a propiedades anidadas profundas de forma directa en los componentes si podemos evitarlo, utilizando patrones de diseño más limpios o selectores de estado.
3. **Tratar las props y el estado como estructuras claras:** Cuando manejamos datos puros (como los objetos que vienen directamente de una API REST o un archivo JSON), los tratamos como estructuras de datos simples orientadas a transportar información hacia la interfaz.
4. **Separar la representación visual de la lógica de datos:** Evitamos mezclar cálculos complejos de transformación de datos directamente dentro del JSX; preferimos funciones o selectores puros que preparen los datos antes de renderizarlos.