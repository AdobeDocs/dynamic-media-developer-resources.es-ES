---
description: estilo
solution: Experience Manager
title: estilo
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 7%

---


# estilo{#style}

Puede aplicar el siguiente comando tanto desde la cadena de consulta de URL como desde la configuración. El comando aplicado en la cadena de consulta de URL siempre tiene prioridad sobre el mismo comando presente en la configuración.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Ubicación CSS relativa o absoluta. </p> <p>Especifica la ubicación del archivo CSS personalizado. Si el <span class="codeph"><span class="varname"> cssPath</span></span> es relativo, se resuelve en relación con la ubicación de la página HTML del visor y el valor del parámetro <span class="codeph"> contentUrl=</span>. </p> </td> 
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
