---
description: nulo
seo-description: nulo
seo-title: estilo
solution: Experience Manager
title: estilo
topic: Dynamic media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# estilo{#style}

Puede aplicar el siguiente comando desde la cadena de consulta URL y desde la configuración. El comando aplicado en la cadena de consulta URL siempre tiene prioridad sobre el mismo comando presente en la configuración.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span></span> </p> </td> 
   <td colname="col2"> <p> Ubicación CSS relativa o absoluta. </p> <p>Especifica la ubicación del archivo CSS personalizado. Si <span class="codeph"><span class="varname"> cssPath</span></span> es relativo, se resuelve en la ubicación de la página HTML del visor y en el valor del parámetro <span class="codeph"> contentUrl=</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

Todas las referencias de recursos dentro del archivo CSS se resuelven en la ubicación del archivo CSS, no en la ubicación de la página HTML que realiza la llamada.

## Propiedades {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Opcional.

## Predeterminado {#section-79a827f7a3bb4f36b3d72c309155059e}

Ninguno.

## Ejemplos {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
