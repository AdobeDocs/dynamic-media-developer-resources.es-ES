---
description: Ajustar contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.
seo-description: Ajustar contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.
seo-title: op_compare
solution: Experience Manager
title: op_compare
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# op_contraste{#op-contrast}

Ajustar contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de contraste en porcentaje (-100...100 int). </p></td> 
 </tr> 
</table>

## Propiedades {#section-d319ed55057344eab0a3c93f720acdbf}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos.

## Predeterminado {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, sin cambios en contraste. Las imágenes o capas CMYK se convierten a RGB antes de que se aplique la operación.

## Ejemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Disminuya el contraste y el enfoque de una capa de imagen de mayor calidad para que coincida visualmente con una foto de fondo de baja calidad:

... `&op_blur=3&op_contrast=-12&`

Una versión futura puede utilizar el brillo medio de la imagen en lugar de un brillo fijo del 50%.
