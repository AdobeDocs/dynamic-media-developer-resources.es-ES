---
title: opaco
description: Ajuste la opacidad de la imagen. Permite reducir la opacidad de primer plano de una imagen, texto, color sólido o capa de efecto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# opaco{#opac}

Ajuste la opacidad de la imagen. Permite reducir la opacidad de primer plano de una imagen, texto, color sólido o capa de efecto.

`opac= *`opacidad`*[, *`fillOpacidad`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> opacidad</span> </p> </td> 
  <td class="stentry"> <p>Opacidad primaria (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Opacidad de relleno (0...100 int). </p></td> 
 </tr> 
</table>

La opacidad de primer plano de una capa de imagen viene determinada por la máscara de capa o el canal alfa de la imagen o, si no hay ninguno presente, es del 100%. La opacidad de primer plano de una capa de texto es del 100% y la de una capa de color sólido está establecida por `color=`.

`opac=` nunca modifica la opacidad de las áreas rellenadas con `color=` o `bgColor=`, excepto las áreas de primer plano de las capas de color sólido y efecto (establecidas con `color=`).

Cuando se especifica en una capa de imagen, texto o color sólido, *`opacity`* aplica toda la capa, incluidas todas las capas de efecto asociadas, mientras que *`fillOpacity`* se aplica sólo al contenido de la capa principal. Cuando se especifica en una capa de efecto, *`opacity`* se aplica a la capa de efecto, mientras que *`fillOpacity`* se omite.

La opacidad efectiva para el contenido de la capa principal es ( *`opacity`* &#42; *`fillOpacity`* / 100). La opacidad efectiva para las capas de efecto es (principal *`opacity`* &#42; efecto *`opacity`* / 100).

## Propiedades {#section-ac3f136ff1584a2eab87500b7164f7fa}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`.

## Predeterminado {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, para que no haya cambios en la opacidad de la capa.

## Ejemplo {#section-9710810e96af40538652e8ae4aadd3be}

... `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`...

La opacidad del texto en este ejemplo es 90&#42;70/100=63% y la opacidad de la capa de efecto es 90&#42;50/100=45%.

## Véase también {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
