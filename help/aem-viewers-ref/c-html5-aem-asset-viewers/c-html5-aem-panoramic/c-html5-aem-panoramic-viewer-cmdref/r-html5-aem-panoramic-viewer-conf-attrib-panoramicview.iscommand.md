---
title: PanoramicView.iscommand
description: Atributo de configuración para el visor panorámico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Atributo de configuración para el visor panorámico.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> La cadena de comando del servicio de imágenes que se aplica a la imagen.  Si se especifica en la dirección URL, asegúrese de codificar mediante HTTP todas las apariciones de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> as <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

No hay valor predeterminado.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Cuando se especifica en la dirección URL del visor.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Cuando se especifica en los datos de configuración.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
