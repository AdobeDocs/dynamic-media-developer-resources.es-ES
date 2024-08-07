---
title: clipXPath
description: Ruta de clip de capa invertida. Especifica una ruta de recorte de exclusión para la capa actual. Todas las partes de la capa que se encuentren dentro del área definida por clipXPath= se procesarán como transparentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

Ruta de clip de capa invertida. Especifica una ruta de recorte de exclusión para la capa actual. Todas las partes de la capa que se encuentren dentro del área definida por clipXPath= se procesarán como transparentes.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Datos de ruta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre de la ruta incrustada en la imagen de origen de la capa (solo ASCII). </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obtener información adicional, incluida una descripción de `*`pathName`*` y `*`pathDefinition`*`.

## Propiedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Se omite si `clipPath=` no se especifica. Ignorado por las capas de efecto.

## Predeterminado {#section-d1986aa31af14767aeb1b4a57add67f4}

Ninguno.

## Véase también {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
