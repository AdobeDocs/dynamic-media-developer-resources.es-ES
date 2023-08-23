---
title: red
description: Obtenga información acerca de cómo utilizar la optimización del ancho de banda de la red para ajustar la calidad de imagen que se proporciona en función del ancho de banda real de la red.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 96b60fd5f6e3550993cd7640138df4c9bbf6b955
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---

# red{#network}

Al activar Ancho de banda de red, se ajusta automáticamente la calidad de imagen que se proporciona en función del ancho de banda real de la red. Para un ancho de banda de red deficiente, [DPR (proporción de píxeles del dispositivo)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) la optimización se desactiva automáticamente, incluso si ya está activada.

Si lo desea, su empresa puede excluirse de la optimización del ancho de banda de la red en el nivel de imagen individual adjuntando `network=off` a la URL de la imagen.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> activado|desactivado </span> </p> </td> 
  <td class="stentry"> <p>Especifica si el ancho de banda de la red ajusta la calidad de imagen que se proporciona en función del ancho de banda de la red real (activado) o si la optimización del ancho de banda de la red está desactivada para que no se ajuste la calidad de imagen.</p> </td> 
 </tr> 
</table>

Los valores del ancho de banda de la red se basan en los valores detectados del lado del cliente de la CDN agrupada.

## Propiedades



## Predeterminado

`network=off`

## Ejemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Véase también

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [gota](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Imágenes inteligentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)