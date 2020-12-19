---
description: Últimas notas de la versión de Adobe Scene7 de otoño de 2016, parte de la solución Adobe Experience Manager en Adobe Marketing Cloud.
seo-description: Últimas notas de la versión de Adobe Scene7 de otoño de 2016, parte de la solución Adobe Experience Manager en Adobe Marketing Cloud.
seo-title: Versión de otoño de 2016 de Scene7
solution: Experience Manager
title: Versión de otoño de 2016 de Scene7
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Versión de Scene7 de otoño de 2016{#scene-fall-release}

Últimas notas de la versión de Adobe Scene7 de otoño de 2016, parte de la solución Adobe Experience Manager en Adobe Marketing Cloud.

## Versión de Scene7 de otoño de 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Últimas notas de la versión de [!DNL Adobe Scene7] otoño de 2016, parte de la solución [!DNL Adobe Experience Manager] en [!DNL Adobe Marketing Cloud].

* [General](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visores (servicio de imágenes 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visores (servicio de imágenes 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visores (servicio de imágenes 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Image Serving 6.3.2 y procesamiento de imágenes 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## General {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe está emocionado de anunciar la disponibilidad del envío de contenido HTTP/2 con el beneficio general de mejorar el rendimiento.

Consulte [Preguntas más frecuentes sobre el Envío HTTP2](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Para obtener la documentación completa, consulte [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Nuevas funciones, mejoras y correcciones de errores**

* Se ha eliminado la función de reedición de vídeo de la interfaz de usuario [!DNL Adobe Scene7 Publishing System].
* Autenticación añadida a todos los servlets de Scene7 cuando sea necesario y posible.
* Corrección de errores que involucra la Vista de Lista en la papelera.
* Se ha eliminado **Crear la función de usuario SPSAdmin** de Administración de usuarios por problemas de seguridad.
* FTP WebAdmin ahora admite la autenticación OKTA.
* Se ha eliminado la función de la contraseña predeterminada que se creó para los nuevos usuarios de Media Portal.
* Corrección de errores que implica la contraseña temporal que se generó al agregar un nuevo usuario. La contraseña no cumplía los requisitos de contraseña necesarios.
* Se han resuelto problemas con el disco raíz de WebAdmin lleno.
* La corrección de errores que implica la desactivación de un usuario no se refleja inmediatamente en la interfaz de usuario.
* Corrección de errores que implicaba la eliminación de un usuario que no le permitía volver a crear el usuario más adelante.
* Corrección de errores relacionados con el correo electrónico de bienvenida enviado a nuevos usuarios de Scene7 que no incluían autenticación para controlar determinadas opciones.
* Corrección de errores que implican el error al recuperar una lista de carpeta FTP si alguna de las carpetas tiene caracteres especiales en su nombre.
* Configurar proveedores de servicio OKTA para entornos Scene7.
* Compatibilidad añadida con el ID de organización de Marketing Cloud para Viewer Analytics.
* Se ha implementado el cliente SAML de Scene7.

## Visores (servicio de imágenes 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Corrección de errores para el servicio de imágenes 5.5.3**

* Compatibilidad con las bibliotecas RequireJS y DOJO.

   Caché de SDK JS consolidado durante la implementación del visor.

## Visores (servicio de imágenes 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Corrección de errores para el servicio de imágenes 5.5.2**

* No se pudo reproducir el vídeo en Internet Explorer 11 en Windows 7.
* `initialframe` no afectaba al modo vertical en dispositivos móviles para el catálogo electrónico HTML5.

## Visores (servicio de imágenes 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Nuevas funciones, mejoras y correcciones de errores para el servicio de imágenes 5.5.1**

* Visor de catálogos electrónicos HTML5 con función de búsqueda.
* Reproducción de vídeo de flujo continuo HLS añadida como método de envío de vídeo predeterminado para la mayoría de los sistemas de escritorio. El flujo de vídeo basado en Flash HDS sigue estando disponible como opción de reproducción alternativa.
* Compatibilidad añadida para dispositivos con entrada táctil y de ratón que ejecutan el navegador Chrome.
* Compatibilidad añadida del ID de organización de Marketing Cloud con la integración de Analytics.
* Actualice la biblioteca JavaScript de AppMeasurement a la versión 1.6.1.
* Se ha añadido la compatibilidad con la orientación de derecha a izquierda en el visor de catálogos electrónicos.
* Se ha solucionado el problema por el que `tip=0,-1,0` generaba un error fuera de rango.

**Notas de compatibilidad**

* Blackberry

   * Incompatibilidad con conjuntos AVS antiguos. Es posible que los clientes necesiten volver a cargar conjuntos AVS para permitir la reproducción.

* General

   * La escala del lado del explorador puede hacer que la interfaz de usuario y las imágenes se desdibujen a medida que el usuario se acerque a la página. El formato de la interfaz de usuario también puede mostrarse incorrectamente en función del zoom. Esto pasará a la pantalla completa.
   * Debido a la limitación de tamaño en dispositivos móviles, el visor de medios mixtos utiliza gestos de diapositiva para intercambiar fotogramas en conjuntos de imágenes incrustadas en lugar de tocar el componente de muestras incrustadas. El componente está allí como indicador visual.
   * En los navegadores Internet Explorer y algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * El botón Cerrar no funciona con iOS 8.0 y 8.1, pero ya no aparece en iOS 8.2

* Galaxy SIII

   * Se ha producido una fuga de memoria con los visores de zoom y catálogos electrónicos HTML5. La navegación repetida a través de marcos puede provocar que el navegador se bloquee.
   * El toque de doble en el visor puede hacer que toda la página se acerque en lugar de solo en el visor con la escala del lado del navegador activada.

* Galaxia S4

   * Dispositivo detectado como tableta en modo vertical con pantalla completa marcada en la configuración del navegador.

* Nexo de galaxia

   * El toque de doble en el visor puede hacer que toda la página se acerque en lugar de solo en el visor con la escala del lado del navegador activada.

* Galaxy Nexus 10 y Galaxy Tablet

   * Catálogo electrónico que muestra una distribución de páginas incorrecta con orientaciones vertical y horizontal.

* Dispositivos móviles HTC

   * Nuestros hallazgos de dispositivos móviles HTC muestran que la incapacidad de desactivar el zoom de pellizco nativo es una &quot;característica&quot; del envoltorio HTC UI (HTC Sense). Esto puede hacer que toda la página se acerque al usar el gesto de &quot;pellizcar para hacer zoom&quot; en el visor. En su lugar, sugiera utilizar el toque de doble.
   * Los iconos de mapas de imagen pueden superponerse si los mapas de imagen son pequeños y están próximos entre sí.

* Vídeo HTML5

   * Internet Explorer 9: las imágenes de póster personalizadas no se muestran.
   * `IntialBitRate` solo se admite con la reproducción de software HLS y Flash HDS. No funciona cuando la reproducción utiliza el reproductor nativo.
   * No se admite la reproducción progresiva de OGG y WebM en este momento.
   * El ajuste de escala del explorador puede hacer que el reproductor de vídeo se muestre con un tamaño incorrecto (incluye los ajustes de visualización del panel de control del sistema operativo Windows)
   * La búsqueda de vídeos mediante flujo HLS en Safari puede ser incoherente.

* Internet Explorer

   * En este momento no se admite el modo de preguntas y respuestas.
   * El modo de compatibilidad no es compatible en este momento.
   * Internet Explorer en dispositivos móviles no es compatible en este momento.

* iOS

   * Los catálogos electrónicos grandes pueden provocar el bloqueo del explorador en el iPad 2.
   * Los visores detectan los teléfonos iPhone 6+ como tablets.

* Safari

   * Safari 6.1 o posterior: La configuración de los complementos de Internet puede impedir la reproducción de vídeo Flash.
   * La &quot;búsqueda&quot; de vídeos mediante el flujo HLS en Safari puede ser incoherente.
   * No se puede buscar el final del vídeo en Safari 6 mediante el flujo HLS.

**Problemas y restricciones conocidos**

* Los modificadores del servicio de imágenes de `iscommands` no se agregan a la solicitud `req=set` por diseño. Los modificadores que solo afectan a la visualización de la imagen funcionan bien. Los modificadores que afectan al tamaño deben utilizarse en un recurso complejo. Por ejemplo,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] FlyoutIE9 a veces permanece en la pantalla después de que el ratón se apague.
* El cambio de tamaño del explorador provoca un cambio de tamaño incorrecto.
* iPad 2: El recurso de catálogo electrónico grande bloqueará Safari en iOS.
* Todos los visores

   * No se admiten marcas de agua, confusión ni bloqueo.
   * No se admiten los ajustes preestablecidos de imagen.
   * En este momento no se admite añadir o quitar el visor del DOM mediante `display:none` CSS o desconectándolo dinámicamente del nodo principal.

* Todos los visores de HTML5

   * La incrustación de un visor en una tabla puede provocar un tamaño o una colocación incorrectos del visor en el modo de pantalla completa no nativo. Sugerir usar DIV en su lugar.
   * Los parámetros con nombres de instancia explícitos en el código requieren que los nombres de instancia en la dirección URL también se sobrescriban (por ejemplo, `zoomView.iconfeffect=0`).
   * El recorte de comandos del servicio de imágenes no se admite en este momento.
   * El botón Cerrar solo funciona si el visor está abierto en la ventana secundaria.
   * El modificador `iscommands` no admite los modificadores de servicio de imágenes que afectan al tamaño de la imagen.

* Catálogo electrónico HTML5

   * Al desplazarse a otra página HTML y volver ocasionalmente, el visor vuelve a la primera página.
   * El diseño de página se muestra de forma ocasional incorrectamente después de rotar el dispositivo iOS. Al acercar la página se corrige el diseño.
   * Los vínculos internos solo conducen a la página más a la izquierda en los pliegos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * InitalFrame solo vincula a la página situada más a la izquierda en los pliegos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * Debido a las limitaciones del navegador, la función de impresión no está disponible en IE9.

* Medios mixtos HTML5

   * Actualmente no se admite la reproducción de pistas de sonido.

* HTML5 Social

   * Para procesar las miniaturas correctamente en el correo electrónico saliente, el modificador `serverurl` debe tener una dirección URL absoluta.

* Vídeo HTML5

   * La imagen de póster puede encontrar el error &quot;tamaño máximo&quot;. Es posible que la compañía necesite aumentar la configuración de límite para la publicación con servicio de imágenes.
   * Los subtítulos de vídeo requieren un conjunto de reglas de compañía si el alojamiento de la página HTML se proporciona desde un servidor externo (no desde un servidor Scene7). Póngase en contacto con el servicio de asistencia al Adobe para obtener ayuda.
   * El seguimiento de Analytics puede notificar un porcentaje de reproducción incorrecto debido al almacenamiento en búfer
   * En dispositivos iPad o Android, es posible que se muestre un marco negro en lugar de una imagen de póster.
   * El marco negro puede parpadear en la pantalla durante la carga del visor en dispositivos iPad o Android.
   * Los bordes negros se muestran en un lado del componente VideoPlayer cuando el fondo se establece en blanco/transparente en dispositivos iPad.
   * El último fotograma de vídeo se puede distorsionar en el iPad con iOS 7.
   * Puede que se produzcan bloqueos ocasionales durante la búsqueda de vídeo en el modo de flujo HLS en los navegadores Chrome, Firefox e Internet Explorer.
   * Es posible que la imagen de póster no se muestre en el explorador Microsoft Edge por primera vez en el visitante.
   * La imagen de póster puede ocultarse tras la carga de vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## SDK de visor HTML5 para Scene7 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guía del usuario se encuentra en la carpeta SDK del visor HTML5 de Adobe de la instalación del cliente. La documentación de la API de componente se encuentra en la subcarpeta docs de la instalación del cliente.

**Corrección de errores para 3.0.2**

* VideoPlayer: no se pudo reproducir el vídeo en Internet Explorer 11 en Windows 7
* TableOfContents - `initialframe` no afectó al modo vertical en dispositivos móviles para el visor de catálogos electrónicos HTML5.

**Nuevas funciones, mejoras y correcciones de errores para 3.0.1**

* General

   * Reproducción de vídeo de flujo continuo HLS añadida como método de envío de vídeo predeterminado para la mayoría de los sistemas de escritorio. El flujo de vídeo basado en Flash HDS sigue estando disponible como opción de reproducción alternativa.
   * Se añadieron los componentes SearchManager, SearchPanel, SearchEffect y SearchButton para admitir la nueva función de búsqueda en los visores de catálogos electrónicos.
   * Compatibilidad añadida para dispositivos con entrada táctil y de ratón que se ejecutan en el navegador Chrome.
   * Se ha refactorizado la detección de versiones de Android para admitir versiones futuras del SO
   * Añada la compatibilidad con la orientación de derecha a izquierda en los componentes del SDK específicos del catálogo electrónico.

* Barra de control

   * Se añadió el desplazamiento opcional para el contenido de la barra de control en caso de que no se ajuste a la anchura disponible.

* Vista de zoom flotante

   * Se corrigió el caso en el que `tip=0,-1,0` causaba un error fuera de rango.

**Notas de compatibilidad**

* Android 4.x

   * Para desactivar el valor predeterminado, es necesario agregar el azul de resaltado para el componente la siguiente regla CSS:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * La reproducción de vídeo puede cesar al cambiar flujos de velocidad de bits en conjuntos AVS.

* Chrome

   * Cualquier llamada de API que obligue a la reconstrucción de componentes puede ignorarse debido al almacenamiento en caché interno de Chrome.

* Galaxy SIII

   * A veces, el visor no se carga en la pantalla completa.
   * Pageview sufre de una fuga de memoria en el dispositivo en este momento.
   * El gesto de toque de doble amplía el visor y la página cuando el escalado de lado del navegador está activo.

* Nexo de galaxia

   * Objetos que se muestran sobre algunos componentes de vista.
   * El gesto de toque de doble amplía el visor y la página cuando el escalado de lado del navegador está activo.

* iPad 3

   * El iPad 3 tiene una resolución nativa de 2048 x 1536. Esto puede provocar problemas de visualización si el IS de la compañía se publica, el límite de tamaño de la imagen se establece por debajo de ese valor.

* iPhone 4

   * El icono de reproducción del efecto de iconos se sustituye por el icono de reproducción después de desplazarse por la página.

* Internet Explorer

   * En IE 10 y el modo de pantalla completa anterior no ocupa toda la pantalla, sino que simplemente cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * No se admite el modo de procesamiento rápido.
   * Internet Explorer en dispositivos móviles no es compatible en este momento.
   * Util.js puede no cargarse si se incluye de forma asíncrona.
   * El icono IconEffect bloquea los eventos de clic en los componentes de vista de giros y vista de zoom.

* Reproductores de vídeo de dispositivos nativos

   * Los componentes de interfaz de usuario de capas sobre VideoPlayer no son compatibles cuando VideoPlayer se utiliza para llamar al reproductor nativo del dispositivo.
   * La reproducción de vídeo en modo nativo no es coherente en Safari 6.
   * La reproducción nativa reemplaza el icono de reproducción con el icono de reproducción después de desplazarse por la página.

* Dispositivos táctiles

   * El modo de pantalla completa no ocupa toda la pantalla del dispositivo, sino que simplemente cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * Los cursores personalizados no funcionan en dispositivos táctiles.
   * En este momento no se admite el escalado de página en dispositivos táctiles. La incrustación de visores HTML5 requiere una etiqueta meta de ventanilla con la configuración adecuada.

* Xoom

   * El gesto de toque de doble amplía el visor y la página cuando el escalado de lado del navegador está activo.

**Problemas y restricciones conocidos**

* Todos los componentes

   * En las versiones 2.7.2 y anteriores, algunos componentes se agregaban al DOM mediante la API `insertBefore()`. Como resultado, dichos componentes se colocarían en la parte inferior del orden de apilamiento, independientemente de que se cree una instancia de componente en relación con otros componentes. Con la versión 2.8.1, todos los componentes utilizan la API `appendChild()` ahora, lo que significa que el orden de apilamiento de componentes coincidiría con el orden de creación de instancias.

   * No se admite el uso del modificador `iscommand` para establecer el formato de canal alfa de la imagen. Utilice el parámetro de componente `FMT` en su lugar.
   * La propiedad de transformación CSS no se admite en este momento.

* Dispositivos táctiles

   * El gesto de pellizco en los dispositivos táctiles no genera un evento de zoom

* Contenedor

   * El borde, el relleno y los márgenes del contenedor no son compatibles. Adobe sugiere agregar elementos de estilo a DIV principal.
   * Es necesario definir explícitamente el tamaño del contenedor o los componentes se pueden ajustar correctamente.

* Imprimir componente

   * Debido a las limitaciones del navegador, en Internet Explorer 9, es posible que el componente de impresión no escale el contenido correctamente en el papel.

* IconEffect, componente

   * IconEffect genera un error de secuencia de comandos en Internet Explorer si `autohide` está deshabilitado (establecido en `0`).

* Componente ImageMapEffect

   * Retraso con el icono de cambio de posición al desplazar la imagen en el componente de vista.

* Componente MediaSet

   * Los recursos en línea solicitan la misma codificación que en la URL.

* Componente NavigationView

   * Actualmente, el componente no admite el cambio de tamaño.

* PageScrubber, componente

   * En el iPhone 5, cuando la burbuja PageScrubber se establece en texto, muestra artefactos al desplazar el botón por la pista. El uso de `-webkit-background-clip: content;` en el estilo funciona en torno al problema.

* Componente SpinView

   * En ocasiones, la vista de giros aparece congelada tras un gesto de barrido y al girar el dispositivo mientras la imagen gira.

* Componente Muestras

   * Al seleccionar una muestra fuera de los límites, se muestran 2 resaltados.
   * El desplazamiento automático con el método `selectSwatch()` no funciona correctamente.

* VideoPlayer

   * El fotograma de vídeo no se actualiza si la búsqueda se establece en 100 por ciento con la opción de reserva definida en auto.
   * Puede que se produzcan bloqueos ocasionales de macros durante la búsqueda de vídeo en el modo de flujo HLS en los navegadores Chrome, Firefox e Internet Explorer.
   * Es posible que la imagen de póster no se muestre en el explorador Microsoft Edge por primera vez en el visitante.
   * La imagen de póster puede ocultarse tras la carga de vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## Scene7 Image Serving 6.3.2 y Procesamiento de imágenes 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilidad IC: ya no se admite el indicador `downsample2x2`. Este indicador era un downsampler 2x2 de mala calidad que IPS ya no utiliza.
* Encabezado CORS: actualmente, el encabezado CORS está configurado para `/is/content/` solicitudes.

