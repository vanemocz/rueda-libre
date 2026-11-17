# Rueda Libre \| Ecosistema web

Sitio web de **Rueda Libre**, un proyecto de alquiler, compra y
mantenimiento de bicicletas, integrado con **Rueda Nocturna**, una
landing page para promocionar recorridos nocturnos en bicicleta por
Medellín.

El proyecto reúne dos experiencias conectadas mediante navegación entre
páginas y una identidad visual coherente.

## Sitios publicados

-   **Rueda Libre:** https://vanemocz.github.io/rueda-libre/
-   **Rueda Nocturna:**
    https://vanemocz.github.io/rueda-libre/nocturna/index.html

## Descripción del proyecto

### Rueda Libre

El sitio principal presenta los servicios del negocio y permite
consultar información para alquilar bicicletas.

Páginas principales:

-   `index.html`: portada, servicios, información del negocio y
    ubicación.
-   `paginas/tarifas.html`: tarifas de alquiler y recorridos.
-   `paginas/reservas.html`: formulario para solicitar una reserva.

El formulario de reservas agrupa los datos personales, la información
del alquiler y la confirmación de políticas. Se utilizan controles HTML
adecuados para cada dato y validaciones nativas como `required`, `min`,
`max` y tipos específicos de entrada.

### Rueda Nocturna

Landing page promocional desarrollada con Tailwind CSS. Presenta las
rutas nocturnas, sus características, el proceso de participación, los
planes disponibles y el formulario de inscripción.

La landing se conecta con Rueda Libre para que las personas puedan
regresar al sitio principal y continuar hacia la reserva de una
bicicleta.

## Estructura general

``` text
RUEDA-LIBRE/
├── CSS/
│   └── styles.css
├── img/
├── nocturna/
│   ├── src/
│   ├── index.html
│   ├── componentes.html
│   ├── prototipo.html
│   ├── package.json
│   └── package-lock.json
├── paginas/
│   ├── tarifas.html
│   ├── reservas.html
│   └── bitacora.txt
├── pruebas/
│   └── catalogo-bootstrap.html
└── index.html
```

*La estructura muestra los archivos y carpetas principales del proyecto.
`node_modules` se omite porque corresponde a dependencias instaladas
localmente.*

## Tecnologías y herramientas

  -----------------------------------------------------------------------
  Tecnología o herramienta            Uso en el proyecto
  ----------------------------------- -----------------------------------
  HTML5                               Estructura semántica de las páginas
                                      y formularios.

  CSS3                                Estilos propios, variables,
                                      tipografías y ajustes responsive.

  Bootstrap                           Sistema de cuadrícula, componentes
                                      y utilidades del sitio Rueda Libre.

  Tailwind CSS                        Diseño mediante clases de utilidad
                                      para Rueda Nocturna.

  JavaScript                          Interactividad y comportamiento de
                                      los componentes cuando aplica.

  Google Fonts                        Tipografías Montserrat y Open Sans.

  DevTools                            Inspección de estilos, pruebas
                                      responsive y revisión de
                                      comportamiento.

  W3C Validator                       Validación del marcado HTML.

  Git y GitHub                        Control de versiones y publicación
                                      del proyecto.

  GitHub Pages                        Despliegue de los sitios.
  -----------------------------------------------------------------------

## Identidad visual

### Rueda Libre

La identidad visual utiliza una paleta cálida y contrastada:

  Color           Código      Uso
  --------------- ----------- -----------------------------------
  Crema           `#FAF6EF`   Fondo general.
  Gris Asfalto    `#5B6470`   Texto secundario.
  Azul Noche      `#14213D`   Títulos y encabezados.
  Verde Ruta      `#1E7A4F`   Botones y enlaces.
  Naranja Pedal   `#F39A2B`   Destacados y botones secundarios.

Tipografías: - **Montserrat:** encabezados. - **Open Sans:** textos
generales.

Se revisaron combinaciones de color y contraste para seleccionar usos
legibles. El Naranja Pedal se reserva para elementos destacados y no se
utiliza como color principal de texto.

### Rueda Nocturna

La landing conserva los elementos de marca compartidos y añade el color
**Amarillo Faro (`#FFD166`)** como acento propio de la campaña nocturna.

## Decisiones técnicas y aprendizajes

### Estructura y semántica HTML

Se organizaron las páginas mediante elementos semánticos como `header`,
`nav`, `main`, `section`, `article`, `aside` y `footer`. Los formularios
se agruparon con `fieldset` y `legend`, y sus controles se asociaron con
etiquetas.

### CSS, herencia y especificidad

Se comprobaron mediante DevTools: - La herencia de `font-family` desde
`body`. - El comportamiento no heredado de `background-color`. - La
aplicación de tipografías específicas en los encabezados. - La prioridad
de selectores con distinta especificidad. - El efecto de cambiar
temporalmente `box-sizing` de `border-box` a `content-box`.

### Grid y Flexbox

CSS Grid se utilizó para distribuir contenidos en dos dimensiones, como
la flota de bicicletas, las rutas y la relación entre formulario e
información de contacto. Flexbox se aplicó en distribuciones de una
dimensión, como encabezados, pies de página y contenido interno de
tarjetas.

En las tarjetas, `margin-top: auto` permitió mantener los botones
alineados al final.

### Diseño responsive

Se realizaron pruebas con DevTools en diferentes anchos de pantalla.

En Rueda Libre, la cuadrícula de bicicletas mostró: - 4 columnas a 1280
px. - 3 columnas a 900 px. - 2 columnas a 500 px.

También se verificaron las vistas de 360 px, 768 px y 1280 px. En Rueda
Nocturna se aplicó un enfoque Mobile-First y se probaron anchos de 360,
640, 768, 1024 y 1280 px.

### Comparación de frameworks --- MiniReto 8

En la comparación realizada se observaron estas diferencias:

  -----------------------------------------------------------------------
  Criterio                Bootstrap               Tailwind CSS
  ----------------------- ----------------------- -----------------------
  Curva de aprendizaje    Más sencillo para       Requiere familiarizarse
                          iniciar con componentes con clases utilitarias.
                          y clases predefinidas.  

  Personalización         Se apoya en componentes Permite controlar los
                          y CSS adicional.        estilos directamente
                                                  desde las utilidades.

  Tamaño medido en la     CSS: 40,9 KB; JS: 25,2  CSS minificado: 20,6
  actividad               KB.                     KB; JS adicional: 0 KB.

  Uso observado           Sitios que aprovechan   Diseños personalizados
                          componentes             e identidad visual
                          prediseñados.           propia.
  -----------------------------------------------------------------------

**Recomendación aplicada al proyecto:** Bootstrap resulta conveniente
para Rueda Libre por su cuadrícula y componentes prediseñados; Tailwind
CSS se adapta a Rueda Nocturna por la flexibilidad para construir una
landing con una presentación personalizada. La elección se hizo según
las necesidades de cada producto, no como una afirmación de que un
framework sea siempre superior al otro.

En la migración de Rueda Libre a Bootstrap, la hoja CSS pasó de 494 a
375 líneas: una reducción aproximada del 24,1 %. La actividad permitió
observar que Bootstrap agiliza la distribución responsive, aunque
requiere conocer sus clases y revisar posibles conflictos con los
estilos propios.

### Formularios y accesibilidad

Se implementaron validaciones nativas de HTML para los campos requeridos
y se probaron formularios vacíos, con datos inválidos y completos.
También se revisó la navegación mediante teclado y la presentación en
diferentes temas.

### Integración del ecosistema

Se enlazaron Rueda Libre y Rueda Nocturna mediante la navegación, el
logo y los botones de acción. Se revisaron las rutas relativas entre la
raíz del repositorio y la carpeta `nocturna`, además de los enlaces en
local y en GitHub Pages.

## Capturas del proyecto

Agrega las capturas en la carpeta `img/capturas/` con estos nombres para
que aparezcan en el README:

### Rueda Libre --- escritorio

![Rueda Libre en escritorio](img/capturas/rueda-libre-escritorio.png)

### Rueda Libre --- celular

![Rueda Libre en celular](img/capturas/rueda-libre-celular.png)

### Rueda Nocturna --- escritorio

![Rueda Nocturna en
escritorio](img/capturas/rueda-nocturna-escritorio.png)

### Rueda Nocturna --- celular

![Rueda Nocturna en celular](img/capturas/rueda-nocturna-celular.png)

### Rueda Nocturna --- modo oscuro

![Rueda Nocturna en modo
oscuro](img/capturas/rueda-nocturna-modo-oscuro.png)

> Sustituye o completa estas imágenes con las capturas finales tomadas
> durante la verificación. Los nombres anteriores indican dónde debe
> guardarse cada archivo; no son capturas incluidas automáticamente.

## Verificación final

Antes de la entrega se revisaron los siguientes aspectos:

-   Navegación entre el sitio principal y la landing.
-   Enlaces hacia tarifas, reservas e inscripción.
-   Visualización responsive en diferentes tamaños.
-   Formulario de reservas y sus validaciones.
-   Formulario de inscripción y navegación mediante teclado.
-   Presentación en modo claro y oscuro en Rueda Nocturna.
-   Revisión del HTML con el validador W3C y corrección de los errores
    detectados.
-   Publicación mediante GitHub Pages.

## Aprendizajes

Durante el desarrollo reforcé mis conocimientos sobre estructura
semántica HTML, CSS, especificidad, herencia, box model, Grid, Flexbox y
diseño responsive. También aprendí a trabajar con Bootstrap y Tailwind
CSS, comparar sus ventajas según el contexto y conectar dos sitios
publicados dentro de un mismo ecosistema.

El proceso de pruebas con DevTools y el validador W3C fue importante
para detectar y corregir problemas antes de la entrega.

## Autora

**Vanessa Montoya Cruz**\
Proyecto académico --- Rueda Libre / Rueda Nocturna\
2026
