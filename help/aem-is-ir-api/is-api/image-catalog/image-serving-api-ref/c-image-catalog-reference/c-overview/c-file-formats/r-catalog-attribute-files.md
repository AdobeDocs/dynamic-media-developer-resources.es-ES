---
description: Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
title: Archivos de atributos del catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# Archivos de atributos del catálogo{#catalog-attribute-files}

Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos del catálogo constan de un conjunto de registros de texto separados por un único `<CR>` (Código ASCII `0xD`), un solo `<LF>` (Código ASCII `0xA`) o a `<CR><LF>` par. Cada registro consta de un nombre de atributo y uno o varios valores de atributo separados por coma:

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo. Puede constar de una o más letras, números, - y _. No distingue entre mayúsculas y minúsculas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valor de atributo. No debe incluir <span class="codeph"> &lt;cr&gt;</span> o <span class="codeph"> &lt;lf&gt;</span> , a menos que se haya escapado con una sola barra invertida justo antes del carácter de nueva línea. </p></td> 
 </tr> 
</table>

El espacio en blanco entre tokens es opcional.

Los registros con nombres de atributo desconocidos se ignoran mediante la variable [!DNL Platform Server].

Los nombres de atributos pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot;, &quot;_&quot; y &quot;.&quot;.

Si el mismo nombre de atributo se produce más de una vez en el mismo archivo de atributos, prevalecerá el último encontrado.

Utilice # como primer carácter para marcar cualquier registro como comentario, lo que el analizador ignora.
