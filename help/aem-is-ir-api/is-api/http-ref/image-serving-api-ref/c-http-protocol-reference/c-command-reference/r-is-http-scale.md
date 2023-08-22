---
title: scale
description: Escalar imagen. Escala una imagen de origen de capa por factor en relación con la imagen de resolución completa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 9%

---

# scale{#scale}

Escalar imagen. Escala una imagen de origen de capa por factor en relación con la imagen de resolución completa.

`scale= *`factor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> factor</span> </p> </td> 
  <td class="stentry"> <p>Factor de escala (real, mayor que 0,0). </p></td> 
 </tr> 
</table>

No se aplica ninguna escala cuando `scale=1`. *`factor`* con una escala inferior a 1,0 y superior a 1,0, la imagen de origen se amplía.

## Propiedades {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Atributo de imagen/máscara de origen. Ignorado si `size=` también se especifica para la capa actual. Invalidaciones `res=`. Se aplica a la capa 0 si se especifica para `layer=comp`. Se ignora si la capa no está asociada a una imagen o máscara.

## Predeterminado {#section-26e64904362342a5a62c5f6598f330c4}

Si no se especifica, `res=` se utiliza. If `res=` no se ha especificado, la imagen se utiliza sin escalar.

## Véase también {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
