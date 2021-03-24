---
description: Ajuste el contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# op_contrast{#op-contrast}

Ajuste el contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de contraste en porcentaje (-100...100 int). </p></td> 
 </tr> 
</table>

## Propiedades {#section-d319ed55057344eab0a3c93f720acdbf}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, sin ningún cambio en el contraste. Las imágenes o capas CMYK se convierten a RGB antes de aplicar la operación.

## Ejemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Disminuya el contraste y la nitidez de una capa de imagen de mayor calidad para que coincida visualmente con una foto de fondo de baja calidad:

... `&op_blur=3&op_contrast=-12&`

Una versión futura puede utilizar el brillo medio de la imagen en lugar de un brillo fijo del 50%.
