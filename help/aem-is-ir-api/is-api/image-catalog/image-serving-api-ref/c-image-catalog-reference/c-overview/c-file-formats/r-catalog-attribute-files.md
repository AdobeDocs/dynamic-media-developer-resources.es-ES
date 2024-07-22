---
description: Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
title: Archivos de atributos de catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Archivos de atributos de catálogo{#catalog-attribute-files}

Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos de catálogo constan de un conjunto de registros de texto, separados por un único `<CR>` (código ASCII `0xD`), un único `<LF>` (código ASCII `0xA`) o un par `<CR><LF>`. Cada registro consta de un nombre de atributo y uno o más valores de atributo separados por comas:

`*`nombre`*= *`valores`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valores</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nombre</span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo. Puede constar de una o más letras, números, - y _. No distingue entre mayúsculas y minúsculas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valor de atributo. No debe incluir <span class="codeph"> &lt;CR&gt;</span> o <span class="codeph"> &lt;LF&gt;</span> caracteres, a menos que se escape con una sola barra invertida justo antes del carácter de nueva línea. </p></td> 
 </tr> 
</table>

El espacio en blanco entre tokens es opcional.

El [!DNL Platform Server] omite los registros con nombres de atributo desconocidos.

Los nombres de atributo pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot;, &quot;_&quot; y &quot;.&quot;.

Si el mismo nombre de atributo aparece más de una vez en el mismo archivo de atributos, prevalecerá el último que se encuentre.

Utilice # como primer carácter para marcar cualquier registro como comentario, lo que el analizador ignora.
