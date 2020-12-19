---
description: La biblioteca de imágenes adaptable es un módulo JavaScript que ajusta dinámicamente la calidad de las imágenes servidas desde Scene7 e incorporadas en páginas web adaptables. Además, proporciona una calidad de imagen mejorada en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar los resultados de Smart Crop y Smart Swatch de forma interactiva.
seo-description: La biblioteca de imágenes adaptable es un módulo JavaScript que ajusta dinámicamente la calidad de las imágenes servidas desde Scene7 e incorporadas en páginas web adaptables. Además, proporciona una calidad de imagen mejorada en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar los resultados de Smart Crop y Smart Swatch de forma interactiva.
seo-title: Acerca de la biblioteca de imágenes interactivas
solution: Experience Manager
title: Acerca de la biblioteca de imágenes interactivas
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# Acerca de la biblioteca de imágenes interactivas{#about-responsive-image-library}

La biblioteca de imágenes adaptable es un módulo JavaScript que ajusta dinámicamente la calidad de las imágenes servidas desde Scene7 e incorporadas en páginas web adaptables. Además, proporciona una calidad de imagen mejorada en dispositivos con pantallas de alta densidad. La biblioteca también puede procesar los resultados de Smart Crop y Smart Swatch de forma interactiva.

## Direcciones URL de demostración {#section-4f72c1dc38bf4e03acfa5205733a05a5}

El caso de uso más sencillo de la biblioteca de imágenes interactivas es definir una lista de los valores de los puntos de interrupción para la anchura de la imagen. Esta lista garantiza que la representación adecuada se cargue y muestre cuando se cambia el tamaño de una imagen debido a que el diseño de la página web cambia de un usuario que cambia el tamaño de la ventana del navegador o la orientación del dispositivo. La biblioteca monitorea continuamente el tamaño de la imagen en pantalla y cada vez que se alcanza un nuevo ancho de punto de interrupción, obtiene una nueva representación de imagen de Scene7.

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
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>A continuación se muestra un ejemplo sencillo en el que la imagen adaptable se encuentra dentro de un contenedor que toma el 50 % del ancho de la página web. Cada vez que se cambia el tamaño de la ventana del navegador, cambia el ancho del contenedor. Cuando la anchura de la imagen alcanza uno de los puntos de interrupción configurados (definidos en 200, 400, 600 y 800 píxeles con fines ilustrativos), se descarga y muestra una nueva representación. El objetivo es evitar la carga de imágenes grandes innecesarias y ahorrar ancho de banda de red. </p> <p>Haga clic en la URL para abrir la página web, cambiar el tamaño de la ventana del explorador y supervisar el tráfico de red. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>El siguiente ejemplo de Bootstrap ilustra el mismo caso de uso en una página web. Según CSS Bootstrap, la celda de diseño a la que se agrega la imagen adaptable puede tener una de las siguientes anchuras: 360, 720 y 940 píxeles. Estos son los valores exactos que se pasan como puntos de interrupción a la biblioteca de imágenes interactivas. Como tal, Scene7 garantiza que el ancho de banda de red del cliente se utilice de manera eficaz. Además, garantiza que la imagen se muestre con el tamaño exacto necesario, dado el diseño de la página web actual, sin que ningún artefacto visual pueda cambiar la escala del navegador del cliente. </p> <p>Haga clic en la dirección URL para abrir la página web, cambie el tamaño de la ventana del explorador para que se acerque a diferentes puntos de interrupción del diseño y supervise el tráfico de red. </p> <p>Entre los casos de uso más avanzados se incluyen la asociación de diferentes ajustes preestablecidos de imagen, comandos de servicio de imágenes o ambos, con diferentes valores de punto de interrupción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>En este siguiente ejemplo, se utilizan ajustes preestablecidos de imagen de diferente calidad y formato para diferentes tamaños de punto de interrupción. Para un pequeño punto de interrupción, se aplica un ajuste preestablecido de baja calidad que fuerza al servicio de imágenes a devolver la imagen GIF comprimida a seis colores solamente. Un punto de interrupción medio utiliza un ajuste preestablecido de imagen configurado para JPEG con compresión alta. El punto de interrupción más grande se asocia con un ajuste preestablecido de imagen de alta calidad mediante PNG sin pérdida. Este método garantiza que las imágenes de alta calidad se entreguen a dichos dispositivos, en función del supuesto de que los dispositivos con pantallas más grandes tienen un ancho de banda bueno y una potencia de procesamiento. </p> <p>Haga clic en la URL para abrir la página web, cambie el tamaño de la ventana del explorador web de mayor a menor y observe cómo se degrada la calidad de la imagen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Además de los ajustes preestablecidos de imagen, es posible asociar comandos específicos de servicio de imágenes con puntos de interrupción. El siguiente ejemplo muestra cómo es posible recortar gradualmente la imagen de la pancarta en la región de interés a medida que el tamaño de la imagen en pantalla se reduce. Aquí, el punto de interrupción más grande no tiene ningún comando de servicio de imágenes, por lo que la imagen del letrero es totalmente visible. En el punto de interrupción medio se aplica un recorte moderado, haciendo que solo esté visible el cursor con el texto "En ejecución". En un punto de interrupción pequeño, se aplica más recorte para que solo se muestre el producto. </p> <p>Haga clic en la URL para abrir la página web y cambiar el tamaño de la ventana del explorador. Observe cómo la imagen recorta gradualmente a medida que va de un tamaño mayor a uno más pequeño. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>También puede utilizar comandos de servicio de imágenes con plantillas de servicio de imágenes para controlar determinados parámetros de plantilla según el tamaño de la imagen. En este ejemplo siguiente, se utiliza una plantilla de servicio de imágenes en la que el tamaño de fuente de la superposición de texto se parametriza con el parámetro <span class="codeph"> $fontsize </span>. La imagen adaptable está configurada para utilizar un tamaño de fuente mayor para tamaños de imagen más pequeños, a fin de garantizar que el texto siempre sea legible: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos del sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware y software del servidor**

* Scene7 Image Serving 6.0.1 o posterior.

**Requisitos mínimos del explorador del cliente**

* Microsoft® Windows® 7 o posterior; Mac OS X 10.8 o posterior.
* Firefox 23, Safari 6, Chrome 29, IE 9 o posterior.
* iOS 6 o posterior.
* Certificado en iPhone3GS o posterior y en iPad2 o posterior (solo navegadores nativos).
* Android OS 2.3 o posterior.
* Internet Explorer en dispositivos móviles no es compatible en este momento.

