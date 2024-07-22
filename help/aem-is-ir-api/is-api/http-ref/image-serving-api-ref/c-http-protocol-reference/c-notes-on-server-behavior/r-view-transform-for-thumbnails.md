---
description: 'La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.'
solution: Experience Manager
title: Ver transformación para miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Ver transformación para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute::DefaultThumbPix y attribute::MaxPix.

1. **Calcular el recto de vista** - Usar `wid=` o el valor de anchura de `attribute::DefaultThumbPix` para el ancho del recto de vista. Use `hei=` o el valor de altura de `attribute::DefaultThumbPix` para la altura. La vista rect debe especificarse completamente en este paso. (Tenga en cuenta que la redirección de la vista es la misma que la redirección de la capa 0, si no se ha especificado ningún `size=` para la capa 0).
1. **Escalar el compuesto**: si se usa `catalog::ThumbType=Crop`, el compuesto se reducirá a la imagen más pequeña posible mientras se sigue rellenando toda la vista recta; se recortarán los datos de imagen adicionales. Si es `catalog::ThumbType= Fit`, el compuesto se escala a la imagen más grande posible mientras se sigue ajustando todo el compuesto en la vista recta. Si se usa `catalog::ThumbType=Texture`, el compuesto no se escalará para conservar la resolución especificada en `catalog::ThumbRes`.
1. **Rellenar y recortar**: la vista recta se rellena con el color `bgc=` (o, si no se especifica, con `attribute::ThumbBkgColor`). El compuesto a escala se alinea con la vista recta mediante el atributo: `ThumbHorizAlign` y el atributo: `ThumbVertAlign`. A continuación, el compuesto a escala se combina con la vista rellena recta sin escalar más. Las áreas del compuesto que se extienden más allá de la dirección de vista se recortan.
