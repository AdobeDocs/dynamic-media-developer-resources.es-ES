---
description: Ver transformación para imágenes
solution: Experience Manager
title: Ver transformación para imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Ver transformación para imágenes{#view-transform-for-images}

La imagen devuelta al cliente en respuesta a una solicitud `req=img` se deriva de la imagen compuesta teniendo en cuenta los siguientes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`, y el tamaño de la imagen compuesta.

Si se especifican `wid=` y `hei=`, y no se especifica `scl=`, la imagen compuesta se escalará para que se ajuste completamente a la dirección de vista definida por `wid=` y `hei=`. Si la proporción de aspecto de la redirección de vista es diferente de la de la imagen compuesta, la imagen compuesta a escala se alinea dentro de la redirección de vista con el valor `align=`, si se especifica, o se centra en caso contrario. Cualquier espacio no cubierto por datos de imagen se rellena con `bgc=` o, si no se especifica, con `attribute::BkgColor`.

Si se especifica `scl=`, la imagen compuesta se escala según ese factor de escala. Si `wid=` y/o `hei=` también se especifican, la imagen a escala se recorta a `wid=` y/o a `hei=`, o se agrega espacio adicional, según sea necesario. `align=` especifica dónde se recorta la imagen o dónde se agrega espacio adicional, y cualquier espacio adicional se rellena con `bgc=` o `attribute::BkgColor`.

Si no se especifica ni `wid=`, `hei=` ni `scl=`, y si la anchura o la altura de la imagen compuesta supera `attribute::DefaultPix`, la imagen compuesta se escalará para no superar `attribute::DefaultPix`. De lo contrario, la imagen compuesta se utiliza sin escalar.

Para garantizar que la imagen de vista se devuelva sin cambiar su escala, especifique `scl=1`.

Si se especifica `rgn=`, la imagen de respuesta se recorta según corresponda para llegar al tamaño final de la imagen de respuesta. Este tamaño se compara con `attribute::MaxPix` (si se define) y se genera un error si la imagen de respuesta es más grande en cualquiera de las dimensiones.

Si `fmt=` especifica datos sin alfa, las áreas transparentes de la imagen de respuesta se rellenarán con `bgc=` o `attribute::BkgColor`.
