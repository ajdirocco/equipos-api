# Genera Aplicaciones - Utilidades
## Snippets
<p>Escriba con Markdown y algunos snippets.</p>
Los snippets son fragmentos de texto que representan de forma simplicada un bloque HTML o Markdown a generar.
La regla es sencialla, escriba "." y seguido el nombre del snippet.

#### Center
".center." más el elemento HTML Heading (h1 al h5) o Paragraphs. (p)
<pre>.center.h1 Soy un H1 centrado</pre>
<pre>.center.p Soy un Paragraphs centrado</pre>

#### InputBox
".inputbox" más texto opcional a la izquierda. Anteponer "t" si deseamos un inputbox dentro de un table.
<pre>.inputbox Ingrese un texto:</pre>
<pre>t.inputbox</pre>

#### TextArea
".textarea" más texto opcional a la izquierda. Anteponer "t" si deseamos un textarea dentro de un table.
<pre>.textarea Ingrese un texto:</pre>
<pre>t.textarea</pre>

#### CheckBox
".checkbox" más texto opcional a la derecha entre corchetes.
<pre>.checkbox[Ok entendido]</pre>

#### RadioBox
".radiobox" más una lista de texto separada por comas y entre corchetes. La primer coma representa el name (evita la multiselección de los radio buttons).
<pre>.radiobox[name_radio,option-1,option-n]</pre>

#### HyperLinkBlank
"." más la URL y el nombre a mostrar. El link se abrirá en un nuevo tab del navegador.
<pre>.https://google.com Google</pre>

#### HyperLink
".a" más la URL y el nombre a mostrar. El link se abrirá en la misma ventana.
<pre>.a https://google.com Google</pre>

#### Section
".section" para navegar dentro del documento.
<pre>t.section [section_name,sectionLabel]</pre>

#### Select
".select" más una lista de texto separada por comas y entre corchetes. La primer coma representa el titulo.
<pre>.select[title,option-1,option-n]</pre>
ejemplo:
<pre>.select[Saludos,,Hola,Como va, Que tal]</pre>

#### Table - Markdown
".table.m" genera un snippet de table Markdown de dos columnas y dos filas.
<pre>.table.m</pre>

#### Table - HTML
".table.h" genera un snippet de table HTML de tres columnas y dos filas.
<pre>.table.h</pre>

