---
description: Se admiten cuatro tipos generales de viñetas de producción.
seo-description: Se admiten cuatro tipos generales de viñetas de producción.
seo-title: Escala de viñeta
solution: Experience Manager
title: Escala de viñeta
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Escala de viñeta{#vignette-scaling}

Se admiten cuatro tipos generales de viñetas de producción.

* Una sola resolución

   Solo se recomienda cuando esté seguro de que solo se requiere un solo tamaño de imagen de procesamiento.
* Varias resoluciones

   Se recomienda cuando se conozcan todos los tamaños de imagen de procesamiento deseados. Proporciona una mejor calidad y una representación más rápida que las viñetas de una sola resolución y pirámide, ya que no es necesario ajustar la escala de la imagen después del procesamiento.
* Pirámide

   Lo mejor para todo tipo de funciones, se recomienda cuando se necesitan varios tamaños de imagen y los tamaños exactos no están predeterminados y cuando se utiliza uno de los visores de zoom Flash de Scene7.
* Pirámide con una o más resoluciones adicionales

   Proporciona una alta calidad para tamaños específicos, al tiempo que proporciona flexibilidad y compatibilidad con el visor de zoom.

En la práctica, cada resolución se guarda en la viñeta de producción como una vista independiente con su propia anchura y altura de imagen.

El tamaño de vista de una viñeta de una sola resolución se especifica con `-width`, `-height` o ambos. Si se especifican ambos valores, la viñeta se escalará para que ninguna dimensión sea mayor que el tamaño especificado. Si no se especifica ningún valor, la viñeta de salida tendrá el mismo tamaño que la viñeta de entrada. No se aplicará ninguna ampliación; si el tamaño especificado es mayor que el tamaño de la viñeta de entrada, la viñeta de salida tendrá el mismo tamaño que la viñeta de entrada.

En la práctica, las mismas reglas se aplican a las viñetas de varias resoluciones; el tamaño del primer nivel de resolución es similar al de una viñeta de una sola resolución. Las resoluciones adicionales se especifican con valores separados por comas adicionales para `-width` o `-height`. No es necesario ordenar los valores. Si `-width` especifica varios valores, `-height` sólo debe proporcionar un valor único y viceversa, de lo contrario se devuelve un error.

Se crea una viñeta piramidal especificando `-pyramid`. El mayor nivel de resolución de una viñeta de este tipo se determina exactamente como para una viñeta de una sola resolución. Los niveles de resolución adicionales se determinan automáticamente escalando cada nivel a 0,5 veces el nivel anterior, con el nivel más pequeño no superior a 128 x 128 píxeles.

Se pueden especificar niveles de resolución adicionales para una viñeta piramidal, al igual que para una viñeta de varias resoluciones.
