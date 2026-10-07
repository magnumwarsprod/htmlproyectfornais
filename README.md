# Otra vuelta

Obligatorio de Diseño web 2: sitio sobre cuidar, reparar y reutilizar ropa,
vinculado al ODS 12. HTML y CSS puro, sin JavaScript, frameworks ni librerías.

## Ver el sitio

Abrir `index.html` en un navegador. Para probarlo mediante un servidor local:

```sh
cd /workspace/htmlproyectfornais
python3 -m http.server 8000
```

No hay dependencias que instalar ni paso de compilación.

## Estructura

- `index.html`: página principal y secciones navegables.
- `css/estilos.css`: estilos mobile first, variables y media queries.
- `imagenes/`: ilustraciones SVG locales y livianas.
- `fuentes/`: Manrope, de Google Fonts, con su licencia.
- `gracias.html`: destino de demostración del formulario.
- `entrega.txt`: enfoque, ODS, créditos y pendientes de publicación.

Las vistas siguen el orden de los wireframes provistos. Desde 640 px hay
cuatro hábitos, dos columnas de recursos y texto ampliado en la sección
central. Desde 1024 px, cuatro columnas de hábitos, mosaico junto al texto
y tres recursos. En móvil se muestran dos hábitos y dos recursos.

El menú móvil usa `details` y `summary`. Las guías se pueden desplegar sin
JavaScript. El formulario valida email y consentimiento con `required`.
Su envío es una demostración local: no suscribe, no almacena datos y usa
un correo de ejemplo en la URL de destino. Para recepción real hace falta
configurar un servicio o backend; no se incluye una dirección ficticia.

## Antes de entregar

1. Revisar y personalizar textos, diseño y código.
2. Validar ambos HTML en https://validator.w3.org/ y el CSS en
   https://jigsaw.w3.org/css-validator/.
3. Publicar, por ejemplo mediante GitHub Pages, y completar `entrega.txt`.
4. Comprimir los archivos fuente, sin incluir `.git` ni los PDFs adjuntos.

La fuente se distribuye localmente porque el entorno bloquea Google Fonts
en tiempo de ejecución. Procede del repositorio oficial `google/fonts`.
Los textos, ilustraciones y código inicial se realizaron con asistencia
de OpenAI Codex. Los créditos están en el sitio y en `entrega.txt`.

## Comprobaciones realizadas

- Chromium: vistas de 320, 375, 640, 768, 1024, 1440 y 1920 px, sin
  desbordamiento horizontal; fuente e imágenes cargadas correctamente.
- Menú móvil y guía desplegable comprobados.
- Formulario: rechazo de campos vacíos, email inválido y casilla sin marcar;
  navegación a la página de demostración con datos de ejemplo válidos.
- Validador Nu ejecutado localmente: ambos HTML y el CSS sin errores.

Las validaciones web indicadas por la consigna todavía deben completarse:
el entorno bloquea el acceso a los dominios de los validadores W3C.
