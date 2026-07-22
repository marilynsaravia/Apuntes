# 09. Síntomas y Heurísticas

> *"Si tu código muestra síntomas de deterioro, lo más probable es que algo esté fallando en su diseño."* — Robert C. Martin

## Idea Principal
Los **síntomas de código** (*code smells*) son señales de alerta superficiales de que algo no va bien en la estructura interna de nuestro software. No rompen necesariamente el programa, pero indican una degradación de la calidad que, si ignoramos, terminará convirtiendo el mantenimiento en una pesadilla. Debemos aprender a detectarlos a tiempo para aplicar heurísticas de mejora continua.

## Reglas Clave para Detectar Síntomas de Alerta
* **Evitar la duplicación de código:** El principio DRY (*Don't Repeat Yourself*) es sagrado. Si vemos código repetido, debemos extraerlo a una función o módulo común.
* **Reducir la complejidad innecesaria:** Evitamos sobreingeniería y estructuras crípticas u obvias en exceso que dificulten la lectura lineal.
* **Vigilar el acoplamiento excesivo:** Identificamos cuando un módulo o componente depende demasiado de los detalles internos de otro, rompiendo la independencia.
* **Eliminar código muerto o redundante:** Limpiamos variables, funciones, parámetros o archivos enteros que ya no se utilicen en el sistema.

## Aplicación Práctica en Frontend (React & JavaScript)
Como desarrollores frontend, podemos identificar y corregir estos síntomas comunes en nuestros proyectos:

1. **Detectar componentes o props "inflados":** Si un componente recibe una cantidad exagerada de props o maneja demasiados estados independientes, lo detectamos como un síntoma claro y lo separamos en piezas más pequeñas.
2. **Evitar lógica condicional compleja (*Switch* o *If* anidados):** Si un componente o función está lleno de condiciones anidadas para decidir qué renderizar o ejecutar, refactorizamos usando mapas de opciones o componentes polimórficos limpios.
3. **Erradicar efectos secundarios ocultos:** Nos aseguramos de que los `useEffect` o funciones de nuestros componentes no modifiquen datos globales de forma imprevista o realicen acciones colaterales difíciles de rastrear.
4. **Limpiar dependencias y archivos huérfanos:** Revisamos periódicamente nuestras importaciones para eliminar librerías que ya no usamos, evitando inflar el paquete final (*bundle*) de nuestra aplicación frontend.