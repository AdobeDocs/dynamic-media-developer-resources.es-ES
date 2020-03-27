---
description: El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con ImageSet de catálogo para un registro en particular.
seo-description: El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con ImageSet de catálogo para un registro en particular.
seo-title: Solicitudes de conjuntos de medios
solution: Experience Manager
title: Solicitudes de conjuntos de medios
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Solicitudes de conjuntos de medios{#media-set-requests}

El servicio de imágenes proporciona un mecanismo para recuperar una respuesta de texto jerárquico (xml o json) que representa todos los recursos y metadatos asociados con el catálogo::ImageSet para un registro en particular.

Los visores pueden utilizar este mecanismo para generar respuestas que informen a la presentación de imágenes sencillas, vídeos, conjuntos de vídeos, conjuntos de muestras, conjuntos de giros, conjuntos de páginas (catálogos electrónicos) y conjuntos de medios.

## Sintaxis de solicitud {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

La respuesta establecida para un `catalog::ImageSet` se puede recuperar mediante el `req=set` modificador y haciendo referencia al identificador del registro del catálogo en la ruta de acceso de red. De forma alternativa, el conjunto de imágenes se puede especificar directamente en la URL mediante el `imageset=` modificador. Si el `imageset=` modificador se utiliza para especificar el conjunto de imágenes, el valor completo debe estar entre llaves para evitar el valor del conjunto de imágenes y asegurarse de que los modificadores incluidos no se interpreten como parte de la cadena de consulta URL.

## Tipos de respuestas definidas {#section-93eb0a1f70344da2a888e56372ad3896}

El mecanismo establecido admite los siguientes tipos de respuestas:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>imágenes simples </p></td> 
  <td class="stentry"> <p>Un registro de imagen sin <span class="codeph"> catálogo::ImageSet</span> definido. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vídeos sencillos </p></td> 
  <td class="stentry"> <p>Un registro de vídeo en el catálogo de contenido estático. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras </p></td> 
  <td class="stentry"> <p>Conjunto de elementos formado por una referencia a un registro de imagen y una referencia independiente opcional a un registro de imagen utilizado como muestra. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de muestras jerárquicos </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de un elemento de muestra básico o una referencia a un registro de conjunto de muestras. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de giros </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consta de una simple lista de ID de imagen. </p></td> 
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
  <td class="stentry"> <p>Conjunto de elementos que consta de imágenes simples, conjuntos de vídeos, conjuntos de muestras, conjuntos de muestras jerárquicos, conjuntos de giros, conjuntos de giros bidimensionales, conjuntos de páginas y recursos de vídeo. Cada elemento del conjunto de medios también puede contener una muestra opcional. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de vídeos </p></td> 
  <td class="stentry"> <p>Conjunto de elementos que consiste en una lista de vídeos sencillos. </p></td> 
 </tr> 
</table>

## Detección de tipo de conjunto exterior {#section-3dd6e453528d46898e559d31458a59ba}

Cuando se recibe una `req=set` solicitud, el tipo de respuesta que se va a generar se determina por el valor de `catalog::AssetType`. Si no `catalog::AssetType` se define, el tipo de respuesta se determina mediante las siguientes reglas:

* Si el registro se encuentra en el catálogo de imágenes Y `catalog::ImageSet` está definido

   * Supongamos que el catálogo electrónico está configurado si al menos una entrada del campo Conjunto de imágenes del registro contiene dos puntos
   * Supongamos que el conjunto de medios contiene dos puntos y comas al menos en una entrada del campo Conjunto de imágenes del registro.
   * Supongamos que el conjunto de imágenes contiene al menos un punto y coma en una entrada del campo Conjunto de imágenes del registro.
   * Supongamos un conjunto de giros si ninguna entrada contiene dos puntos o punto y coma pero al menos una entrada contiene un conjunto de giros referenciado o un conjunto en línea (es un conjunto de giros 2D).
   * Supongamos un conjunto desconocido si ninguna entrada contiene dos puntos, punto y coma, conjunto al que se hace referencia o conjunto en línea (es decir, lista de imágenes separada por comas).

* Si el registro se encuentra en los catálogos de contenido estático AND de imágenes

   * Supongamos que la extensión de archivo se encuentra en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Suponer imagen de otro modo

* Si el registro se encuentra en el catálogo de contenido estático pero NO en el catálogo de imágenes

   * Supongamos que la extensión de archivo se encuentra en el siguiente conjunto: mp3, mp4, flv, f4v, swf, xml
   * Supongamos estático de lo contrario

* Si el registro se encuentra en el catálogo de imágenes pero NO en el catálogo de contenido estático

   * Suponer imagen

* Si el registro NO se encuentra en el catálogo de imágenes y NO en el catálogo de contenido estático

   * Supongamos que el vídeo basado en archivos tiene la siguiente extensión: mp3, mp4, flv, f4v, swf, xml
   * Supongamos que la imagen basada en archivos no es así

En todos los casos, la respuesta xml resultante se ajustará al documento XML especificado con el nodo raíz establecido correspondiente al tipo detectado.

## Detección de tipo de conjunto interior {#section-8f46490e467247e69ce284704def06f3}

Cuando se detecta el conjunto exterior como conjunto de medios de tipo, la respuesta contendrá un conjunto de elementos de conjunto de medios correspondientes a cada entrada de conjunto de medios en `catalog::ImageSet`. Si se especifica el parámetro de tipo opcional para una entrada de conjunto de medios en particular, se asignará a un tipo de salida según la siguiente tabla:

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

El `labelkey=` modificador se utiliza junto con el `catalog::UserData`campo para generar etiquetas para imágenes y muestras. El `catalog:UserData` campo se analiza como un conjunto de pares clave/valor y la clave de etiquetado se indexa en este conjunto para recuperar el valor de la clave dada. A continuación, este valor se devuelve en el *`l`* atributo para el *`s`* y *`i`*.

## Restricciones impuestas {#section-b9f042873bee45a5ae11b69fd42f2bca}

Para limitar el tamaño de la respuesta y evitar problemas de autorreferencia, la propiedad server controla la profundidad máxima de anidación. `PS::fvctx.nestingLimit` Si se supera este límite, se mostrará un error.

Para limitar el tamaño de las respuestas xml de los grandes conjuntos de catálogos electrónicos, se suprimen los metadatos privados de los elementos de conjunto de folletos según la propiedad server `PS::fvctx.brochureLimit`. Todos los metadatos privados asociados con el folleto se exportarán hasta que se alcance el límite de folletos. Una vez superado el límite, se suprimirán los mapas privados y los datos de usuario y se establecerá un indicador correspondiente para indicar qué tipo de datos se suprimió.

No se admiten conjuntos de medios anidados. Un conjunto de medios anidado se define como un conjunto de medios que contiene un elemento de conjunto de medios de tipo conjunto de medios. Si se detecta esta condición, se mostrará un error.

## Ejemplos {#section-588c9d33aa05482c86cd2b1936887228}

Para obtener respuestas XML de ejemplo para `req=set` solicitudes, consulte la página Propiedades en el encabezado Ejemplos HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Véase también {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), referencia [del catálogo de imágenes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

