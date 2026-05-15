---
title: lechada
description: Grosor y color de la lechada de mosaico. Simula la lechada para azulejos de cerámica y piedra natural.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# lechada {#grout}

Grosor y color de la lechada de mosaico. Simula la lechada para azulejos de cerámica y piedra natural.

lechada= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>Color de la agrupación (gris o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ancho </span> </span> </p> </td>
  <td class="stentry"> <p>Grosor de la agrupación; unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td>
 </tr> 
</table>

Para un control máximo del aspecto de la lechada, se aplican los siguientes requisitos:

* El mosaico debe ser cuadrado o rectangular; actualmente no se admiten otras formas.
* La imagen solo debe contener un único mosaico.
* La lechada por defecto de la imagen (si la hay) debe tener el mismo espesor en los cuatro bordes.
* El grosor de la lechada predeterminada debe especificarse en el catálogo de materiales ( `catalog::GroutWidth`).

## Propiedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*`color`*` debe ser un valor de color RGB. `*`width`*` debe ser un valor real de 0 o superior.

Se ignora si la repetición = 4, 5, 7, 8, 9, 14 o más, o si se especifica para materiales que no sean texturas repetibles.

## Predeterminado {#section-bfab3621f70b4489a21994ab11b20cc6}

Si no se especifica `grout=`, la lechada de la imagen no se modificará. Si se especifica `grout= *`color`*`, `*`width`*` toma el valor predeterminado `catalog::GroutWidth`.

## Véase también {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
