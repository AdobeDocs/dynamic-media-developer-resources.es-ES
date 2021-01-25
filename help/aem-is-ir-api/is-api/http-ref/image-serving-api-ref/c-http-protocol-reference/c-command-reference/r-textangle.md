---
description: Dirección de procesamiento de texto. Especifica el ángulo en el que se coloca el texto especificado con textPs= y se procesa en el cuadro de texto (definido con size= o textFlowPath=).
seo-description: Dirección de procesamiento de texto. Especifica el ángulo en el que se coloca el texto especificado con textPs= y se procesa en el cuadro de texto (definido con size= o textFlowPath=).
seo-title: textAngle
solution: Experience Manager
title: textAngle
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ac54c186-1fc5-479a-89f2-ff2da5e7999a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# textAngle{#textangle}

Dirección de procesamiento de texto. Especifica el ángulo en el que se coloca el texto especificado con textPs= y se procesa en el cuadro de texto (definido con size= o textFlowPath=).

` textAngle= *`Ángulo`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Ángulo </span> </p> </td> 
  <td class="stentry"> <p>Ángulo de dirección (grados). </p> </td> 
 </tr> 
</table>

Los valores positivos rotan el texto en el sentido de las agujas del reloj; `textAngle=90` dibuja el texto de arriba abajo.

## Propiedades {#section-6d586a632daa4261a8ce62db56140b36}

Atributo de capa. Se aplica a `layer=0` si `layer=comp`. Se omite si no se especifica `textPs=` para esta capa o si se especifica `textPath=`.

## Predeterminado {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` sin rotación.

## Véase también {#section-dccc29ff33704061b2519b56b7be45fd}

[Formato](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) de texto,  [posición](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87) de texto,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
