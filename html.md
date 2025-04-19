# :memo: Notes
## HTML
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Web Standards Project](https://www.webstandards.org/)
- [W3C](https://www.w3.org/)
- [WHATWG](https://whatwg.org/)
- [MDN Web Docs](https://developer.mozilla.org/en-US/)
- [HTML Reference](https://htmlreference.io/)
- [All HTML tags](https://allthetags.com/)
- [W3C HTML5 Reference](https://dev.w3.org/html5/html-author/)
- [MDN HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [W3Schools HTML Element Reference](https://www.w3schools.com/TAGS/default.ASP)
- [HTML: Hypertext Markup Language](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3C Developers](https://www.w3.org/developers/)
- [The HTML validator](https://validator.w3.org/)
- [W3C](https://www.w3.org/)
- [W3C HTML5 Reference](https://dev.w3.org/html5/html-author/)
- [The HTML validator](https://validator.w3.org/)
- [W3C Developers](https://www.w3.org/developers/)
- [WHATWG](https://whatwg.org/)
- [HTML: Hypertext Markup Language](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML 5 en la educación](http://www.ite.educacion.es/formacion/materiales/182/cd/indice.htm)
- [WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/wcag3-intro/)
- [W3C Making the Web Accessible](https://www.w3.org/WAI/)
- [HTML5 Accessibility](https://html5accessibility.com/)
- [MDN A good basis for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
- [HTML Dog](https://www.htmldog.com/)
### Terms and concepts
- HTML or HyperText Markup Language
- Syntax
- Indention
- Comments
- Case-insensitive
* File HTML
	* Basic structure
		- Document type declaration
		* Root element
			- Basic elements
* Metadata
	- Basic
	- Advanced
* Markup or Tag or Element
	- Attribute
	- Value
	* Default properties
		- Block type
		- Line type
* Tag
	- Open tag
	- Close tag
	- Self-closing tag
* Hierarchy
	- Parent element
	- Sibling element
	- Child element
- Generic elements
* Semantic tags
	* Structure
		- Header
		- Nav
		- Main
		- Aside
		- Footer
	* Substructure
		- Section
		- Article
	* Typography
		- Headings
		- Headings group
		- Paragraph
	* Content
		- Image
		* Link
			- Dead link
			- Internal
			* external
				-	Prevent Tabnabbing
		- Lists
		- Table
		- Address
		- Interactive
		- Multimedia
		- Iframes
		- Horizontal line
		- Line Break
		- Buttons
		* Form
			- Labels
			- Inputs
			- Groups
			- Selects
			- Areas
		- Script
- Character entities
- Character sets
- Tree structure
- Accessibility
- SEO
- DOM and tree DOM
#### Examples
```
<!-- HTML comments -->
<!--  -->
<!DOCTYPE html><!-- declaración estandar HTML5 -->
<html lang="en" dir="ltr"><!-- indicar el idioma del contenido del documento -->
<html lang="es-co"><!-- mejores resultados a nivel local -->
	<head><!-- información para navegadores y buscadores -->
    <meta charset="UTF-8"><!-- indicar codificación, interpretación de acentos y caracteres especiales -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover"><!-- responsive -->
    <title>Tags</title><!-- título de la pestaña del documento -->
    <meta name="google-site-verification" content=""><!-- código de verificación del sitio suministrado por google -->
  	<meta http-equiv="X-UA-Compatible" content="IE=edge"><!-- compatibilidad iexplorer -->
		<meta name="robots" content=""><!-- permisos al robot de busqueda -->
		<meta name="copyright" content=""><!-- copyright del documento -->
		<meta name="owner" content=""><!-- propietario del documento -->
		<meta name="author" content=""><!-- autor del contenido del documento -->
		<meta name="web_author" content=""><!-- developer del documento -->
		<meta name="description" content=""><!-- descripción del sitio, hasta 170 caracteres-->
		<meta name="keywords" content=""><!-- palabras clave, recomendado 10 palabras -->
		<meta http-equiv="refresh" content=""><!-- programar un refresco o redireccionamiento de la página -->
		<meta name="theme-color" content=""><!-- color barra navegador -->
		<meta property="" content=""><!-- The Open Graph protocol -->
		<base href="" target="_blank"><!-- Specify a default URL and a default target for all links on a page -->
		<link rel="canonical" href=""><!-- página canonica -->
		<link rel="apple-touch-icon" href=""><!-- ícono dispositivos touch -->
		<link rel="shortcut icon" type="image/x-icon" href=""><!-- agregar icono "favicon" -->
		<link rel="icon" href=""><!-- otra forma de agregar icono "favicon" -->
		<link rel="stylesheet" type="text/css" href=""><!-- enlazar hoja de estilos css -->
    <link rel="preconnect" href="" /><!-- -->
    <link rel="preload" href="" as="style" /><!-- -->
		<style type="text/css"></style><!-- agregar estilos css dentro del mismo html -->
 		<script type="text/javascript"></script><!-- agregar código javascript -->
		<script language="javascript" type="text/javascript" src=""></script><!-- Llamar librerías externas -->
		<noscript></noscript><!-- para mostrar mensaje si no tiene habilitado javascript -->
	</head>
	<body><!-- lo incluido en "body" es lo que visualiza el usuario en el navegador -->
		<noscript>
      It looks like JavaScript is currently disabled in your browser. For the
      best experience and full functionality of this site, please enable
      JavaScript.
    </noscript>
		<!-- Semánticos -->
		<header></header><!-- encabezamiento -->
		<nav></nav><!-- menu de navegación -->
		<main role="main"></main><!-- contenido principal -->
		<aside></aside><!-- contenido secundario -->
		<footer></footer><!-- pie de página -->
		<article></article><!-- articulo, area especifica -->
		<section></section><!-- sección, area global -->
		<h1></h1><!-- encabezados, para definir orden de importancia, tipo h1 solo 1 -->
		<h2></h2><!-- encabezado tipo h2, puede haber más de uno -->
		<h3></h3><!-- encabezado tipo h3, puede haber más de uno -->
		<h4></h4><!-- encabezado tipo h4, puede haber más de uno -->
		<h5></h5><!-- encabezado tipo h5, puede haber más de uno -->
		<h6></h6><!-- encabezado tipo h6, puede haber más de uno -->
		<hgroup></hgroup><!-- agrupar, relacionar encabezados -->
		<address></address><!-- dirección -->
		<time></time><!-- representa la fecha de publicación de su elemento padre "article" o "body" -->
		<details></details>
		<figure></figure><!-- contenedor para imagen -->
		<figcaption></figcaption><!-- acompañar la imagen con un texto -->
		<mark></mark><!-- texto marcado resaltado -->
		<summary></summary>
		<p></p><!-- parrafos -->
		<em></em>
		strong
		b
		small
		cite
		<!-- No semánticos -->
		<div></div><!-- contenedor generico, no semántico -->
		<span></span><!-- no semántico, dar estilo, funciona el línea, no cambia comportamiento  -->
		<small></small><!-- texto pequeño -->
		<br/><!-- salto de línea -->
		<a href="tel:+57-300-560-0756">+57 300 560 0756</a><!-- teléfono -->
		<a href="#" title="" target=""></a><!-- agregar enlace, link o vínculo -->
		<a href="mailto:#"></a><!-- link a email -->
		<a name="nombre"></a><!-- nombrar sección -->
		<a href="#nombre"></a><!-- crear enlace a la sección nombrada-->
		<a href="#menu" title="" style="display:none">Ir a menú</a><!-- agregar enlace o link a un punto especifico dentro de la misma página -->
		<hr/><!-- línea horizontal -->
		<strong></strong><!-- negritas, "strong" tiene importancia semántica -->
		<em></em><!-- enfasis, tiene importancia semántica -->
		<blockquote></blockquote><!-- citar texto, identar dentro es mejor agregar parrafo dentro -->
		<cite></cite><!-- citar texto -->
		<code></code><!-- encerrar fragmentos de código fuente que se muestran en línea con el texto -->
		<abbr></abbr><!-- abreviatura -->
		<img src="" alt="" title="" longdesc=""><!-- agregar imagen -->
		<svg></svg><!-- imagen en formato SVG -->
    <picture></picture><!-- -->
		<audio src="" controls="" autoplay="" loop="" preload=""></audio><!-- agregar audio -->
		<video src="" controls="" autoplay="" loop="" width="" height=""></video><!-- agregar vídeo -->
		<source src="" type=""><!-- útil al agregar varios audios y\o videos -->
		<iframe src="" width="" height="" scrolling="" frameborder="" allowfullscreen></iframe><!-- incrustar una página web dentro de otra -->
		<map></map><!-- identificar un mapa de imágenes -->
		<area shape="" coords="" href=""><!-- definir las areas que voy a activar en la imagen -->
		<ul></ul><!-- lista desordenada -->
		<ol></ol><!-- lista ordenada -->
		<li></li><!-- elemento de la lista -->
		<dl><!-- lista de definiciones -->
			<dt></dt><!-- término a definir -->
			<dd></dd><!-- definición del término -->
		</dl>
		<form action="" method="" enctype=""><!-- agregar formularios -->
			<legend></legend><!--  -->
			<label for=""></label><!-- etiquetar -->
			<fieldset></fieldset><!-- enmarcar los elementos -->
			<legend></legend><!-- titular lo enmarcado -->
      <label></label><!-- para etiquetar y "for" para relacionar con el "id" -->
			<input type="text"><!-- tipo texto -->
			<input type="email"><!-- tipo email -->
      <input type="radio"><!-- tipo radio, para seleccionar una de las opciones -->
			<input type="checkbox"><!-- tipo checkbox, para seleccionar o no -->
			<input type="password"><!-- tipo password, para no revelar en pantalla -->
			<input type="color"><!-- tipo color, permite seleccionar el color y enviar su nombre hexa -->
      <input type="image"><!-- tipo color, permite seleccionar el color y enviar su nombre hexa -->
			<input type="number"><!-- tipo número -->
			<input type="range"><!-- tipo rango, entre un rango determinado -->
			<input type="url"><!-- tipo url, permite recibir una dirección url -->
      <input type="date"><!-- tipo date, permite recibir una fecha -->
      <input type="month"><!-- permite recibir un mes -->
      <input type="week"><!-- recibir una semana -->
      <input type="time"><!-- recibir una hora -->
      <input type="datetime"><!-- recibir fecha y hora -->
			<optgroup></optgroup><!--  -->
			<textarea></textarea><!-- área de texto -->
			<select><!-- lista desplegable de selección, para seleccionar alguna o algunas de los opciones -->
				<option></option><!-- definir opciones -->
			</select>
      <datalist>
        <option></option><!-- definir opciones -->
      </datalist>
			<input type="value="><!-- botones -->
			<input type="hidden"><!-- tipo oculto, permite enviar datos sin la interacción del usuario, necesita un atributo radio con un valor, sino, no tendria dato a enviar -->
			<input type="reset"><!-- tipo reinicio, para restablecer todos los valores a predeterminados -->
			<input type="submit"><!-- botón para enviar los datos -->
			<input type=button><!-- botón normal -->
			<input type=submit><!-- botón de envío -->
		</form>
		<table><!-- crear tabla -->
			<caption></caption><!-- titular una tabla -->
			<thead></thead><!-- indica cabecera de la tabla -->
			<tbody></tbody><!-- indica cuerpo de la tabla -->
			<tfoot></tfoot><!-- indica pie de la tabla -->
				<tr><!-- table row, para agregar fila a la tabla -->
				<th></th><!-- table head, para poner encabezados (celda) -->
				<th rowspan=""></th><!-- combinar filas -->
				<th colspan=""></th><!-- combinar columnas -->
			</tr>
			<tr><!-- table row, para agregar fila a la tabla -->
				<td headers=""></td><!-- table data, elemento, celda -->
				<td rowspan=""></td><!-- combinar filas -->
				<td colspan=""></td><!-- combinar columnas -->
			</tr>
		</table>
		<meter min="" max="" high=""></meter><!-- indicador de valores -->
		<progress min="" max=""></progress><!-- indicador de valores -->
		<q></q><!-- citar texto en comillas -->
		<b></b><!-- negritas -->
		<i></i><!-- italica, por ej se usa en términos técnicos -->
		<u></u><!-- subraya el texto afectado -->
		<pre></pre><!-- preformatear el texto -->
		<del></del><!-- tachar texto, mostrar texto borrado -->
 		<ins></ins><!-- mostrar texto insertado, agregado -->
		<sup></sup><!-- texto pequeño arriba -->
		<sub></sub><!-- texto pequeño abajo -->
		<samp></samp><!-- apariencia similar a code -->
		<kbd></kbd><!-- texto que el usuario debe escribir -->
		<var></var><!-- nombre de una variable que deba ser reemplazada por su valor real, generalmente en cursiva o subrayada -->
		<dfn></dfn><!-- resaltar una palabra que se va a definir -->
		<pre></pre><!-- mostrar bloques de código, asegúrarse de reemplazar los caracteres < por &lt; y > por &gt; para evitar problemas al mostrar el código -->
		<details></details><!--  -->
		<summary></summary><!--  -->
		<button></button>
		<object type="" data=""></object><!--  -->
		<div data-miAtributo="misValores"></div><!-- Atributos personalizados -->
		<!-- caracteres especiales = inicia con: & termina con: ;  -->
		&nbsp; &lt; &gt; &amp; &cent; &pound; &yen; &euro; &copy; &reg; &trade; &times; &divide;
		<!-- OBSOLETAS -> Evitar TODAS las que dan estilos -> para estilos está CSS -->
		<center></center>
		<acronym></acronym>
		<tt></tt>
		<applet></applet>
	</body>
</html>
```
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
