---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
TQID: 'https://experienceleague.adobe.com/x43ipzx6iKOODZ10S8o8yJA9pg0Gl8mldfS5fEiVQJ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> resaltar|cursor </span> </p> </td> 
   <td colname="col2"> <p> Especifica el tipo de marco de navegación que se va a utilizar. Cuando se establece en <span class="codeph"> el cursor </span>, el componente utiliza un cursor de referencia de tamaño fijo. Es posible tener diferentes imágenes del cursor para sistemas de escritorio y dispositivos táctiles. Esta capacidad se controla con <span class="codeph"> .s7cursor </span> clase CSS y <span class="codeph"> input=mouse|touch </span> selector de atributos. En los sistemas de escritorio, un punto de ancla se establece en el centro del área del cursor, mientras que en los dispositivos táctiles, el punto de ancla se encuentra en el centro inferior del cursor. Cuando se establece en <span class="codeph"> para resaltar </span>, el componente utiliza un marco de navegación de tamaño variable; el tamaño y la forma del marco dependen del factor de zoom y del tamaño de la vista flotante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tiempo de muestra </span> </span> </p> </td> 
   <td colname="col2"> <p> Establece el tiempo (en segundos) que tarda el resaltado o el cursor en aparecer después de que el usuario lo active. La aparición gradual solo se aplica en dispositivos táctiles; en sistemas de escritorio, el componente la ignora. </p> <p>La aparición se aplica a los siguientes elementos de la interfaz de usuario: marco de resaltado, cursor fijo, superposición (en el caso de que la superposición <span class="codeph">, el parámetro </span> esté establecido en <span class="codeph"> 1 </span>). La animación de vista flotante comienza solo después de que se complete la transición de resaltado/cursor en la animación. No hay animación de atenuación. Cuando el usuario desactiva el menú flotante, los elementos de la interfaz de usuario correspondientes (cursor, resaltado y superposición) se ocultan instantáneamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> en la imagen|libre </span> </p> </td> 
   <td colname="col2"> <p> Controla la posición del marco de navegación. </p> <p>Si se establece en <span class="codeph"> en la imagen </span>, el marco de navegación solo se puede colocar dentro del área de imagen real dentro de la vista principal. </p> <p>Si se establece en <span class="codeph"> </span> libre, un usuario puede mover el marco de navegación a cualquier lugar del área de vista principal lógica, incluso fuera del contenido de la imagen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
