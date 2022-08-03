# Genera Aplicaciones - Utilidades
## Snippets
<p>Escriba con Markdown y algunos snippets.</p>
Los snippets son fragmentos de texto que representan de forma simplicada un bloque HTML o Markdown a generar.
La regla es sencialla, escriba "." y seguido el nombre del snippet.

#### Center
".center" más el elemento HTML a centrar con su texto, seprado entre comas y todo entre corchetes. Se puede usar un Heading (h1 a h6) o Paragraphs (p).
<pre>.center[tag, text]</pre>
Ejemplos
<pre>.center[h1, Hola mundo]</pre>
<pre>.center[h2, Hola mundo]</pre>
<pre>.center[h3, Hola mundo]</pre>
<pre>.center[h4, Hola mundo]</pre>
<pre>.center[h5, Hola mundo]</pre>
<pre>.center[h6, Hola mundo]</pre>
<pre>.center[p, Hola mundo]</pre>
Nota: este snippet agrega formato al texto para reducir el espacio entre lineas con el siguiente style:
 style="margin-top:10px;margin-bottom:0px;"

#### InputBox
".inputbox" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input.
<pre>.inputbox[]</pre>
<pre>.inputbox[Ingrese un texto:]</pre>

#### TextArea
".textarea" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input.
<pre>.textarea[]</pre>
<pre>.textarea[Ingrese un texto:]</pre>

#### CheckBox
".checkbox" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input. Puede generar más de un checkbox si los separa entre comas.
<pre>.checkbox[option-1,option-n]</pre>
Ejemplos
<pre>.checkbox[]</pre>
<pre>.checkbox[Ok entendido]</pre>
<pre>.checkbox[Manzana, Naranja, Frutilla]</pre>

#### RadioBox
".radiobox" más una lista de texto separada por comas y entre corchetes. La primer coma representa el name (evita la multiselección de los radio buttons).
<pre>.radiobox[name_radio,option-1,option-n]</pre>

#### Link
".a" más la URL y el nombre a mostrar, todo entre corchetes. El link se abrirá en la misma ventana.
<pre>.a[https://google.com Google]</pre>

#### LinkBlank
".a.b" más la URL y el nombre a mostrar, todo entre corchetes. El link se abrirá en un nuevo tab del navegador.
<pre>.a.b[https://google.com Google (new Tab)]</pre>

#### Section
".section" para navegar dentro del documento.
<pre>.section[section_name,sectionLabel]</pre>

#### Select
".select" más una lista de texto separada por comas y entre corchetes. La primer coma representa el titulo.
<pre>.select[title,option-1,option-n]</pre>
Ejemplo:
<pre>.select[Saludos,,Hola,Como va, Que tal]</pre>

#### Table - Markdown
".table.m" genera un snippet de table Markdown de dos columnas y dos filas.
<pre>.table.m</pre>

#### Table - HTML
".table.h" genera un snippet de table HTML de tres columnas y dos filas.
<pre>.table.h</pre>

