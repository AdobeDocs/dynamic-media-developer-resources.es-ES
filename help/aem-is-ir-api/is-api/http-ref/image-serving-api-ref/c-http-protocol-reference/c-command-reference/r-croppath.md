---
description: Permite recortar al cuadro delimitador de una ruta de acceso con nombre incrustada. Este recorte, a su vez, cambia el tamaño de la imagen.
seo-description: Permite recortar al cuadro delimitador de una ruta de acceso con nombre incrustada. Este recorte, a su vez, cambia el tamaño de la imagen.
seo-title: cutPathE
solution: Experience Manager
title: cutPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cutPathE{#croppathe}

Permite recortar al cuadro delimitador de una ruta de acceso con nombre incrustada. Este recorte, a su vez, cambia el tamaño de la imagen.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nombre de la ruta incrustada en la imagen de origen de la capa (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> es el nombre de una ruta incrustada en la imagen de origen de la capa. La ruta se transforma automáticamente según sea necesario para mantener la alineación relativa con el contenido de la imagen. Si se especifica más de un <span class="codeph"><span class="varname"> pathName</span></span> , el servidor recorta el cuadro delimitador de cada ruta, de uno en uno. Se ignora cualquier <span class="codeph"><span class="varname"> pathName</span></span> que no se encuentre en la imagen de origen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Omitido por capas de efectos.

`cropPathE=` se omite si no se encuentra ninguna ruta con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-d1986aa31af14767aeb1b4a57add67f4}

Ninguno, para no recortar la capa de forma adicional.

## Véase también {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[recortar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
