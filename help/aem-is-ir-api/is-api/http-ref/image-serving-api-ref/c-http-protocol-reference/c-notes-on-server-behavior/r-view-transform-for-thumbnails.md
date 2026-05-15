---
description: 'La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute DefaultThumbPix y attribute MaxPix.'
solution: Experience Manager
title: Ver transformación para miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
TQID: 'https://experienceleague.adobe.com/yx1jgWnx-cwMDmBY2NOzYEyEjCqehPqGBK31MvGo-4o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# Ver transformación para miniaturas{#view-transform-for-thumbnails}

La imagen devuelta al cliente en respuesta a una solicitud req=tmb se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: wid=, hei=, attribute::DefaultThumbPix y attribute::MaxPix.

1. **Calcular el recto de vista** - Usar `wid=` o el valor de anchura de `attribute::DefaultThumbPix` para el ancho del recto de vista. Use `hei=` o el valor de altura de `attribute::DefaultThumbPix` para la altura. La vista rect debe especificarse completamente en este paso. (Tenga en cuenta que la redirección de la vista es la misma que la redirección de la capa 0, si no se ha especificado ningún `size=` para la capa 0).
1. **Escalar el compuesto**: si se usa `catalog::ThumbType=Crop`, el compuesto se reducirá a la imagen más pequeña posible mientras se sigue rellenando toda la vista recta; se recortarán los datos de imagen adicionales. Si es `catalog::ThumbType= Fit`, el compuesto se escala a la imagen más grande posible mientras se sigue ajustando todo el compuesto en la vista recta. Si se usa `catalog::ThumbType=Texture`, el compuesto no se escalará para conservar la resolución especificada en `catalog::ThumbRes`.
1. **Rellenar y recortar**: la vista recta se rellena con el color `bgc=` (o, si no se especifica, con `attribute::ThumbBkgColor`). El compuesto a escala se alinea con la vista recta mediante el atributo: `ThumbHorizAlign` y el atributo: `ThumbVertAlign`. A continuación, el compuesto a escala se combina con la vista rellena recta sin escalar más. Las áreas del compuesto que se extienden más allá de la dirección de vista se recortan.
