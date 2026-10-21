# Carnicería · Directorio de clientes

Página web de una sola pieza (`index.html`, sin instalar nada) para guardar y buscar clientes de una carnicería en Culiacán, Sinaloa.

- Busca por teléfono (10 dígitos), parte del número o nombre.
- Si el número no existe, aparece el botón **Registrar**.
- Colonias de Culiacán con código postal automático.
- Pestaña **Todos** con la base de datos completa, filtros y exportar a Excel (CSV).
- Pestaña **Resumen** con estadísticas.
- Botón para mandar los datos del cliente por WhatsApp al número que elijas.
- Se ve bien en celular, tablet y laptop.

## Cómo publicarla en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `carniceria`).
2. Sube **todos** los archivos (`index.html`, `sw.js`, `manifest.webmanifest`, `icon.svg` y este `README.md`) a la rama `main`.
3. Entra a **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
5. En uno o dos minutos la página queda en `https://TU-USUARIO.github.io/carniceria/`.

## Con datos móviles o sin señal

La página no depende de ningún servicio externo para abrir. La primera vez necesita internet. Después el teléfono la guarda y abre aunque no haya señal.
Para que funcione así, `sw.js` tiene que estar subido junto con `index.html`.
Cuando subas una versión nueva, ábrela dos veces para que se actualice.

## Dónde se guardan los datos

Los clientes se guardan en el navegador de cada dispositivo (localStorage). Eso significa que el celular y la laptop **no comparten** la lista automáticamente.

Para pasar los clientes de un dispositivo a otro usa los botones **Respaldo** (descarga un archivo .json) y **Restaurar** (lo carga en el otro dispositivo).

Si borras los datos del navegador se pierde la lista, así que haz un respaldo de vez en cuando.

Para una base de datos compartida entre todos los dispositivos se necesita un servicio como Firebase o Supabase.
