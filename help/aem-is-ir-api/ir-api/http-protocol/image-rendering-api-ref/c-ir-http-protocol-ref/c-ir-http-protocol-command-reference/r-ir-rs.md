---
title: rs
description: Configuración avanzada de procesamiento. Especifica la configuración de procesamiento avanzada que se aplicará al procesar la selección actual.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---

# rs{#rs}

Configuración avanzada de procesamiento. Especifica la configuración de procesamiento avanzada que se aplicará al procesar la selección actual.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Cadena de configuración de procesamiento. </p></td> 
 </tr> 
</table>

Se utiliza para ajustar el aspecto del procesamiento. Para crear cadenas de configuración de procesamiento, utilice la función de renderización de la herramienta de creación de viñetas (parte del paquete de creación de imágenes de Dynamic Media).

## Propiedades {#section-9a2b2228789046658cb80eddf343af75}

Atributo de material.

## Predeterminado {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Ejemplo {#section-47e4811882574441a4d517e42a35f352}

Después de algunos experimentos en la creación de imágenes, se determina que la máscara de enfoque (USM) proporciona la cantidad correcta de enfoque para la aplicación y el material dados. La cadena de configuración de procesamiento que configura USM se copia en la variable `rs=` para usar con este material:

`…&rs=U2V20W50X2&…`

## Véase también {#section-930116e735024a008c994547ba36ee40}

[catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
