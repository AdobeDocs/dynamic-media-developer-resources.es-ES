---
description: Aplicar indicadores. Especifica opciones de procesamiento adicionales.
solution: Experience Manager
title: indicadores
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# indicadores{#flags}

Aplicar indicadores. Especifica opciones de procesamiento adicionales.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valor de marca. </p></td> 
 </tr> 
</table>

Actualmente sólo se utiliza para materiales de gabinete.

`flags=0` (predeterminado) representa los gabinetes superiores con puertas sólidas.

`flags=1` presenta los gabinetes superiores con puertas de cristal (si la viñeta se creó con puertas de cristal).

## Propiedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo de material. Se ignora si no es un material de gabinete, o si el objeto de gabinete de destino no permite puertas de cristal.

## Predeterminado {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` sin puertas de cristal.
