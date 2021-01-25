---
description: Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
seo-description: Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
seo-title: Plantillas
solution: Experience Manager
title: Plantillas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# Plantillas{#templates}

Las plantillas pueden utilizarse para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.

Las variables personalizadas pueden utilizarse para simplificar aún más el uso de la plantilla. Las plantillas suelen configurarse para facilitar el intercambio de imágenes o texto o para definir otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en los catálogos de imágenes, con el cuerpo de la plantilla en el campo `catalog::Modifier` y el campo `catalog::Path` vacío o especificando una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con el comando `template=` o en el componente de ruta de la dirección URL de la solicitud. Para la mayoría de las aplicaciones, se recomienda utilizar el comando `template=` para especificar plantillas. El comando `template=`no debe producirse en el campo `catalog::PostModifier` y sólo puede ocurrir en el campo `catalog::Modifier` en una solicitud IS anidada (es decir, en una construcción `src=is{...}`). No se puede hacer referencia a los registros de plantilla en los comandos `src=` o `mask=`.

Cualquier comando `src=` o `mask=`incrustado en la plantilla puede resolverse en el catálogo principal de la solicitud o en otro catálogo de imágenes. Si no se especifica ningún `rootId` explícitamente, se asume el catálogo principal. La plantilla especificada con `template=` también puede encontrarse en el catálogo principal o en otro catálogo de imágenes.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, el resultado de la imagen de la plantilla siempre se puede ver simplemente especificando su `attribute::RootId` y `catalog::Id`, sin tener que saber qué variables se utilizan en la plantilla.

La variable de sustitución de ruta predefinida `$object$` puede utilizarse para aplicar el objeto de imagen especificado en la ruta de URL a cualquier origen de capa o máscara ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
