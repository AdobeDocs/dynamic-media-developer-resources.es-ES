---
description: La biblioteca de imágenes adaptables es un módulo de JavaScript que ajusta dinámicamente la calidad de las imágenes proporcionadas desde Dynamic Media e incrustadas en páginas web adaptables. Además, proporciona una calidad de imagen mejorada en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar de forma interactiva los resultados de Recorte inteligente y Muestra inteligente.
solution: Experience Manager
title: Acerca de la biblioteca de imágenes adaptables
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Acerca de la biblioteca de imágenes adaptables{#about-responsive-image-library}

La biblioteca de imágenes adaptables es un módulo de JavaScript que ajusta dinámicamente la calidad de las imágenes proporcionadas desde Dynamic Media e incrustadas en páginas web adaptables. Además, proporciona una calidad de imagen mejorada en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar de forma interactiva los resultados de Recorte inteligente y Muestra inteligente.

## URL de demostración {#section-4f72c1dc38bf4e03acfa5205733a05a5}

El caso de uso más sencillo de la biblioteca de imágenes adaptables es definir una lista de valores de punto de interrupción para el ancho de la imagen. Esta lista garantiza que la representación adecuada se cargue y se muestre cuando se cambie el tamaño de una imagen debido a los cambios en el diseño de la página web producidos por un usuario que cambia el tamaño de la ventana del explorador o la orientación del dispositivo. La biblioteca supervisa continuamente el tamaño de la imagen en pantalla y, cada vez que se alcanza un nuevo ancho de punto de interrupción, obtiene una nueva representación de imagen de Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>URL de demostración </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>El siguiente es un ejemplo sencillo en el que la imagen adaptable se encuentra dentro de un contenedor que ocupa el 50 % del ancho de la página web. Cada vez que se cambia el tamaño de la ventana del explorador, cambia la anchura del contenedor. Cuando el ancho de la imagen alcanza uno de los puntos de interrupción configurados (que se establecen en 200, 400, 600 y 800 píxeles para fines ilustrativos), se descarga y muestra una nueva representación. El objetivo es evitar la carga de imágenes de gran tamaño innecesarias y ahorrar ancho de banda de la red. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador y supervisar el tráfico de red. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>El siguiente ejemplo de Bootstrap ilustra el mismo caso de uso en una página web. Según Bootstrap CSS, la celda de diseño a la que se agrega la imagen adaptable puede tener una de las siguientes anchuras: 360, 720 y 940 píxeles. Estos valores son exactamente lo que se pasa como puntos de interrupción a la biblioteca de imágenes adaptables. De este modo, Dynamic Media garantiza que el ancho de banda de red del cliente se utilice de forma eficaz. Además, también garantiza que la imagen se muestre en el tamaño exacto necesario, dado el diseño actual de la página web, sin que ningún artefacto visual escale el explorador del lado del cliente. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador para alcanzar diferentes puntos de interrupción del diseño y supervisar el tráfico de red. </p> <p>Los casos de uso más avanzados incluyen la asociación de diferentes ajustes preestablecidos de imagen, comandos del servicio de imágenes o ambos con valores de punto de interrupción diferentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>En el siguiente ejemplo, se utilizan ajustes preestablecidos de imagen de diferente calidad y formato para diferentes tamaños de punto de interrupción. Para un pequeño punto de interrupción, se aplica un ajuste preestablecido de baja calidad que obliga al servicio de imágenes a devolver la imagen de GIF comprimida solo a seis colores. Un punto de interrupción medio utiliza un ajuste preestablecido de imagen configurado para JPEG con compresión alta. El punto de interrupción más grande está asociado a un ajuste preestablecido de imagen de alta calidad que utiliza PNG sin pérdidas. Este método garantiza la entrega de imágenes de alta calidad a dichos dispositivos, partiendo del supuesto de que los dispositivos con pantallas más grandes tienen un mayor ancho de banda y potencia de procesamiento. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador web de mayor a menor y observar cómo se degrada la calidad de la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Además de los ajustes preestablecidos de imagen, es posible asociar comandos específicos del servicio de imágenes con puntos de interrupción. El siguiente ejemplo muestra cómo es posible recortar gradualmente la imagen del titular a la región de interés a medida que el tamaño de la imagen en pantalla se reduce. En este caso, el punto de interrupción más grande no tiene ningún comando de servicio de imágenes, por lo que la imagen del titular es totalmente visible. En el punto de interrupción medio se aplica un recorte moderado, por lo que solo es visible el ejecutor con el texto "En ejecución". En un pequeño punto de interrupción, se aplica más recorte para que solo se muestre el producto. </p> <p>Haga clic en la dirección URL para abrir la página web y cambiar el tamaño de la ventana del explorador. Observe cómo la imagen se recorta gradualmente a medida que pasa de un tamaño mayor a uno más pequeño. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>También puede utilizar los comandos del servicio de imágenes con las plantillas del servicio de imágenes para controlar determinados parámetros de plantilla en función del tamaño de la imagen. En el siguiente ejemplo, se usa una plantilla del servicio de imágenes donde el tamaño de fuente de la superposición de texto está parametrizado con el parámetro <span class="codeph"> $fontsize </span>. La imagen adaptable está configurada para utilizar un tamaño de fuente más grande para tamaños de imagen más pequeños a fin de garantizar que el texto siempre sea legible: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos del sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware y software de servidor**

* Dynamic Media Image Serving 6.0.1 o posterior.

**Requisitos mínimos para el explorador del cliente**

* Microsoft® Windows® 7 o posterior; macOS X 10.8 o posterior.
* Firefox 23, Safari 6, Chrome 29, IE 9 o posterior.
* iOS 6 o posterior.
* Certificado en iPhone3GS o posterior y iPad2 o posterior (solo exploradores nativos).
* Android™ OS 2.3 o posterior.
* Internet Explorer en dispositivos móviles no es compatible actualmente.
