---
title: Reflexiones
description: Se pueden crear viñetas para incluir datos de reflexión casi 3D.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# Reflexiones{#reflections}

Se pueden crear viñetas para incluir datos de reflexión casi 3D.

Si así se ha creado, se utilizan los siguientes atributos de material para definir las propiedades de superficie reflectante del material:

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> brillo=</span> </a> </p> </td> 
   <td> <p>Brillo superficial </p> </td> 
   <td> <p>Desde la viñeta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Variación del brillo (imagen en escala de grises) </p> </td> 
   <td> <p>Ninguno </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> aproximado= </span> </a> </p> </td> 
   <td> <p>Rugosidad superficial </p> </td> 
   <td> <p>40 % </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> tipo=</span> </a> </p> </td> 
   <td> <p>Tipo de material </p> </td> 
   <td> <p>0 (desconocido) </p> </td> 
  </tr> 
 </tbody> 
</table>

El procesador ajusta el intervalo del atributo `gloss=` y `rough=` según `type=`. Algunos tipos de material, como la tela, son menos reflectantes que otros como la piedra o el metal. Además, la misma cantidad de brillo especificada para uno suele producir un efecto de reflexión diferente al otro. El atributo `gloss=` y la rugosidad tienen una gama bastante amplia si `type=` no se especifica o se establece en `0`.

`glossmap=` Se usa para controlar el brillo de un material píxel a píxel.
