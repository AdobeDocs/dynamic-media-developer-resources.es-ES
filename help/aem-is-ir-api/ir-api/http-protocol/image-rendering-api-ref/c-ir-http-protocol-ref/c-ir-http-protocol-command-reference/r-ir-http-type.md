---
description: Tipo de superficie de material. Especifica el tipo de superficie del material.
solution: Experience Manager
title: tipo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 333b8954-e256-4ba1-8055-c4d625470673
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 22%

---

# tipo{#type}

Tipo de superficie de material. Especifica el tipo de superficie del material.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Desconocido, el servidor utiliza el valor predeterminado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Otro </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Madera natural </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Metal pulido </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>Metal cepillado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>Metal anticuado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>Pintura </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>Ensamblado/Laca </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>Papel pintado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>Plástico </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>Superficie sólida </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>Laminado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>Vinilo </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>Cerámica </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>Piedra natural </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>Vidrio </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>Espejo </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>Tela </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>Tejido de hojas </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>Alfombra </p></td> 
 </tr> 
</table>

Se utiliza junto con `gloss=` y `rough=` para controlar los comportamientos de efecto de reflejo y brillo. Los diferentes materiales producirán diferentes efectos, incluso si `gloss=` y `rough=` son iguales.

## Propiedades {#section-2345b2508273426295ce8ac46182ea64}

Atributo de material. Se omite si la viñeta no incluye datos de reflejo 3D o si los efectos de brillo están desactivados en la viñeta.

## Predeterminado {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` si el material está basado en una entrada de catálogo. De lo contrario `type=0`. Si no se especifica, o si es `type=0`, el servidor seleccionará un valor predeterminado adecuado en función del objeto de destino y los demás atributos de material.

## Véase también {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[glose=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [aproximado=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
