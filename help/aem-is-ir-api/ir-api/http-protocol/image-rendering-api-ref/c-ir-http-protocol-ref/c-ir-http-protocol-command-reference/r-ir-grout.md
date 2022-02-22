---
title: grut
description: Color y grosor del grupo de mosaicos. Simula el suelo para cerámica y piedra natural.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# grut {#grout}

Color y grosor del grupo de mosaicos. Simula el suelo para cerámica y piedra natural.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>Color de grupo (gris o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Grosor de la banda; unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td>
 </tr> 
</table>

Para un control máximo del aspecto del grupo, se aplican los siguientes requisitos:

* El mosaico debe ser cuadrado o rectangular; actualmente no se admiten otras formas.
* La imagen debe contener un solo mosaico.
* El grupo predeterminado de la imagen (si lo hay) debe tener el mismo grosor en los cuatro bordes.
* El grosor del grupo predeterminado debe especificarse en el catálogo de materiales ( `catalog::GroutWidth`).

## Propiedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*`color`*` Debe ser un valor de color RGB. `*`width`*` debe ser un valor real 0 o mayor.

Se ignorará si repetir = 4, 5, 7, 8, 9, 14 o superior, o cuando se especifique para materiales que no sean texturas repetibles.

## Predeterminado {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` no se especifica, el grupo de la imagen no se modifica. If `grout= *`color`*` se especifica, `*`width`*` toma como valor predeterminado `catalog::GroutWidth`.

## Véase también {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
