---
description: Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes para teléfonos japoneses.
solution: Experience Manager
title: proxy del servidor de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# proxy del servidor de imágenes{#image-server-proxy}

Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes para teléfonos japoneses.

## Formato URL {#section-2e8c40b0547c4f99874cdf502b338940}

El formato de URL para el proxy IS es muy similar al de las solicitudes IS normales. Los modificadores IS que se pasen al proxy se pasan al servidor de imágenes. Puede encontrar información sobre los modificadores IS en [HTTP Protocol Reference](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista de modificadores específicos de proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje del ancho utilizable del dispositivo para utilizarlo como ancho de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la altura utilizable del dispositivo para utilizarla como altura de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la propiedad de medios incrustados de límite de memoria del dispositivo a la que se limita el tamaño de respuesta. Esto solo se aplicará a las respuestas jpg. La calidad de la imagen se reducirá hasta que el tamaño de respuesta se encuentre dentro del porcentaje especificado. </p></td> 
 </tr> 
</table>

## Límite de memoria de imagen incrustada {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Si el dispositivo tiene un límite en el tamaño de las imágenes que se pueden incrustar en una página web, el tamaño de la imagen se restringirá a ese tamaño siempre que el formato de respuesta sea jpg. El proxy limita las respuestas a 500 MB si el dispositivo no tiene límite.

## Procesamiento back-end {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

El proxy descarga, verifica y carga el archivo de datos de Device Atlas una vez al día. La verificación extrae diferentes propiedades para distintos dispositivos y las compara con los valores esperados antes de aceptar los nuevos datos.
