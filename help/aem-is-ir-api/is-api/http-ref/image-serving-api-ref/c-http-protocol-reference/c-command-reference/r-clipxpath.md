---
description: Ruta del clip de capa invertida. Especifica una ruta de clip de exclusión para la capa actual. Todas las partes de la capa que se encuentren dentro del área definida por clipXPath= se procesarán como transparentes.
seo-description: Ruta del clip de capa invertida. Especifica una ruta de clip de exclusión para la capa actual. Todas las partes de la capa que se encuentren dentro del área definida por clipXPath= se procesarán como transparentes.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# clipXPath{#clipxpath}

Ruta del clip de capa invertida. Especifica una ruta de clip de exclusión para la capa actual. Todas las partes de la capa que se encuentren dentro del área definida por clipXPath= se procesarán como transparentes.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de la ruta incrustada en la imagen de origen de la capa (solo ASCII). </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de `*`pathName`*` y `*`pathDefinition`*`.

## Propiedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Se omite si no se especifica `clipPath=`. Omitido por capas de efectos.

## Predeterminado {#section-d1986aa31af14767aeb1b4a57add67f4}

Ninguno.

## Véase también {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
