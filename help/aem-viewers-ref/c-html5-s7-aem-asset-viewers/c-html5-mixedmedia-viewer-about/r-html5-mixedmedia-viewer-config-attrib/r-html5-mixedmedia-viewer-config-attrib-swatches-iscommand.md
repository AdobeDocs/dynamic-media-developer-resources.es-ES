---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3336c4d2-0d1d-4c6f-8163-8a84a8be8c20
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> La cadena de comando del servicio de imágenes que se aplica a todas las muestras. Si se especifica en la dirección URL, asegúrese de codificar mediante HTTP todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota: No se admiten los comandos de manipulación de tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Ninguno.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Cuando se especifica en la dirección URL del visor.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
