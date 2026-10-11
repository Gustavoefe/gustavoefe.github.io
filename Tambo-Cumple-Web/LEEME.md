# Tambo Cumple — distribución 1.0.1

Esta distribución parte del proyecto original encontrado en el equipo. Conserva sus pantallas, datos de demostración y funcionamiento local.

## Abrir en Windows

1. Extrae **todo** el archivo ZIP en una carpeta del equipo.
2. Dentro de **Tambo Cumple**, abre **Iniciar.cmd**.
3. Se abre el navegador en **http://127.0.0.1:3000/**. Mantén abierta la ventana del lanzador mientras trabajas.
4. Para detener el servidor, cierra esa ventana o pulsa Ctrl+C.

Incluye Node.js 24.19.0 para Windows x64. No requiere instalar Node.js, descargar paquetes ni tener conexión a Internet para arrancar. Requiere un navegador actual; las pruebas se realizaron con Google Chrome en Windows. Si el puerto 3000 lo usa otra aplicación, el lanzador te lo indica. No cambia automáticamente de dirección.

## Funciones conservadas

- Inicio y perfiles simulados de gestor, entidad prestadora y Unidad Territorial.
- Caravanas, apertura de casos, consentimiento, plazos, semáforo, bandeja, búsqueda e historial.
- Tablero comunal e indicadores.
- Castellano/Runasimi, glosario editable y grabación/reproducción de mensajes de audio.
- Constancia bilingüe A5 y afiche comunal A4 horizontal.
- Intercambio de casos mediante JSON y exportación CSV.
- Almacenamiento en el navegador y funcionamiento sin conexión.

## Dónde quedan los datos

Los datos se guardan en el navegador y perfil utilizados para **http://127.0.0.1:3000/**. No se guardan dentro del ZIP ni en la carpeta portátil. Copiar esa carpeta a otro equipo no copia tus registros.

Usa siempre el mismo navegador, perfil y dirección. **localhost:3000** es un origen distinto de **127.0.0.1:3000**. Si antes usabas esta última dirección con el mismo perfil, la copia conserva la misma base de datos y su esquema. Las verificaciones de esta distribución se hicieron con un perfil de prueba aislado.

Para transferir casos, abre el botón de sincronización del encabezado, exporta JSON e impórtalo en el otro equipo. Esta versión exporta todos los casos, incluidos los ya sincronizados. Conserva el archivo de respaldo aparte. El CSV es un informe y no se importa como respaldo.

El paquete de casos **no incluye audios, caravanas personalizadas, catálogos ni el glosario**. El glosario tiene su propia exportación/importación. Las grabaciones permanecen en el navegador donde se crearon. No borres los datos del sitio ni uses navegación privada si necesitas conservarlos.

## Alcance del original

Es un prototipo para prueba y capacitación con datos ficticios, con perfiles simulados y sin autenticación. No incluye servidor central, sincronización automática entre equipos, SMS ni WhatsApp. Las traducciones quechuas mantienen su estado de validación del original; algunos textos auxiliares permanecen en castellano. No se afirma que el selector de perfil sea un control de acceso de producción.

Al iniciar por primera vez se cargan datos de demostración. El botón de cargar demostración vuelve a insertar esos ejemplos y puede reemplazar cambios hechos sobre ellos.

## Ajustes de esta distribución

- Lanzador portátil y servidor limitado al propio equipo.
- Iconos locales completos para la aplicación instalable.
- Impresión aislada del fondo de la pantalla.
- Exportación de todos los casos y rechazo de paquetes incompletos.
- Conservación de eventos de operadores distintos en la fusión de historiales.
- Identificadores internos aleatorios para nuevos casos y caravanas.
- Glosario personalizado aplicado también tras recargar.

## Código fuente y versión web

El ZIP de código fuente incluye el archivo de dependencias fijadas y las pruebas.

```text
pnpm install --frozen-lockfile
pnpm test
pnpm build
pnpm package:portable
```

El empaquetado portátil exige Windows x64 y Node.js 24.19.0 para corresponder con la licencia incluida. Genera la carpeta release/Tambo Cumple. Para volver a distribuir, comprime esa carpeta completa.

El ZIP web contiene los archivos compilados para servir desde la raíz de un sitio. Para instalación y uso offline fuera del propio equipo, el alojamiento debe ofrecer HTTPS. No es un APK de Android. La versión portátil Windows y la versión web tienen la misma interfaz.

## Licencias

Se incluyen la [licencia de Node.js 24.19.0](https://raw.githubusercontent.com/nodejs/node/v24.19.0/LICENSE) y los avisos de dependencias en la carpeta licencias. Los avisos de terceros no asignan una licencia nueva al código de la aplicación original.

