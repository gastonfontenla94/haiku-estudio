# Pendientes del sitio

Lo que quedó por hacer después de la pasada de diseño del 11 de octubre de 2026. Cada punto es independiente; se pueden hacer en cualquier orden.

## Contenido

1. **Textos de servicios.** Las descripciones de Mezcla, Mastering, Sonido en vivo y Producción son borradores. Revisarlas y ajustarlas en `index.html`, bloque `services-list`. Las frases cortas que aparecen al pasar el mouse por la rueda están en los atributos `data-desc` de cada `snode`.
2. **Alquiler de sala.** Figura como opción en el formulario de contacto pero no entre los servicios. Decidir: agregarlo como sexto servicio (con una línea de descripción) o sacarlo del `<select>`.
3. **Fotos del estudio.** Dos o tres fotos horizontales de la sala, de al menos 1600 px de ancho, más una lista de 6 a 10 ítems de equipamiento (monitores, interfaz, micrófonos, previos, DAW). Van en la sección Estudio.
4. **Testimonios.** Dos o tres frases cortas de artistas con los que se trabajó, con nombre y proyecto, y su permiso para publicarlas. Irían entre Trabajos y Contacto.
5. **Trabajo destacado.** El reproductor de la sección Trabajos muestra Constelación. Para cambiarlo, editar el ID del álbum de Spotify en el `src` del iframe y los textos del bloque `works-player`.

## Cuenta y dominio

6. **Mail en el dominio.** El dominio está en Porkbun y no tiene correo configurado. Opción rápida y gratuita: en Porkbun, dominio → Email Forwarding → crear `hola@haikuestudio.com` reenviando al Gmail. Para responder desde esa dirección, en Gmail → Configuración → Cuentas → "Enviar como". Opción con casilla propia: Zoho Mail (gratis) o el correo pago de Porkbun. Cuando exista la dirección, buscar y reemplazar el Gmail actual en `index.html` (aparece en los datos estructurados, en Contacto y en el footer).
7. **Enforce HTTPS.** En GitHub: repositorio → Settings → Pages → tildar "Enforce HTTPS". Si la casilla está deshabilitada, esperar unos minutos a que GitHub termine de emitir el certificado y recargar.

## Cómo editar el sitio

- Todo el sitio es un solo archivo, `index.html`. Lo que se sube a `main` se publica solo en uno o dos minutos.
- Para agregar un trabajo: copiar un bloque `<a class="work" ...>` de la grilla, cambiar imagen, textos y link. Las tapas van en `trabajos/`, JPG de 600 × 600 px.
- El formulario de contacto envía por Formspree sin salir de la página. Si hay que cambiar el destinatario, se hace desde la cuenta de Formspree, no en el código.
