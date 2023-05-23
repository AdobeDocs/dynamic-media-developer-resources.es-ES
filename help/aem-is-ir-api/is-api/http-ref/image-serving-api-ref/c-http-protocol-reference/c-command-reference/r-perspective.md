---
description: Transformación en perspectiva. Aplique una transformación de perspectiva a la imagen de origen de la capa para rellenar la región especificada con el cuadrilátero. Otras áreas de la capa permanecen transparentes.
solution: Experience Manager
title: perspectiva
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# perspectiva{#perspective}

Transformación en perspectiva. Aplique una transformación de perspectiva a la imagen de origen de la capa para rellenar la región especificada con el cuadrilátero. Otras áreas de la capa permanecen transparentes.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Coordenadas cuadrilaterales en píxeles de perspectiva (8 reales, separados por comas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Coordenadas cuadrilaterales normalizadas en perspectiva (8 reales, separados por comas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opciones de remuestreo (consulte más abajo). </p></td> 
 </tr> 
</table>

*`perspQuad`* consta de cuatro valores de coordenadas de píxel en el espacio de coordenadas compuesto (o capa 0), que se origina en la esquina superior izquierda de la imagen compuesta.

`perspQuadN` consta de cuatro valores de coordenadas normalizados, donde `0.0,0.0` corresponde a la esquina superior izquierda de la imagen compuesta/de capa 0 y `1.0,1.0` en la esquina inferior derecha.

La imagen de entrada se transforma de modo que la esquina superior izquierda de la imagen de entrada se asigna al primer valor de coordenada de `perspQuad[N]`, la esquina superior derecha a la segunda coordenada, la esquina inferior derecha a la tercera coordenada y la esquina inferior izquierda a la cuarta coordenada.

>[!NOTE]
>
>`pos=` se puede utilizar para situar aún más la capa transformada en la imagen compuesta.

Las coordenadas cuadrilaterales en perspectiva pueden estar ubicadas fuera de la imagen compuesta.

El comportamiento es indefinido si el cuadrilátero no es adecuado para una transformación en perspectiva (por ejemplo, si dos o más vértices coinciden, si tres o todos los vértices están en la misma línea o si el cuadrilátero es autointersecante o cóncavo).

## Consideraciones de calidad {#section-7cc9056afa614300a9b8844d39739fc3}

Aunque la implementación predeterminada produce un compromiso razonable entre calidad y rendimiento, a veces puede ser necesario aumentar la resolución de la imagen de origen para mejorar la nitidez o reducirla para reducir los defectos de solapamiento.

Si el origen es una imagen, utilice `scale=` para elegir una resolución diferente (relativa a la resolución completa de la imagen). El especificado `scale=` El valor se redondea al siguiente nivel de resolución PTIF superior. En el caso de un origen de solicitud anidado, el tamaño de la imagen producido por la solicitud anidada se puede ajustar para lograr la nitidez deseada. Para las capas de texto, la resolución de la imagen de entrada (el texto procesado) se ajusta seleccionando un tamaño= valor más grande junto con el aumento de la resolución especificada con `textAttr=`.

*`resOptions`* permite seleccionar un algoritmo de remuestreo alternativo. Se admiten los siguientes valores (distingue entre mayúsculas y minúsculas):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Valor</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> El vecino más cercano. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bi-linear. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Supermuestreo estándar (predeterminado). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Supermuestreo con vibración ajustable (<span class="varname"> n</span> debe ser un valor entero entre 0 y 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-818e57df0a1b4449888543bc6af77751}

Capa, comando. Se aplica a la capa actual o a la capa 0 si `layer=comp`. Ignorado por las capas de efecto.

`res=` siempre se ignora cuando la perspectiva está presente en la misma capa. `size=` se ignora cuando se especifica para capas de imagen. `size=` y `res=` en capas con `perspective=` están reservadas para uso futuro.

## Predeterminado {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, para una transformación sin perspectiva.

## Véase también {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
