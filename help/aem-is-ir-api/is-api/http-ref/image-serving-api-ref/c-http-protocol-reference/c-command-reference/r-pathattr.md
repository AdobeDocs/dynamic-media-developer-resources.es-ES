---
title: pathAttr
description: Atributos de texto en ruta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# pathAttr{#pathattr}

Atributos de texto en ruta.

` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> dirección </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> | <span class="codeph"> inverso </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Posición de inicio del texto en la ruta (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Posición final del texto en la ruta (real 0,0...&lt;2,0). </p> </td> 
 </tr> 
</table>

Especifique `norm` para dibujar texto comenzando cerca del primer vértice de ruta de acceso y `reverse` para dibujar texto en la dirección opuesta, comenzando cerca del último vértice.

*`startPos`* y *`endPos`* permiten ajustar dónde se dibuja el texto en la ruta. 0,0 corresponde al primer vértice del trazado y 1,0 al último vértice; los valores intermedios expresan la distancia a lo largo del trazado entre el primer y el último vértice.

## Propiedades {#section-80f266da4e2549d89f022a3f9ff4584d}

Atributo de capa. Se omite si la capa no incluye los comandos `textPs=` y `textPath=`.

*`startPos`* debe ser mayor o igual que 0 y menor que 1.0. *`endPos`* debe ser mayor o igual que *`startPos`* y menor o igual que 1.0 cuando se aplica a una ruta de acceso abierta, o menor o igual que ( *`startPos`* + 1.0) cuando se aplica a una ruta de acceso cerrada.

## Predeterminado {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Véase también {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
