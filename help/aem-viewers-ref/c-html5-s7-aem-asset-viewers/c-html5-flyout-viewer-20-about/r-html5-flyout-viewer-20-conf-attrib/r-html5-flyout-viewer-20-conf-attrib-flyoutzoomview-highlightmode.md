---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor  </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de marco de navegación que se va a utilizar. Cuando se define como <span class="codeph"> cursor </span>, el componente utiliza un cursor de referencia de tamaño fijo. Es posible tener distintas imágenes de cursor para sistemas de escritorio y dispositivos táctiles, esto se controla con <span class="codeph"> .s7cursor </span> clase CSS y <span class="codeph"> selector de atributos input=mouse|touch </span>. En los sistemas de escritorio, se establece un punto de ancla en el medio del área del cursor, mientras que en los dispositivos táctiles el anclaje se encuentra en el centro inferior del cursor. Cuando se configura como <span class="codeph"> resaltado </span>, el componente utiliza un marco de navegación de tamaño variable; el tamaño y la forma del marco dependen del factor de zoom y del tamaño de la vista flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Define el tiempo (en segundos) que tarda el resaltado o el cursor en aparecer después de que el usuario lo active. La entrada de fundido solo se aplica en dispositivos táctiles; en sistemas de escritorio, el componente lo ignora. </p> <p>La función Desvanecer se aplica a los siguientes elementos de la interfaz de usuario: marco de resaltado, cursor fijo, superposición (en caso de que el parámetro <span class="codeph"> superposición </span> esté establecido en <span class="codeph"> 1 </span>). La animación de vista flotante solo comienza después de que se haya completado la atenuación de resaltado/cursor en la animación. No hay animación de atenuación. Cuando el usuario desactiva el menú flotante, los elementos de la interfaz de usuario correspondientes (cursor, resaltado y superposición) se ocultan instantáneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> Controla la posición del marco de navegación. </p> <p>Si se define como <span class="codeph"> en la imagen </span>, el marco de navegación solo se puede colocar dentro del área de la imagen real dentro de la vista principal. </p> <p>Si se establece en <span class="codeph"> free </span>, un usuario puede mover el marco de navegación a cualquier lugar del área de vista principal lógica, incluso fuera del contenido de la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
