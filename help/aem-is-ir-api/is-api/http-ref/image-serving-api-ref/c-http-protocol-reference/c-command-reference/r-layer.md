---
title: capa
description: Seleccione Capa. Selecciona una capa e inicia un nuevo segmento de definición de capa en la secuencia de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# capa{#layer}

Seleccione Capa. Selecciona una capa e inicia un nuevo segmento de definición de capa en la secuencia de comandos.

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Número de capas que se van a seleccionar (0 o mayor int). </p></td> 
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

Todos los comandos del segmento de capa se aplican a la capa especificada. Un segmento de capa finaliza en la siguiente `layer=` o `effect=` o el final de la solicitud.

Especificar `layer=comp` para seleccionar la imagen compuesta (o vista, para algunos comandos).

El número de capa especifica de forma efectiva el orden Z de la capa. Las capas con números más altos se colocan sobre las capas con números más bajos.

Los números de capa no tienen que ser consecutivos. Se requiere la capa 0.

Se puede asignar un nombre a una capa con `layer= *`n`*, *`name`*` variante del comando. Una vez definida una capa con nombre, se puede hacer referencia a ella con ` layer= *`name`*`, sin necesidad de conocer el número de capa. Se pueden asignar varios nombres a la misma capa, utilizando varios `layer= *`n`*, *`name`*` comandos.

>[!NOTE]
>
>La capa 0 determina el tamaño total del lienzo de composición. Todas las partes de las capas que se encuentran fuera de los límites de la capa 0 se recortan cuando se crea el compuesto.

## Propiedades {#section-499963ee52c14f2898f0d0f90c1d01be}

Capa, comando. Las referencias de variables de sustitución no son compatibles con `layer=`.

`comp` no está permitido como *`name`* cadena. Se devuelve un error si el mismo *`name`* está asignada a más de una capa, o si hace referencia a una capa *`name`* que no se ha definido anteriormente.

## Predeterminado {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muchos comandos y atributos se aplican a la capa 0 si `layer=comp`.

## Casos especiales {#section-e087cb2e3562473e8d391abfa3b9489f}

* Si el mismo nombre se asigna a varias capas (por ejemplo: `layer=1,image&layer=2,image`), se produce un error.
* Si el mismo nombre se asigna a una sola capa varias veces (por ejemplo: `layer=1,image&layer=1,image`), el ámbito se establece de la forma habitual, sin errores.
* Se admiten varios nombres para la misma capa.

  Se puede utilizar cualquiera de los nombres para hacer referencia a la capa (por ejemplo: `layer=1,image&layer=1,picture`).
* Si un nombre al que se hace referencia nunca se asigna a un número de capa (por ejemplo: `layer=1,image&layer=picture`), se produce un error.
* Las variables de sustitución no son compatibles con los modificadores de capa (por ejemplo: `layer=$image$`).

  Esto se aplica a todas las permutaciones, no solo a los nombres de las capas, sino también a los modificadores de capas en general.

* Todas las reglas de combinación y anulación deben funcionar exactamente como cuando se hace referencia a la misma capa en varias fuentes (registros de catálogo de modificadores de solicitud, previos o posteriores, macros, etc.).

## Ejemplo {#section-cc40de6a0a754178aa752601539c815b}

Consulte los ejemplos de [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
