---
description: La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta considerando los siguientes valores wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.
solution: Experience Manager
title: Ver transformación para miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Ver transformación para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute::DefaultThumbPix y attribute::MaxPix.

1. **Calcule el recto de vista** : utilice  `wid=` o el valor de anchura de  `attribute::DefaultThumbPix` para el ancho del recto de vista. Utilice `hei=` o el valor de altura `attribute::DefaultThumbPix` para la altura. El registro de vista debe especificarse completamente en este paso. (Tenga en cuenta que el recto de vista será el mismo que el recto de capa 0, si no se especifica `size=`para la capa 0).
1. **Escalar el compuesto** : si  `catalog::ThumbType=Crop`, el compuesto se escala a la imagen más pequeña posible mientras se sigue llenando el recto de vista completo; los datos de imagen extra se cortan. Si es `catalog::ThumbType= Fit`, el compuesto se escala a la imagen más grande posible y, al mismo tiempo, se ajusta todo el compuesto en el recto de vista. Si es `catalog::ThumbType=Texture`, el compuesto no se escala para conservar la resolución especificada en `catalog::ThumbRes`.
1. **Relleno y recorte** : el recto de vista se rellena con el  `bgc=` color (o, si no se especifica, con  `attribute::ThumbBkgColor`). El compuesto escalado se alinea con el recto de vista mediante el atributo : `ThumbHorizAlign` y atributo: `ThumbVertAlign`. A continuación, el compuesto escalado se combina con el recto de vista rellenado sin escalar más. Las áreas de la composición que se extiendan más allá del borde de la vista se recortan.
