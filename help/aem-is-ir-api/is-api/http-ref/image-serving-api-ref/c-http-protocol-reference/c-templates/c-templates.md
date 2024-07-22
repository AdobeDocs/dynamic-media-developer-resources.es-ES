---
title: Plantillas
description: Las plantillas se pueden utilizar para reducir la longitud y la complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato RTF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Plantillas{#templates}

Las plantillas se pueden utilizar para reducir la longitud y la complejidad de las solicitudes que componen varias capas de imagen o que incluyen texto con formato RTF.

Se pueden utilizar variables personalizadas para simplificar aún más el uso de la plantilla. A menudo, las plantillas se configuran para facilitar el intercambio de imágenes o texto, o para configurar otras opciones en tiempo de ejecución.

Las plantillas se almacenan como registros en catálogos de imágenes, con el cuerpo de la plantilla en el campo `catalog::Modifier` y el campo `catalog::Path` vacío o especificando una imagen de fondo estática que no se puede cambiar dinámicamente.

Las plantillas se especifican con el comando `template=` o en el componente de ruta de acceso de la dirección URL de la solicitud. Para la mayoría de las aplicaciones, se recomienda usar el comando `template=` para especificar las plantillas. El comando `template=` no debe aparecer en el campo `catalog::PostModifier` y solo puede aparecer en el campo `catalog::Modifier` en una solicitud de IS anidada (es decir, en una construcción `src=is{...}`). No se puede hacer referencia a los registros de plantilla en `src=` o `mask=`comandos.

Cualquier comando `src=` o `mask=`incrustado en la plantilla puede resolverse en el catálogo principal de la solicitud o en un catálogo de imágenes diferente. Si no se especifica ningún `rootId` de forma explícita, se asume el catálogo principal. La plantilla especificada con `template=` también puede encontrarse en el catálogo principal o en un catálogo de imágenes diferente.

Se recomienda incluir siempre definiciones predeterminadas para todas las variables utilizadas en una plantilla. De este modo, la salida de imagen de la plantilla siempre se puede ver simplemente especificando sus `attribute::RootId` y `catalog::Id`, sin tener que saber qué variables se utilizan en la plantilla.

La variable de sustitución de ruta predefinida `$object$` se puede usar para aplicar el objeto de imagen especificado en la ruta de acceso de la dirección URL a cualquier origen o máscara de capa ( `src=` o `mask=`), incluso en solicitudes anidadas o incrustadas.

* [Ejemplo A](r-example-a.md)
* [Ejemplo B](r-example-b.md)
* [Ejemplo C](r-example-c.md)
