---
title: estilo
description: estilo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: 'https://experienceleague.adobe.com/vkV2CfEEhJmPdQg64y0G-5Ep-T6SPd4tQX88CWbPryw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 7%

---

# estilo{#style}

Puede aplicar el siguiente comando desde la cadena de consulta URL y la configuración. El comando aplicado en la cadena de consulta URL siempre tiene prioridad sobre el mismo comando presente en la configuración.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Ubicación CSS relativa o absoluta. </p> <p>Especifica la ubicación del archivo CSS personalizado. Si <span class="codeph"><span class="varname"> cssPath</span></span> es relativo, se resuelve con la ubicación de la página de HTML del visor y el valor del parámetro <span class="codeph"> contentUrl=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Todas las referencias de recursos dentro del archivo CSS se resuelven en la ubicación del archivo CSS, no en la ubicación de la página de HTML que realiza la llamada.

## Propiedades {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Opcional.

## Predeterminado {#section-79a827f7a3bb4f36b3d72c309155059e}

Ninguno.

## Ejemplos {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
