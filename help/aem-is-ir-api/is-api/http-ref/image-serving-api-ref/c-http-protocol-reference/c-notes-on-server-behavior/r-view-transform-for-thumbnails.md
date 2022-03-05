---
description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta considerando los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
solution: Experience Manager
title: Ver transformación para miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Ver transformación para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute::DefaultThumbPix y attribute::MaxPix.

1. **Calcular el extremo de la vista** - Uso `wid=` o el valor de anchura de `attribute::DefaultThumbPix` para la anchura del recto de vista. Uso `hei=` o el valor de altura de `attribute::DefaultThumbPix` para la altura. El registro de vista debe especificarse completamente en este paso. (Tenga en cuenta que el recto de vista es el mismo que el recto de la capa 0, si no `size=`se especifica para la capa 0).
1. **Escalar el compuesto** - Si `catalog::ThumbType=Crop`y, a continuación, el compuesto se escala a la imagen más pequeña posible, mientras se sigue llenando el recto de vista completo; los datos de imagen extra se cortan. If `catalog::ThumbType= Fit`, luego el compuesto se escala a la imagen más grande posible y, al mismo tiempo, se ajusta todo el compuesto en el recto de visualización. If `catalog::ThumbType=Texture`, el compuesto no se escala para preservar la resolución especificada en `catalog::ThumbRes`.
1. **Rellenar y recortar** - El recto de vista se rellena con la variable `bgc=` color (o, si no se especifica, con `attribute::ThumbBkgColor`). El compuesto escalado se alinea con el recto de vista mediante el atributo : `ThumbHorizAlign` y atributo: `ThumbVertAlign`. A continuación, el compuesto escalado se combina con el recto de vista rellenado sin escalar más. Las áreas de la composición que se extiendan más allá del borde de la vista se recortan.
