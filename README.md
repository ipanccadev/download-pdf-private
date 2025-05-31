# 🧾 Descargar PDF desde imágenes privadas en Google Drive

Este proyecto contiene un script en JavaScript que permite generar y descargar un PDF a partir de imágenes cargadas desde enlaces **privados** (por ejemplo, con URLs tipo `blob:`) como las generadas al visualizar archivos privados en Google Drive.

## 📄 Descripción

El script detecta todas las imágenes visibles en la página que tienen URLs con el esquema `blob:`, las convierte en imágenes embebidas (`dataURL`) y las añade a un documento PDF utilizando la biblioteca [jsPDF](https://github.com/parallax/jsPDF). Luego descarga automáticamente el PDF generado.

## 🧠 ¿Cómo funciona?

1. Carga la biblioteca `jsPDF` de forma segura (usando `Trusted Types` si está disponible).
2. Escanea todas las etiquetas `<img>` de la página.
3. Para cada imagen con una URL tipo `blob:`, crea un `<canvas>` temporal para capturar la imagen.
4. Convierte la imagen a formato JPEG y la agrega al documento PDF.
5. Genera y descarga automáticamente un archivo llamado `download.pdf`.

## 📥 Instrucciones de uso

1. Abre una página en Google Drive donde estés visualizando imágenes privadas.
2. Abre la consola del navegador (F12 o clic derecho → "Inspeccionar" → pestaña "Consola").
3. Copia y pega el siguiente código en la consola y presiona `Enter`.
[Ver script.js](./script.js)
