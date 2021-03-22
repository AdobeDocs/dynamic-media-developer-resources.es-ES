---
description: El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con el conjunto de imágenes del catálogo para un registro en particular.
seo-description: El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con el conjunto de imágenes del catálogo para un registro en particular.
seo-title: Solicitudes de conjuntos de medios
solution: Experience Manager
title: Solicitudes de conjuntos de medios
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---


# Solicitudes de conjuntos de medios{#media-set-requests}

Image Serving proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con catalog::ImageSet para un registro en particular.

Los visualizadores pueden utilizar este mecanismo para generar respuestas que informen a la presentación de imágenes simples, vídeos, conjuntos de vídeos, conjuntos de muestras, conjuntos de giros, conjuntos de páginas (catálogos electrónicos) y conjuntos de medios.

## Sintaxis de solicitud {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La respuesta establecida para un `catalog::ImageSet` se puede recuperar utilizando el modificador `req=set` y haciendo referencia al id del registro de catálogo en la ruta de acceso de red. De forma alternativa, el conjunto de imágenes se puede especificar directamente en la URL utilizando el modificador `imageset=`. Si se utiliza el modificador `imageset=` para especificar el conjunto de imágenes, todo el valor debe escribirse entre llaves para omitir el valor del conjunto de imágenes y asegurarse de que los modificadores incluidos no se interpreten como parte de la cadena de consulta de URL.

## Tipos de respuestas definidas {#section-93eb0a1f70344da2a888e56372ad3896}

El mecanismo de conjunto admite los siguientes tipos de respuestas:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>imágenes simples </p></td> 
  <td class="stentry"> <p>Un registro de imagen sin <span class="codeph"> catálogo::ImageSet</span> definido. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vídeos simples </p></td> 
  <td class="stentry"> <p>Un registro de vídeo en el catálogo de contenido estático. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una referencia a un registro de imagen y una referencia opcional independiente a un registro de imagen utilizado como muestra. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras jerárquicos </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de un elemento de muestra básico o una referencia a un registro de conjunto de muestras. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de giros </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una lista sencilla de ID de imagen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de giros bidimensionales </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una imagen simple o una referencia a un conjunto de giros básico. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de páginas </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una lista de hasta tres imágenes de página </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de medios </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de imágenes simples, conjuntos de vídeos, conjuntos de muestras, conjuntos de muestras jerárquicas, conjuntos de giros, conjuntos de giros bidimensionales, conjuntos de páginas y recursos de vídeo. Cada elemento del conjunto de medios también puede contener una muestra opcional. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de vídeos </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una lista de vídeos sencillos. </p></td> 
 </tr> 
</table>

## Detección de tipo de conjunto exterior {#section-3dd6e453528d46898e559d31458a59ba}

Cuando se recibe una solicitud `req=set`, el tipo de respuesta que se va a generar viene determinado por el valor de `catalog::AssetType`. Si no se define `catalog::AssetType` , el tipo de respuesta se determina mediante las siguientes reglas:

* Si el registro se encuentra en el catálogo de imágenes Y `catalog::ImageSet` está definido

   * Supongamos que el catálogo electrónico está configurado si al menos una entrada del campo de conjunto de imágenes del registro contiene dos puntos
   * Supongamos que el conjunto de medios contiene al menos una entrada en el campo de conjunto de imágenes de registro que contiene dos punto y coma.
   * Supongamos que el conjunto de imágenes contiene al menos una entrada en el campo de conjunto de imágenes de registro que contiene un punto y coma.
   * Supongamos que el conjunto de giros no contiene dos puntos ni punto y coma, pero al menos una entrada contiene un conjunto o conjunto en línea al que se hace referencia (se trata de un conjunto de giros 2D).
   * Supongamos que no se conoce el conjunto si ninguna entrada contiene dos puntos o punto y coma, no se hace referencia al conjunto ni al conjunto en línea (es decir, una lista de imágenes separadas por comas).

* Si el registro se encuentra en los catálogos de contenido estático AND de imagen

   * Supongamos que el vídeo está en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Suponer imagen de otro modo

* Si el registro se encuentra en el catálogo de contenido estático pero NO en el catálogo de imágenes

   * Supongamos que el vídeo está en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Supongamos que es estático de lo contrario

* Si el registro se encuentra en el catálogo de imágenes pero NO en el catálogo de contenido estático

   * Suponer imagen

* Si el registro NO se encuentra en el catálogo de imágenes y NO se encuentra en el catálogo de contenido estático

   * Supongamos que el vídeo basado en archivos está en el siguiente conjunto de extensiones de archivo: mp3, mp4, flv, f4v, swf, xml
   * Supongamos que la imagen basada en archivos no es así

En todos los casos, la respuesta xml resultante se ajustará al documento XML especificado con el nodo raíz configurado correspondiente al tipo detectado.

## Detección de tipo de conjunto interno {#section-8f46490e467247e69ce284704def06f3}

Cuando se detecta el conjunto exterior como conjunto de medios de tipo , la respuesta contendrá un conjunto de elementos de conjuntos de medios correspondientes a cada entrada de conjunto de medios en `catalog::ImageSet`. Si se especifica el parámetro de tipo opcional para una entrada de conjunto de medios en particular, se asigna a un tipo de salida según la siguiente tabla:

| Tipo de entrada | Tipo de salida |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Si no se especifica el parámetro de tipo opcional para una entrada de conjunto de medios determinada o corresponde a un tipo no admitido, el tipo de elemento de conjunto de medios se detecta automáticamente utilizando las mismas reglas que se aplicaron en el nivel de conjunto exterior.

## Especificación XML {#section-c1bd60948ef545759a16885bb6fcc607}

La respuesta xml devuelta se ajusta a la siguiente especificación:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

El modificador `labelkey=` se utiliza junto con el campo `catalog::UserData`para generar etiquetas para imágenes y muestras. El campo `catalog:UserData` se analiza como un conjunto de pares clave/valor y la clave de etiqueta se indexa en este conjunto para recuperar el valor de la clave dada. Este valor se devuelve en el atributo *`l`* para *`s`* y *`i`*.

## Restricciones aplicadas {#section-b9f042873bee45a5ae11b69fd42f2bca}

Para limitar el tamaño de la respuesta y evitar problemas de referencia automática, la profundidad de anidación máxima se controla mediante la propiedad del servidor `PS::fvctx.nestingLimit`. Si se supera este límite, se devuelve un error.

Para limitar el tamaño de las respuestas xml para grandes conjuntos de catálogos electrónicos, se eliminan los metadatos privados para los elementos de conjuntos de folletos de acuerdo con la propiedad del servidor `PS::fvctx.brochureLimit`. Todos los metadatos privados asociados con el folleto se exportarán hasta que se alcance el límite de folletos. Una vez superado el límite, se suprimirán los mapas privados y los datos de usuario, y se establecerá un indicador correspondiente para indicar qué tipo de datos se suprimió.

No se admiten conjuntos de medios anidados. Un conjunto de medios anidado se define como un conjunto de medios que contiene un elemento de conjunto de medios de tipo conjunto de medios. Si se detecta esta condición, se devuelve un error.

## Ejemplos {#section-588c9d33aa05482c86cd2b1936887228}

Para obtener respuestas XML de ejemplo para solicitudes `req=set` , consulte la página Propiedades en el encabezado Ejemplos HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Véase también {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), referencia del catálogo de  [imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

