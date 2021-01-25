---
description: Seleccione Capa. Selecciona una capa y inicio un nuevo segmento de definición de capa en la secuencia de comandos.
seo-description: Seleccione Capa. Selecciona una capa y inicio un nuevo segmento de definición de capa en la secuencia de comandos.
seo-title: capa
solution: Experience Manager
title: capa
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# layer{#layer}

Seleccione Capa. Selecciona una capa y inicio un nuevo segmento de definición de capa en la secuencia de comandos.

`layer= *``*|comp[, *`nname`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Número de capas que se van a seleccionar (0 o bueno int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Seleccione la imagen compuesta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de capa. </p></td> 
 </tr> 
</table>

Todos los comandos del segmento de capa se aplican a la capa especificada. Un segmento de capa finaliza con el siguiente comando `layer=` o `effect=` o el final de la solicitud.

Especifique `layer=comp` para seleccionar la imagen compuesta (o vista, para algunos comandos).

El número de capa especifica de forma efectiva el orden z de la capa. Las capas con mayor número se colocan encima de las capas con menor número.

Los números de capa no necesitan ser consecutivos. Se requiere la capa 0.

Se puede asignar un nombre a una capa con la variante de comando `layer= *`n`*, *`name`*`. Una vez definida una capa con nombre, se puede hacer referencia a ella con ` layer= *`nombre`*`, sin necesidad de conocer el número de capa. Se pueden asignar varios nombres a la misma capa mediante varios comandos `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>La capa 0 determina el tamaño total del lienzo de composición. Todas las partes de las capas que caen fuera de los límites de la capa 0 se cortan cuando se crea la composición.

## Propiedades {#section-499963ee52c14f2898f0d0f90c1d01be}

Capa. Las referencias de variables de sustitución no se admiten en `layer=`.

`comp` no se permite como  *`name`* cadena. Se devuelve un error si el mismo *`name`* está asignado a más de una capa o si *`name`* hace referencia a una capa que no se ha definido anteriormente.

## Predeterminado {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muchos comandos y atributos se aplican a la capa 0 si `layer=comp`.

## Casos especiales {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si se asigna el mismo nombre a varias capas (por ejemplo: `layer=1,image&layer=2,image`), se produce un error.
* Si el mismo nombre se asigna a una sola capa varias veces (por ejemplo: `layer=1,image&layer=1,image`), el ámbito se establece como de costumbre, sin errores.
* Se admiten varios nombres para la misma capa.

   Se puede utilizar cualquiera de los dos nombres para hacer referencia a la capa (por ejemplo: `layer=1,image&layer=1,picture`).
* Si un nombre al que se hace referencia nunca se asigna a un número de capa (por ejemplo: `layer=1,image&layer=picture`), se produce un error.
* Los modificadores de capa no admiten variables de sustitución (por ejemplo: `layer=$image$`).

   Esto se aplica a todas las permutaciones, no sólo a los nombres de capas, sino también a los modificadores de capas en general.

* Todas las reglas de combinación y anulación deben funcionar exactamente como cuando se hace referencia a la misma capa en varios orígenes (solicitudes, registros de catálogo de modificadores anteriores o posteriores, macros, etc.).

## Ejemplo {#section-cc40de6a0a754178aa752601539c815b}

Consulte los ejemplos en [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
