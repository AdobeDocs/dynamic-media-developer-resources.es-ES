---
description: La biblioteca de imágenes interactiva es un módulo JavaScript que ajusta dinámicamente la calidad de las imágenes proporcionadas desde Dynamic Media e incrustadas en páginas web adaptables. Además, proporciona una mejor calidad de imagen en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar de forma interactiva resultados de Recorte inteligente y Muestra inteligente.
solution: Experience Manager
title: Acerca de la biblioteca de imágenes adaptables
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Acerca de la biblioteca de imágenes adaptables{#about-responsive-image-library}

La biblioteca de imágenes interactiva es un módulo JavaScript que ajusta dinámicamente la calidad de las imágenes proporcionadas desde Dynamic Media e incrustadas en páginas web adaptables. Además, proporciona una mejor calidad de imagen en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar de forma interactiva resultados de Recorte inteligente y Muestra inteligente.

## Mostrar direcciones URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

El caso de uso más sencillo de la biblioteca de imágenes interactivas es definir una lista de valores de puntos de interrupción para el ancho de la imagen. Esta lista garantiza que la representación adecuada se cargue y se muestre cuando se cambie el tamaño de una imagen debido a los cambios en el diseño de la página web de un usuario que cambia el tamaño de la ventana del explorador o cambia la orientación del dispositivo. La biblioteca supervisa continuamente el tamaño de la imagen en pantalla y cada vez que se alcanza un nuevo ancho de punto de interrupción, obtiene una nueva representación de imagen de Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Dirección URL de la demostración </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>A continuación se muestra un ejemplo sencillo en el que la imagen interactiva se encuentra dentro de un contenedor que toma el 50 % del ancho de la página web. Cada vez que se cambia el tamaño de la ventana del explorador, cambia la anchura del contenedor. Cuando la anchura de la imagen alcanza uno de los puntos de interrupción configurados (que se establecen en 200, 400, 600 y 800 píxeles para fines ilustrativos), se descarga y muestra una nueva representación. El objetivo es evitar cargar imágenes grandes innecesarias y ahorrar ancho de banda de red. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador y supervisar el tráfico de red. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>El siguiente ejemplo de Bootstrap ilustra el mismo caso de uso en una página web. Según el CSS Bootstrap, la celda de diseño a la que se agrega la imagen interactiva puede tener una de las siguientes anchuras: 360, 720 y 940 píxeles. Estos valores son exactamente los que se pasan como puntos de interrupción a la biblioteca de imágenes adaptables. Como tal, Dynamic Media garantiza que el ancho de banda de red del cliente se utilice de manera eficaz. Además, también garantiza que la imagen se muestre con el tamaño exacto necesario (dado el diseño de la página web actual) sin que ningún artefacto visual pueda escalar el navegador del lado del cliente. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador para llegar a diferentes puntos de interrupción del diseño y monitorizar el tráfico de red. </p> <p>Los casos de uso más avanzados incluyen la asociación de diferentes ajustes preestablecidos de imagen, comandos de servicio de imágenes o ambos, con distintos valores de puntos de interrupción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>En este ejemplo siguiente, se utilizan ajustes preestablecidos de imagen de diferente calidad de imagen y formato para diferentes tamaños de punto de interrupción. Para un punto de interrupción pequeño, se aplica un ajuste preestablecido de baja calidad que obliga a Image Serving a devolver la imagen GIF comprimida a solo seis colores. Un punto de interrupción medio utiliza un ajuste preestablecido de imagen configurado para JPEG con una compresión alta. El punto de interrupción más grande está asociado con un ajuste preestablecido de imagen de alta calidad que utiliza PNG sin pérdidas. Este método garantiza que las imágenes de alta calidad se entreguen a estos dispositivos, según el supuesto de que los dispositivos con pantallas más grandes tienen un ancho de banda bueno y una potencia de procesamiento. </p> <p>Haga clic en la dirección URL para abrir la página web, cambiar el tamaño de la ventana del explorador web de mayor a menor y observar cómo se degrada la calidad de la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Además de los ajustes preestablecidos de imagen, es posible asociar comandos específicos de Image Serving con puntos de interrupción. El siguiente ejemplo muestra cómo es posible recortar gradualmente la imagen del banner a la región de interés a medida que el tamaño de la imagen en pantalla se reduce. En este caso, el punto de interrupción más grande no tiene ningún comando de servicio de imágenes, por lo que la imagen del banner es totalmente visible. En el punto de interrupción medio aplica un recorte moderado, lo que hace que solo esté visible el cursor con el texto "En ejecución". En un punto de interrupción pequeño, se aplica más recorte para que solo se muestre el producto. </p> <p>Haga clic en la dirección URL para abrir la página web y cambiar el tamaño de la ventana del explorador. Observe cómo la imagen recorta gradualmente a medida que va de un tamaño mayor a uno más pequeño. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>También puede utilizar comandos de servicio de imágenes con plantillas de servicio de imágenes para controlar ciertos parámetros de plantilla según el tamaño de la imagen. En este ejemplo siguiente, se utiliza una plantilla de servicio de imágenes en la que el tamaño de fuente de la superposición de texto se parametriza con el parámetro <span class="codeph"> $fontsize </span>. La imagen interactiva está configurada para usar un tamaño de fuente mayor para los tamaños de imagen más pequeños, con el fin de garantizar que el texto siempre sea legible: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos del sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware y software del servidor**

* Dynamic Media Image Serving 6.0.1 o posterior.

**Requisitos mínimos del explorador del cliente**

* Microsoft® Windows® 7 o posterior; macOS X 10.8 o posterior.
* Firefox 23, Safari 6, Chrome 29, IE 9 o posterior.
* iOS 6 o posterior.
* Certificado en iPhone3GS o posterior y en iPad2 o posterior (solo navegadores nativos).
* Android™ OS 2.3 o posterior.
* Actualmente no se admite Internet Explorer en dispositivos móviles.
