---
title: Archivos de atributos de catálogo
description: Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Archivos de atributos de catálogo{#catalog-attribute-files}

Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un `.ini` sufijo de archivo. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos de catálogo constan de un conjunto de registros de texto, separados por un único `<CR>` (código ASCII 0xD), un solo `<LF>` (código ASCII 0xA), o a `<CR><LF>` par. Cada registro consta de un nombre de atributo y uno o más valores de atributo separados por comas:

`*`name`*= *`valor`*&#42;[, *`valor`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo; puede constar de una o más letras, números, - (guión) y _ (guion bajo); no distingue entre mayúsculas y minúsculas.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor del atributo; no debe incluir <span class="codeph"> &lt;cr&gt; </span>, o <span class="codeph"> &lt;lf&gt; </span> caracteres, a menos que se escape mediante una sola barra invertida justo antes del carácter de nueva línea. </p> </td> 
 </tr> 
</table>

* El espacio en blanco entre tokens es opcional.
* El [!DNL Platform Server] ignora los registros con nombres de atributo desconocidos.
* Los nombres de atributo pueden constar de cualquier combinación de letras ASCII, números y `-`, `_`, y `.` caracteres.
* Si el mismo nombre de atributo aparece más de una vez en el mismo archivo de atributos, prevalecerá el último que se encuentre.
* Uso `#` como el primer carácter que marca un registro como comentario que el analizador ignora.
