---
description: Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
seo-description: Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
seo-title: Archivos de atributos del catálogo
solution: Experience Manager
title: Archivos de atributos del catálogo
topic: Scene7 Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Archivos de atributos del catálogo{#catalog-attribute-files}

Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos del catálogo constan de un conjunto de registros de texto, separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un `<CR><LF>` par. Cada registro consta de un nombre de atributo y uno o varios valores de atributo separados por coma:

` *``*= *`namevalúa`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo. Puede constar de una o más letras, número, - y _. No distingue entre mayúsculas y minúsculas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valor de atributo. No debe incluir <span class="codeph"> &lt;CR&gt;</span> ni <span class="codeph"> &lt;LF&gt;</span> caracteres, a menos que se escape con una sola barra invertida justo antes del carácter de nueva línea. </p></td> 
 </tr> 
</table>

El espacio en blanco entre tokens es opcional.

El servidor de plataformas ignora los registros con nombres de atributos desconocidos.

Los nombres de atributo pueden constar de cualquier combinación de letras ASCII, números, así como &quot;-&quot;, &quot;_&quot; y &quot;.&quot;.

Si el mismo nombre de atributo aparece más de una vez en el mismo archivo de atributo, prevalecerá el último que se encuentre.

Utilice # como el primer carácter para marcar cualquier registro como comentario, lo que el analizador omite.
