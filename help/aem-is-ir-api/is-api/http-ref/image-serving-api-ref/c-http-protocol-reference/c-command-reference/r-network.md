---
title: red
description: Obtenga información acerca de cómo utilizar la optimización del ancho de banda de la red para ajustar la calidad de imagen que se proporciona en función del ancho de banda real de la red.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 3%

---

# red{#network}

Al activar Ancho de banda de red, se ajusta automáticamente la calidad de imagen que se proporciona en función del ancho de banda real de la red. Para un ancho de banda de red deficiente, la optimización [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) se desactiva automáticamente, incluso si ya está activada.

Si lo desea, su empresa puede excluirse de la optimización del ancho de banda de la red en el nivel de imagen individual adjuntando `network=off` a la dirección URL de la imagen.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> activado|desactivado </span> </p> </td> 
  <td class="stentry"> <p>Especifica si el ancho de banda de la red ajusta la calidad de imagen que se proporciona en función del ancho de banda de la red real (activado) o si la optimización del ancho de banda de la red está desactivada para que no se ajuste la calidad de imagen.</p> </td> 
 </tr> 
</table>

Los valores del ancho de banda de la red se basan en los valores detectados del lado del cliente de la CDN agrupada.

## Propiedades

Un atributo de solicitud. No tiene ningún efecto si las condiciones de la red son excelentes.

## Predeterminado

`network=off`

## Ejemplo

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Véase también

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Imágenes inteligentes](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
