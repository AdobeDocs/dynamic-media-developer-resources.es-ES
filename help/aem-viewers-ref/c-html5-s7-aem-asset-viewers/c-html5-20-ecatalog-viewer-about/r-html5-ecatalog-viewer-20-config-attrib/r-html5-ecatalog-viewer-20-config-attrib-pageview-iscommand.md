---
description: nulo
seo-description: nulo
seo-title: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic media
uuid: 6c853c6a-a57d-4cab-ad71-74baf9e870d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> La cadena de comandos del servicio de imágenes que se aplica a la imagen de página. Si se especifica en la dirección URL, todas las incidencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben estar codificadas en HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota:  No se admiten los comandos de manipulación de tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-df5a0604766b4ac2b9a6742b377e427c}

Opcional.

## Predeterminado {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Ninguno.

## Ejemplo {#section-813de2905d6c44c0991cfe0931581462}

Cuando se especifica en la URL del visor.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
