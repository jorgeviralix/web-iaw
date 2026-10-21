# web-iaw

Práctica de Git y GitHub para la asignatura de Implantación de Aplicaciones Web (IAW), 2.º ASIR, SAFA Andújar.

## Descripción
Proyecto web sencillo construido con HTML y CSS que sirve para practicar el flujo completo de Git: crear repositorio local, hacer commits, publicar en GitHub, trabajar con ramas, resolver conflictos y usar Issues y Pull Requests.

## Contenido del proyecto
- `index.html` — Página principal.
- `contacto.html` — Página de contacto.
- `servicios.html` — Página con la lista de servicios.
- `sobre-mi.html` — Página personal del autor.
- `estilos.css` — Hoja de estilos del proyecto.
- `.gitignore` — Reglas para que Git ignore `.env` y archivos `*.log`.

## Requisitos
- Git instalado
- Un editor de código (Visual Studio Code)
- Cuenta de GitHub

## Instalación
Clonar el repositorio con `git clone git@github.com:jorgeviralix/web-iaw.git`

## Ejecución
Abrir `index.html` en el navegador.

## Uso de IA en el proyecto

Durante el desarrollo se ha utilizado la IA (Claude Pro conectado a GitHub) en dos momentos clave:

**1. Interpretar la salida de `git status` y revisar cambios antes de commitear.**
Pedí a la IA que explicara una salida de `git status` y propusiera el siguiente paso más seguro. La IA identificó los archivos preparados y los sin seguimiento, y recomendó usar `git diff --staged` para revisar los cambios antes del commit. Decidí seguir su consejo porque me permite ver exactamente qué va a entrar en el próximo commit y evitar subir archivos no deseados.

**2. Decidir dónde crear la sección "Sobre mí".**
Pedí a la IA que me propusiera qué archivo tenía más sentido modificar o crear para añadir una sección "Sobre mí". La IA recomendó crear un archivo nuevo (`sobre-mi.html`) en lugar de meterlo en `index.html`, justificando que el proyecto sigue el patrón de "una página por tema" (`contacto.html`, `servicios.html`). Acepté la propuesta porque mantiene la coherencia del proyecto y permite practicar el flujo completo (rama, commit, merge) con un cambio bien aislado.

## Decisiones tomadas
- Rama por defecto: `main` (en vez de `master`), para coincidir con el estándar actual de GitHub.
- Autenticación por SSH para no tener que meter contraseña en cada push.
- Un archivo HTML por sección para mantener la estructura limpia.
- Mensajes de commit descriptivos, enlazando con Issues cuando corresponde (por ejemplo, `Añade página de servicios (#1)`).
- Uso de ramas de funcionalidad (`feature/contacto`, `feature/servicios`) para cambios no triviales, con Pull Request para integrarlas en `main`.
- `.gitignore` configurado desde el principio para que `.env` y los `*.log` nunca lleguen al remoto.

## Autoría
Jorge de la Fuente Gutiérrez — 2.º ASIR