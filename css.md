# :memo: Notes
## CSS
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [W3C CSS](https://www.w3.org/Style/CSS/)
- [The CSS validator](https://jigsaw.w3.org/css-validator/)
- [CSS: Cascading Style Sheets](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [MDN web docs](https://developer.mozilla.org/en-US/)
- [CSS Reference](https://cssreference.io/)
- [How CSS works](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works)
- [CSS Cascading and Inheritance Level 5](https://www.w3.org/TR/css-cascade-5/)
- [Introducing the CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)
- [Learn CSS](https://web.dev/learn/css/)
- [Learn Responsive Design](https://developers.google.com/web/fundamentals/design-and-ui/responsive/?hl=es)
- [CSS pixel](https://developer.mozilla.org/en-US/docs/Glossary/CSS_pixel)
### Terms and concepts
- CSS or Cascading Style Sheets
- Box model
* Syntax
	- Shorthand
- Indention
- Comments
* Rules
	* Parts
		- Selector
		* Declaration
			- Property
			- Value
	* Implement
		- inline, in element with attribute style
		- in block, in style element
		- link to external css file
		- import a style sheet into another style sheet
* Selector
	* Element
		- Block
		- Line
	* Declaration or block
		- Attribute or Property
		- Value
* Selectors
	- Universal selector
	- Mark or Tag or Element or Type selector
	- Class selector
	- Attribute selector / Attribute and value [ * ^ $ ~ | ]
	- Id selector
	- Grouping selectors
* Selector Combinations or Grouping selectors
	* Sibling element
		- General ~
		- Adjacent +
	* Child element
		- Direct >
		- Descendant 
	* Pseudo-class :
		- State
		- Position
		- Relation
	* Pseudo-element ::
		- Typographic
		- Content
* Attributes
	- Box or container
	- Typography
	- Other content
* Values and Units
	- Absolute (ej: px, 1px = 1/96th of 1in)
	- Relative (ej: %, em, rem)
	* Recommended
		- Font size: rem
		- Padding and margin: em 
		- Widths: em or percentage
* DOM
	- Flow
	- Default values
	- Inheritance
	- Overriding
* Cascade
	* Algorithm
		- Origin
		- Specificity
		- Order
* Origin
	1. Author
	2. User custom
	3. User Agent stylesheet / Browser
* Specificity
	1. !important keyword
	2. Inline
	3. Identifier
	4. Class and pseudo-class
	5. Element and pseudo-element
- Collision
*	Prioritize
	1. !important keyword
	2. Inline
	3. Identifier
	4. Class and pseudo-class
	5. Element and pseudo-element
	6. Order
	7. Author
	8. User custom
	9. User Agent stylesheet / Browser
* Hierarchy
	- Descendant
	- Parent element
	- Sibling element
	- Child element
	- Automatic or default mode
	- Manually or force mode
	* CSS Combinators
* Color
	- color-scheme
	* Values
		- keywords
		- Hexadecimal
		- Hexadecimal with Alpha
	* Functions
		- RGB
		- RGBA
		- HSL
		- HSLA
- Fonts
- Layout
* Media queries
	* Breakpoint
		- 320px, 480px, 600px, 768px, 1024px, 1200px
	* X-device first
		- Mobile first
		- Desktop firts
	* Prefer Ems
		- 320px / 16px = 20em
		- 480px / 16px = 30em
		- 600px / 16px = 37.5em
		- 768px / 16px = 48em
		- 1024px / 16px = 64em
		- 1200px / 16px = 75em
- Positioning
- Feature queries
- Custom properties or Variables
* Reset styles
	- Reset
	- Normalize
* CSS browser prefixes
	- -webkit-	Chrome, Safari, Android
	- -moz-		Firefox
	- -o-			Opera
	- -ms-		Internet Explorer
	- -khtml-		Konqueror
* CSS effects
	* Shadows
		- box-shadow
		- text-shadow
		- drop-shadow
	* Gradients
		- linear
		- radial
		- conic
	* Filters
		- blur
		- brightness
		- contrast
		- grayscale
		- sepia
		- hue-rotate
		- invert
		- opacity
		- saturate
		- backdrop-filter
	* Blend modes
		- mix-blens-mode
		- background-blend-mode
	* Masking
		- clip-path
	* Forms
		- shape-outside
	* Scrolling
		- scroll-behavior
		- scroll-margin
		- scroll-snap-type
		- scroll-snap-align
	* Transitions
		- transition
		- transition-property
		- transition-duration
		- transition-timing-function
		- transition-delay
	* Transforms
		- transform
		- transform-origin
		- translate
		- scale
		- rotate
		- skew
		- matrix
		- perspective
		- transform-style
		- backface-visibility
	* Animations
		- animation
		- animation-name
		- animation-duration
		- @keyframes
		- animation-timing-function
		- animation-delay
		- animation-iteration-count
		- animation-direction
		- animation-fill-mode
		- animation-play-state
* Multi device
	- Responsive design
	- Adaptive design
	- Responsive design + Server Side Components (RESS)
	- Responsible responsive design
	- Fluid design
- SEO
* CSS architecture
	- Predictable
	- Reusable
	- Stable
	- Scalable
* Components
	- One only function
	- Independent
	- Auto-content
	- Reusable
* Tools
	- Methodologies
	- Frameworks
	- Processors
	- Style guide
#### example.css
```
/* RESET STYLES MANUALLY */
*,
*::before,
*::after {
  box-sizing: border-box;
}
html {
  height: 100%;
  font-size: 62.5%;
  scroll-behavior: smooth;
}
body {
  height: 100%;
	margin: 0;
}
a {
  text-decoration: none;
  color: inherit;
}
img, audio, video, iframe, canvas, svg, picture {
	max-width: 100%;
	height: auto;
}
img {
	width: 100%;
	height: 100%;
	object-fit: cover;
	object-position: 0 50%;
}

/* SEUDOCLASES ":" de estado, de posición, de relación  */
ELEMENTO:SEUDOCLASE {}
a:link {}/* apariencia de enlaces no visitados */
a:visited {}/* enlaces ya visitados */
a:hover {}/* cuando el puntero del mouse esté sobre */
a:active {}/* cuando se selecciona, un click */
a:focus {}/* otro estado, cuando esté seleccionado */
p:first-line {}/* dar estilos a la primera línea del parrafo */
p:nth-child(número de la línea){}/* dar estilo a otras líneas del parrafo */
:not(elemento)/* dar estilos a los elementos que NO sean <elemento> */

/* SEUDOELEMENTOS "::" tipográficos, de contenido */
SELECTOR::SEUDOELEMENTO {}
SELECTOR::before{}/* seudoelemento */
SELECTOR::after{}/* seudoelemento */
p::first-letter {}/* dar estilo a la primera letra del parrafo */
p::first-line {}/* dar estilo a la primera línea del parrafo */
div::before {}/* agregar un elemento despues de nuestra caja */
div::after {}/* agregar un elemento antes de nuestra caja */
li::nth-of-type()/* hacer referencia a un elemento del tipo ...  */
elemento::selection {}/* dar estilo cuando lo seleccione */
#nombreIdentificador {}/* selector id, crear un id, no usar id para estilos, solo para javascript */
.nombreClase {}/* selector class, crear una clase */

/* COMBINAR SEUDOCLASES CON SEUDOELEMENTOS */
SELECTOR:SEUDOCLASE:SEUDOELEMENTO {}
div:hover::before {}
div:hover::after {}

/* CSS Combinators */
[atributo ~ ="valor"]/* ~ para apuntar a elementos que contengan una palabra especifica */
[atributo | ="valor"]/* | para apuntar a elementos que comiencen con una palabra especifica */
[atributo ^ ="valor"]/* signo paraguas para apuntar a elementos que comiencen con un valor especifico */
[atributo $ ="valor"]/* $ para apuntar a elementos que terminen con un valor especifico */
[atributo * ="valor"]/* * para apuntar a elementos que contengan un valor especifico */
selector + selector {}/* apuntar a elementos hermanos adyacentes */
selector ~ selector {}/* apuntar a elementos hermanos inmediatos (todos los hermanos) */

@font-face {}/* agregar fuentes */

/* MEDIAQUERIES */
@media (width >= 576px) {}
@media (width >= 768px) {}
@media (width >= 992px) {}
@media (width >= 1200px) {}
@media (width >= 1400px) {}
/* MOBILE FIRST - consiste en codificar para dispositivos moviles y dar cambios a medida que crecen las pantallas */
.container {
  width: 100%;
  padding-left: 1rem;
  padding-right: 1rem;
}
@media (width >= 576px) {
  .container {
    max-width: 540px;
    margin: auto;
    padding-left: 0;
    padding-right: 0;
  }
}
@media (width >= 768px) {
  .container {
    max-width: 720px;
  }
}
@media (width >= 992px) {
  .container {
    max-width: 960px;
  }
}
@media (width >= 1200px) {
  .container {
    max-width: 1140px;
  }
}
@media (width >= 1400px) {
  .container {
    max-width: 1320px;
  }
}
/* cambios a partir de 480px en adelante */
@media screen and (min-width: 480px) {
	max-width: 420px;
}
/* cambios a partir de 768px en adelante */
@media screen and (min-width: 768px) {
	max-width: 720px;
}
/* cambios a partir de 992px en adelante */
@media screen and (min-width: 992px) {
	max-width: 960;
}

/* es clave trabajar con medidas porcentuales y no fijas */

/* crear animaciones */
@keyframes{}

/*  */
@-webkit-keyframes {
	from {}
	to {}
}

SELECTOR {
	/* ATRIBUTOS \ PROPIEDADES */
	width:;/* ancho */
	height:;/* alto */
	margin:;/* margen externo */
	padding:;/* margen interno */
	border:;/* borde */
	border-style:;/* estilo del borde */
	border-width:;/* ancho del borde */
	border-color:;/* color del borde */
	border-radius:;/* bordes redondeados, ovalos, circulos */
	border-collapse:;/* unificar bordes */
	border-spacing:;/* espaciado de los bordes */
	box-shadow:;/* dar sombra a las cajas */
	box-sizing:;/* incluir el padding a su tamaño, que el padding no sume a su tamaño -webkit- -moz- */
	cursor:;/* cambiar aspecto del cursor  */
	vertical-align:;/* alineción vertical, con el valor "top" quito espacios */
	display/* controlar la ubicación tipo bloque, tipo línea, flex */
	display: flex;/* con el valor "flex" habilitamos "flexbox", contenedor padre */
	opacity:;/* dar opacidad */
	color:;/* dar color */
	justify-content:;/*  */
	align:;/*  */
	align-items:;/*  */
	align-content:;/*  */
	order:;/*  */
	align-self:;/*  */
	visibility:;/* controlar la visivilidad, ocultar sin quitar */
	position:;/* controlar la posición, normal, relativo, absoluto, fijo, flotante */
	top:; right:; bottom:; left:;/* controlar la flotación, la ubicación de un elemento tipo bloque */
	float:;/* que el elemento flote a la derecha, izquierda,  */
	clear:;/* permite limpiar, resetear, corrige errores de float */
	content: "";/*  */
	overflow:;/* otra manera de corregir errores de float, más recomendada */
	overflow:;/* evitar que el contenido se desborde de su contenedor */
	overflow-x:;/* eliminar cualquier scroll horizontal */
	overflow-y:;/*  */
	overflow-wrap:;/*  */
	z-index/* establecer el nivel de capa, controlar sobreposición de cajas - SIEMPRE debe ir acompañado de "position"*/
	background:;/* fondo */
	background: url();/* imagen de fondo */
	background-image:;/* imagen de fondo */
	background-repeat:;/* repetición de la imagen de fondo */
	background-size:;/* tamaño del fondo */
	background-size:cover;/* tamaño imagen del fondo al 100% */
	background-attachment:;/* fijar el fondo o dejarlo scroll */
	background-position:;/* posición de la imagen */
	background-color:;/* color de fondo */
	font-size:;/* tamaño de la fuente */
	text-decoration:;/* decoración del texto */
	font-family:;/* fuente familia */
	font-style:;/* estilo del texto */
	font-weight:;/* ancho del texto */
	font-variant:;/* modificar el aspecto de la fuente, ej que las primeras sean mayusculas */
	font:;/* shorthand o método abreviado */
	text-align:;/* alinear texto */
	text-transform:;/* transformar todo el texto a mayusculas, minuscula, capital */
	text-shadow:;/* poner sombra al texto */
	text-overflow:;/*  */
	text-indent:;/* identar */
	text-decoration:;/* decorar */
	letter-spacing:;/* ajustar espaciado entre letras */
	word-spacing:;/* ajustar espaciado entre palabras */
	line-height:;/* ajustar espaciado de altura de línea de texto */
	list-style:;/* dar estilo a las listas */
	list-style-type:;/* dar estilo a las listas */
	list-style-image:;/* para poner una imagen */
	list-style-position:;/* dar estilo a las listas */
	empty-cells:;/* dar estilo a las tablas a las celdas vacias */
	cursor:;/* cambiar el puntero */
		transform:;/* hacer transformaciones,  animaciones -webkit- -moz- */
	transform:perspective()/* cambios en perspectiva visual */
	transform:translate();/* trasladar elemento */
	transform:scale();/* escalar elemento */
	transform:rotate();/* rotar elemento */
	transform:skew();/* sesgar elemento */
	transform-origin/*  */
	transition:nombre del elemento valores ease linear;/* transiciones */
	transition-property:;/* especificar aplicación por ejemplo cuando tengo varias tranciciones */
	transition-delay:;/* un retrazo en la transición */
	transition-duration:;/* especificar tiempo en la transición */
	transition-timing-function:;/* especificar tiempo en la transición en sus diferentes estados */
	animation-name:;/* manejar animaciones */
	animation-duration:;/* establecer duración de la animación */
	animation-iteration-count:;/* establecer cuanto tiempo durará la animación */
	animation-delay:;/*  */
	animation-timing-function:;/*  */
	@keyframes{}/* crear animaciones */
	/* FLEXBOX PADRE */
	display: flex;/* Habilitar, activar FLEXBOX, flex o inline-flex */
    flex-direction: row;/* row, row-reverse, column, column-reverse */
	flex-wrap: nowrap;/* nowrap, wrap */
    justify-content: flex-start;/* flex-start, flex-end, center, space-between, space-around - alineación de ítems sobre eje principal */
	align-items: stretch;/* stretch, flex-start, flex-end, center - alineación de ítems sobre el eje cruzado*/
	flex-flow:;/* combina "flex-direction" con "flex-wrap" */
	/* FLEXBOX HIJO */
	flex-shrink:;/* controla como se contrae */
	flex-grow:;/* añade espacio sobre eje principal */
	flex-basis: auto;/* define el tamaño de un ítem en términos del espacio que deja como espacio disponible */
	align-self:;/*  */
	flex:;/* combina "flex-shrink" "flex-grow" "flex-basis" */
	flex: initial;/* el ítem se restablece con los valores iniciales de Flexbox */flex: 0 1 auto;
	flex: auto;/* los ítems pueden crecer y llenar el contendor así como encoger si se requiere */flex:1 1 auto;
	flex: none;/* se crearán ítems flex totalmente inflexibles */flex: 0 0 auto;
	flex:; /* <positive-number>*/flex: x x x;
	flex: 0 0 calc(33.3% - 1rem);/* Ej. aquí el rem es como un padding */
	top: 80vh;
}
```
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
