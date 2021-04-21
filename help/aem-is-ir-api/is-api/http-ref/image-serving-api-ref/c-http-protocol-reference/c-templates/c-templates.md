---
description: Las plantillas se pueden utilizar para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
solution: Experience Manager
title: Plantillas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Plantillas{#templates}

Las plantillas se pueden utilizar para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.

Las variables personalizadas pueden utilizarse para simplificar aún más el uso de la plantilla. Las plantillas suelen configurarse para facilitar el intercambio de imágenes o texto, o para configurar otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en catálogos de imágenes, con el cuerpo de la plantilla en el campo `catalog::Modifier` y el campo `catalog::Path` vacío o especificando una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con el comando `template=` o en el componente de ruta de la dirección URL de la solicitud. Para la mayoría de las aplicaciones, se recomienda utilizar el comando `template=` para especificar plantillas. El comando `template=`no debe producirse en el campo `catalog::PostModifier` y solo puede producirse en el campo `catalog::Modifier` de una solicitud IS anidada (es decir, en una construcción `src=is{...}`). No se puede hacer referencia a los registros de plantilla en los comandos `src=` o `mask=`.

Cualquier comando `src=` o `mask=`incrustado en la plantilla puede resolverse en el catálogo principal de la solicitud o en un catálogo de imágenes diferente. Si no se especifica ningún `rootId` explícitamente, se asume el catálogo principal. La plantilla especificada con `template=` también puede estar ubicada en el catálogo principal o en un catálogo de imágenes diferente.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, el resultado de la imagen de la plantilla siempre se puede ver simplemente especificando su `attribute::RootId` y `catalog::Id`, sin tener que saber qué variables se utilizan en la plantilla.

La variable de sustitución de ruta predefinida `$object$` puede utilizarse para aplicar el objeto de imagen especificado en la ruta url a cualquier origen de capa o máscara ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
