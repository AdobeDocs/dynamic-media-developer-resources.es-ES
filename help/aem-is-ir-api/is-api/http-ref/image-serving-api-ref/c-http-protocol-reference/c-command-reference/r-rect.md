---
title: recto
description: Rectángulo de vista final. Permite desmontar la imagen de vista final en varias tiras o mosaicos, que el cliente puede enviar por separado y volver a montar sin problemas, sin artefactos a lo largo de los bordes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# recto{#rect}

Rectángulo de vista final. Permite desmontar la imagen de vista final en varias tiras o mosaicos, que el cliente puede enviar por separado y volver a montar sin problemas, sin artefactos a lo largo de los bordes.

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la esquina superior izquierda de la imagen de vista hasta la parte superior izquierda del rectángulo de vista (int, int), expresado en píxeles, después de aplicar la escala <span class="varname"> </span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> tamaño</span> </p></td> 
  <td class="stentry"> <p>Tamaño del ROI en píxeles (int, int). Especifica el tamaño de la imagen de respuesta. La imagen se ha rellenado con <span class="codeph"> bgc=</span> en áreas no cubiertas por la imagen de vista (o se ha dejado transparente, si <span class="codeph"> fmt=*-alpha</span> está presente en la solicitud). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> escala</span> </p></td> 
  <td class="stentry"> <p>Factor de escala (real). Los valores menores que 1,0 reducen la resolución y los valores mayores que 1,0 aumentan la resolución. </p></td> 
 </tr> 
</table>

Con este comando, el servicio de imágenes puede entregar imágenes grandes mediante HTTP que, de lo contrario, excedería el límite de tamaño configurado con `attribute::MaxPix`.

>[!NOTE]
>
>Para obtener los mejores resultados, cuando se utiliza la compresión del JPEG, el tamaño de la tira o del mosaico debe ser un múltiplo del tamaño del mosaico de codificación del JPEG (16 x 16 píxeles).

## Ejemplo {#section-932fcfcb41d74a29bc929e4430c49601}

Separe una imagen CMYK imprimible en varias tiras de resolución completa para reducir los tamaños de archivo de descarga. Si ha solicitado una imagen contigua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

En primer lugar, se obtiene información relevante sobre la imagen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La respuesta de texto incluye estas propiedades:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Según esta información, se desean cuatro tiras de píxeles de 600x2000. El comando `rect=` se usa para describir los tamaños y las posiciones de las bandas.

Dado que esta imagen cambia con frecuencia, se incluye el comando `id=`. Al hacerlo, se minimiza la posibilidad de terminar con una o más tiras de una versión anterior de la imagen que puede haberse almacenado en caché en un servidor CDN o proxy. El valor de la propiedad `image.version` se usa para este propósito.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Propiedades {#section-aae223cee13e46d38b74680c048d945b}

Ver atributo. Se aplica independientemente de la configuración de capa actual.

Cualquier área del ROI que se extienda fuera de la imagen de vista se rellenará con `bgc=`.

Importante `rect=` se ha aplicado *después de* el escalado final y la conexión con `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` y `align=`.

## Predeterminado {#section-b296d3bbfb19441f87137a452b70f19a}

Imagen de vista completa sin modificar (`rect=0,0,width,height,1.0`).

## Véase también {#section-74015202c0c545ec82aec614d74b4bbd}

[recorte=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [extensión=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
