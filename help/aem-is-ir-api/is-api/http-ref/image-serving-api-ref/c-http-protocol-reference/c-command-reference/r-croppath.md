---
description: Permite recortar al cuadro delimitador de una ruta con nombre integrada. Este recorte, a su vez, cambia el tamaño de la imagen.
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# cropPathE{#croppathe}

Permite recortar al cuadro delimitador de una ruta con nombre integrada. Este recorte, a su vez, cambia el tamaño de la imagen.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nombre de la ruta de acceso incrustada en la imagen de origen de la capa (solo ASCII). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName es el nombre de una ruta integrada en la imagen de origen de la capa. La ruta se transforma automáticamente según sea necesario para mantener la alineación relativa con el contenido de la imagen. Si se especifica más de un <span class="codeph"><span class="varname"> pathName</span></span>, el servidor recorta el cuadro delimitador de cada ruta, de una en una. Cualquier <span class="codeph"><span class="varname"> pathName</span></span> no encontrado en la imagen de origen se ignora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

`cropPathE=` se ignora si no se encuentra ninguna ruta con el nombre especificado en la imagen de origen de la capa o si el origen de la capa no es una imagen.

## Predeterminado {#section-d1986aa31af14767aeb1b4a57add67f4}

Ninguno, para no recortar más la capa.

## Véase también {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[recorte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
