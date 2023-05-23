---
title: lechada
description: Grosor y color de la lechada de mosaico. Simula la lechada para azulejos de cerámica y piedra natural.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

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
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Grosor de la agrupación; unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td>
 </tr> 
</table>

Para un control máximo del aspecto de la lechada, se aplican los siguientes requisitos:

* El mosaico debe ser cuadrado o rectangular; actualmente no se admiten otras formas.
* La imagen solo debe contener un único mosaico.
* La lechada por defecto de la imagen (si la hay) debe tener el mismo espesor en los cuatro bordes.
* El espesor de la lechada por defecto debe especificarse en el catálogo de materiales ( `catalog::GroutWidth`).

## Propiedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*`color`*` Debe ser un valor de color RGB. `*`anchura`*` debe ser un valor real 0 o superior.

Se ignora si la repetición = 4, 5, 7, 8, 9, 14 o más, o si se especifica para materiales que no sean texturas repetibles.

## Predeterminado {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` no se ha especificado, la lechada de la imagen no se modifica. If `grout= *`color`*` se ha especificado, `*`anchura`*` el valor predeterminado es `catalog::GroutWidth`.

## Véase también {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
