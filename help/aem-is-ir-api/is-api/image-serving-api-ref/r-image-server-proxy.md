---
description: Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes de los teléfonos japoneses.
solution: Experience Manager
title: Proxy de servidor de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Proxy de servidor de imágenes{#image-server-proxy}

Se puede utilizar un proxy de servidor de imágenes para cambiar el tamaño de las imágenes de los teléfonos japoneses.

## Formato URL {#section-2e8c40b0547c4f99874cdf502b338940}

El formato de URL del proxy IS es muy similar a las solicitudes IS normales. Cualquier modificador IS pasado al proxy se pasa al servidor de imágenes. Puede encontrar información sobre los modificadores IS en la [Referencia de protocolo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista de modificadores específicos de proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;número&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje del ancho utilizable del dispositivo que se utilizará como ancho de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;número&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la altura utilizable del dispositivo que se utilizará como altura de la imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica el porcentaje de la propiedad de medios incrustados de límite de memoria del dispositivo al que se va a limitar el tamaño de la respuesta. Esto solo se aplica a las respuestas jpg. La calidad de la imagen se reduce hasta que el tamaño de respuesta se encuentra dentro del porcentaje especificado. </p></td> 
 </tr> 
</table>

## Límite de memoria de imagen incrustada {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Si el dispositivo tiene un límite en el tamaño de las imágenes que se pueden incrustar en una página web, el tamaño de la imagen se restringe a ese tamaño siempre y cuando el formato de respuesta sea jpg. El proxy limita las respuestas a 500 MB si el dispositivo no tiene ningún límite.

## Procesamiento back-end {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

El proxy descarga, verifica y carga el archivo de datos Device Atlas una vez al día. La verificación extrae diferentes propiedades para diferentes dispositivos y las compara con los valores esperados antes de aceptar los nuevos datos.
