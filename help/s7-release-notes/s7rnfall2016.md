---
title: Versión de otoño de 2016 de Scene7
description: Últimas notas de la versión de Adobe Scene7 de otoño de 2016, parte de la solución Adobe Experience Manager en Adobe Experience Cloud.
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2236'
ht-degree: 0%

---

# Versión de otoño de 2016 de Scene7{#scene-fall-release}

Últimas notas de la versión de Adobe Scene7: parte de la solución Adobe Experience Manager de otoño de 2016 en Adobe Experience Cloud.

## Versión de otoño de 2016 de Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Últimas notas de la versión de [!DNL Adobe Scene7]: parte de la versión de otoño de 2016 de la solución [!DNL Adobe Experience Manager] en [!DNL Adobe Experience Cloud].

* [General](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizadores (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizadores (servicio de imágenes 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizadores (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## General {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe anuncia la disponibilidad del envío de contenido HTTP/2 con el beneficio general de mejorar el rendimiento.

Consulte [Preguntas frecuentes sobre la entrega de contenido HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html?lang=es#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Para obtener toda la documentación, consulte [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=es](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=es)

**Nuevas funciones, mejoras y correcciones de errores**

* Se ha eliminado la característica de reedición de vídeo de la interfaz de usuario [!DNL Adobe Scene7 Publishing System].
* Se ha añadido autenticación a todos los servlets de Scene7 cuando era necesario y posible
* Corrección de errores que implicaban la vista de lista en la papelera.
* Se ha eliminado la función de usuario **Crear administrador de Dynamic Media Classic (Scene7)** de Administración de usuarios debido a problemas de seguridad.
* FTP WebAdmin ahora admite la autenticación OKTA.
* Se ha eliminado la función de la contraseña predeterminada que se creó para los nuevos usuarios de Media Portal.
* Corrección de errores que implica la contraseña temporal que se generó cuando se agregó un usuario nuevo. La contraseña no cumplía los requisitos de contraseña necesarios.
* Se han resuelto problemas de disco raíz de WebAdmin lleno.
* Corrección de errores que implica la desactivación de un usuario y que no se refleja inmediatamente en la interfaz de usuario.
* Corrección de errores que implicaba la eliminación de un usuario, lo que no le permitía volver a crear el usuario más tarde.
* Corrección de errores que implica el correo electrónico de bienvenida enviado a los nuevos usuarios de Scene7 que no incluía autenticación para controlar determinadas configuraciones.
* Corrección de errores que implica un error al recuperar una lista de carpetas FTP si alguna carpeta tenía caracteres especiales en su nombre.
* Configure los proveedores de servicios OKTA para los entornos de Scene7.
* Se ha agregado compatibilidad con el ID de organización de Experience Cloud para Viewer Analytics.
* Se ha implementado Scene7 SAML consumer.

## Visualizadores (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=es).

**Correcciones de errores para el servicio de imágenes 5.5.3**

* Compatibilidad con las bibliotecas RequireJS y DOJO.

  Almacenamiento en caché de SDK JS consolidado durante la implementación del visor.

## Visualizadores (servicio de imágenes 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=es).

**Correcciones de errores para el servicio de imágenes 5.5.2**

* No se pudo reproducir el vídeo en Internet Explorer 11 en Windows 7.
* `initialframe` no afectaba al modo vertical en dispositivos móviles para el catálogo electrónico de HTML5.

## Visualizadores (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obtener documentación completa, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=es).

**Nuevas funciones, mejoras y correcciones de errores para el servicio de imágenes 5.5.1**

* Visor de catálogos electrónicos HTML5 con función de búsqueda.
* Se ha añadido la reproducción de vídeo de flujo continuo de HLS como método de entrega de vídeo predeterminado para la mayoría de los sistemas de escritorio. La transmisión de vídeo HDS basada en Flash sigue estando disponible como opción de reproducción alternativa.
* Se ha agregado compatibilidad para dispositivos con entrada táctil y de ratón que ejecutan el explorador Chrome.
* Se ha agregado compatibilidad con ID de organización de Experience Cloud a la integración de Analytics.
* Actualice la biblioteca JavaScript de AppMeasurement a la versión 1.6.1.
* Se ha añadido compatibilidad con la orientación de derecha a izquierda en el visor de catálogos electrónicos.
* Se ha corregido un problema en el cual `tip=0,-1,0` provocaba un error fuera del intervalo.

**Notas de compatibilidad**

* BlackBerry®

   * Incompatibilidad con conjuntos AVS más antiguos. Los clientes deben volver a cargar los conjuntos de AVS para permitir la reproducción.

* General

   * La escala del lado del explorador puede provocar que la interfaz de usuario y las imágenes se vuelvan borrosas a medida que el usuario amplía la página. El formato de la IU también puede mostrarse incorrectamente en función del zoom. Este efecto se transmite a pantalla completa.
   * Debido a la limitación de tamaño en dispositivos móviles, el visualizador de medios mixtos utiliza el gesto de diapositiva para intercambiar fotogramas en conjuntos de imágenes incrustados en lugar de pulsar el componente de muestras incrustado. El componente se encuentra allí como indicador visual.
   * En los exploradores de Internet Explorer y en algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación según el tamaño de la ventana del explorador.
   * El botón Cerrar no funciona en iOS 8.0 ni 8.1, pero ya no se utiliza en iOS 8.2

* Galaxia SIII

   * Pérdida de memoria con visores Zoom y eCatalog HTML5. La navegación repetida a través de fotogramas puede provocar el bloqueo del explorador.
   * Si se pulsa dos veces en el visor, puede que toda la página se haga zoom en lugar de solo en el visor con la escala lateral del explorador habilitada.

* Galaxy S4

   * El dispositivo se ha detectado como tablet en modo vertical con pantalla completa activada en la configuración del navegador.

* Nexo galáctico

   * Si se pulsa dos veces en el visor, puede que toda la página se haga zoom en lugar de solo en el visor con la escala lateral del explorador habilitada.

* Galaxy Nexus 10 y Galaxy Tablet

   * Catálogo electrónico que muestra un pliego de página incorrecto con orientaciones verticales y horizontales.

* Dispositivos móviles HTC

   * Los resultados de Adobe muestran que la incapacidad para deshabilitar el zoom de pellizco nativo es una &quot;característica&quot; del envoltorio de la interfaz de usuario de HTC (HTC Sense). Este problema puede hacer que toda la página se haga zoom al utilizar el gesto de &quot;pellizco para zoom&quot; en el visor. Sugiera utilizar el doble toque en su lugar.
   * Los iconos de mapa de imagen pueden superponerse si los mapas de imagen son pequeños y están muy juntos.

* Vídeo de HTML5

   * Internet Explorer 9: las imágenes de póster personalizadas no se muestran.
   * El modificador `IntialBitRate` solo se admite con la reproducción de HLS y Flash HDS de software. No funciona cuando la reproducción utiliza el reproductor nativo.
   * Actualmente no se admite la reproducción progresiva OGG y WebM.
   * La escala del explorador puede hacer que el reproductor de vídeo se muestre en un tamaño incorrecto (incluye la configuración de pantalla del panel de control del sistema operativo Windows).
   * La búsqueda de vídeo mediante el streaming de HLS en Safari puede ser incoherente.

* Internet Explorer

   * Actualmente no se admite el modo Quirks.
   * Actualmente no se admite el modo de compatibilidad.
   * Internet Explorer en dispositivos móviles no es compatible actualmente.

* iOS

   * Los catálogos electrónicos grandes pueden bloquear el explorador en iPad 2.
   * Los visores detectan los teléfonos iPhone 6 y posteriores como tabletas.

* Safari

   * Safari 6.1 o posterior: la configuración de los complementos de Internet puede impedir la reproducción de vídeo Flash.
   * La búsqueda de vídeo mediante el streaming de HLS en Safari puede ser incoherente.
   * No se puede buscar el final del vídeo en Safari 6 mediante el streaming de HLS.

**Problemas y restricciones conocidos**

* Los modificadores del servicio de imágenes de `iscommands` no se agregan a la solicitud `req=set` por diseño. Los modificadores que solo afectan a la visualización de la imagen funcionan bien. Los modificadores que afectan al tamaño deben utilizarse en un recurso complejo. Por ejemplo:

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flotante] IE9 permanece a veces en pantalla después de que el ratón se apague.
* El cambio de tamaño del explorador provoca un cambio de tamaño incorrecto.
* iPad 2: El recurso de catálogo electrónico grande bloquea Safari en iOS.
* Todos los visores

   * No se admiten marcas de agua, ofuscación ni bloqueo.
   * No se admiten ajustes preestablecidos de imagen.
   * Actualmente no se admite agregar o quitar el visor del DOM mediante CSS `display:none` o desasociándolo dinámicamente del nodo principal.

* Todos los visores de HTML5

   * La incrustación del visor en la tabla puede provocar un tamaño o una ubicación incorrectos del visor en un modo de pantalla completa no nativo. Sugiera usar DIV en su lugar.
   * Los parámetros con nombres de instancia explícitos en el código también requieren nombres de instancia en la dirección URL para sobrescribirse (por ejemplo, `zoomView.iconfeffect=0`).
   * Actualmente no se admite el recorte de comandos del servicio de imágenes.
   * El botón Cerrar solo funciona si el visor está abierto en la ventana secundaria.
   * El modificador `iscommands` no admite modificadores del servicio de imágenes que afecten al tamaño de la imagen.

* Catálogo electrónico de HTML5

   * Si se desplaza a otra página de HTML y regresa ocasionalmente, el visor vuelve a la primera página.
   * En ocasiones, el diseño de página se muestra incorrectamente después de girar el dispositivo iOS. Al acercar la página se corrige el diseño.
   * Los vínculos internos solo dirigen a la página situada más a la izquierda en pliegos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * InitialFrame vincula únicamente a la página situada más a la izquierda en pliegos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * Debido a las limitaciones del explorador, la función de impresión no está disponible en IE9.

* Medios mixtos HTML5

   * No se admite la reproducción de banda sonora.

* HTML5 Social

   * Para procesar las miniaturas correctamente en el correo electrónico saliente, el modificador `serverurl` debe tener una dirección URL absoluta.

* Vídeo de HTML5

   * La imagen del póster puede encontrar el error &quot;tamaño máximo&quot;. La compañía debe aumentar el ajuste de límite para la publicación del servicio de imágenes.
   * Los subtítulos de vídeo requieren un conjunto de reglas de empresa si el alojamiento de la página de HTML se proporciona desde un servidor externo (no desde un servidor de Scene7). Póngase en contacto con el Soporte técnico de Adobe para obtener ayuda.
   * El seguimiento de Analytics puede informar de un porcentaje de reproducción incorrecto debido al almacenamiento en búfer
   * El marco negro en lugar de la imagen del póster puede mostrarse en dispositivos iPad o Android™.
   * El marco negro puede parpadear en la pantalla durante la carga del visor en dispositivos iPad o Android™.
   * Los bordes negros se muestran en la parte lateral del componente VideoPlayer cuando el fondo está establecido en blanco/transparente en dispositivos iPad.
   * El último fotograma de vídeo puede distorsionarse en iPad con iOS 7.
   * Se pueden producir ocasionalmente bloqueos de macros durante la búsqueda de vídeo en el modo de streaming de HLS en los navegadores Chrome, Firefox e Internet Explorer.
      * Es posible que la imagen del póster no se muestre en el explorador Microsoft® Edge por primera vez en el visitante.
      * La imagen de póster puede ocultarse después de la carga del vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guía del usuario se encuentra en la carpeta Adobe HTML5 Viewer SDK de la instalación del cliente. La documentación de la API de componente se encuentra en la subcarpeta docs de la instalación del cliente.

**Correcciones de errores para 3.0.2**

* VideoPlayer: error al reproducir el vídeo en Internet Explorer 11 en Windows 7.
* TableOfContents - `initialframe` no afectó al modo vertical en dispositivos móviles para el visor de catálogos electrónicos HTML5.

**Nuevas funciones, mejoras y correcciones de errores para 3.0.1**

* General

   * Se ha añadido la reproducción de vídeo de flujo continuo de HLS como método de entrega de vídeo predeterminado para la mayoría de los sistemas de escritorio. La transmisión de vídeo HDS basada en Flash sigue estando disponible como opción de reproducción alternativa.
   * Se han agregado los componentes SearchManager, SearchPanel, SearchEffect y SearchButton para admitir la nueva función de búsqueda en los visores de catálogos electrónicos.
   * Se ha agregado compatibilidad para dispositivos con entrada táctil y de ratón en ejecución en el explorador Chrome.
   * Se ha refactorizado la detección de versiones de Android™ para admitir versiones futuras del sistema operativo.
   * Añada compatibilidad con la orientación de derecha a izquierda en los componentes SDK específicos del catálogo electrónico.

* BarraDeControl

   * Se ha agregado desplazamiento opcional para el contenido de ControlBar en caso de que no se ajuste al ancho disponible.

* FlyoutzoomView

   * Se ha corregido un caso en el cual `tip=0,-1,0` provocaba un error fuera del intervalo.

**Notas de compatibilidad**

* Android™ 4.x

   * Para deshabilitar el valor predeterminado, resalte en azul la siguiente regla CSS debe agregarse para el componente:

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * La reproducción de vídeo puede interrumpirse al cambiar la velocidad de bits de los flujos en conjuntos AVS.

* Chrome

   * Cualquier llamada a la API que obligue a la reconstrucción del componente puede ignorarse debido al almacenamiento en caché interno de Chrome.

* Galaxia SIII

   * El visor a veces no se puede cargar en pantalla completa.
   * La vista de página sufre una fuga de memoria en el dispositivo actualmente.
   * El gesto de doble toque amplía el visor y la página cuando la escala del lado del explorador está activa.

* Nexo galáctico

   * Artefactos que se muestran sobre algunos componentes de la vista.
   * El gesto de doble toque amplía el visor y la página cuando la escala del lado del explorador está activa.

* IPAD 3

   * El iPad 3 tiene una resolución nativa de 2048 x 1536. Esta resolución puede causar problemas de visualización si se publica el servicio de imágenes de la empresa y el límite de tamaño de imagen se establece en un nivel inferior.

* IPHONE4

   * Icono Icono de reproducción reemplazado por icono de reproducción después de desplazarse por la página.

* Internet Explorer

   * En IE 10 y versiones anteriores, el modo de pantalla completa no ocupa toda la pantalla, sino que solo cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * El modo de procesamiento Quirks no es compatible.
   * Internet Explorer en dispositivos móviles no es compatible actualmente.
   * Util.js puede no cargarse si se incluye asincrónicamente.
   * El icono IconEffect bloquea los eventos de clic en los componentes SpinView y ZoomView.

* Reproductores de vídeo de dispositivo nativos

   * Los componentes de la interfaz de usuario de capas a través de VideoPlayer no son compatibles cuando se utiliza VideoPlayer para llamar al reproductor nativo del dispositivo.
   * La reproducción de vídeo en modo nativo es incoherente en Safari 6.
   * La reproducción nativa sustituye el icono de reproducción por el icono de reproducción después de desplazarse por la página.

* Dispositivos táctiles

   * el modo de pantalla completa no ocupa toda la pantalla del dispositivo, sino que solo cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * Los cursores personalizados no funcionan en dispositivos táctiles.
   * Actualmente no se admite el escalado de página en dispositivos táctiles. La incrustación de visores de HTML5 requiere una metaetiqueta de ventanilla móvil con la configuración adecuada.

* Xoom

   * El gesto de doble toque amplía el visor y la página cuando la escala del lado del explorador está activa.

**Problemas y restricciones conocidos**

* Todos los componentes

   * En las versiones 2.7.2 y anteriores, algunos componentes se añadían al DOM mediante la API `insertBefore()`. Como resultado, estos componentes se colocarían en la parte inferior del orden de apilamiento, independientemente de cuándo se cree una instancia de componente en relación con otros componentes. Con la versión 2.8.1, todos los componentes utilizan ahora la API `appendChild()`, lo que significa que el orden de apilamiento de los componentes coincidirá con el orden de creación de la instancia.

   * No se admite el uso del modificador `iscommand` para establecer el formato de canal alfa de imagen. En su lugar, utilice el parámetro `FMT` del componente.
   * Actualmente, la propiedad de transformación de CSS no es compatible.

* Dispositivos táctiles

   * El gesto de pellizco en dispositivos táctiles no genera un evento de zoom

* Contenedor

   * No se admite el borde, relleno y márgenes del contenedor. Adobe sugiere agregar elementos de estilo al DIV principal.
   * Debe establecer explícitamente el tamaño del contenedor o los componentes pueden tener un tamaño correcto.

* Imprimir componente

   * Debido a las limitaciones del explorador, en Internet Explorer 9, es posible que el componente de impresión no escale el contenido correctamente en el papel.

* Componente IconEffect

   * IconEffect genera un error de script en Internet Explorer si `autohide` está deshabilitado (establecido en `0`).

* Componente ImageMapEffect

   * Retraso con el icono de cambio de posición al desplazarse por la imagen en el componente de vista.

* Componente MediaSet

   * Los recursos en línea solicitan la misma codificación que en la dirección URL.

* Componente NavigationView

   * Actualmente, el componente no admite el cambio de tamaño.

* Componente PageScrubber

   * En iPhone 5, cuando la burbuja PageScrubber está configurada como texto, muestra artefactos al deslizar el botón a lo largo de la pista. Usar `-webkit-background-clip: content;` en el estilo soluciona el problema.

* Componente SpinView

   * A veces, SpinView parece congelarse después de realizar un gesto de barrido y girar el dispositivo mientras la imagen está girando.

* Componente Muestras

   * Al seleccionar una muestra fuera de los límites, se muestran dos puntos resaltados.
   * El desplazamiento automático con el método `selectSwatch()` no funciona correctamente.

* VideoPlayer

   * El fotograma de vídeo no se actualiza si la búsqueda se establece en el 100 % y la reserva en auto.
   * En ocasiones, se pueden producir bloqueos de macros durante la búsqueda de vídeo en el modo de flujo continuo de HLS en los navegadores Chrome, Firefox e Internet Explorer.
   * Es posible que la imagen del póster no se muestre en el explorador Microsoft® Edge por primera vez en el visitante.
   * La imagen de póster puede ocultarse después de la carga del vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## Dynamic Media Image Serving 6.3.2 e Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilidad IC: ya no se admite el indicador `downsample2x2`. Este indicador era un downsampler 2x2 de baja calidad que ya no se utiliza en IPS.
* Encabezado CORS: actualmente, el encabezado CORS está configurado para `/is/content/` solicitudes.
