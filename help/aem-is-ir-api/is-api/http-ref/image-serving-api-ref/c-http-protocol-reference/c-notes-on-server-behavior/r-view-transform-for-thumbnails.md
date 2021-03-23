---
description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta considerando los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
seo-description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta considerando los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
seo-title: Ver transformación para miniaturas
solution: Experience Manager
title: Ver transformación para miniaturas
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# Ver transformación para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute::DefaultThumbPix y attribute::MaxPix.

1. **Calcule el recto de vista** : utilice  `wid=` o el valor de anchura de  `attribute::DefaultThumbPix` para el ancho del recto de vista. Utilice `hei=` o el valor de altura `attribute::DefaultThumbPix` para la altura. El registro de vista debe especificarse completamente en este paso. (Tenga en cuenta que el recto de vista será el mismo que el recto de capa 0, si no se especifica `size=`para la capa 0).
1. **Escalar el compuesto** : si  `catalog::ThumbType=Crop`, el compuesto se escala a la imagen más pequeña posible mientras se sigue llenando el recto de vista completo; los datos de imagen extra se cortan. Si es `catalog::ThumbType= Fit`, el compuesto se escala a la imagen más grande posible y, al mismo tiempo, se ajusta todo el compuesto en el recto de vista. Si es `catalog::ThumbType=Texture`, el compuesto no se escala para conservar la resolución especificada en `catalog::ThumbRes`.
1. **Relleno y recorte** : el recto de vista se rellena con el  `bgc=` color (o, si no se especifica, con  `attribute::ThumbBkgColor`). El compuesto escalado se alinea con el recto de vista mediante el atributo : `ThumbHorizAlign` y atributo: `ThumbVertAlign`. A continuación, el compuesto escalado se combina con el recto de vista rellenado sin escalar más. Las áreas de la composición que se extiendan más allá del borde de la vista se recortan.

