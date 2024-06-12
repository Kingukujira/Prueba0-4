flowchart TD
    A[Usuario escribe una nota y hace clic en "Save"] -->|B|
    B[El navegador captura el evento de clic] -->|C|
    C[El navegador envía una solicitud HTTP POST al servidor con la nueva nota] -->|D|
    D[El servidor recibe la solicitud y guarda la nota] -->|E|
    E[El servidor responde con una redirección a /exampleapp/notes] -->|F|
    F[El navegador sigue la redirección y solicita la página de notas] -->|G|
    G[El servidor responde con el HTML de la página de notas] -->|H|
    H[El navegador carga el HTML y solicita los recursos adicionales (CSS, JavaScript)] -->|I|
    I[El navegador ejecuta el JavaScript y solicita los datos JSON de las notas] -->|J|
    J[El servidor responde con los datos JSON] -->|K|
    K[El navegador procesa los datos JSON y actualiza el DOM para mostrar las notas, incluida la nueva nota] -->|L|
