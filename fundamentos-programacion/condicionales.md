# 🧠 Fundamentos: Condicionales

Los condicionales son estructuras que permiten que el programa tome decisiones. Se basan en evaluar si una condición es `true` o `false`.

---

## 1. Operadores de Comparación
Se usan para comparar valores:
* `===` : Igualdad estricta (valor y tipo).
* `!==` : Diferente de.
* `>` / `<` : Mayor o menor que.
* `>=` / `<=` : Mayor o igual / Menor o igual.

## 2. Tipos de Condicionales

### 🚩 Estructura `if / else`
Es el estándar para tomar decisiones basadas en una o varias condiciones.

```typescript
let puntos = 85;

if (puntos >= 90) {
    console.log("Excelente");
} else if (puntos >= 70) {
    console.log("Aprobado");
} else {
    console.log("Reprobado");
}
```

# 🗺️ Diagramas de Flujo y Lógica

El diagrama de flujo es la representación gráfica de un **algoritmo**. En programación, antes de tocar el teclado, solemos pensar en estos símbolos para entender los condicionales.

---

## 1. Simbología Básica
Para entender condicionales, estos son los 3 símbolos que debes conocer:

| Símbolo | Nombre | Función en Código |
| :--- | :--- | :--- |
| **Óvalo** | Inicio / Fin | Inicio o cierre del programa/función. |
| **Rectángulo** | Proceso | Asignación de variables (ej: `x = 10`). |
| **Rombo** | **Decisión** | Representa el `if`. Tiene una entrada y dos salidas (Sí / No). |

<img width="395" height="500" alt="image" src="https://github.com/user-attachments/assets/5aeaf1d8-464f-4e99-9642-406e15145dfd" />


---

## 2. El Rombo: El corazón del condicional
En un diagrama, el rombo es donde ocurre la magia del `if`. 

### Ejemplo Visual (Lógica):
1. **Inicio**
2. **Proceso:** Leer `edad`.
3. **Decisión (Rombo):** ¿Es `edad >= 18`?
    * **SÍ (Camino A):** Imprimir "Puedes pasar".
    * **NO (Camino B):** Imprimir "Acceso denegado".
4. **Fin**

---

## 3. Relación Directa con el Código

Lo que dibujas en el papel se traduce así a **TypeScript**:

| En el Diagrama | En el Código |
| :--- | :--- |
| El interior del rombo | La condición dentro del `if ( ... )` |
| La flecha del "SÍ" | El bloque de código `{ ... }` |
| La flecha del "NO" | El bloque `else { ... }` |

---

## 4. Ejemplo de Lógica Compleja (Anidada)
Cuando tienes un rombo después de otro, en código se llama **if anidado**.

**Diagrama de un login:**
1. ¿Usuario existe?
   - **NO:** "Error: Usuario no encontrado".
   - **SÍ:** ¿Contraseña correcta?
     - **NO:** "Error: Password incorrecto".
     - **SÍ:** "Bienvenido al sistema".

```typescript
if (usuarioExiste) {
    if (passwordCorrecto) {
        console.log("Bienvenido");
    } else {
        console.log("Password incorrecto");
    }
} else {
    console.log("Usuario no encontrado");
}
