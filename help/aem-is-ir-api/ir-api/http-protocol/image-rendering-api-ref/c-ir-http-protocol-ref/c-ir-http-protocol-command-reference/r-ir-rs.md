---
title: rs
description: Configuración de procesamiento avanzada. Especifica la configuración de procesamiento avanzada que se aplicará al procesar la selección actual.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
TQID: 'https://experienceleague.adobe.com/-wOy--XUu7TX6-rwrUFpuqz82bOwb4wpA9Pa0pM8J-4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# rs{#rs}

Configuración de procesamiento avanzada. Especifica la configuración de procesamiento avanzada que se aplicará al procesar la selección actual.

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Cadena de configuración de procesamiento. </p></td> 
 </tr> 
</table>

Se utiliza para ajustar la apariencia del procesamiento. Para crear cadenas de configuración de procesamiento, utilice la función de procesamiento de la herramienta de creación de viñetas (parte del paquete de creación de imágenes de Dynamic Media).

## Propiedades {#section-9a2b2228789046658cb80eddf343af75}

Atributo de material.

## Predeterminado {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## Ejemplo {#section-47e4811882574441a4d517e42a35f352}

Después de algunos experimentos en la creación de imágenes, se determina que el enmascaramiento de enfoque (USM) proporciona la cantidad correcta de enfoque para la aplicación y el material dados. La cadena de configuración de procesamiento que configura USM se copia en el comando `rs=` para su uso con este material:

`…&rs=U2V20W50X2&…`

## Véase también {#section-930116e735024a008c994547ba36ee40}

[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
