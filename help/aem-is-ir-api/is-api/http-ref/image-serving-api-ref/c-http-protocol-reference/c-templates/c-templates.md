---
title: Plantillas
description: Las plantillas se pueden utilizar para reducir la longitud y la complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato RTF.
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

Las plantillas se pueden utilizar para reducir la longitud y la complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato RTF.

Se pueden utilizar variables personalizadas para simplificar aún más el uso de la plantilla. A menudo, las plantillas se configuran para facilitar el intercambio de imágenes o texto, o para configurar otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en catálogos de imágenes, con el cuerpo de la plantilla en la `catalog::Modifier` y el campo `catalog::Path` vacío o especificando una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con `template=` o en el componente de ruta de la URL de solicitud. Para la mayoría de las aplicaciones, se recomienda utilizar la variable `template=` para especificar plantillas. El `template=`El comando no debe aparecer en `catalog::PostModifier` y solo pueden aparecer en el campo `catalog::Modifier` en una solicitud IS anidada (es decir, en una `src=is{...}` construcción). No se puede hacer referencia a los registros de plantilla en `src=` o `mask=`comandos.

Cualquiera `src=` o `mask=`los comandos incrustados en la plantilla pueden resolverse en el catálogo principal de la solicitud o en un catálogo de imágenes diferente. Si no `rootId` se especifica explícitamente, se asume el catálogo principal. La plantilla especificada con `template=` también puede encontrarse en el catálogo principal o en un catálogo de imágenes diferente.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, la salida de imagen de la plantilla siempre se puede ver simplemente especificando su `attribute::RootId` y `catalog::Id`, sin tener que saber qué variables se utilizan en la plantilla.

La variable de sustitución de rutas predefinida `$object$` se puede utilizar para aplicar el objeto de imagen especificado en la ruta url a cualquier origen de capa o máscara ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
