# 02. Nombres con Sentido

> *"El nombre de una variable, función o clase debe responder a todas las grandes preguntas. Debe decirte por qué existe, qué hace y cómo se usa. Si un nombre requiere un comentario para ser entendido, no revela su intención."* — Robert C. Martin

## Idea Principal
Elegir buenos nombres nos llevará tiempo, pero **ahorra mucho más tiempo del que consume**. Los nombres malos obligan a adivinar y generan confusión mental, haciendo que el código sea difícil de mantener y propenso a errores.

## Reglas Clave para Nombres
* **Usa nombres que revelen intenciones:** Si una variable se llama `d`, no dice nada. Si se llama `elapsedTimeInDays`, su propósito es evidente al instante.
* **Evita la desinformación:** No usaremos nombres que confundan el significado real. Por ejemplo, no llamaremos `accountList` a un grupo de cuentas a menos que sea literalmente una estructura de datos `List`. Si es un array genérico o un objeto, mejor `accounts`.
* **Haz distinciones con sentido:** Evitaremos nombres redundantes o ruidosos como `variableData`, `userInfo` (si `user` ya es suficiente) o numeraciones arbitrarias (`a1`, `a2`).
* **Usa nombres pronunciables y buscables:** Si no podemos pronunciarlo, no podemos comentarlo en una charla técnica. Además, las letras o números sueltos (`e`, `j`) son imposibles de buscar eficientemente en nuestro editor de código.

## Aplicación Práctica en Frontend (React & JavaScript)
Como desarrolladores frontend, podemos aplicar estas reglas al nombrar elementos de nuestra interfaz y lógica:

1. **Prefijos claros para funciones manejadoras (*Handlers*):** Usaremos verbos o prefijos estándar en la comunidad para eventos, como `handleClick`, `onSubmit`, o `toggleModal`, en lugar de nombres ambiguos como `action` o `doSomething`.
2. **Nombres booleanos como preguntas:** Los estados o variables que solo guardan `true` o `false` deben leerse como una pregunta afirmativa. Por ejemplo: `isVisible`, `isLoading`, `hasError` o `isLoggedIn`.
3. **Componentes como sustantivos:** Los componentes de React representan entidades o elementos visuales, por lo que deben nombrarse con sustantivos limpios (PascalCase), como `UserProfile`, `NavigationMenu` o `SubmitButton`.
4. **Constantes globales en mayúsculas:** Para valores fijos que no cambian (como endpoints de una API o configuraciones), usa mayúsculas separadas por guiones bajos, por ejemplo: `MAX_VISIBLE_ITEMS` o `API_BASE_URL`.