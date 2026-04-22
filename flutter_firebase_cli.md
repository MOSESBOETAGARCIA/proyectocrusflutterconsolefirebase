Para convertirte en un experto creador de software, el manejo de la terminal y las herramientas de línea de comandos (CLI) es vital. Aquí tienes la guía técnica paso a paso para configurar el entorno de Firebase y Node.js de manera profesional.

---

## 1. Verificación de Node.js y npm
Antes de instalar nada, debemos auditar el sistema para ver si ya contamos con las herramientas. **npm** (Node Package Manager) viene incluido siempre con **Node.js**.

Para verificar, abre tu terminal (CMD, PowerShell o Terminal de VS Code) y ejecuta:

* **Para Node.js:** `node -v`
* **Para npm:** `npm -v`

> Si el sistema responde con una versión (ej. `v20.10.0`), ya lo tienes. Si dice *"no se reconoce como un comando interno"*, procede al paso 2.

---

## 2. Instalación de Node.js (Paso a paso)
Si no lo tienes instalado, sigue este procedimiento:

1.  **Descarga:** Ve al sitio oficial [nodejs.org](https://nodejs.org/).
2.  **Versión Recomendada:** Selecciona la versión **LTS** (Long Term Support). Es la más estable para desarrollo profesional.
3.  **Instalador:** Ejecuta el archivo `.msi` (Windows) o `.pkg` (Mac).
4.  **Configuración Clave:** Durante la instalación, asegúrate de que la casilla **"Add to PATH"** esté marcada. Esto permite que los comandos funcionen en cualquier carpeta.
5.  **Finalización:** Al terminar, **reinicia tu terminal** para que reconozca los nuevos caminos del sistema.

---

## 3. Instalación Global de Firebase CLI
Una vez que `npm` funciona, instalaremos las herramientas de Firebase de forma **global**. Esto significa que podrás usar el comando `firebase` en cualquier proyecto de Flutter sin importar la carpeta.

Ejecuta el siguiente comando:

```bash
npm install -g firebase-tools
```

* **-g**: Es la bandera de "global".
* **firebase-tools**: Es el nombre oficial del paquete que contiene el CLI.

---

## 4. Uso de Comandos y Autenticación

### A. Cómo usar Firebase Tools
Las `firebase-tools` te permiten administrar tu base de datos Firestore, reglas de seguridad y hosting desde la consola. Los comandos principales que usarás como desarrollador son:

* `firebase list`: Muestra todos los proyectos que tienes en tu consola de Firebase.
* `firebase init`: Inicia la configuración de Firebase en tu carpeta de Flutter (vincula el proyecto local con la nube).
* `firebase deploy`: Sube tus reglas de seguridad o funciones a la nube.

### B. Cómo acceder con tu cuenta de Google
Para que tu computadora tenga permiso de modificar tus proyectos de Firebase, debes "loguearte" mediante el navegador:

1.  En la terminal, escribe:
    ```bash
    firebase login
    ```
2.  **Interacción:** La terminal te preguntará si permites recopilar información de error (puedes poner `Y` o `N`).
3.  **Navegador:** Se abrirá automáticamente una pestaña de Google Chrome/Edge.
4.  **Selección:** Elige tu cuenta de Gmail donde creaste el proyecto del Barbero.
5.  **Permitir:** Haz clic en "Permitir".
6.  **Confirmación:** Verás un mensaje que dice: *"Success! Logged in as tu-correo@gmail.com"*.



---

## 5. El toque final para Flutter (FlutterFire)
Como estás trabajando en Flutter, después de lo anterior, el estándar actual de la industria es usar el **FlutterFire CLI** para configurar automáticamente los archivos de Firebase en Dart:

1.  Instala el activador: `dart pub global activate flutterfire_cli`
2.  Ejecuta la configuración: `flutterfire configure`

Esto generará el archivo `firebase_options.dart` automáticamente, evitando que tengas que copiar y pegar códigos manualmente en Android e iOS.

¿Lograste completar el login de Firebase o te apareció algún error de "permisos de ejecución" en la terminal?
