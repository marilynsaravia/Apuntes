# Introducción a HTML5

HTML5 es la versión actual del lenguaje de marcado utilizado para estructurar contenido en la web.  
Su objetivo es ofrecer una estructura más semántica, accesible y compatible con dispositivos modernos.

## ¿Qué es HTML5?

HTML5 (HyperText Markup Language 5) es un **lenguaje de marcado** que define el contenido y la estructura de una página web.  
Incluye nuevas etiquetas, APIs nativas y mejoras respecto a versiones anteriores.

## Estructura básica de un documento en HTML5

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documento HTML5</title>
  </head>

  <body>
    <!-- Contenido visible por el usuario -->
  </body>
</html>

```

## Explicación de la estructura HTML5

A continuación se detalla cada parte del documento base en HTML5:

### `<!DOCTYPE html>`
Indica al navegador que el documento está escrito en **HTML5**.  
Ayuda a que el navegador interprete correctamente el contenido.

---

### `<html lang="es">`
Es el elemento **raíz** del documento HTML.  
El atributo `lang="es"` indica que el contenido está en español, lo que mejora:

- la accesibilidad
- la optimización SEO
- el funcionamiento de lectores de pantalla

---

### `<head>`
El `<head>` contiene información **no visible** directamente en la página.  
Incluye elementos como:

- metadatos
- enlaces a hojas de estilo (CSS)
- iconos
- scripts que deben cargarse antes del cuerpo
- título del documento

---

### `<meta charset="UTF-8">`
Define la **codificación de caracteres** del documento.  
`UTF-8` permite usar letras con tilde, ñ, símbolos y emojis sin problemas.

---

### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
Hace que la página sea **responsive**.  
Indica al navegador que:

- el ancho de la pantalla se adapte al dispositivo (`width=device-width`)
- el nivel de zoom inicial sea 1 (`initial-scale=1.0`)

Sin este meta, una web puede verse gigante o muy pequeña en móvil.

---

### `<title>`
Define el **título de la pestaña** en el navegador.  
También influye en SEO y en accesibilidad.

---

### `<body>`
Contiene todo el **contenido visible** por el usuario:

- texto
- imágenes
- botones
- estructuras semánticas (`header`, `nav`, `section`, `footer`, etc.)
- formularios
- componentes interactivos

El navegador **representa en pantalla** todo lo que está dentro del `<body>`.

---
