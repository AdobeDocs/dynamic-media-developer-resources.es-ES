---
description: Color y grosor del grupo de mosaicos. Simula el suelo para cerámica y piedra natural.
solution: Experience Manager
title: grut
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# grout{#grout}

Color y grosor del grupo de mosaicos. Simula el suelo para cerámica y piedra natural.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>Color de grupo (gris o RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Grosor de la banda; unidades de coordenadas de escena (normalmente pulgadas) (real). </p> </td> 
 </tr> 
</table>

Para un control máximo del aspecto del grupo se aplican los siguientes requisitos:

* El mosaico debe ser cuadrado o rectangular; no se admiten otras formas en este momento.
* La imagen debe contener un solo mosaico.
* El grupo predeterminado de la imagen (si lo hay) debe tener exactamente el mismo grosor en los cuatro bordes.
* El grosor del grupo predeterminado debe especificarse en el catálogo de materiales ( `catalog::GroutWidth`).

## Propiedades {#section-de78b678245b4ffda48097c345949e77}

Atributo de material. `*``*` el color debe ser un valor de color RGB. `*``*` el ancho debe ser un valor real 0 o mayor.

Se ignorará si repetir = 4, 5, 7, 8, 9, 14 o superior, o cuando se especifique para materiales que no sean texturas repetibles.

## Predeterminado {#section-bfab3621f70b4489a21994ab11b20cc6}

Si no se especifica `grout=`, el grupo de la imagen no se modifica. Si se especifica ` grout= *`color`*`, `*`width`*` toma el valor predeterminado `catalog::GroutWidth`.

## Véase también {#section-8d472906a44943f5a8557e98f2fbc71f}

[Valores de color](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
