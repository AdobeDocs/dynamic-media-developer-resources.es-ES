---
description: Color y grosor del grueso del mosaico. Simula la roca para baldosas de cerámica y piedra natural.
seo-description: Color y grosor del grueso del mosaico. Simula la roca para baldosas de cerámica y piedra natural.
seo-title: grout
solution: Experience Manager
title: grout
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# grout{#grout}

Color y grosor del grueso del mosaico. Simula la roca para baldosas de cerámica y piedra natural.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Color de grupo (gris o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Espesor del grupo; unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Para el máximo control del aspecto del grupo se aplican los siguientes requisitos:

* El mosaico debe ser cuadrado o rectangular; no se admiten otras formas en este momento.
* La imagen debe contener un solo mosaico.
* El grupo predeterminado de la imagen (si lo hay) debe tener exactamente el mismo grosor en los cuatro bordes.
* El grosor del grupo predeterminado debe especificarse en el catálogo de materiales ( `catalog::GroutWidth`).

## Propiedades {#section-de78b678245b4ffda48097c345949e77}

Atributo Material. ` *`el `*` color debe ser un valor de color RGB. ` *`El `*` ancho debe ser un valor real 0 o mayor.

Se omite si la repetición es igual o superior a 4, 5, 7, 8, 9, 14 o superior, o cuando se especifica para materiales que no sean texturas repetibles.

## Predeterminado {#section-bfab3621f70b4489a21994ab11b20cc6}

Si no se especifica `grout=`, el grupo de la imagen no se modifica. Si se especifica ` grout= *`color`*`, ` *`anchura`*` tiene el valor predeterminado `catalog::GroutWidth`.

## Véase también {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
