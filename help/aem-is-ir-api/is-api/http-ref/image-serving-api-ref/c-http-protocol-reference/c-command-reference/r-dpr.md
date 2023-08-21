---
title: dpr
description: Proporción de píxeles del dispositivo (DPR)&mdash;también conocido como proporción de píxeles CSS&mdash;es la relación entre los píxeles físicos de un dispositivo y los píxeles lógicos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# dpr{#dpr}

La proporción de píxeles del dispositivo (DPR), también conocida como proporción de píxeles CSS, es la relación entre los píxeles físicos de un dispositivo y los píxeles lógicos. Especialmente con la llegada de las pantallas de retina, la resolución de píxeles de los dispositivos móviles modernos está creciendo a un ritmo rápido.

Al habilitar la optimización de la proporción de píxeles del dispositivo, la imagen se procesa con la resolución nativa de la pantalla, lo que la hace nítida.

Actualmente, la densidad de píxeles de la visualización proviene de los valores del encabezado CDN de Akamai.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> desactivado </span> </span> </p> </td> 
  <td class="stentry"> <p>Desactive la optimización del RGPD en un nivel de URL de imagen individual. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> activado, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Anule el valor del DPR detectado por Imágenes inteligentes, con un valor personalizado (tal y como lo detecta cualquier lógica del lado del cliente u otro medio). El valor permitido para dprValue es cualquier número mayor que 0. </p> </td> 
 </tr> 
</table>


Puede utilizar `dpr=on,dprValue` incluso si la configuración del DPR a nivel de compañía está desactivada.

Debido a la optimización del RGPD, cuando la imagen resultante es mayor que la configuración de MaxPix Dynamic Media, la anchura de MaxPix siempre se reconoce manteniendo la proporción de aspecto de la imagen.

| Tamaño de imagen solicitado | Valor de DPR | Tamaño de imagen entregado |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

## Propiedades



## Predeterminado

`dpr=off`


## Ejemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Véase también

[network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imágenes inteligentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)