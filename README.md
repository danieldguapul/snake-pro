# Plantilla Phaser Vite TypeScript

Esta es una plantilla de proyecto **Phaser 3** que utiliza **Vite** para el empaquetado. Soporta recarga en caliente (hot-reloading) para un flujo de desarrollo rápido, incluye soporte para **TypeScript** y scripts para generar builds listos para producción.

**Esta plantilla también está disponible en versión JavaScript.**

### Versiones

Esta plantilla ha sido actualizada para:

- [Phaser 3.90.0](https://github.com/phaserjs/phaser)
- [Vite 6.3.1](https://github.com/vitejs/vite)
- [TypeScript 5.7.2](https://github.com/microsoft/TypeScript)

## Requisitos

Se requiere [Node.js](https://nodejs.org) para instalar dependencias y ejecutar scripts mediante `npm`.

## Comandos disponibles

| Comando              | Descripción                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `npm install`        | Instala las dependencias del proyecto                                       |
| `npm run dev`        | Inicia un servidor web de desarrollo                                        |
| `npm run build`      | Crea un build de producción en la carpeta `dist`                            |
| `npm run dev-nolog`  | Inicia el servidor de desarrollo sin enviar datos anónimos (ver "Sobre log.js" más abajo) |
| `npm run build-nolog`| Crea un build de producción sin enviar datos anónimos                       |

## Escribir código

Después de clonar el repositorio, ejecuta `npm install` desde el directorio del proyecto. Luego, puedes iniciar el servidor de desarrollo local con `npm run dev`.

El servidor de desarrollo se ejecuta por defecto en `http://localhost:8080`. Consulta la documentación de Vite si deseas cambiar este puerto o agregar soporte SSL.

Una vez que el servidor esté corriendo, puedes editar cualquier archivo en la carpeta `src`. Vite recompilará automáticamente tu código y recargará el navegador.

## Estructura del proyecto de la plantilla

Hemos proporcionado una estructura de proyecto predeterminada para que puedas comenzar rápidamente:

| Ruta                     | Descripción                                                              |
|--------------------------|--------------------------------------------------------------------------|
| `index.html`             | Una página HTML básica que contiene el juego                             |
| `public/assets`          | Sprites del juego, audio, etc. Servidos directamente en tiempo de ejecución |
| `public/style.css`       | Estilos globales de layout                                               |
| `src/main.ts`            | Punto de entrada de la aplicación                                        |
| `src/game`               | Carpeta que contiene el código del juego                                 |
| `src/game/main.ts`       | Punto de entrada del juego: configura e inicia Phaser                    |
| `src/game/scenes`        | Carpeta con todas las escenas del juego Phaser                           |

## Manejo de assets

Vite permite cargar assets mediante sentencias `import` en JavaScript.

Esta plantilla soporta tanto la inclusión de assets embebidos como la carga desde una carpeta estática. Para embeber un asset, puedes importarlo al inicio del archivo JavaScript donde lo uses:

```ts
import logoImg from './assets/logo.png'
