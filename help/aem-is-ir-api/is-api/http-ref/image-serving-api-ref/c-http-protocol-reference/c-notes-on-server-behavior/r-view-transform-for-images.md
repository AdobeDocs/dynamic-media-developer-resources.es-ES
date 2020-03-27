---
description: nulo
seo-description: nulo
seo-title: Transformación de Vista para imágenes
solution: Experience Manager
title: Transformación de Vista para imágenes
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Transformación de Vista para imágenes{#view-transform-for-images}

La imagen devuelta al cliente en respuesta a una `req=img` solicitud se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`y el tamaño de la imagen compuesta.

Si `wid=` se especifican y `hei=` , y no `scl=` lo son, la imagen compuesta se redimensiona de modo que se ajuste completamente al rectángulo de vista definido por `wid=` y `hei=`. Si la relación de aspecto del rectángulo de vista es diferente a la de la imagen compuesta, la imagen compuesta escalada se alinea dentro del rectángulo de vista utilizando el `align=` valor, si se especifica, o se centra de lo contrario. Cualquier espacio no cubierto por los datos de imagen se rellena con `bgc=` o, si no se especifica, con `attribute::BkgColor`.

Si `scl=` se especifica, la imagen compuesta se escala con ese factor de escala. Si también se especifica `wid=` y/o `hei=` , la imagen escalada se recorta `wid=` y/o se agrega `hei=` o espacio adicional, según sea necesario. `align=` especifica dónde se recorta la imagen o se agrega espacio adicional, y cualquier espacio adicional se rellena con `bgc=` o `attribute::BkgColor`.

Si no `wid=`se especifica ni `hei=` ni `scl=` , y si la anchura o la altura de la imagen compuesta superan `attribute::DefaultPix`, la imagen compuesta se redimensiona para no superar `attribute::DefaultPix`. De lo contrario, la imagen compuesta se utiliza sin escalar.

Para garantizar que la imagen de vista se devuelve sin ninguna otra escala, especifique `scl=1`.

Si `rgn=` se especifica, la imagen de respuesta se recorta según corresponda para llegar al tamaño de imagen de respuesta final. Este tamaño se compara con `attribute::MaxPix` (si se define) y se genera un error si la imagen de respuesta es más grande en cualquiera de las dimensiones.

Si `fmt=` especifica datos sin alfa, las áreas transparentes de la imagen de respuesta se rellenan con `bgc=` o `attribute::BkgColor`.
