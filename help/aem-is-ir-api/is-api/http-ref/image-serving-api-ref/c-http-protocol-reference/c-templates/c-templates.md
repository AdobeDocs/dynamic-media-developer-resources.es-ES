---
description: Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
seo-description: Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
seo-title: Plantillas
solution: Experience Manager
title: Plantillas
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Plantillas{#templates}

Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.

Las variables personalizadas pueden utilizarse para simplificar aún más el uso de la plantilla. Las plantillas suelen configurarse para facilitar el intercambio de imágenes o texto o para definir otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en los catálogos de imágenes, con el cuerpo de la plantilla en el `catalog::Modifier` campo y el `catalog::Path` campo vacío o especificando una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con el comando `template=` o en el componente de ruta de la dirección URL de la solicitud. Para la mayoría de las aplicaciones, se recomienda utilizar el `template=` comando para especificar plantillas. El `template=`comando no debe aparecer en el `catalog::PostModifier` campo y solo puede ocurrir en el `catalog::Modifier` campo de una solicitud IS anidada (es decir, en una `src=is{...}` construcción). No se puede hacer referencia a los registros de plantilla en `src=` ni en `mask=`los comandos.

Cualquier `src=` o `mask=`comando incrustado en la plantilla puede resolverse en el catálogo principal de la solicitud o en otro catálogo de imágenes. Si no `rootId` se especifica ninguna, se asume el catálogo principal. La plantilla especificada con `template=` también puede encontrarse en el catálogo principal o en otro catálogo de imágenes.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, el resultado de la imagen de la plantilla siempre se puede ver simplemente especificando su valor `attribute::RootId` y `catalog::Id`, sin necesidad de saber qué variables se utilizan en la plantilla.

La variable de sustitución de ruta predefinida `$object$` puede utilizarse para aplicar el objeto de imagen especificado en la ruta de URL a cualquier origen de capa o máscara ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
