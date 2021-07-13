---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Developer,User
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> La cadena de comando del Servidor de imágenes que se aplica a la imagen de la página. Si se especifica en la dirección URL, todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben codificarse con HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota:  No se admiten los comandos de manipulación del tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-df5a0604766b4ac2b9a6742b377e427c}

Opcional.

## Predeterminado {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Ninguno.

## Ejemplo {#section-813de2905d6c44c0991cfe0931581462}

Cuando se especifique en la dirección URL del visor.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Cuando se especifique en los datos de configuración.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
