---
title: efecto
description: Seleccione Capa de efecto. Selecciona una capa de efecto e inicia un nuevo segmento de capa en la cadena de solicitud, que está asociado con la capa actual.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---

# efecto{#effect}

Seleccione Capa de efecto. Selecciona una capa de efecto e inicia un nuevo segmento de capa en la cadena de solicitud, que está asociado con la capa actual.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Número de capa del efecto (int no igual a 0). </p></td> 
 </tr> 
</table>

Todos los comandos del nuevo segmento se aplican a la capa de efecto especificada. Un segmento de capa de efecto finaliza en el siguiente `layer=` o `effect=` o al final de la solicitud.

El valor *`n`* debe ser menor que 0 para los efectos de capa exterior (es decir, los efectos situados detrás de la capa principal) y mayor que 0 para los efectos de capa interior (es decir, los efectos dentro de la capa principal). Los números de capa de efecto no tienen que ser consecutivos.

El número de capa de efecto especifica el orden Z, si hay varias capas de efecto para la misma capa principal. Las capas con números más altos se colocan sobre las capas con números más bajos.

Las capas de efecto se pueden adjuntar a `layer=comp`.

## Propiedades {#section-e11f795deff345779ce280a82cf221ca}

Comando de capa de efecto. El valor *`n`* no debe ser 0.

## Predeterminado {#section-84bbe1cfe7a94040827c994323ac59d4}

Ninguno.

## Ejemplo {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Véase también {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
