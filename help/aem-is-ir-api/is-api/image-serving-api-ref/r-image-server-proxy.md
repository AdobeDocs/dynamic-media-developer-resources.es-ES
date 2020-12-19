---
description: Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes de los teléfonos japoneses.
seo-description: Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes de los teléfonos japoneses.
seo-title: Proxy del servidor de imágenes
solution: Experience Manager
title: Proxy del servidor de imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Proxy de servidor de imágenes{#image-server-proxy}

Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes de los teléfonos japoneses.

## Formato URL {#section-2e8c40b0547c4f99874cdf502b338940}

El formato de URL para el proxy IS es muy similar al de las solicitudes IS normales. Los modificadores IS que se pasan al proxy se pasan al servidor de imágenes. Puede encontrar información sobre los modificadores IS en la [Referencia del protocolo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista de modificador específica de proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje del ancho utilizable del dispositivo para utilizarlo como ancho de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la altura utilizable del dispositivo para utilizarlo como altura de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la propiedad de medios incrustados de límite de memoria del dispositivo para limitar el tamaño de respuesta a. Esto solo se aplicará a las respuestas jpg. La calidad de la imagen se reducirá hasta que el tamaño de respuesta esté dentro del porcentaje especificado. </p></td> 
 </tr> 
</table>

## Límite de memoria de imagen incrustada {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Si el dispositivo tiene un límite en el tamaño de las imágenes que se pueden incrustar en una página web, el tamaño de la imagen se restringirá a ese tamaño siempre que el formato de respuesta sea jpg. El proxy limita las respuestas a 500 MB si el dispositivo no tiene límite.

## Procesamiento back-end {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

El proxy descarga, verifica y carga el archivo de datos de Device Atlas una vez al día. La verificación extrae diferentes propiedades para distintos dispositivos y las compara con los valores esperados antes de aceptar los nuevos datos.
