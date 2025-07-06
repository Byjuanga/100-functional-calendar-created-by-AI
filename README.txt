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
   git clone [ https://github.com/Byjuanga/100-functional-calendar-created-by-AI.git] # 
   cd MiCalendarioApp
   ```

2. Instalar Dependencias:
   Una vez dentro del directorio `MiCalendarioApp`, instala las dependencias de Node.js:
   ```bash
   npm install
   ```

3. Ejecutar la Aplicación (Modo Desarrollo):
   Para ejecutar la aplicación en modo desarrollo:
   ```bash
   npm start
   ```

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
   Los ejecutables se encontrarán en la carpeta `release-builds`.

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
