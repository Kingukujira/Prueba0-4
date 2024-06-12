# Diagrama de Proceso para Crear una Nueva Nota

```mermaid
flowchart TD
    A[Usuario escribe una nota y hace clic en "Save"] --> B[El navegador captura el evento de clic]
    B --> C[El navegador envía una solicitud HTTP POST al servidor con la nueva nota]
    C --> D[El servidor recibe la solicitud y guarda la nota]
    D --> E[El servidor responde con una redirección a /exampleapp/notes]
    E --> F[El navegador sigue la redirección y solicita la página de notas]
    F --> G[El servidor responde con el HTML de la página de notas]
    G --> H[El navegador carga el HTML y solicita los recursos adicionales (CSS, JavaScript)]
    H --> I[El navegador ejecuta el JavaScript y solicita los datos JSON de las notas]
    I --> J[El servidor responde con los datos JSON]
    J --> K[El navegador procesa los datos JSON y actualiza el DOM para mostrar las notas, incluida la nueva nota]
