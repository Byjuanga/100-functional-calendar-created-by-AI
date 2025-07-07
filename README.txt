MiCalendarioApp

Descripción:
MiCalendarioApp es una aplicación de calendario y gestión de tareas simple y local, construida con HTML, Tailwind CSS y JavaScript puro. Ahora, ha sido empaquetada como una aplicación de escritorio utilizando Electron, lo que permite su ejecución nativa en Windows, macOS y Linux.

Características:
- Navegación por los meses.
- Añadir y gestionar notas/tareas para días específicos.
- Marcar tareas como completadas y eliminarlas.
- Gestionar tareas generales mensuales y metas anuales.
Los datos se guardan localmente en el almacenamiento del navegador (localStorage) dentro de la aplicación de escritorio.

Instalación y Uso (Versión de Escritorio):

Requisitos:
- Node.js y npm (Node Package Manager) instalados.
- Git (opcional, para clonar el repositorio).

1. Clonar el Repositorio:
   Abre tu terminal o línea de comandos y ejecuta:
   ```bash
   git clone https://github.com/Byjuanga/100-functional-calendar-created-by-AI.git
   cd 100-functional-calendar-created-by-AI
   ```

2. Instalar Dependencias:
   Una vez dentro del directorio `100-functional-calendar-created-by-AI`, instala las dependencias de Node.js:
   ```bash
   npm install
   ```

3. Ejecutar la Aplicación (Modo Desarrollo):
   Para ejecutar la aplicación en modo desarrollo:
   ```bash
   npm start
   ```

Con eso la aplicacíon ya estaria funcionando si quieres tener un ejecutable en tu escritorio sigue leyendo y no tener que abir todo el rato con la terminal sigue leyendo...


4. Empaquetar la Aplicación (Para Distribución):
   Puedes crear ejecutables para diferentes plataformas. Asegúrate de tener las herramientas de compilación necesarias para cada plataforma (por ejemplo, Xcode para macOS, Visual Studio para Windows).

   - Para macOS:
     ```bash
     npm run package-mac
     ```
   - Para Windows:
     ```bash
     npm run package-win
     ```
   - Para Linux:
     ```bash
     npm run package-linux
     ```
   Los ejecutables se encontrarán en la carpeta `release-builds` dentro del directorio de tu proyecto.

5. Lanzar la Aplicación Empaquetada:

   - **Windows:** Navega a la carpeta `release-builds/micalendarioapp-win32-ia32` (o `x64` si empaquetaste para 64-bit) y haz doble clic en `micalendarioapp.exe`.

   - **macOS:** Navega a la carpeta `release-builds/micalendarioapp-darwin-x64` y haz doble clic en `micalendarioapp.app`.

   - **Linux:**
     1. Navega a la carpeta `release-builds/micalendarioapp-linux-x64`.
     2. Haz clic derecho en el archivo `micalendarioapp` (el ejecutable) y selecciona "Propiedades" o "Permisos". Asegúrate de que la opción "Permitir ejecutar el archivo como un programa" (o similar) esté marcada.
     3. Para crear un acceso directo con un icono en tu menú de aplicaciones, crea un archivo `.desktop` en `~/.local/share/applications/` (si no existe, crea la carpeta `applications`). Puedes hacerlo con el siguiente comando (asegúrate de reemplazar `/ruta/a/tu/proyecto` con la ruta real donde clonaste el repositorio):

        ```bash
        nano ~/.local/share/applications/micalendarioapp.desktop
        ```

        Pega el siguiente contenido en el archivo, **ajustando la ruta `Exec` e `Icon`** a la ubicación real de tu aplicación:

        ```
        [Desktop Entry]
        Name=MiCalendarioApp
        Comment=Aplicación de calendario y gestión de tareas
        Exec=/ruta/a/tu/proyecto/release-builds/micalendarioapp-linux-x64/micalendarioapp
        Icon=/ruta/a/tu/proyecto/assets/icon.png
        Terminal=false
        Type=Application
        Categories=Office;Calendar;
        ```

        Guarda el archivo (Ctrl+O, Enter, Ctrl+X en `nano`).

     4. Dale permisos de ejecución al archivo `.desktop`:
        ```bash
        chmod +x ~/.local/share/applications/micalendarioapp.desktop
        ```
     5. Es posible que necesites cerrar sesión y volver a iniciarla, o reiniciar tu sistema, para que el entorno de escritorio detecte el nuevo archivo `.desktop` y muestre el icono en el menú de aplicaciones.

Compatibilidad:
La aplicación empaquetada es compatible con:
- Windows (32-bit y 64-bit)
- macOS
- Linux (64-bit)

Cómo usar la aplicación:
- Navegación: Usa las flechas de "anterior" y "siguiente" en la parte superior izquierda para cambiar de mes.
- Notas Diarias: Haz clic en cualquier día del calendario para abrir el panel lateral. Aquí puedes añadir nuevas notas, marcarlas como completadas o eliminarlas.
- Tareas Generales: Haz clic en el botón "Tareas Generales" en la parte superior derecha para ver y gestionar tus tareas mensuales y metas anuales.

Persistencia de Datos:
Todas tus notas y tareas se guardan automáticamente en el almacenamiento local de la aplicación de escritorio. Esto significa que tus datos estarán disponibles la próxima vez que abras la aplicación.
