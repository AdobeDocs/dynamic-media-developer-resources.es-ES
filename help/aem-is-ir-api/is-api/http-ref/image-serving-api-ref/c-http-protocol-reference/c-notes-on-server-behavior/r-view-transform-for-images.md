---
description: Ver transformación para imágenes
solution: Experience Manager
title: Ver transformación para imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Ver transformación para imágenes{#view-transform-for-images}

La imagen devuelta al cliente en respuesta a una solicitud `req=img` se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` y el tamaño de la imagen compuesta.

Si se especifican `wid=` y `hei=`, y `scl=` no, la imagen compuesta se escala de modo que se ajuste completamente al directorio de vista definido por `wid=` y `hei=`. Si la relación de aspecto del recto de vista es diferente a la de la imagen compuesta, la imagen compuesta escalada se alinea dentro del recto de vista utilizando el valor `align=`, si se especifica, o está centrada en caso contrario. Cualquier espacio que no esté cubierto por los datos de imagen se rellena con `bgc=` o, si no se especifica, con `attribute::BkgColor`.

Si se especifica `scl=`, la imagen compuesta se escala por ese factor de escala. Si también se especifica `wid=` o `hei=`, la imagen escalada se recorta a `wid=` y/o `hei=` o se añade espacio adicional, según sea necesario. `align=` especifica dónde se recorta la imagen o se agrega espacio adicional, y cualquier espacio adicional se rellena con  `bgc=` o  `attribute::BkgColor`.

Si no se especifica `wid=`, `hei=` ni `scl=` y si la anchura o la altura de la imagen compuesta exceden `attribute::DefaultPix`, la imagen compuesta se escalará para no superar `attribute::DefaultPix`. De lo contrario, la imagen compuesta se utiliza sin escala.

Para garantizar que la imagen de vista se devuelva sin más escalado, especifique `scl=1`.

Si se especifica `rgn=`, la imagen de respuesta se recorta según corresponda para llegar al tamaño de la imagen de respuesta final. Este tamaño se compara con `attribute::MaxPix` (si está definido) y se genera un error si la imagen de respuesta es más grande en cualquiera de las dimensiones.

Si `fmt=` especifica datos sin alfa, las áreas transparentes de la imagen de respuesta se rellenarán con `bgc=` o `attribute::BkgColor`.
