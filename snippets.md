# Genera Forms - Utilidades
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

## Form - CRUD (DOM)
<p>Combinando los snippets y los HML data-* attribute puede generar un CRUD sobre los mismos elementos del documento de la página, es decir, se realiza la manipulación del DOM para agregar o quitar elementos HTML. Vea los siguientes ejemplos:</p>

#### CRUD de formulario
s.form + s.button + data-gx-crud-type + data-gx-fieldset-index + data-gx-form-index
```
<center><h1 style="margin-top:10px;margin-bottom:20px;">Form CRUD</h1></center>  
<form>
<fieldset id="fieldset0">
<label for="inputbox">Hola:&nbsp;</label><input type="text" id="inputbox" name="inputbox" placeholder=" mundo..." style="border-radius:0.25rem;border-width:1px;border-color:black;margin-bottom:10px;width: 62%;">&nbsp;<button class="gxButton" data-gx-crud-type="remove" data-gx-form-index="0" data-gx-fieldset-index="0" type="button" style="border-radius:0.25rem;border-width:1px;border-color:black;padding-left:5px;padding-right:5px;" >Quitar</button><br></fieldset>
<button class="gxButton" data-gx-crud-type="clone-clean" data-gx-form-index="0"  data-gx-fieldset-index="0" type="button" style="border-radius:0.25rem;border-width:1px;border-color:black;padding-left:5px;padding-right:5px;float: right;" >Agregar</button>
</form>
```

#### CRUD de table
s.form + s.datatable + s.button + data-gx-crud-type + data-gx-fieldset-index + data-gx-form-index + data-gx-html-target
```
<form>
<table>
<tbody id="target0">
  <tr>
    <th>Columna 1</th>
    <th>Columna 2</th>
    <th>Columna 3</th>
  </tr>
  <tr id="fieldset0">
    <td>hola</td>
    <td>mundo</td>
    <td>como va</td>
  </tr>
</tbody>
</table>
<button class="gxButton" data-gx-html-target="target0" data-gx-crud-type="clone-clean" data-gx-form-index="0" data-gx-fieldset-index="0" type="button" style="border-radius:0.25rem;border-width:1px;border-color:black;padding-left:5px;padding-right:5px;float: right;">Agregar</button>
</form>
```

## HTML data-* attribute
<p>Con los siguientes tags puede marcar el HTML y generar la funcionalidad de agregar o eliminar elementos:</p>

#### data-gx-form-index
Indica el index del form al que quiere hacer referencia.

#### data-gx-html-target
Indica el id del del elemento al que quiere hacer referencia. Se suele usar cuando se quiere hacer el insert o delete de elementos HTML que no estan agrupados en un fielset o el fieldset se encuentra anidado o dentro de un elemento que no puede cortarse con fieldset, por ejemplo un table.

#### data-gx-form-index
Indica el index del form al que quiere hacer referencia.

#### data-gx-crud-type
Indica el tipo de manipulación sobre los elementos HML:
 1. clone  
    Duplica los elementos HTML agrupados por otro elemento marcado con el atributo id="fieldsetN" (n = número de índice único).
 2. clone-clean  
    La misma funcionalidad de clone pero limpia todos los imputs.
 4. remove  
    Permite eliminar un grupo de elementos HTML.

#### data-gx-fieldset-index
Indica el index del fielset al que quiere hacer referencia. Recuede que para manipular un grupo de elementos a la vez debe encerrar dichos elementos por otro (div, fieldset, row, etc) y agregarle el atributo id con el siguiente formato:  
 id="fieldsetN" (n = número de índice único).
 
#### data-gx-form-persist
Atributo para persistir los datos del form en [JSONBlob](https://jsonblob.com/) (ver para más detalle [Persistencia - JSONBlob](#JSONBob))

## Persistencia
### Local
<p>Se persiste el valor de los HTML inputs que se encuentren dentro de un HTML form y que posean el atributo name en el localStorage de cada dispositivo.</p>
### JSONBob
<p>Se persiste el valor de los HTML inputs que se encuentren dentro de un HTML form y que posean el atributo name más el HTML data-* attribute **data-gx-form-persist.</p>

## Librerias externas
<p>generaForms y generaCRUD por defecto soportan Alpinejs y Tailwindcss.</p>

```
<h1 x-data="{ message: 'I ❤️ Alpine' }" x-text="message" style="text-align: center;"></h1>
<a href="" class="block overflow-hidden rounded-2xl" >
  <img style="margin-bottom: 0px;margin-top: 0px;"class="object-cover w-full h-56" src="https://images.unsplash.com/photo-1524758631624-e2822e304c36?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80" alt="" />
 <div class="p-4 bg-gray-900">
 <p class="text-xs text-gray-500">website.com</p>
<h5 class="text-sm text-white">How to position your furniture for positivity</h5>
<p class="mt-1 text-xs text-gray-500">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum nobis aliquid accusamus? Sint, sequi voluptas.</p>
 </div>
</a>
```
## Form css
<p>generaForms y generaCRUD poseen su propio css (static/form.css) con las siguientes clases:</p>

#### ga-disabled
esta clase desabilita todo el conjunto de elementos contenidos dentro de otro elemento HTML.
```
<form class="ga-disabled" action="/action_page.php">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname"><br><br>
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname"><br><br>
  <input type="submit" value="Submit">
</form>
```
