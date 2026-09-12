# Reconstrucción de COMGECEY

Base revisada: `octaviozm82-sketch/comgecey`, rama `main`, commit `8338752`. El repositorio tenía `index.html` (239.575 bytes, CSS embebido e imágenes base64) y `.gitignore`. No tenía scripts, framework ni configuración de Vercel. Se modificó directamente ese HTML; la propuesta anterior quedó fuera de este repositorio.

## P1

- H01/H02: convocatoria como hero, ficha visible sin scroll a 1400 × 900; fechas, cuota, modalidad y audiencia explícitas. Chat simulado eliminado. Referencia de días restantes fechada; actualizar manualmente al publicar.
- H03: proceso después del hero; consejo cerca del final, sin tarjetas de valores. Nombre de presidenta conservado. Foto oficial pendiente del cliente; no se inventó una persona ni una foto. El reconocimiento ante SEP se atribuye a CONAMEGE, no a un registro estatal no demostrado.
- H04: solicitud oficial nacional servida localmente, descarga a un clic desde hero y requisitos. Dirección/plazo junto a lista. Horario y confirmación de pago marcados expresamente como pendientes, según autorización del usuario. Confirmar con el cliente si requiere anexos estatales.
- H07: header móvil de 61 px y barra adicional de anclas; Requisitos accesible con un toque a 390 px.
- H08: contenedor único; a 1400 px los bordes útiles son 110/1290. Se usa max-width exterior 1260 con padding 40 y border-box para obtener los 1180 útiles del criterio. El literal max-width 1180 más padding con border-box contradice esas coordenadas.
- H11: verde #1B7A43 con blanco, contraste 5,37:1; texto normal ≥14 px, 13 px solo en pie. Colores secundarios también superan 4,5:1.
- H13: HTML inferior a 40 KB y sello externo SVG de 3.492 bytes, con dimensiones declaradas. Se conservó el JPEG original del cliente y se creó una copia optimizada dentro de un SVG con recorte circular: elimina el rectángulo exterior sin recrear el emblema. Se usa el mismo SVG en cabecera, pie, favicon, Open Graph y Organization. Se descartaron los intentos de extracción generativa porque dejaban fondo gris. El JPEG queda como fuente de respaldo y no se descarga en la página.
- H18: title, description, canonical, OG, favicon, robots y sitemap implementados; todos los recursos locales responden 200. Search Console, indexación y enlace desde el consejo nacional requieren cuentas/acciones externas y no se declaran completados.
- H19: un solo JSON-LD (Organization, Event, FAQPage, ContactPoint, PostalAddress) y llms.txt. Las 10 preguntas y respuestas del esquema coinciden exactamente con el HTML. Validación externa en schema.org e isitagentready pendiente; las comprobaciones locales no sustituyen esos servicios.
- H20: se conserva dominio Vercel y Gmail según el fallback explícito del anexo. Registro de dominios, DNS/TLS, correo propio, redirecciones y cambios en perfiles externos pendientes. No se apuntó el canonical a un dominio sin configurar.

## P2 y P3

La instrucción posterior del cliente reemplaza el hero centrado en el examen: el título principal ahora es «Consejo de Médicos Generales Certificados del Estado de Yucatán, A.C.» y el examen aparece como subtítulo. Se retiró la frase «Medicina general · Yucatán» de la cabecera. Se expandieron las menciones institucionales a sus nombres completos con A.C., confirmado por el cliente; se añadieron tonos plateados para texto secundario y dorado para datos destacados. La denominación abreviada solo permanece como alias técnico en los datos estructurados.

Actualización de identidad solicitada por el cliente: vino #4A1220, blanco roto #FAF7F2 y vino claro #E7CCD3 en cabecera, ficha, contacto y pie; dorado decorativo #B08D45. El JPEG entregado no contiene una muestra identificable de vino, por lo que se utiliza la referencia del cliente. Se conserva un único tema claro con superficies institucionales vino. Logo original entregado, sin recreación, en cabecera y pie; rutas relativas compatibles con apertura local.

- H05/H09/H10/H14: sin franja de promesas, pastillas, valores, tarjetas, sombras ni tema oscuro. Requisitos numerados con casillas vacías y pasos en lista. Dos fuentes de sistema: Arial y Georgia.
- H06: diez preguntas con enlaces a fuentes oficiales. Vigencia de cinco años y 300 puntos explicados. La fuente no publica número de preguntas, duración ni condiciones de reintento: se indica ese límite sin inventar respuestas.
- H12: todos los enlaces y summaries miden al menos 44 px en móvil. El enlace para saltar al contenido se muestra al foco. Sin desbordamiento horizontal a 320/390/1180/1280/1400 px.
- H15: solicitud, COMGECEY y en línea como vocabulario uniforme. Nombre legal una vez en el cuerpo; no devolución una vez en el cuerpo. Fechas y domicilio repetidos únicamente donde los criterios exigen hero, requisitos y contacto.
- H16: Contacto propio, WhatsApp, correo y búsqueda por dirección en Maps. Horario pendiente y Google Business Profile sin crear. El enlace de Maps no representa una ficha verificada.
- H17: main, salto al contenido probado con teclado y dimensiones de imágenes. FAQ nativa con details/summary; impresión expande todas las respuestas mediante CSS.

## Verificación

Pruebas realizadas en Edge/Chromium: cinco anchos, anclas existentes, descarga real del PDF, estado abierto de FAQ, foco del enlace de salto y llegada al main, tema claro con preferencia oscura, tamaño de texto, objetivos táctiles, JSON-LD/FAQ y respuestas HTTP 200. Se inspeccionaron capturas y la salida de impresión; el PDF incluye respuestas de preguntas cerradas en pantalla.

No hay archivos JavaScript, dependencias, build ni configuración de Vercel. El único elemento script es JSON-LD inerte, pedido por el blueprint. Las herramientas de prueba y capturas están fuera del repositorio.

No se verificó Safari real, LCP/3G, indexación ni funcionamiento en el dominio propio. No se enviaron mensajes al consejo ni se modificaron cuentas externas.

## Fuentes

- [Convocatoria nacional](https://www.consejonacionalcmg.org.mx/certificado-primera-vez).
- [PDF original](https://userfiles.sfo3.digitaloceanspaces.com/brochure/Solicitud-Certificacion.pdf), descargado sin modificar como solicitud-certificacion.pdf; dos páginas.
- [Renovación](https://www.consejonacionalcmg.org.mx/certificado-renovacion).
- [Directorio estatal](https://consejonacionalcmg.org.mx/micrositio/Yucat%C3%A1n).
- [Composición del consejo nacional](https://www.consejonacionalcmg.org.mx/quienes-somos).
- [Idoneidad ante SEP](https://www.consejonacionalcmg.org.mx/certificado-idoneidad).
- Dirección, CURP y datos locales: index.html original de main y blueprint.md. Domicilio sin corroboración externa.
