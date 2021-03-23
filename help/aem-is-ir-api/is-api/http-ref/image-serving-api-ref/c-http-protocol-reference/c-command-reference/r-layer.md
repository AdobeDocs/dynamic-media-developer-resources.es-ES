---
description: Seleccione Capa. Selecciona una capa e inicia un nuevo segmento de definición de capa en la secuencia de comandos.
seo-description: Seleccione Capa. Selecciona una capa e inicia un nuevo segmento de definición de capa en la secuencia de comandos.
seo-title: capa
solution: Experience Manager
title: capa
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---


# layer{#layer}

Seleccione Capa. Selecciona una capa e inicia un nuevo segmento de definición de capa en la secuencia de comandos.

`layer= *``*|comp[, *`nname`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Número de capa que se va a seleccionar (0 o bueno int). </p></td> 
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

Todos los comandos del segmento de capa se aplican a la capa especificada. Un segmento de capa termina con el siguiente comando `layer=` o `effect=` o el final de la solicitud.

Especifique `layer=comp` para seleccionar la imagen compuesta (o vista, para algunos comandos).

El número de capa especifica efectivamente el orden z de la capa. Las capas con mayor número se colocan encima de las capas con menor número.

Los números de capa no necesitan ser consecutivos. Se requiere la capa 0.

Se puede asignar un nombre a una capa con la variante de comando `layer= *`n`*, *`name`*`. Una vez definida una capa con nombre, se puede hacer referencia a ella con ` layer= *`name`*`, sin necesidad de conocer el número de capa. Se pueden asignar varios nombres a la misma capa, utilizando varios comandos `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>La capa 0 determina el tamaño general del lienzo de composición. Todas las partes de capas que caen fuera de los límites de la capa 0 se cortan cuando se crea la composición.

## Propiedades {#section-499963ee52c14f2898f0d0f90c1d01be}

Capa. Las referencias de variables de sustitución no son compatibles con `layer=`.

`comp` no está permitido como  *`name`* cadena. Se devuelve un error si se asigna el mismo *`name`* a más de una capa o si *`name`* hace referencia a una capa que no se ha definido anteriormente.

## Predeterminado {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muchos comandos y atributos se aplican a la capa 0 si `layer=comp`.

## Casos especiales {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si el mismo nombre está asignado a varias capas (por ejemplo: `layer=1,image&layer=2,image`), se produce un error.
* Si el mismo nombre se asigna a una sola capa varias veces (por ejemplo: `layer=1,image&layer=1,image`), el ámbito se configura de la forma habitual, sin errores.
* Se admiten varios nombres para la misma capa.

   Se puede utilizar cualquiera de los nombres para hacer referencia a la capa (por ejemplo: `layer=1,image&layer=1,picture`).
* Si un nombre al que se hace referencia nunca se asigna a un número de capa (por ejemplo: `layer=1,image&layer=picture`), se produce un error.
* Las variables de sustitución no son compatibles con los modificadores de capa (por ejemplo: `layer=$image$`).

   Esto se aplica a todas las permutaciones, no solo a los nombres de capa, sino también a los modificadores de capa en general.

* Todas las reglas de combinación y anulación deben funcionar exactamente igual que cuando se hace referencia a la misma capa en varias fuentes (solicitudes, registros de catálogo de modificadores anteriores o posteriores, macros, etc.).

## Ejemplo {#section-cc40de6a0a754178aa752601539c815b}

Consulte los ejemplos en [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
