---
title: op_contrast
description: Ajuste el contraste. Ajusta el contraste de la imagen aumentando el brillo de los píxeles con más del 50% de brillo y reduciendo el brillo de los píxeles con menos del 50% de brillo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

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

Capa, comando. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto.

## Predeterminado {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, sin cambio de contraste. Las imágenes o capas CMYK se convierten a RGB antes de que se aplique la operación.

## Ejemplo {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Disminuya el contraste y la nitidez de una capa de imagen de mayor calidad para hacerla coincidir visualmente con una foto de fondo de baja calidad:

... `&op_blur=3&op_contrast=-12&`

Una versión futura puede utilizar el brillo medio de la imagen en lugar de un brillo fijo del 50 %.
