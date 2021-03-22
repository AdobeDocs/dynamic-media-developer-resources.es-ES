---
description: Las viñetas son imágenes creadas con la creación de imágenes de Dynamic Media para su uso con la representación de imágenes.
solution: Experience Manager
title: Viñetas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Viñetas{#vignettes}

Las viñetas son imágenes creadas con la creación de imágenes de Dynamic Media para su uso con la representación de imágenes.

IR admite dos tipos básicos de viñetas, *2D* y *3D*. Las escenas de las habitaciones suelen ser viñetas 3D que pueden representar reflejos, mientras que la mayoría de las demás escenas, como ropa o tapicería, son normalmente viñetas 2D que no tienen capacidad de representación de reflejo.

Las viñetas contienen una *vista* y una jerarquía de *objetos*.

La vista es el contenedor de la imagen principal, mapas de iluminación compartidos, mapas de reflejo compartidos y otros datos asociados con toda la imagen.

La jerarquía de objetos consta de *grupos de objetos*, *objetos estándar* y *objetos superpuestos*.

Cada objeto estándar controla un área de la imagen de vista, definida con una *máscara* de escala gris. Las máscaras de objetos estándar nunca se superponen. Los objetos estándar no se pueden ocultar directamente, pero pueden cubrirse parcial o totalmente con objetos superpuestos. La mayoría o todos los objetos de una viñeta típica son objetos estándar.

Superponga la capa de objetos encima de la imagen de vista y entre ellos. El orden de la superposición se define mediante un valor z asignado al objeto. Los objetos de superposición son útiles cuando es necesario mostrar u ocultar partes de una escena de forma dinámica.

Se admiten varios tipos de objetos (estándar y superpuestos), cada uno con su propio propósito:

* **Los objetos**  planos (en viñetas 3D) y los objetos  **planos**  (en viñetas 2D) aceptan materiales de textura repetibles. Normalmente se utilizan para suelos, encimeras y otras superficies planas que solo requieren asignación de perspectiva.

* **Los** objetos de línea de flujo utilizan superficies curvadas de forma suave, como tapicería, y también se utilizan ocasionalmente para objetos de ropa. Pueden utilizarse en viñetas 2D y 3D y, si están totalmente creadas, participarán en el procesamiento de la reflexión.
* **Los** objetos no texturables solo permiten cambios de color. Están permitidos en viñetas 2D y 3D. Son inherentemente no texturables, o pueden ser un objeto plano o de línea de flujo con un indicador especial &quot;Sin textura&quot; establecido. Esto resulta útil en las viñetas 3D para permitir que los objetos participen en la representación de reflejo, aunque el objeto sólo acepte materiales de color sólido.
* **Los** objetos de boceto se utilizan mejor para objetos de tela con pliegues y arrugas, como artículos de ropa. Al igual que los objetos de línea de flujo, pueden utilizarse en viñetas 2D y 3D, aunque la aplicación en viñetas 3D es limitada.
* **Los** objetos Wall son similares a los objetos planares y solo se admiten en viñetas 3D. Disponen de información especial que permite aplicar dos acabados de pared diferentes (superior e inferior) y hasta tres materiales de borde de pared. Cuando se crea correctamente, los materiales aplicados a las paredes fluirán de manera precisa y fluida entre paredes adyacentes, para aplicaciones realistas de papel pintado/borde de pared. Los objetos de pared no admiten la rotación de textura.
* **Los** objetos de gabinete solo están permitidos en viñetas 3D. Se utilizan para crear cabinas de cocina y baño con requisitos de diseño complejos. Los objetos de gabinete aceptan texturas repetibles, así como *archivos de estilo archivador* creados especialmente que contienen imágenes de panel de archivador redimensionables.

Además de los tipos de objeto básicos, se admiten dos tipos especiales de objetos de superposición:

* **Los** objetos de superposición estáticos son objetos que no aceptan materiales. Están permitidos en viñetas 2D y 3D. Son útiles para accesorios extraíbles en una escena de habitación, para sombras paralelas detrás de objetos superpuestos procesables y aplicaciones similares.
* **Los** objetos de marco que cubren la ventana proporcionan información de colocación para la aplicación de archivos de estilo de coberturas de ventana, que se crean independientemente de la viñeta y se pueden compartir entre las viñetas.

Los objetos se recopilan en *grupos de objetos*, de forma similar a un sistema de archivos. La agrupación se basa normalmente en la estructura de los objetos físicos que representan (por ejemplo, un grupo &quot;Todos los gabinetes&quot; puede contener &quot;gabinetes base&quot; y &quot;gabinetes de pared&quot;). Se permite cualquier número de niveles de grupo. La agrupación admite la aplicación de materiales a varios objetos similares.

* [Coordenadas de escena](c-ir-scene-coordinates.md)
* [Resolución del material](c-ir-material-resolution.md)
