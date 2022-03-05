---
description: Atributos de texto en ruta.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

---

# pathAttr{#pathattr}

Atributos de texto en ruta.

` pathAttr= *`Dirección`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> dirección </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> | <span class="codeph"> reverse </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Posición de inicio del texto en la ruta (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Posición del final del texto en la ruta (real 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Especifique `norm` para dibujar texto comenzando cerca del primer vértice de la ruta y `reverse` para dibujar el texto en la dirección opuesta, empezando por el último vértice.

*`startPos`* y *`endPos`* permite ajustar dónde se dibuja el texto en la ruta. 0,0 corresponde al primer vértice de la ruta y 1,0 al último vértice; los valores intermedios expresan la distancia a lo largo de la ruta entre el primer y el último vértice.

## Propiedades {#section-80f266da4e2549d89f022a3f9ff4584d}

Atributo de capa. Se omite si la capa no incluye `textPs=` y `textPath=` comandos.

*`startPos`* debe ser bueno o igual a 0 y menor que 1.0. *`endPos`* debe ser bueno que *`startPos`* y menor o igual que 1.0 cuando se aplican a una ruta abierta, o menor o igual que ( *`startPos`* + 1,0) cuando se aplica a una ruta cerrada.

## Predeterminado {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Véase también {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
