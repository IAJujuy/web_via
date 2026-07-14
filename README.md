# VIA Sistemas Digitales — Web v2 Producto

Versión reconstruida para que la web deje de ser solo una landing y empiece a funcionar como sistema comercial.

## Qué trae esta versión

- Catálogo comercial de productos VIA.
- Fichas concretas por producto: cliente, dolor, entregable, exclusiones, plazo, precio/canal y CTA.
- Formulario mínimo de diagnóstico en `contratar.html`.
- Página de confirmación en `gracias.html`.
- Demo navegable EVIN Trace en `evin-trace-demo.html`.
- Páginas legales mínimas: `privacidad.html` y `terminos.html`.
- JS de seguimiento básico de conversiones en `js/main.js`.
- Configuración de WhatsApp, email y links de Mercado Pago en `js/config.js`.

## Archivos principales

- `index.html`: home comercial.
- `catalogo.html`: catálogo de productos.
- `diagnostico.html`: Diagnóstico Inicial VIA.
- `agente-ia-administrativo.html`: Agente IA Administrativo / Comercial.
- `automatizacion-documental.html`: Automatización Documental.
- `landing-agente-empresa.html`: Landing + Agente.
- `trazabilidad-operativa.html`: Sistema Operativo / EVIN Trace Inicial.
- `evin-trace-demo.html`: demo estática interactiva.
- `contratar.html`: formulario comercial.

## Configuración necesaria antes de publicar

Abrir `js/config.js` y revisar:

```js
window.VIA_CONFIG = {
  whatsappNumber: "5493883292812",
  contactEmail: "viasistemasdigitales@gmail.com",
  mercadoPagoLinks: {
    diagnostico: "",
    "agente-ia-administrativo": "",
    "automatizacion-documental": "",
    "landing-agente-empresa": "",
    "trazabilidad-operativa": ""
  }
};
```

Cuando existan links reales de Mercado Pago, pegarlos ahí o reemplazar los botones correspondientes.

## Subida a GitHub Pages

1. Copiar todos los archivos al repositorio publicado.
2. Mantener la carpeta `assets/` y `js/`.
3. Subir cambios a `main`.
4. Esperar el deploy de GitHub Pages.
5. Probar en celular: el orden de la home debe ser logo VIA primero y avatar CAP VIA después.

## Nota técnica

Esta versión evita los fallbacks base64 inline para reducir peso. Las imágenes se cargan desde `assets/`.
