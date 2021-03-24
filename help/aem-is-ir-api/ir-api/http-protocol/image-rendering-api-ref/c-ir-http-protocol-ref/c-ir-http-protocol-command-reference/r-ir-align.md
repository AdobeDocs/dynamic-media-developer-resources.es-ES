---
description: Alineación de renderizado de textura. Especifica cuál de los puntos de origen definidos por el objeto de viñeta seleccionado se va a utilizar.
solution: Experience Manager
title: align
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 4%

---


# align{#align}

Alineación de renderizado de textura. Especifica cuál de los puntos de origen definidos por el objeto de viñeta seleccionado se va a utilizar.

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
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>Origen definido por el usuario. </p></td> 
 </tr> 
</table>

El renderizador aplica la textura al objeto para que el punto de ancla de textura ( `anchor=`) coincida con el punto de origen especificado.

Cada objeto puede definir hasta 6 puntos de origen (0, 1, 3, 4, 5, 6). Si se especifica un valor `align` pero el punto de origen correspondiente no está definido por el objeto de viñeta, se utiliza el punto de origen predeterminado (coincidencia central).

`align=2` especifica la alineación de textura aleatoria, en cuyo caso  `anchor=` se ignora de forma efectiva.

Se utiliza principalmente para materiales de tapicería, posiblemente para tejidos de prendas de vestir, para gestionar la alineación de la textura entre objetos adyacentes.

## Propiedades {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Atributo de material. Se ignorará si está seleccionado un objeto de marco de pared, gabinete, dispositivo o cubierta de ventana, o si el material no es una textura repetible.

## Predeterminado {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si el material se basa en una entrada de catálogo, de lo contrario 0 (coincidencia central).

## Véase también {#section-945d1ce275df487d9d564d4043156c79}

[catálogo::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
