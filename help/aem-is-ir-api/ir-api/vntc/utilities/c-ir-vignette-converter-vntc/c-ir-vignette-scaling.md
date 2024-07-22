---
description: Se admiten cuatro tipos generales de viñetas de producción.
solution: Experience Manager
title: Escala de viñeta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f9f92254-41d8-4d22-a168-78b49dd55478
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Escala de viñeta{#vignette-scaling}

Se admiten cuatro tipos generales de viñetas de producción.

* De resolución única

  Solo se recomienda cuando se sabe con seguridad que solo se necesita un tamaño de imagen de procesamiento único.
* De resolución múltiple

  Se recomienda cuando se conocen todos los tamaños de imagen de procesamiento deseados. Proporciona una mejor calidad y una representación más rápida que las viñetas piramidales y de una sola resolución, ya que no es necesario escalar la imagen después del procesamiento.
* Pirámide

  Ideal para todos los usos, se recomienda cuando se necesitan varios tamaños de imagen y los tamaños exactos no están predeterminados y cuando se utiliza el visor de zoom de Dynamic Media.
* Pirámide con una o más resoluciones adicionales

  Proporciona alta calidad para tamaños específicos y, al mismo tiempo, proporciona flexibilidad y compatibilidad con el visor de zoom.

De hecho, cada resolución se guarda en la viñeta de producción como una vista independiente con su propia anchura y altura de imagen.

El tamaño de vista de una viñeta de una sola resolución se ha especificado con `-width`, `-height` o ambos. Si se especifican ambos valores, la viñeta se escala de modo que ninguna dimensión sea mayor que el tamaño especificado. Si no se especifica ningún valor, la viñeta de salida tendrá el mismo tamaño que la viñeta de entrada. No se aplica ninguna ampliación; si el tamaño especificado es mayor que el tamaño de la viñeta de entrada, la viñeta de salida tiene el mismo tamaño que la viñeta de entrada.

En la práctica, las mismas reglas se aplican a las viñetas de varias resoluciones, con el primer nivel de resolución que se dimensiona igual que una viñeta de una sola resolución. Las resoluciones adicionales se especifican con valores separados por comas adicionales para `-width` o `-height`. No es necesario ordenar los valores. Si `-width` especifica varios valores, `-height` solo debe proporcionar un valor único y viceversa; de lo contrario, se devuelve un error.

Se crea una viñeta piramidal especificando `-pyramid`. El nivel de resolución más alto de una viñeta de este tipo se determina exactamente igual que para una viñeta de una sola resolución. Los niveles de resolución adicionales se determinan automáticamente escalando cada nivel a 0,5 veces el nivel anterior, con el nivel más pequeño que no supere los 128 x 128 píxeles.

Se pueden especificar niveles de resolución adicionales para una viñeta piramidal, al igual que para una viñeta de resolución múltiple.
