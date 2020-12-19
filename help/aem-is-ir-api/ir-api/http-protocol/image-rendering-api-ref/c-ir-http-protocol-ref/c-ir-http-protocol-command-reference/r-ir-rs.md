---
description: Configuración avanzada de procesamiento. Especifica una configuración de procesamiento avanzada que se aplicará al procesar la selección actual.
seo-description: Configuración avanzada de procesamiento. Especifica una configuración de procesamiento avanzada que se aplicará al procesar la selección actual.
seo-title: rs
solution: Experience Manager
title: rs
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ff7fcb4-a10a-4e82-80a1-edf79ae1f717
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# rs{#rs}

Configuración avanzada de procesamiento. Especifica una configuración de procesamiento avanzada que se aplicará al procesar la selección actual.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Cadena de configuración de procesamiento. </p></td> 
 </tr> 
</table>

Se utiliza para ajustar el aspecto del procesamiento. Utilice la función de procesamiento de la herramienta de creación de viñetas (que forma parte del paquete de creación de imágenes de Scene7) para crear cadenas de configuración de procesamiento.

## Propiedades {#section-9a2b2228789046658cb80eddf343af75}

Atributo Material.

## Predeterminado {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Ejemplo {#section-47e4811882574441a4d517e42a35f352}

Después de algunos experimentos con la creación de imágenes, se determina que la máscara de enfoque (USM) proporciona la cantidad correcta de enfoque para la aplicación y el material en cuestión. La cadena de configuración de procesamiento que configura USM se copia al comando `rs=` para utilizarlo con este material:

`…&rs=U2V20W50X2&…`

## Véase también {#section-930116e735024a008c994547ba36ee40}

[catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
