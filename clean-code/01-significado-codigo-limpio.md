# 01. Código Limpio: El Significado

> *"El código limpio siempre parece que fue escrito por alguien a quien le importa."* — Michael Feathers

## Idea Principal
Escribir código limpio no es solo una cuestión de estética, es una cuestión de supervivencia y escalabilidad del proyecto. El mal código (conocido como "el lodo") ralentiza el desarrollo, lo que parece rápido de hacer hoy, hará que todo sea más lento mañana.

## Conceptos Clave

* **La trampa de "lo limpio después":** Todos hemos dicho *"sé que es un desastre, pero luego lo arreglo"*. El problema es que la Ley de LeBlanc no perdona: **"Después significa nunca"**.
* **Lectura vs. Escritura:** Como desarrolladores, pasamos mucho más tiempo leyendo código antiguo que escribiendo código nuevo (la proporción es de 10 a 1). Hacer que el código sea fácil de leer ahorra horas de frustración.
* **El coste del caos:** A medida que el desorden crece, la productividad del equipo tiende a cero. La única forma real de ir rápido en un proyecto es mantener el código limpio desde el primer día.

## La Regla del Boy Scout (Fundamental)
> *"Deja el campamento un poco más limpio de lo que lo encontraste."*

No basta con escribir buen código hoy; tenemos que evitar que se degrade. Si abrimos un archivo para arreglar un bug o añadimos un feature, y vemos una variable mal nombrada o una función confusa, **lo arréglaremos en ese momento**. El código debe mejorar con el paso del tiempo, no pudrirse.

## Aplicación Práctica en Frontend
Como desarrolladores frontend, podemos aplicar esta filosofía directamente en proyectos con React y JavaScript de la siguiente manera:

1. **Evita el código zombi:** No dejaremos bloques enteros de componentes o lógica comentados "por si acaso". Para recuperar versiones anteriores ya tienes Git.
2. **Cero basura visual:** Eliminaremos los `console.log()` antes de hacer un commit o subir código a producción. Mantendremos los archivos lo más limpios y minimalistas posible.
3. **Consistencia en la nomenclatura:** Mantendremos un criterio claro y unificado al nombrar componentes, variables y funciones (por ejemplo, usaremos inglés de forma consistente o seguir la misma convención de nombres para archivos y carpetas).
4. **Refactorización constante:** Si abrimos un archivo de un componente de React que hicimos hace meses y cuesta entenderlo, aprovecharemos para renombrar un par de variables o simplificar un condicional.