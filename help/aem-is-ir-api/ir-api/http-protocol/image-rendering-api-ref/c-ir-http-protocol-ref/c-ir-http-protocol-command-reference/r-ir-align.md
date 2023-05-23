---
title: alinear
description: Alineación de renderización de textura. Especifica los puntos de origen definidos por el objeto de viñeta seleccionado que se van a utilizar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 3%

---

# alinear {#align}

Alineación de renderización de textura. Especifica los puntos de origen definidos por el objeto de viñeta seleccionado que se van a utilizar.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origen predeterminado (coincidencia central). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origen de coincidencia continua. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alineación aleatoria. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Origen definido por el usuario. </p></td> 
 </tr> 
</table>

El procesador aplica la textura al objeto de forma que el punto de ancla de la textura ( `anchor=`) coincide con el punto de origen especificado.

Cada objeto puede definir hasta seis puntos de origen (0, 1, 3, 4, 5, 6). Si un `align` se especifica el valor, pero el punto de origen correspondiente no está definido por el objeto de viñeta; se utiliza el punto de origen predeterminado (coincidencia central).

`align=2` Especifica una alineación de textura aleatoria, en cuyo caso `anchor=` se ignora de forma efectiva.

Se utiliza principalmente para materiales de tapicería, posiblemente para telas de ropa, para administrar la alineación de la textura entre objetos adyacentes.

## Propiedades {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Atributo de material. Se ignora si se selecciona un objeto de marco de revestimientos de pared, armario, equipo o ventana, o si el material no es una textura repetible.

## Predeterminado {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si el material se basa en una entrada de catálogo; en caso contrario, 0 (centrado).

## Véase también {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
