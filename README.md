# YAHBA — Ritual del Agua

Sitio de marca y tienda para **YAHBA**, una línea de skincare de la Riviera Maya:
alma maya, método coreano. Agua de cenote filtrada por caliza sascab, miel de
abeja melipona, chukum y ramón, en un ritual de cinco pasos.

**Ver el sitio → https://madebynaxxo.github.io/yahba-ritual-del-agua/**

> Proyecto de diseño y desarrollo. La marca, los productos y los precios son
> ficticios; la pasarela de pago es una maqueta y no procesa cobros.

## Qué incluye

- **Portada** — hero editorial, carrusel infinito de producto, bloque héroe del
  SAK Tonic, sección *Alma maya · Método coreano* y manifiesto de marca.
- **Ritual** — ficha completa de los cinco pasos: textura, ingredientes, modo de
  uso y sello de sustentabilidad.
- **Tienda** — catálogo con carrito persistente, pack *Ritual Completo* y envío
  gratis a partir de cierto importe.
- **Carrito y pasarela** — cantidades, resumen, cinco métodos de pago, validación
  de tarjeta con algoritmo de Luhn y pantalla de confirmación con folio.
- **Multimoneda** — MXN, USD, EUR, CAD y GBP, con formato local por divisa.
- **Nosotros** — origen del agua, la caliza sascab, el cangrejo azul y el
  compromiso reef safe.

## Cómo está hecho

Un único `index.html` sin dependencias ni compilación: HTML, CSS y JavaScript a
mano. Tipografía Syne desde Google Fonts. Los packshots son PNG recortados sobre
fondo transparente y las fotos de ambiente van en WebP.

```
index.html          el sitio entero
imagenes/           packshots (PNG con alfa) y fotografía de ambiente (WebP/JPG)
video/              reel vertical 1080x1920 de la línea completa
```

Para verlo en local basta abrir `index.html` en el navegador. Si quieres que el
carrito recuerde el contenido entre recargas, sírvelo por HTTP:

```bash
python3 -m http.server 8000
```

## Notas de diseño

- Paleta: verde cenote `#2D8B7A`, beige `#F0EBE3`, sascab `#F5F1E8`, lima `#B2E364`.
- Escala de producto unificada: cada packshot se dimensiona por altura con una
  variable propia, para que los envases guarden entre sí su proporción real.
- Accesible desde teclado en navegación, logotipo y carrito; sin desbordes de
  texto ni solapes entre 390 y 1680 px de ancho.

## Pendientes conocidos

- Los logotipos de Xcaret, Xel-Há, Visa, Mastercard, Amex, Apple Pay y Google Pay
  son marcas tipográficas provisionales, no los oficiales. El HTML lleva
  comentarios con el punto exacto donde insertar los archivos de marca.
- Los tipos de cambio son constantes fijas; en producción irían contra una API.
- El cobro real requiere Stripe o Mercado Pago con servidor.
