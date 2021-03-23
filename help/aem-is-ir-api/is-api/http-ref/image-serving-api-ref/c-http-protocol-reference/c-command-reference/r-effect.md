---
description: Seleccione Capa de efectos. Selecciona una capa de efecto e inicia un nuevo segmento de capa en la cadena de solicitud, que está asociada a la capa actual.
seo-description: Seleccione Capa de efectos. Selecciona una capa de efecto e inicia un nuevo segmento de capa en la cadena de solicitud, que está asociada a la capa actual.
seo-title: effect
solution: Experience Manager
title: effect
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---


# effect{#effect}

Seleccione Capa de efectos. Selecciona una capa de efecto e inicia un nuevo segmento de capa en la cadena de solicitud, que está asociada a la capa actual.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Número de capa de efecto (int no igual a 0). </p></td> 
 </tr> 
</table>

Todos los comandos del nuevo segmento se aplican a la capa de efecto especificada. Un segmento de capa de efecto se termina por el siguiente comando `layer=` o `effect=` o por el final de la solicitud.

*`n`* debe ser menor que 0 para los efectos de capa externa (es decir, los efectos detrás de la capa principal) y bueno que 0 para los efectos de capa interna (es decir, los efectos dentro de la capa principal). Los números de capa de efecto no tienen que ser consecutivos.

El número de capa de efecto especifica el orden z, en el caso de varias capas de efecto para la misma capa principal. Las capas con mayor número se colocan encima de las capas con menor número.

Las capas de efecto se pueden adjuntar a `layer=comp`.

## Propiedades {#section-e11f795deff345779ce280a82cf221ca}

Capa de efecto. *`n`* no debe ser 0.

## Predeterminado {#section-84bbe1cfe7a94040827c994323ac59d4}

Ninguno.

## Ejemplo {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Véase también {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
