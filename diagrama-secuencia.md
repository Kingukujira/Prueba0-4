# Diagrama de Secuencia para Crear una Nueva Nota

```mermaid
sequenceDiagram
    participant user as Usuario
    participant browser as Navegador
    participant server as Servidor

    Note over user, browser: Usuario escribe una nota y hace clic en "Save"

    user->>browser: Click en "Save"
    browser->>server: HTTP POST /exampleapp/new_note con contenido de la nota
    server-->>browser: Respuesta HTTP (Redirección)

    Note over browser: El navegador redirige a /exampleapp/notes

    browser->>server: HTTP GET /exampleapp/notes
    server-->>browser: HTML de la página de notas

    Note over browser: El navegador carga el HTML y solicita los recursos adicionales (CSS, JavaScript)

    browser->>server: HTTP GET /exampleapp/main.css
    server-->>browser: main.css

    browser->>server: HTTP GET /exampleapp/main.js
    server-->>browser: main.js

    Note over browser: El navegador ejecuta main.js

    browser->>server: HTTP GET /exampleapp/data.json
    server-->>browser: data.json

    Note over browser: El navegador procesa data.json y actualiza el DOM para mostrar las notas, incluida la nueva nota
