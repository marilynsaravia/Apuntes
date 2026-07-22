# ¿Qué es TypeScript?
TypeScript es un lenguaje de programación de código abierto desarrollado por Microsoft. Se define técnicamente como un superconjunto (superset) de JavaScript, lo que significa que "envuelve" a JavaScript y le añade superpoderes.

* La esencia: Básicamente, es JavaScript con tipado estático y una estructura orientada a objetos (basada en clases).

* Compatibilidad: Al ser un superconjunto, cualquier código JavaScript es válido en un archivo de TypeScript.

# Origen y Razón de Ser
La creación de este lenguaje no fue casualidad, surgió para solucionar los problemas de escalabilidad en la web.

## El Creador 

Fue diseñado por Anders Hejlsberg, el mismo arquitecto detrás de C#. Esto explica por qué TypeScript se siente tan robusto y profesional.

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/ae010981-9383-4225-895f-1b3d6a1ed535" />


## La Misión

Traer el orden de los lenguajes tipados (como C# o Java) al ecosistema flexible de JavaScript.

## El Problema

En JavaScript puro (tipado dinámico), los errores de valores suelen saltar cuando el usuario ya está usando la app.

## La Solución

TypeScript actúa como una "validación tipo SQL": si defines que un dato es un número, el sistema te impide meter texto mientras programas, ahorrándote errores en producción.

<img width="965" height="276" alt="image" src="https://github.com/user-attachments/assets/44df2eac-8dfa-4eee-b2d2-a6a044a955ba" />


# El Proceso de Transpilación
Es importante entender que los navegadores no entienden TypeScript directamente.

* El Transpiler: TypeScript incluye una herramienta que traduce tu código a JavaScript puro.

# Tipado Explícito y de Inferencia

En JavaScript, una variable puede cambiar de tipo (de número a texto) sin avisar. En TypeScript, tú defines qué "forma" tiene la información.

* Inferencia: Si declaras let ciudad = "Madrid", TypeScript ya sabe que es un string.

* Explícito: Tú defines el tipo usando : tipo.

* Versatilidad: Puedes configurar este traductor para que genere código en ES5 (la versión que entienden todos los navegadores antiguos) o ES6 (versiones más modernas).

* Ecosistema: Está pensado para proyectos de gran escala. De hecho, herramientas famosas como Angular están construidas totalmente con TypeScript, y es compatible con librerías como Node.js, MongoDB y D3.js.

<img width="680" height="84" alt="image" src="https://github.com/user-attachments/assets/b89a6eb4-e5c3-4ab8-a08d-56c2a82fb4bd" />

# Tipos de Datos Básicos

Además de los clásicos, TypeScript introduce herramientas para ser más precisos:

* Arrays: let lista: number[] = [1, 2, 3];

* Any: (Úsalo con cuidado) permite cualquier tipo de dato. Es como volver a JavaScript puro.

* Void: Se usa en funciones que no retornan ningún valor.

* Enums: Permiten definir un conjunto de constantes con nombre (ej. Color.Rojo, Color.Azul).

# Interfaces y Types

Son "contratos" que definen la estructura que debe tener un objeto. Son fundamentales para el desarrollo a gran escala.

## Interface

<img width="683" height="312" alt="image" src="https://github.com/user-attachments/assets/aea385b3-9c7e-434d-9a48-9bc4d3eb299b" />

* Define la forma de un objeto

* Ideal para modelos, props, clases

* Muy usada en Angular




## Type

<img width="676" height="357" alt="image" src="https://github.com/user-attachments/assets/8037e63c-cca5-41b4-b072-da4be9357738" />

* Define tipos más flexibles

* Sirve para uniones, primitivos y funciones
