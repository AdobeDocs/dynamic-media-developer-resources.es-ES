---
title: FlyoutZoomView.imagereload
description: Configura cómo el componente recupera nuevas imágenes para la vista principal y flotante durante el cambio de tamaño.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
TQID: 'https://experienceleague.adobe.com/vyA-GdKo06kVi3jO6wlBIyov3XvKVo1vwPj3mzqyoc4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configura cómo el componente recupera nuevas imágenes para la vista principal y flotante durante el cambio de tamaño.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`ancho`*[; *`ancho`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Cuando se establece en <span class="codeph"> 0 </span>, el componente no carga nuevas imágenes durante el cambio de tamaño y la resolución de la imagen en la vista flotante no cambia. </p> <p>Cuando se establece en <span class="codeph"> 1 </span> permite especificar uno o más puntos de interrupción de anchura para la imagen cargada en la vista principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> punto de interrupción, <span class="varname"> ancho </span>[; <span class="varname"> ancho </span>] </span> </p> </td> 
   <td colname="col2"> <p>Puntos de interrupción de anchura para la imagen cargada en la vista principal. El componente siempre utiliza el mejor tamaño de ajuste para la carga inicial. Después del cambio de tamaño, se garantiza que la imagen en la vista principal siempre se descargue con la anchura igual al punto de interrupción más grande más cercano y se reduzca la escala en el cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
