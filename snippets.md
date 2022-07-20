<h1 style="text-align: center;margin-top: 5px; margin-bottom: 5px;">Genera Aplicaciones</h1>
<h2 style="text-align: center;margin-top: 0px;margin-bottom: 5px;">.Tags</h2>
<p style="text-align: center;">Escriba con Markdown y algunos snippets.</p>

### .Tags
Los ".Tags" o snippets (fragmentos de código) representan de forma simplicada un tag HTML.
La regla es sencialla, escriba "." y seguido el nombre del snippet.

- #### Center
    ".center." más el elemento HTML Heading (h1 al h5) o Paragraphs. (p)
<pre>.center.h1 Soy un H1 centrado</pre>
<pre>.center.p Soy un Paragraphs centrado</pre>

- #### InputBox
    ".inputbox" más texto opcional a la izquierda. Anteponer "t" si deseamos un inputbox dentro de un table.
<pre>.inputbox Ingrese un texto:</pre>
<pre>t.inputbox</pre>

- #### TextArea
    ".textarea" más texto opcional a la izquierda. Anteponer "t" si deseamos un textarea dentro de un table.
<pre>.textarea Ingrese un texto:</pre>
<pre>t.textarea</pre>

- #### CheckBox
    ".checkbox" más texto opcional a la derecha. Anteponer "t" si deseamos un checkbox dentro de un table.
<pre>.checkbox Me gusta este checkbox.</pre>
<pre>t.checkbox</pre>

- #### RadioBox
    ".radiobox" más una lista de texto separada por comas. La primer coma representa el name (evita la multiselección de los radio buttons). Anteponer "t" si deseamos un radiobox dentro de un table del tipo HTML (no funciona en Table - Markdown).
<pre>.radiobox radio_name,hola,chau,com va</pre>
<pre>t.radiobox [name_radio,option-2,option-n]</pre>

- #### HyperLinkBlank
    "." más la URL y el nombre a mostrar. El link se abrirá en un nuevo tab del navegador.
<pre>.https://google.com Google</pre>

- #### HyperLink
    ".a" más la URL y el nombre a mostrar. El link se abrirá en la misma ventana.
<pre>.a https://google.com Google</pre>

- #### Section
    ".section" para navegar dentro del documento.
<pre>t.section [section_name,sectionLabel]</pre>


- #### Select
    ".select" más una lista de texto separada por comas. La primer coma representa el titulo. Anteponer "t" si deseamos un select dentro de un table del tipo HTML (no funciona en Table - Markdown).
<pre>.select Esto es el titulo,,hola,chau,com va</pre>
<pre>.select ,,hola,chau,com va</pre>
<pre>t.select [,option-2,option-n]</pre>
"Nota: en el "t.select" no se contempla titulo como la primer coma, son todos elementos del select.

- #### Table - Markdown
    ".table" genera un snippet de table Markdown de dos columnas y dos filas.
    <pre>.table</pre>

- #### Table - HTML
    "t.table" genera un snippet de table HTML de tres columnas y dos filas.
<pre>t.table</pre>
    Es útil para insertar dentre de los <td></td> tags HTML como el snippet t.select [,option-2,option-n] que no funciona en el Table - Markdown.
