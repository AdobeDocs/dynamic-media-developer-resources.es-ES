---
title: cropPathE
description: Permite recortar hasta el cuadro delimitador de una ruta con nombre incrustada. Este recorte, a su vez, cambia el tamaño de la imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# cropPathE{#croppathe}

Permite recortar hasta el cuadro delimitador de una ruta con nombre incrustada. Este recorte, a su vez, cambia el tamaño de la imagen.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nombre de la ruta incrustada en la imagen de origen de la capa (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> es el nombre de una ruta incrustada en la imagen de origen de la capa. La ruta se transforma automáticamente según sea necesario para mantener la alineación relativa con el contenido de la imagen. Si se especifica más de un <span class="codeph"><span class="varname"> pathName</span></span>, el servidor recorta el cuadro delimitador de cada ruta de acceso, de uno en uno. Se omite cualquier <span class="codeph"><span class="varname"> pathName</span></span> que no se encuentre en la imagen de origen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por las capas de efecto.

`cropPathE=` se omitirá si no se encuentra ninguna ruta de acceso con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-d1986aa31af14767aeb1b4a57add67f4}

Ninguno, ya que no hay recorte adicional de la capa.

## Véase también {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[recorte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [rutaDeAccesoDeClip](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
