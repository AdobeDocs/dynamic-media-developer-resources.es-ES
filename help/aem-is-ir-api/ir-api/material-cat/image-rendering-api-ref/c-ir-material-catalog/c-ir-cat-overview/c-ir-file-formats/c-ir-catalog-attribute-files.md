---
description: Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
title: Archivos de atributos del catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Archivos de atributos del catálogo{#catalog-attribute-files}

Los archivos de atributos del catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos del catálogo constan de un conjunto de registros de texto, separados por un único `<CR>` (código ASCII 0xD), un único `<LF>` (código ASCII 0xA) o un par `<CR><LF>`. Cada registro consta de un nombre de atributo y uno o varios valores de atributo separados por coma:

`*``*= *``*&#42;[, *`valorDeEvaluaciónDeNombres`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo; puede constar de una o varias letras, números, '-' y '_'; no distingue entre mayúsculas y minúsculas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de atributo; no debe incluir caracteres <span class="codeph"> &lt;CR&gt; </span> ni <span class="codeph"> &lt;LF&gt; </span>, a menos que se evite con una sola barra invertida justo antes del carácter de nueva línea. </p> </td> 
 </tr> 
</table>

* El espacio en blanco entre tokens es opcional.
* Platform Server ignora los registros con nombres de atributos desconocidos.
* Los nombres de atributos pueden consistir en cualquier combinación de letras ASCII, números, así como &quot;-&quot;, &quot;_&quot; y &quot;.&quot;
* Si el mismo nombre de atributo se produce más de una vez en el mismo archivo de atributos, prevalecerá el último encontrado.
* Utilice &#39;#&#39; como primer carácter para marcar cualquier registro como comentario que el analizador ignore.

