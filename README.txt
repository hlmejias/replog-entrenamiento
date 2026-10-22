REPLOG — APP MÓVIL DE ENTRENAMIENTO
===================================

Qué incluye
- Registro de sesiones con fecha, notas, ejercicios, series, repeticiones, peso, RIR (0–10) y series completadas.
- Consulta de las marcas de la última sesión registrada de cada ejercicio mientras entrenas.
- Historial consultable y eliminable.
- Rutinas reutilizables.
- Temporizador de descanso (60, 90, 120 y 180 segundos).
- Estadísticas y récords personales de peso.
- Exportación CSV compatible con Excel.
- Copia completa e importación en JSON.
- Interfaz oscura adaptable a móvil.
- PWA con caché para uso sin conexión después de instalar/cargar.

IMPORTANTE SOBRE LOS DATOS
Los entrenamientos se guardan en localStorage del navegador del dispositivo. No se suben a ningún servidor. No borres los datos del sitio ni desinstales/limpies el navegador sin exportar primero una copia JSON. CSV sirve para analizar los registros; JSON conserva también rutinas e historial y es el formato para restaurar la app.

INSTALACIÓN EN ANDROID (RECOMENDADA)
Una PWA necesita servirse desde HTTPS (o localhost para pruebas); abrir index.html directamente como archivo no permite instalarla correctamente ni activar el service worker.

Opción sencilla: GitHub Pages
1. En un PC, descomprime RepLog_PWA.zip.
2. Crea/inicia sesión en GitHub y crea un repositorio nuevo, por ejemplo "replog".
3. Sube al repositorio los archivos index.html, manifest.json, sw.js, icon-192.png e icon-512.png (puedes subir README.txt también).
4. En Settings > Pages, elige desplegar desde la rama principal (main), carpeta /(root), y guarda.
5. Espera a que GitHub Pages publique la web. Abre la URL HTTPS que te indique GitHub en Chrome en tu Android.
6. En Chrome, menú ⋮ > "Instalar aplicación" o "Añadir a pantalla de inicio" (el texto depende de la versión).
7. Abre RepLog desde el icono. Tras la primera carga, la interfaz puede abrirse sin conexión.

COPIAS DE SEGURIDAD
1. En RepLog, pulsa "Copia" o entra en Progreso > "Exportar copia JSON".
2. Guarda el archivo JSON en una ubicación segura (por ejemplo, Descargas y luego otra copia en Drive/ordenador/USB).
3. Para restaurar, abre RepLog > Progreso > "Importar copia" y selecciona el JSON.
4. La importación reemplaza los datos actuales; exporta primero una copia de lo que tengas.
5. "CSV" exporta los registros de series para abrirlos en Excel. El CSV no restaura rutinas ni toda la estructura; usa JSON para restaurar.

USO SIN PUBLICAR EN INTERNET
Puedes abrir index.html en un navegador de PC para probarla, aunque el modo PWA/offline completo requiere HTTPS o localhost. Para uso privado en el móvil, también puedes alojarla en un servidor local de tu red, pero necesitarás configurar HTTPS o una solución equivalente para la instalación PWA.

NOTAS
- Los registros se almacenan en el navegador/dispositivo y no se sincronizan automáticamente con otros móviles.
- Los récords se calculan como el mayor peso de una serie marcada como completada.
- El volumen se calcula como peso (kg) × repeticiones de series completadas; las series de peso corporal sin carga no añaden volumen.
- La duración de sesión queda a 0 hasta que se añada una función de cronometraje de sesión; por eso las estadísticas de duración son orientativas en esta versión.
