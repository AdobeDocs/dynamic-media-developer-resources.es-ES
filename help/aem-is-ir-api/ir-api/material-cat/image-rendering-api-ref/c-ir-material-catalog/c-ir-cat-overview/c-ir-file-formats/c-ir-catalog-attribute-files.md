---
title: Archivos de atributos del catálogo
description: Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Archivos de atributos del catálogo{#catalog-attribute-files}

Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un `.ini` sufijo de archivo. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos del catálogo constan de un conjunto de registros de texto separados por un único `<CR>` (Código ASCII 0xD), una sola `<LF>` (código ASCII 0xA), o `<CR><LF>` par. Cada registro consta de un nombre de atributo y uno o varios valores de atributo separados por coma:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo; puede constar de una o varias letras, números, '-' y '_'; no distingue entre mayúsculas y minúsculas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de atributo; no debe incluir <span class="codeph"> &lt;cr&gt; </span>o <span class="codeph"> &lt;lf&gt; </span> , a menos que se haya escapado con una sola barra invertida justo antes del carácter de nueva línea. </p> </td> 
 </tr> 
</table>

* El espacio en blanco entre tokens es opcional.
* Los registros con nombres de atributo desconocidos se ignoran mediante la variable [!DNL Platform Server].
* Los nombres de atributos pueden constar de cualquier combinación de letras ASCII, números y &quot;-&quot;, &quot;_&quot; y &quot;.&quot;
* Si el mismo nombre de atributo se produce más de una vez en el mismo archivo de atributos, prevalecerá el último encontrado.
* Utilice &#39;#&#39; como primer carácter para marcar cualquier registro como comentario que el analizador ignore.
