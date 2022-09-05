# Genera Aplicaciones - Utilidades
## Snippets
<p>Escriba con Markdown y algunos snippets.</p>
Los snippets son fragmentos de texto que representan de forma simplicada un bloque HTML o Markdown a generar.
La regla es sencialla, escriba "s." y seguido el nombre del snippet.

#### InputBox
"s.inputbox" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input.
<pre>s.inputbox[]</pre>
<pre>s.inputbox[Ingrese un texto:]</pre>

#### TextArea
"s.textarea" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input.
<pre>s.textarea[]</pre>
<pre>s.textarea[Ingrese un texto:]</pre>

#### Select
"s.select" más una lista de texto separada por comas y entre corchetes. La primer coma representa el titulo.
<pre>.select[title,option-1,option-n]</pre>
Ejemplo:
<pre>s.select[Saludos,,Hola,Como va, Que tal]</pre>

#### CheckBox
"s.checkbox" más texto opcional entre corchetes. El texto se mostrará a la izquierda del input. Puede generar más de un checkbox si los separa entre comas.
<pre>.checkbox[option-1,option-n]</pre>
Ejemplos
<pre>s.checkbox[]</pre>
<pre>s.checkbox[Ok entendido]</pre>
<pre>s.checkbox[Manzana, Naranja, Frutilla]</pre>

#### RadioBox
"s.radiobox" más una lista de texto separada por comas y entre corchetes. La primer coma representa el name (evita la multiselección de los radio buttons).
<pre>s.radiobox[name_radio,option-1,option-n]</pre>

#### Link
"s.a" más la URL y el nombre a mostrar, todo entre corchetes. El link se abrirá en la misma ventana.
<pre>s.a[https://google.com Google]</pre>

#### LinkBlank
"s.a.b" más la URL y el nombre a mostrar, todo entre corchetes. El link se abrirá en un nuevo tab del navegador.
<pre>.a.b[https://google.com Google (new Tab)]</pre>

#### Section
"s.section" para navegar dentro del documento.
<pre>.section[section_name,sectionLabel]</pre>

#### Table - Markdown
"s.table.m" genera un snippet de table Markdown de dos columnas y dos filas.
<pre>s.table.m</pre>

#### Table - HTML
"s.table.h" genera un snippet de table HTML de tres columnas y dos filas.
<pre>s.table.h</pre>

#### Center
"s.center" más el elemento HTML a centrar con su texto, seprado entre comas y todo entre corchetes. Se puede usar un Heading (h1 a h6) o Paragraphs (p).
<pre>.center[tag, text]</pre>
Ejemplos
<pre>s.center[h1, Hola mundo]</pre>
<pre>s.center[h2, Hola mundo]</pre>
<pre>s.center[h3, Hola mundo]</pre>
<pre>s.center[h4, Hola mundo]</pre>
<pre>s.center[h5, Hola mundo]</pre>
<pre>s.center[h6, Hola mundo]</pre>
<pre>s.center[p, Hola mundo]</pre>
**Nota:** este snippet agrega formato al texto para reducir el espacio entre lineas con el siguiente style:
 <pre>style="margin-top:10px;margin-bottom:0px;"</pre>

#### Comment
"s.comment" agrega un comentario dentro del documento fuente.
<pre>s.comment</pre>

#### Form
"s.form" genera un HTML form mas un boton que imprime todos los elementos mas sus valores que incluya dentro del form.
<pre>s.form</pre>

#### Button
"s.button" genera un HTML button.
<pre>s.button</pre>

#### Date
"s.button" genera un HTML date picker.
<pre>s.date</pre>

#### Time
"s.button" genera un HTML time picker.
<pre>s.time</pre>

#### Color
"s.color" genera un HTML color picker.
<pre>s.color</pre>


