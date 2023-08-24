---
title: dpr
description: Proporción de píxeles del dispositivo (DPR)&mdash;también conocido como proporción de píxeles CSS&mdash;es la relación entre los píxeles físicos de un dispositivo y los píxeles lógicos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

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

Los valores de DPR se basan en los valores detectados del lado del cliente de la CDN agrupada. Estos valores a veces son inexactos. Por ejemplo, iPhone5 con `dpr=2`y iPhone12 con dpr=3; ambos muestran `dpr=2`. Sin embargo, para dispositivos de alta resolución, enviar `dpr=2` es mejor que enviar `dpr=1`. Sin embargo, la mejor manera de superar esta inexactitud es utilizar la DPR del lado del cliente para ofrecerle valores 100% precisos. Y funciona para cualquier dispositivo, ya sea Apple o cualquier otro dispositivo que se haya iniciado. Consulte [Uso de imágenes inteligentes con proporción de píxeles de dispositivo del lado del cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Propiedades

Un atributo de solicitud. No tiene ningún efecto si `dpr` está desactivado o si `dprValue=1`.

## Predeterminado

`dpr=off`


## Ejemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Véase también

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imágenes inteligentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)