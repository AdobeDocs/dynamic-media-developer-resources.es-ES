---
description: Ver transformación para imágenes
solution: Experience Manager
title: Ver transformación para imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Ver transformación para imágenes{#view-transform-for-images}

La imagen devuelta al cliente en respuesta a un error `req=img` La solicitud se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`y el tamaño de la imagen compuesta.

If `wid=` y `hei=` se especifican, y `scl=` no es, la imagen compuesta se escala de modo que se ajusta completamente a la dirección de vista definida por `wid=` y `hei=`. Si la proporción de aspecto de la reedición de la vista es diferente a la de la imagen compuesta, la imagen compuesta a escala se alinea dentro de la reedición de la vista utilizando `align=` valor, si se especifica, o si está centrado en caso contrario. Cualquier espacio no cubierto por datos de imagen se rellena con `bgc=` o, si no se especifica, con `attribute::BkgColor`.

If `scl=` se especifica, la imagen compuesta se escala según ese factor de escala. If `wid=` y/o `hei=` también se especifica, la imagen a escala se recorta a `wid=` y/o `hei=` o se añade espacio adicional, según sea necesario. `align=` especifica dónde se recorta la imagen o se añade espacio adicional, y cualquier espacio adicional se rellena con `bgc=` o `attribute::BkgColor`.

Si ninguno `wid=`, `hei=` ni `scl=` y si la anchura o la altura de la imagen compuesta supera `attribute::DefaultPix`, la imagen compuesta se escalará para no superar `attribute::DefaultPix`. De lo contrario, la imagen compuesta se utiliza sin escalar.

Para garantizar que la imagen de vista se devuelva sin ningún escalado adicional, especifique `scl=1`.

If `rgn=` se especifica, la imagen de respuesta se recorta según corresponda para llegar al tamaño final de la imagen de respuesta. Este tamaño se compara con `attribute::MaxPix` (si se define) y se genera un error si la imagen de respuesta es más grande en cualquiera de las dimensiones.

If `fmt=` especifica datos sin alfa, las áreas transparentes de la imagen de respuesta se rellenan con `bgc=` o `attribute::BkgColor`.
