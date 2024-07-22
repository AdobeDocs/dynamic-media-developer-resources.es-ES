---
title: Viñetas
description: Las viñetas son imágenes creadas con Dynamic Media Image Authoring para utilizarlas con Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Viñetas{#vignettes}

Las viñetas son imágenes creadas con Dynamic Media Image Authoring para utilizarlas con Image Rendering.

IR admite dos tipos básicos de viñetas: *2D* y *3D*. Las escenas de habitación suelen ser viñetas 3D que pueden representar reflejos, mientras que la mayoría de las otras escenas, como ropa o tapicería, son normalmente viñetas 2D que no tienen capacidad de representación de la reflexión.

Las viñetas contienen *view* y una jerarquía de *objetos*.

La vista es el contenedor de la imagen principal, los mapas de iluminación compartida, los mapas de reflexión compartidos y otros datos asociados con toda la imagen.

La jerarquía de objetos consta de *grupos de objetos*, *objetos estándar* y *objetos superpuestos*.

Cada objeto estándar controla un área de la imagen de vista, definida con una *máscara* de escala de grises. Las máscaras de los objetos estándar nunca se superponen. Los objetos estándar no se pueden ocultar directamente, pero pueden estar cubiertos parcial o totalmente por objetos de superposición. La mayoría o todos los objetos de una viñeta típica son objetos estándar.

Superponga la capa de objetos sobre la imagen de vista y entre sí. El orden de superposición se define mediante un valor z asignado al objeto. Los objetos de superposición son útiles cuando partes de una escena deben mostrarse u ocultarse dinámicamente.

Se admiten varios tipos de objetos (tanto estándar como superpuestos), cada uno con su propio propósito:

* **Los objetos planos** (en viñetas 3D) y **objetos planos** (en viñetas 2D) aceptan materiales de textura repetible. Se utilizan normalmente para suelos, encimeras y otras superficies planas que solo requieren una asignación en perspectiva.
* **Los objetos Flowline** asignan superficies curvas con forma suave, como tapicería, y en ocasiones también se utilizan para objetos de ropa. Pueden utilizarse en viñetas 2D y 3D y, si se crean completamente, participar en la renderización de la reflexión.
* **Los objetos no texturables** solo permiten cambios de color. Se permiten tanto en viñetas 2D como en 3D. Son inherentemente no texturables, o pueden ser un objeto plano o de línea de flujo con un indicador especial &quot;Sin textura&quot; establecido. Este método es útil en viñetas 3D para permitir que los objetos participen en la representación de la reflexión, aunque el objeto solo acepte materiales de color sólido.
* **Los objetos de boceto** se usan mejor para objetos de tela con pliegues y arrugas, como prendas de vestir. Al igual que los objetos de línea de flujo, se pueden utilizar en viñetas 2D y 3D, aunque la aplicación en viñetas 3D es limitada.
* **Los objetos de pared** son similares a los objetos planos y sólo se admiten en viñetas 3D. Cuentan con información de diseño especial que permite aplicar dos acabados de pared diferentes (superior e inferior) y hasta tres materiales de borde de pared. Cuando se crea correctamente, los materiales aplicados a las paredes fluyen con precisión y sin problemas entre las paredes adyacentes, para aplicaciones realistas de papel pintado/borde de pared. Los objetos de pared no admiten la rotación de texturas.
* **Sólo se permiten objetos de armario** en viñetas 3D. Se utilizan para crear gabinetes de cocina y baño con requisitos de diseño complejos. Los objetos de armario aceptan texturas repetibles y *archivos de estilo de armario* creados especialmente que contienen imágenes de panel de armario que pueden cambiar de tamaño.

Además de los tipos de objeto básicos, se admiten dos tipos especiales de objetos de superposición:

* **Los objetos de superposición estáticos** son objetos que no aceptan materiales. Se permiten tanto en viñetas 2D como en 3D. Son útiles para accesorios extraíbles en una escena de sala, para sombras paralelas detrás de objetos de superposición procesables y aplicaciones similares.
* **Los objetos de marco de cobertura de ventana** proporcionan información de ubicación para aplicar archivos de estilo de cobertura de ventana, que se crean independientemente de la viñeta y pueden compartirse entre viñetas.

Los objetos se recopilan en *grupos de objetos*, de forma similar a un sistema de archivos. La agrupación se basa normalmente en la estructura de los objetos físicos que representan (por ejemplo, un grupo &quot;Todos los archivadores&quot; puede contener &quot;Archivadores base&quot; y &quot;Archivadores de pared&quot;). Se permite cualquier número de niveles de grupo. La agrupación admite la aplicación de materiales a varios objetos similares.

* [Coordenadas de escena](c-ir-scene-coordinates.md)
* [Resolución de material](c-ir-material-resolution.md)
