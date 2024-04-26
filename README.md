<header>

# Hola GitHub Actions

_Crea y ejecuta un flujo de trabajo de GitHub Actions._

</header>

## Paso 1: Crear un archivo de flujo de trabajo

_¡Bienvenido a "Hola GitHub Actions"! :wave:_

**¿Qué es _GitHub Actions_?**: GitHub Actions es una forma flexible de automatizar casi todos los aspectos del flujo de trabajo de software de tu equipo. Puedes automatizar pruebas, implementaciones continuas, revisar código, gestionar problemas y Pull Requests, y mucho más. La mejor parte es que estos flujos de trabajo se almacenan como código en tu repositorio y se pueden compartir y reutilizar fácilmente entre equipos. Para obtener más información, consulta estos recursos:

- La página de Actions de GitHub Actions, consulta [GitHub Actions](https://github.com/features/actions).
- La documentación de usuario de "GitHub Actions", consulta [GitHub Actions](https://docs.github.com/actions).

**¿Qué es un _flujo de trabajo_?**: Un flujo de trabajo es un proceso automatizado configurable que ejecutará uno o más trabajos. Los flujos de trabajo se definen en archivos especiales en el directorio `.github/workflows` y se ejecutan en función del evento que elijas. Para este ejercicio, utilizaremos un evento `pull_request`.

- Para obtener más información sobre flujos de trabajo, trabajos y eventos, consulta "[Entendiendo GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)".
- Si quieres aprender más sobre el evento `pull_request` antes de usarlo, consulta "[pull_request](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#pull_request)".

Para empezar, ejecutamos un flujo de trabajo de Actions en tu nuevo repositorio que, entre otras cosas, creó una rama para que trabajes en ella, llamada `welcome-workflow`.

### :keyboard: Actividad: Crear un archivo de flujo de trabajo

1. Abre una nueva pestaña del navegador y navega hasta este mismo repositorio. Luego, trabaja en los pasos en tu segunda pestaña mientras lees las instrucciones en esta pestaña.
1. Crea una solicitud de extracción. Esto contendrá todos los cambios que realizarás en esta parte del curso.

   Haz clic en la pestaña **Pull Requests**, haz clic en **New pull request**, establece `base: spanish` y `compare:welcome-workflow`, haz clic en **Create pull request**, luego haz clic en **Create pull request** nuevamente.

1. Navega hasta la pestaña **Código**.
1. Desde el menú desplegable de la rama **spanish**, haz clic en la rama **welcome-workflow**.
1. Navega hasta la carpeta `.github/workflows/`, luego selecciona **Agregar archivo** y haz clic en **Crear nuevo archivo**.
1. En el campo **Nombrar tu archivo**, ingresa `welcome.yml`.
1. Agrega el siguiente contenido al archivo `welcome.yml`:

   ```yaml copy
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   ```

1. Para confirmar tus cambios, haz clic en **Commit changes**.
2. Escribe un mensaje de confirmación, selecciona **Confirmar directamente en la rama welcome-workflow** y haz clic en **Commit changes**.
3. Espera aproximadamente 20 segundos, luego actualiza esta página (la que estás siguiendo las instrucciones). Un flujo de trabajo de Actions separado en el repositorio (no el flujo de trabajo que creaste) se ejecutará y reemplazará automáticamente el contenido de este archivo README con instrucciones para el próximo paso.


<footer>

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/hello-github-actions) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2023 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
