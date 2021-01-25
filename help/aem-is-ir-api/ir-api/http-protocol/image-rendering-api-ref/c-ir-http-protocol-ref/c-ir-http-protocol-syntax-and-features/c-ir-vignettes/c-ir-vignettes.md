---
description: Las viñetas son imágenes creadas con la creación de imágenes de Dynamic Media para su uso con la representación de imágenes.
solution: Experience Manager
title: Viñetas
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---


# Viñetas{#vignettes}

Las viñetas son imágenes creadas con la creación de imágenes de Dynamic Media para su uso con la representación de imágenes.

IR admite dos tipos básicos de viñetas: *2D* y *3D*. Las escenas de las habitaciones suelen ser viñetas 3D que pueden representar reflejos, mientras que la mayoría de las demás escenas, como ropa o tapicería, son normalmente viñetas 2D que no tienen capacidad de representación de reflejo.

Las viñetas contienen una *vista* y una jerarquía de *objetos*.

La vista es el contenedor de la imagen principal, los mapas de iluminación compartida, los mapas de reflexión compartidos y otros datos asociados con toda la imagen.

La jerarquía de objetos consiste en *grupos de objetos*, *objetos estándar* y *objetos de superposición*.

Cada objeto estándar controla un área de la imagen de vista, definida con una *máscara* de escala gris. Las máscaras de los objetos estándar nunca se superponen. Los objetos estándar no se pueden ocultar directamente, pero pueden estar cubiertos total o parcialmente por objetos superpuestos. La mayoría o todos los objetos de una viñeta típica son objetos estándar.

Superponga la capa de objetos sobre la imagen de vista y entre sí. El orden de superposición se define mediante un valor z asignado al objeto. Los objetos de superposición son útiles cuando es necesario mostrar u ocultar partes de una escena de forma dinámica.

Se admiten varios tipos de objetos (tanto estándar como superpuestos), cada uno de los cuales tiene su propio propósito:

* **Los objetos**  planos (en viñetas 3D) y los objetos **** planos (en viñetas 2D) aceptan materiales de textura repetitivos. Normalmente se utilizan para suelos, encimeras y otras superficies planas que sólo requieren asignación de perspectiva.

* **Los** objetos de línea de flujo se ajustan a superficies curvadas de forma suave, como tapicerías, y también se utilizan ocasionalmente para objetos de ropa. Pueden utilizarse en viñetas 2D y 3D y, si se han creado completamente, participarán en el procesamiento de reflexión.
* **Los** objetos no texturables solo permiten cambios de color. Están permitidos en viñetas 2D y 3D. Son inherentemente no texturables o pueden ser un objeto plano o de línea de flujo con un indicador especial &quot;Sin textura&quot;. Esto resulta útil en las viñetas 3D para permitir que los objetos participen en la representación de reflejo, aunque el objeto solo acepte materiales de color sólido.
* **Los** objetos de boceto se utilizan mejor para objetos de tela con pliegues y arrugas, como elementos de ropa. Al igual que los objetos de línea de flujo, pueden utilizarse en viñetas 2D y 3D, aunque la aplicación en viñetas 3D es limitada.
* **Los** objetos de pared son similares a los objetos planares y solo se admiten en viñetas 3D. Disponen de una información de diseño especial que permite la aplicación de dos acabados de pared diferentes (superior e inferior) y hasta tres materiales de borde de pared. Cuando se crean correctamente, los materiales aplicados a las paredes fluirán con precisión y fluidez entre paredes adyacentes, para aplicaciones realistas de papel pintado o borde de pared. Los objetos de pared no admiten la rotación de textura.
* **Los** objetos de archivador solo están permitidos en las viñetas 3D. Se utilizan para crear cabinas de cocina y baño con requisitos de diseño complejos. Los objetos de archivador aceptan texturas repetibles, así como *archivos de estilo archivador* creados especialmente que contienen imágenes de panel archivador redimensionables.

Además de los tipos de objeto básicos, se admiten dos tipos especiales de objetos de superposición:

* **Los** objetos de superposición estáticos son objetos que no aceptan materiales. Están permitidos en viñetas 2D y 3D. Son útiles para accesorios extraíbles en una escena de sala, para sombras paralelas detrás de objetos de superposición procesables y aplicaciones similares.
* **Los** objetos de marco de cobertura de ventana proporcionan información de colocación para aplicar archivos de estilo de coberturas de ventana, que se crean independientemente de la viñeta y se pueden compartir entre viñetas.

Los objetos se recopilan en *grupos de objetos*, de forma similar a un sistema de archivos. La agrupación se basa normalmente en la estructura de los objetos físicos que representan (por ejemplo, un grupo &#39;Todos los gabinetes&#39; puede contener &#39;Cabinas base&#39; y &#39;Cabinas de pared&#39;). Se permite cualquier número de niveles de grupo. La agrupación admite la aplicación de materiales a varios objetos similares.

* [Coordenadas de escena](c-ir-scene-coordinates.md)
* [Resolución de materiales](c-ir-material-resolution.md)
