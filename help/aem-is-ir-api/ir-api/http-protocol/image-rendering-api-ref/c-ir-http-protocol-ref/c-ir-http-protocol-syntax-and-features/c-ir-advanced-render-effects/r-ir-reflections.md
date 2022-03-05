---
title: Reflexiones
description: Las viñetas se pueden crear para incluir datos de reflejo casi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# Reflexiones{#reflections}

Las viñetas se pueden crear para incluir datos de reflejo casi 3D.

Si es así, se utilizan los siguientes atributos de material para definir las propiedades de superficie reflectante del material:

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
   <td> <p>De la viñeta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Variación de brillo (imagen de escala gris) </p> </td> 
   <td> <p>Ninguno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> round= </span> </a> </p> </td> 
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

El renderizador ajusta el rango de la variable `gloss=` y `rough=` de acuerdo con `type=`. Algunos tipos de materiales, como los tejidos, son menos reflectantes que los tipos de materiales, como la piedra o el metal. Además, la misma cantidad de resplandor especificada para uno a menudo produce un efecto de reflejo diferente al otro. El atributo `gloss=` y la fracturación tienen una gama bastante amplia si `type=` no se ha especificado o está establecido en `0`.

`glossmap=` Se utiliza para controlar el brillo de un material de forma píxel a píxel.
