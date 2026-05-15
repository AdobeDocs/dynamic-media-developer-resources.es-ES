---
title: Archivos de atributos de catálogo
description: Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo .ini. Se pueden mantener fácilmente con cualquier editor de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
TQID: 'https://experienceleague.adobe.com/OwtzX3xKh5ByC3eUhz7dmFjGR5HRD9cbE6atUEL0Nic'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# Archivos de atributos de catálogo{#catalog-attribute-files}

Los archivos de atributos de catálogo pueden tener cualquier nombre, pero deben tener un sufijo de archivo `.ini`. Se pueden mantener fácilmente con cualquier editor de texto.

Los archivos de atributos de catálogo constan de un conjunto de registros de texto, separados por un único `<CR>` (código ASCII 0xD), un único `<LF>` (código ASCII 0xA) o un par `<CR><LF>`. Cada registro consta de un nombre de atributo y uno o más valores de atributo separados por comas:

`*`nombre`*= *`valor`*&#42;[, *`valor`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nombre </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre del atributo; puede constar de una o más letras, números, - (guión) y _ (guion bajo); no distingue entre mayúsculas y minúsculas.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor del atributo; no debe incluir <span class="codeph"> &lt;CR&gt; </span> ni <span class="codeph"> &lt;LF&gt; </span> caracteres, a menos que se escape mediante una sola barra invertida justo antes del carácter de nueva línea. </p> </td> 
 </tr> 
</table>

* El espacio en blanco entre tokens es opcional.
* [!DNL Platform Server] ignora los registros con nombres de atributo desconocidos.
* Los nombres de atributo pueden constar de cualquier combinación de letras ASCII, números y `-`, `_` y `.` caracteres.
* Si el mismo nombre de atributo aparece más de una vez en el mismo archivo de atributos, prevalecerá el último que se encuentre.
* Use `#` como primer carácter para marcar cualquier registro como comentario que el analizador ignore.
