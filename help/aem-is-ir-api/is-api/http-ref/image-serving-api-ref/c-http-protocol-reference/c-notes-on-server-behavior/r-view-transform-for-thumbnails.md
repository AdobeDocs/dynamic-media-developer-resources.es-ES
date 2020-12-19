---
description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
seo-description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
seo-title: Transformación de vista para miniaturas
solution: Experience Manager
title: Transformación de vista para miniaturas
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# transformación de vista para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, atributo::DefaultThumbPix y atributo::MaxPix.

1. **Calcule el rect**  de vista: utilice  `wid=` o el valor de anchura  `attribute::DefaultThumbPix` para el ancho del rectángulo de vista. Utilice `hei=` o el valor de altura de `attribute::DefaultThumbPix` para la altura. El rect de vista debe especificarse completamente en este paso. (Tenga en cuenta que el rectángulo de vista será el mismo que el rectángulo de la capa 0, si no se especifica `size=`para la capa 0).
1. **Cambiar la escala del compuesto** : si  `catalog::ThumbType=Crop`, el compuesto se redimensiona a la imagen más pequeña posible mientras se sigue llenando todo el rectángulo de vista; se recortan los datos de imagen adicionales. Si `catalog::ThumbType= Fit`, el compuesto se escala a la imagen más grande posible, mientras se sigue ajustando todo el compuesto al rectángulo de vista. Si `catalog::ThumbType=Texture`, el compuesto no se escala para conservar la resolución especificada en `catalog::ThumbRes`.
1. **Relleno y recorte** : el rectángulo de vista se rellena con el  `bgc=` color (o, si no se especifica, con  `attribute::ThumbBkgColor`). El compuesto escalado se alinea con el rectángulo de vista mediante el atributo: `ThumbHorizAlign` y atributo: `ThumbVertAlign`. A continuación, el compuesto escalado se combina con el rectángulo de vista rellenado sin escalar más. Todas las áreas del compuesto que se extiendan más allá del rectángulo de vista se recortan.

