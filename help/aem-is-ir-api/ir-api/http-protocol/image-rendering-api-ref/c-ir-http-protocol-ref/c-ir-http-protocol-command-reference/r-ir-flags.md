---
description: Aplicar indicadores. Especifica opciones de procesamiento adicionales.
seo-description: Aplicar indicadores. Especifica opciones de procesamiento adicionales.
seo-title: indicadores
solution: Experience Manager
title: indicadores
topic: Scene7 Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# indicadores{#flags}

Aplicar indicadores. Especifica opciones de procesamiento adicionales.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valor del indicador. </p></td> 
 </tr> 
</table>

Actualmente solo se utiliza para materiales de gabinete.

`flags=0` (predeterminado) procesa los armarios superiores con puertas sólidas.

`flags=1` presenta los armarios superiores con puertas de cristal (si la viñeta se ha creado con puertas de cristal).

## Propiedades {#section-a2b00d7bb15e449ea85178acb92d8285}

Atributo Material. Se ignora si no es un material de gabinete o si el objeto de gabinete de destinatario no permite puertas de vidrio.

## Predeterminado {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` sin puertas de cristal.
