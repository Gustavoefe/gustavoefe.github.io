# Tambo Cumple

[**Abrir la aplicación**](https://gustavoefe.github.io/)

Versión web 1.0.1 para registro y seguimiento de casos, caravanas, tablero comunal e indicadores. Incluye castellano/Runasimi, glosario, audio, impresión e intercambio de casos mediante JSON y CSV.

## Uso

Abre el enlace en un navegador actual. Después de la primera carga completa, la aplicación puede trabajar sin conexión. Usa siempre la misma dirección y perfil del navegador para recuperar tus registros.

Los datos se guardan en cada navegador. No hay sincronización automática entre equipos. Para transferir casos, utiliza la exportación e importación JSON de la aplicación; el glosario se transfiere por separado. Los audios, caravanas personalizadas y catálogos no están incluidos en ese respaldo de casos.

Es un prototipo de prueba y capacitación con datos ficticios y perfiles simulados, sin autenticación ni servidor central.

## Publicación

Los archivos de la aplicación se sirven desde la raíz mediante GitHub Pages. El archivo `.nojekyll` permite publicarlos como archivos estáticos. La configuración es la rama `main` y la carpeta `/(root)`.

Los avisos de dependencias se conservan en [licencias](licencias/). [LEEME.md](LEEME.md) contiene la guía general de distribución, incluidas las instrucciones para la versión portátil de Windows; esa versión es un paquete separado.
