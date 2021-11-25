---
title: PanoramicView.iscommand
description: Atributo de configuración para el visor panorámico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 2726733691296fb86b0022ac61ac654848fe83cf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Atributo de configuración para el visor panorámico.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> La cadena de comando del Servidor de imágenes que se aplica a la imagen.  Si se especifica en la dirección URL, asegúrese de codificar HTTP todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

No hay valores predeterminados.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Cuando se especifique en la dirección URL del visor.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Cuando se especifique en los datos de configuración.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
