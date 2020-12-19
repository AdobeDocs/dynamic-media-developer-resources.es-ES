---
description: Las viñetas se pueden crear para incluir datos de reflejo casi 3D.
seo-description: Las viñetas se pueden crear para incluir datos de reflejo casi 3D.
seo-title: Reflexiones
solution: Experience Manager
title: Reflexiones
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Reflexiones{#reflections}

Las viñetas se pueden crear para incluir datos de reflejo casi 3D.

Si se crean, se utilizan los atributos de material siguientes para definir las propiedades de superficie reflectante del material:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Atributo </p> </th> 
   <th class="entry"> <p>Descripción </p> </th> 
   <th class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Luminosidad de la superficie </p> </td> 
   <td> <p>Desde viñeta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Variación de brillo (imagen de escala de grises) </p> </td> 
   <td> <p>Ninguno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> bold=  </span> </a> </p> </td> 
   <td> <p>Endurecimiento de la superficie </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Tipo de material </p> </td> 
   <td> <p>0 (desconocido) </p> </td> 
  </tr> 
 </tbody> 
</table>

El procesador ajusta el intervalo de los atributos `gloss=` y `rough=` según `type=`. Algunos tipos de materiales, como la tela, son por lo general menos reflectantes que los tipos de materiales, como la piedra o el metal, y la misma cantidad de brillo especificada para uno producirá un efecto de reflexión diferente al otro. `gloss=`y la rugosidad tiene una gama bastante amplia si no  `type=` se especifica o se establece en 0.

`glossmap=` puede utilizarse para controlar el brillo de un material píxel a píxel.
