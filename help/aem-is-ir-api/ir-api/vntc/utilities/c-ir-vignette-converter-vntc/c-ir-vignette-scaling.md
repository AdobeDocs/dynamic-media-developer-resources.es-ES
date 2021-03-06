---
description: Se admiten cuatro tipos generales de viñetas de producción.
solution: Experience Manager
title: Escalado de viñeta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Escalado de viñeta{#vignette-scaling}

Se admiten cuatro tipos generales de viñetas de producción.

* Resolución única

   Solo se recomienda cuando esté seguro de que solo se requiere un tamaño de imagen de renderización único.
* Varias resoluciones

   Se recomienda cuando se conozcan todos los tamaños de imagen de renderización deseados. Proporciona una mejor calidad y un procesamiento más rápido que las viñetas de una sola resolución y piramide, ya que no es necesario escalar la imagen después del procesamiento.
* Pirámide

   Lo mejor para cualquier propósito, recomendado cuando se necesitan varios tamaños de imagen y no se han predeterminado los tamaños exactos y cuando se utiliza el visor de zoom de Dynamic Media.
* Pirámide con una o más resoluciones adicionales

   Proporciona alta calidad para tamaños específicos, a la vez que proporciona flexibilidad y compatibilidad con visor de zoom.

En la práctica, cada resolución se guarda en la viñeta de producción como una vista independiente con su propio ancho y alto de imagen.

El tamaño de visualización de una viñeta de una sola resolución se especifica con: `-width` o `-height` o ambas. Si se especifican ambos valores, la viñeta se escala para que ninguna de las dimensiones supere el tamaño especificado. Si no se especifica ningún valor, la viñeta de salida tendrá el mismo tamaño que la viñeta de entrada. No se aplica ningún aumento de escala; si el tamaño especificado es mayor que el tamaño de la viñeta de entrada, la viñeta de salida tendrá el mismo tamaño que la viñeta de entrada.

En la práctica, las mismas reglas se aplican a las viñetas de varias resoluciones, y el primer nivel de resolución tiene el mismo tamaño que una viñeta de una sola resolución. Las resoluciones adicionales se especifican con valores separados por comas adicionales para `-width` o `-height`. No es necesario ordenar los valores. If `-width` especifica varios valores, luego `-height` solo debe proporcionar un valor único y viceversa; de lo contrario, se devuelve un error.

Se crea una viñeta piramidal especificando `-pyramid`. El nivel de resolución más grande de una viñeta de este tipo se determina exactamente como para una viñeta de una sola resolución. Los niveles de resolución adicionales se determinan automáticamente escalando cada nivel a 0,5 veces el nivel anterior, con el nivel más pequeño que no exceda los 128 x 128 píxeles.

Se pueden especificar niveles de resolución adicionales para una viñeta piramidal, al igual que para una viñeta de varias resoluciones.
