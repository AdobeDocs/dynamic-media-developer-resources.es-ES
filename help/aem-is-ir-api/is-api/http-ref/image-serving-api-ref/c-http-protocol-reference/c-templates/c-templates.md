---
title: Plantillas
description: Las plantillas se pueden utilizar para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Plantillas{#templates}

Las plantillas se pueden utilizar para reducir la longitud y complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato rtf.

Las variables personalizadas pueden utilizarse para simplificar aún más el uso de la plantilla. Las plantillas suelen configurarse para facilitar el intercambio de imágenes o texto, o para configurar otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en los catálogos de imágenes, con el cuerpo de la plantilla en la variable `catalog::Modifier` y la variable `catalog::Path` campo vacío o especificación de una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con la variable `template=` o en el componente de ruta de la URL de solicitud. Para la mayoría de las aplicaciones, se recomienda usar la variable `template=` para especificar las plantillas. La variable `template=`no debe producirse en la variable `catalog::PostModifier` y solo puede aparecer en la variable `catalog::Modifier` en una solicitud IS anidada (es decir, en una `src=is{...}` construcción). No se puede hacer referencia a los registros de plantilla en `src=` o `mask=`comandos.

Cualquiera `src=` o `mask=`los comandos incrustados en la plantilla pueden resolverse en el catálogo principal de la solicitud o en un catálogo de imágenes diferente. Si no `rootId` se especifica explícitamente, se asume el catálogo principal. La plantilla especificada con `template=` también puede encontrarse en el catálogo principal o en un catálogo de imágenes diferente.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, la salida de la imagen de la plantilla siempre se puede ver simplemente especificando su `attribute::RootId` y `catalog::Id`, sin tener que saber qué variables se utilizan en la plantilla.

La variable de sustitución de rutas predefinida `$object$` se puede usar para aplicar el objeto de imagen especificado en la ruta url a cualquier origen de capa o máscara ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
