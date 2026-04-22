Configurar Firebase para Flutter es un paso fundamental para profesionalizar tu flujo de trabajo. Aquí tienes la guía técnica para preparar tu entorno desde cero.

---

## 1. Software Necesario: Node.js y NPM

Para usar la Firebase CLI, necesitas **Node.js**, el cual incluye automáticamente **NPM** (Node Package Manager).

### Cómo verificar si ya están instalados
Abre tu terminal (PowerShell, CMD o Terminal de macOS/Linux) y ejecuta:

* **Para Node.js:** `node -v`
* **Para NPM:** `npm -v`

> **Versión recomendada:** Se sugiere utilizar la versión **LTS (Long Term Support)** actual. A día de hoy, cualquier versión superior a la v18.x es adecuada para Firebase Tools.

---

## 2. Instalación de Node.js (Paso a paso)

Si los comandos anteriores fallaron, sigue estos pasos:

1.  **Descarga:** Ve al sitio oficial [nodejs.org](https://nodejs.org/) y selecciona la versión **LTS**.
2.  **Instalación:** Ejecuta el instalador descargado.
    * **Importante:** Durante la instalación en Windows, asegúrate de marcar la casilla que dice *"Automatically install the necessary tools"* (esto configura las variables de entorno o `PATH`).
3.  **Reinicio:** Una vez finalizado, **reinicia tu terminal** (o tu computadora) para que los cambios surtan efecto.
4.  **Verificación:** Vuelve a ejecutar `node -v` y `npm -v` para confirmar.

---

## 3. Instalación Global de Firebase CLI

Una vez que NPM funciona, instalaremos las herramientas de Firebase de forma global para que puedas usarlas en cualquier carpeta de tu sistema.

### El comando de instalación:
Ejecuta el siguiente comando en tu terminal:

```bash
npm install -g firebase-tools
```

* **-g:** Indica que la instalación es **global**.
* **Error común (macOS/Linux):** Si recibes un error de "Permisos denegados", usa `sudo npm install -g firebase-tools`.

### Verificar la instalación:
Para comprobar que la CLI está lista, escribe:
```bash
firebase --version
```

---

## 4. Acceso a Firebase con tu cuenta de Google

Para que la consola de tu computadora "hable" con tus proyectos de Firebase en la nube, debes autenticarte.

### Comando de Login:
Escribe en la terminal:
```bash
firebase login
```

1.  La terminal te preguntará si quieres permitir que Firebase recopile información de error (puedes poner `Y` o `N`).
2.  Se abrirá automáticamente una ventana en tu **navegador web**.
3.  Selecciona tu cuenta de Google asociada a Firebase Console.
4.  Haz clic en **"Permitir"**.
5.  Al finalizar, verás un mensaje de éxito en la terminal: `Success! Logged in as usuario@gmail.com`.

---

## 5. Comandos esenciales de Firebase Tools

Ahora que estás logueado, estos son los comandos que más usarás en el desarrollo con Flutter:

| Comando | Propósito |
| :--- | :--- |
| `firebase projects:list` | Muestra todos los proyectos que tienes en Firebase Console. |
| `firebase login:logout` | Cierra la sesión de tu cuenta en la CLI. |
| `firebase init` | Configura un nuevo proyecto de Firebase en la carpeta actual. |
| `firebase deploy` | Sube tus reglas de seguridad o funciones de Cloud Functions a la nube. |

---

### Siguiente paso para Flutter:
Para conectar esto específicamente con Flutter de la manera moderna, una vez que tengas la CLI instalada, el siguiente paso suele ser instalar el **FlutterFire CLI** ejecutando:
`dart pub global activate flutterfire_cli`

¿Deseas que te explique cómo vincular este entorno con tu código de Flutter usando `flutterfire configure`?
