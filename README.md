# Cotizador Fermetal

Aplicación web para que los vendedores de Fermetal armen cotizaciones de la mercancía de los catálogos **Fermetal, Dijonas y Super Precio**, con precios especiales **Cuenta Clave**.

## Qué hace
- Búsqueda de productos por código o descripción, con foto, existencia / tránsito, box y precio full.
- Filas en rojo cuando la cantidad pedida supera la existencia.
- Descuento (%), IVA 16 % y tasa BCV del día con total en bolívares.
- Borrador → revisión → cotización cerrada (bloqueada) con PDF.
- Envío por WhatsApp, exportación a Excel con fórmulas e historial con resumen por vendedor.
- Diseño adaptado a computadora, iPhone y Android.

## Cómo está construida
- Un solo archivo `index.html` (HTML + CSS + JavaScript, sin servidor).
- El inventario, los precios y las fotos (miniaturas JPEG) van incrustados en el archivo como JSON.
- Librerías por CDN: jsPDF + AutoTable (PDF), SheetJS (Excel), JSZip (lectura de los Excel de inventario).
- Las cotizaciones se guardan en el dispositivo de cada vendedor (localStorage) con numeración por iniciales (ej. AP-0001).

## Actualizar el inventario
1. Abrir la versión publicada en Claude con la cuenta administradora y pulsar **Actualizar inventario desde los Excel**.
2. Pulsar **Descargar index.html para Netlify** (sirve igual para Vercel).
3. Reemplazar `index.html` en este repositorio (GitHub → Add file → Upload files → Commit). Vercel publica la nueva versión automáticamente.

## Despliegue
Repositorio en GitHub conectado a Vercel (framework: *Other*, sin comando de build, carpeta raíz del repositorio).
