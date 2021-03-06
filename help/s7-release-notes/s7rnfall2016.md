---
title: Versión de otoño de 2016 de Scene7
description: '"Últimas notas de la versión de otoño de 2016 de Adobe Scene7, parte de la solución Adobe Experience Manager en Adobe Experience Cloud".'
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Versión de otoño de 2016 de Scene7{#scene-fall-release}

Últimas notas de la versión de Adobe Scene7 de otoño de 2016: parte de la solución Adobe Experience Manager en Adobe Experience Cloud.

## Versión de otoño de 2016 de Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Últimas notas de la versión para [!DNL Adobe Scene7] Versión de otoño de 2016: parte del [!DNL Adobe Experience Manager] en el [!DNL Adobe Experience Cloud].

* [General](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizadores (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizadores (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizadores (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 y Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## General {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe se complace en anunciar la disponibilidad de la entrega HTTP/2 de contenido con la ventaja general de un rendimiento mejorado.

Consulte [Preguntas frecuentes sobre la entrega de contenido HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Para obtener toda la documentación, consulte [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nuevas funciones, mejoras y correcciones de errores**

* Se ha eliminado la función de reedición de vídeo de [!DNL Adobe Scene7 Publishing System] interfaz de usuario.
* Se ha añadido la autenticación a todos los servlets de Scene7 donde sea necesario y posible
* Corrección de errores que afectan a la vista de lista en la papelera.
* Eliminado **Crear administrador de Dynamic Media Classic (Scene7)** característica de usuario de Administración de usuarios debido a problemas de seguridad.
* FTP WebAdmin ahora es compatible con la autenticación OKTA.
* Se ha eliminado la función de la contraseña predeterminada que se había creado para los nuevos usuarios de Media Portal.
* Corrección de errores que implican la contraseña temporal que se generó cuando se agregó un nuevo usuario. La contraseña no cumplía los requisitos de contraseña necesarios.
* Se han resuelto problemas del disco raíz de WebAdmin llenos.
* Corrección de errores que implican la desactivación de un usuario que no se refleja inmediatamente en la interfaz de usuario.
* Corrección de errores que implicaba la eliminación de un usuario que no le permitía volver a crear el usuario más adelante.
* Corrección de errores que implicaba el correo electrónico de bienvenida enviado a nuevos usuarios de Scene7 que no incluían autenticación para controlar determinadas configuraciones.
* Corrección de errores que implican el error al recuperar una lista de carpetas FTP si alguna carpeta tiene caracteres especiales en su nombre.
* Configure los proveedores de servicios OKTA para los entornos Scene7.
* Se ha agregado compatibilidad con el ID de organización de Experience Cloud para el análisis de visualizador.
* Se ha implementado el consumidor de Scene7 SAML.

## Visualizadores (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Para obtener toda la documentación, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correcciones de errores para Image Serving 5.5.3**

* Compatibilidad con las bibliotecas RequireJS y DOJO.

   Almacenamiento en caché de SDK JS consolidado durante la implementación del visor.

## Visualizadores (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Para obtener toda la documentación, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correcciones de errores para Image Serving 5.5.2**

* Error al reproducir el vídeo en Internet Explorer 11 en Windows 7.
* `initialframe` no afectaba al modo vertical en dispositivos móviles para el catálogo electrónico HTML5.

## Visualizadores (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Para obtener toda la documentación, consulte [Guía de referencia de visores](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Nuevas funciones, mejoras y correcciones de errores en Image Serving 5.5.1**

* Visor de catálogos electrónicos HTML5 con función de búsqueda.
* Se ha agregado la reproducción de vídeo de flujo continuo HLS como método de entrega de vídeo predeterminado para la mayoría de los sistemas de escritorio. La transmisión de vídeo del HDS basada en Flash sigue estando disponible como opción de reproducción alternativa.
* Se ha agregado compatibilidad con dispositivos con entrada táctil y de ratón que ejecutan el navegador Chrome.
* Se ha agregado compatibilidad con ID de organización de Experience Cloud a la integración de Analytics.
* Actualice la biblioteca JavaScript de AppMeasurement a la versión 1.6.1.
* Se ha añadido compatibilidad con la orientación de derecha a izquierda en el visor del catálogo electrónico.
* Se ha corregido un problema en el que `tip=0,-1,0` provocó un error fuera de rango.

**Notas de compatibilidad**

* Blackberry®

   * Incompatibilidad con conjuntos AVS antiguos. Los clientes deben volver a cargar los conjuntos AVS para permitir la reproducción.

* General

   * El escalado del lado del explorador puede hacer que la interfaz de usuario y las imágenes se vuelvan borrosas a medida que el usuario amplía la página. El formato de la interfaz de usuario también puede mostrarse incorrectamente según el zoom. Este efecto se transmite a pantalla completa.
   * Debido a la limitación de tamaño de los dispositivos móviles, el visualizador de medios mixtos utiliza un gesto de diapositivas para intercambiar fotogramas en conjuntos de imágenes incrustados en lugar de pulsar el componente de muestras incrustadas. El componente está allí como indicador visual.
   * En los navegadores Internet Explorer y en algunos dispositivos táctiles, el modo de pantalla completa no ocupa toda la pantalla del dispositivo. En su lugar, cambia el tamaño de la aplicación al tamaño de la ventana del explorador.
   * El botón Cerrar no funciona en iOS 8.0 y 8.1, pero ya no aparece en iOS 8.2

* Galaxia SIII

   * Fuga de memoria vista con los visores HTML5 de zoom y catálogo electrónico. La navegación repetida a través de marcos puede causar que el navegador se bloquee.
   * Si se pulsa dos veces en el visor, es posible que toda la página se zoom en lugar de solo el visor con el escalado del lado del navegador activado.

* Galaxia S4

   * Dispositivo detectado como tableta en modo vertical con pantalla completa marcada en la configuración del navegador.

* Nexo de galaxia

   * Si se pulsa dos veces en el visor, es posible que toda la página se zoom en lugar de solo el visor con el escalado del lado del navegador activado.

* Galaxy Nexus 10 y Galaxy Tablet

   * Catálogo electrónico que muestra una página incorrecta con orientaciones verticales y horizontales.

* Dispositivos móviles HTC

   * Los hallazgos del Adobe de dispositivos móviles HTC muestran que la incapacidad de desactivar el zoom de pellizcar nativo es una &quot;función&quot; del envoltorio de la interfaz de usuario de HTC (HTC Sense). Este problema puede hacer que toda la página se zoom al usar el gesto de &quot;pellizcar para hacer zoom&quot; en el visor. Sugiera utilizar el doble toque en su lugar.
   * Los iconos del mapa de imágenes pueden superponerse si los mapas de imágenes son pequeños y están próximos entre sí.

* Vídeo de HTML5

   * Internet Explorer 9: las imágenes de póster personalizadas no se muestran.
   * `IntialBitRate` sólo se admite con el software HLS y la reproducción del HDS en Flash. No funciona cuando la reproducción utiliza el reproductor nativo.
   * Actualmente no se admite la reproducción progresiva de OGG y WebM.
   * El escalado del explorador puede hacer que el reproductor de vídeo se muestre con un tamaño incorrecto (incluye la configuración de visualización del panel de control del sistema operativo Windows).
   * La búsqueda de vídeo mediante el flujo HLS en Safari puede ser incoherente.

* Internet Explorer

   * Actualmente no se admite el modo Quirks.
   * Actualmente no se admite el modo de compatibilidad.
   * Actualmente no se admite Internet Explorer en dispositivos móviles.

* iOS

   * Los catálogos electrónicos grandes pueden provocar el bloqueo del explorador en iPad 2.
   * Los espectadores detectan los teléfonos iPhone 6+ como tabletas.

* Safari

   * Safari 6.1 o posterior: La configuración de complementos de Internet puede impedir la reproducción de vídeo en Flash.
   * La &quot;búsqueda&quot; de vídeo utilizando el flujo HLS en Safari puede ser incoherente.
   * No se puede intentar finalizar el vídeo en Safari 6 mediante el flujo HLS.

**Problemas y restricciones conocidos**

* Los modificadores de servicio de imágenes de `iscommands` no se añaden a la variable `req=set` solicitud por diseño. Los modificadores que solo afectan a la visualización de la imagen funcionan bien. Los modificadores que afectan al tamaño deben utilizarse en un recurso complejo. Por ejemplo,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flotante] IE9 a veces permanece en la pantalla después de apagar el ratón.
* El cambio de tamaño del explorador da lugar a un cambio de tamaño incorrecto.
* iPad 2: Un recurso de catálogo electrónico grande bloquea Safari en iOS.
* Todos los visores

   * Las marcas de agua, la ofuscación y el bloqueo no son compatibles.
   * Los ajustes preestablecidos de imagen no son compatibles.
   * Adición o eliminación de un visor del DOM mediante `display:none` Actualmente no se admite CSS o desasociándolo dinámicamente del nodo principal.

* HTML5 Todos los visores

   * Si se incrusta el visor en la tabla, es posible que el tamaño o la ubicación del visor no sean correctos en el modo de pantalla completa no nativo. Sugiera usar DIV en su lugar.
   * Los parámetros con nombres de instancia explícitos en el código requieren que se sobrescriban los nombres de instancia en la URL (por ejemplo, `zoomView.iconfeffect=0`).
   * Actualmente no se admite el recorte de comandos del servicio de imágenes.
   * El botón Cerrar solo funciona si el visor está abierto en la ventana secundaria.
   * La variable `iscommands` El modificador no admite modificadores de servicio de imágenes que afecten al tamaño de la imagen.

* Catálogo electrónico HTML5

   * Al navegar a otra página de HTML y volver ocasionalmente, el visor vuelve a la primera página.
   * El diseño de la página a veces se muestra incorrectamente después de girar el dispositivo iOS. Al acercar la página se corrige el diseño.
   * Internal solo vincula a la página más a la izquierda en grupos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * InitalFrame solo vincula a la página situada más a la izquierda en pliegos de varias páginas. Afecta a los dispositivos móviles en modo vertical.
   * Debido a las limitaciones del navegador, la función de impresión no está disponible en IE9.

* HTML5 MixedMedia

   * No se admite la reproducción de bandas sonoras.

* HTML5 Social

   * Para procesar las miniaturas correctamente en el correo electrónico saliente, la variable `serverurl` debe tener una dirección URL absoluta.

* Vídeo de HTML5

   * La imagen de póster puede encontrar el error &quot;tamaño máximo&quot;. La empresa debe aumentar la configuración de límite para la publicación de servicio de imágenes.
   * Los subtítulos de vídeo requieren un conjunto de reglas de la empresa si el alojamiento de la página HTML se sirve desde un servidor externo (no un servidor Scene7). Póngase en contacto con el servicio de asistencia al Adobe para obtener ayuda.
   * El seguimiento de Analytics puede notificar un porcentaje de reproducción incorrecto debido al almacenamiento en búfer
   * En los dispositivos iPad o Android™ puede aparecer un marco negro en lugar de una imagen de póster.
   * El marco negro puede parpadear en la pantalla durante la carga del visor en dispositivos iPad o Android™.
   * Los bordes negros se muestran en el lado del componente VideoPlayer cuando el fondo se establece en blanco/transparente en los dispositivos iPad.
   * El último fotograma de vídeo puede distorsionarse en iPad con iOS 7.
   * Durante la búsqueda de vídeo en el modo de flujo continuo HLS, puede producirse un bloqueo de página ocasional en los navegadores Chrome, Firefox e Internet Explorer.
      * Es posible que la imagen de póster no se muestre en el explorador Microsoft® Edge por primera vez.
      * La imagen de póster se puede ocultar después de la carga de vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## SDK 3.0.2 del visor Scene7 HTML5 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guía del usuario se encuentra en la carpeta Adobe HTML5 Viewer SDK de la instalación del cliente. La documentación de la API de componente se encuentra en la subcarpeta docs de la instalación del cliente.

**Correcciones de errores para 3.0.2**

* VideoPlayer: no se pudo reproducir el vídeo en Internet Explorer 11 en Windows 7.
* TablaDeContenido -  `initialframe` no afectaba al modo vertical en dispositivos móviles para el visor de catálogos electrónicos de HTML5.

**Nuevas funciones, mejoras y correcciones de errores en la versión 3.0.1**

* General

   * Se ha agregado la reproducción de vídeo de flujo continuo HLS como método de entrega de vídeo predeterminado para la mayoría de los sistemas de escritorio. La transmisión de vídeo del HDS basada en Flash sigue estando disponible como opción de reproducción alternativa.
   * Se agregaron los componentes SearchManager, SearchPanel, SearchEffect y SearchButton para admitir la nueva función de búsqueda en los visualizadores de catálogos electrónicos.
   * Se ha agregado compatibilidad con dispositivos con entrada táctil y de ratón que se ejecutan en el explorador Chrome.
   * Se ha rediseñado la detección de versiones de Android™ para admitir versiones futuras del sistema operativo.
   * Añada compatibilidad con la orientación de derecha a izquierda en los componentes SDK específicos del catálogo electrónico.

* Barra de control

   * Se ha añadido el desplazamiento opcional para el contenido de la barra de control en caso de que no se ajuste a la anchura disponible.

* Vista de zoom flotante

   * Se ha corregido el caso en el que `tip=0,-1,0` provocó un error fuera de rango.

**Notas de compatibilidad**

* Android™ 4.x

   * Para desactivar el valor predeterminado, se debe añadir un resaltado azul a la siguiente regla CSS para el componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry®

   * La reproducción de vídeo puede interrumpirse al cambiar las emisiones de velocidad de bits en conjuntos AVS.

* Chrome

   * Cualquier llamada de API que obligue a la reconstrucción de componentes puede ignorarse debido al almacenamiento en caché interno de Chrome.

* Galaxia SIII

   * El visor a veces no se carga en la pantalla completa.
   * Pageview sufre de una fuga de memoria en el dispositivo actualmente.
   * El gesto de doble toque reduce el visor y la página cuando el escalado del lado del explorador está activo.

* Nexo de galaxia

   * Objetos que se muestran sobre algunos componentes de la vista.
   * El gesto de doble toque reduce el visor y la página cuando el escalado del lado del explorador está activo.

* iPad 3

   * iPad 3 tiene una resolución nativa de 2048 x 1536. Esta resolución puede causar problemas de visualización si se publica el IS de la empresa, el límite de tamaño de la imagen se establece por debajo.

* iPhone4

   * Icono de reproducción de efecto sustituido por el icono de reproducción después de desplazarse por la página.

* Internet Explorer

   * En IE 10 y el modo de pantalla completa anterior no ocupa la pantalla completa, sino que solo cambia el tamaño de la aplicación al de la ventana del explorador.
   * No se admite el modo de procesamiento de Quirks.
   * Actualmente no se admite Internet Explorer en dispositivos móviles.
   * Util.js puede no cargarse si se incluye de forma asíncrona.
   * El icono IconEffect bloquea los eventos de clic en los componentes de SpinView y ZoomView.

* Reproductores de vídeo de dispositivos nativos

   * Los componentes de IU de capas sobre VideoPlayer no son compatibles cuando VideoPlayer se utiliza para llamar al reproductor nativo del dispositivo.
   * La reproducción de vídeo en modo nativo no es coherente en Safari 6.
   * La reproducción nativa reemplaza el icono de reproducción por el icono de reproducción después de desplazarse por la página.

* Dispositivos táctiles

   * El modo de pantalla completa no ocupa toda la pantalla del dispositivo, sino que solo cambia el tamaño de la aplicación al de la ventana del explorador.
   * Los cursores personalizados no funcionan en dispositivos táctiles.
   * Actualmente no se admite el escalado de página en dispositivos táctiles. La incrustación de los visores HTML5 requiere una metaetiqueta viewport con la configuración adecuada.

* Xoom

   * El gesto de doble toque reduce el visor y la página cuando el escalado del lado del explorador está activo.

**Problemas y restricciones conocidos**

* Todos los componentes

   * En las versiones 2.7.2 y anteriores, se agregaron algunos componentes al DOM mediante `insertBefore()` API. Como resultado, estos componentes se colocarían en la parte inferior del orden de apilamiento, independientemente de si la instancia de componente se crea en relación con otros componentes. Con la versión 2.8.1, todos los componentes utilizan `appendChild()` Ahora API, lo que significa que el orden de apilamiento de componentes coincidiría con el orden de creación de instancias.

   * Uso `iscommand` no se admite el modificador para establecer el formato de canal alfa de la imagen. Uso del componente `FMT` en su lugar.
   * Actualmente no se admite la propiedad de transformación CSS.

* Dispositivos táctiles

   * El gesto de pellizco en los dispositivos táctiles no genera un evento de zoom

* Contenedor

   * El borde, el relleno y los márgenes del contenedor no son compatibles. Adobe sugiere añadir elementos de estilo al DIV principal.
   * Debe establecer explícitamente el tamaño del contenedor o es posible que el tamaño de los componentes sea correcto.

* Imprimir componente

   * Debido a las limitaciones del navegador, en Internet Explorer 9, es posible que el componente de impresión no escale el contenido correctamente en el papel.

* IconoEffect, componente

   * IconEffect genera un error de secuencia de comandos en Internet Explorer si `autohide` está desactivado (establecido en `0`).

* Componente ImageMapEffect

   * Retraso con el icono de cambio de posición al panoramizar la imagen en el componente de vista.

* Componente MediaSet

   * Los recursos en línea solicitan la misma codificación que en la dirección URL.

* Componente NavigationView

   * Actualmente, el componente no admite el cambio de tamaño.

* Componente PageScrubber

   * En iPhone 5, cuando la burbuja PageScrubber está establecida en texto, muestra los artefactos al deslizarse el botón por la pista. Uso `-webkit-background-clip: content;` en el estilo funciona en torno al problema.

* Componente SpinView

   * En ocasiones, SpinView parece congelarse después de un gesto de desliz y de girar el dispositivo mientras la imagen gira.

* Componente Muestras

   * Al seleccionar una muestra fuera de los límites, se muestran dos resaltados.
   * Desplazamiento automático con `selectSwatch()` funciona incorrectamente.

* Reproductor de videos

   * El fotograma de vídeo no se actualiza si la búsqueda está configurada al 100 % con la reserva configurada como automática.
   * Durante la búsqueda de vídeo en el modo de transmisión HLS, puede producirse un bloqueo ocasional de macros en los navegadores Chrome, Firefox e Internet Explorer.
   * Es posible que la imagen de póster no se muestre en el explorador Microsoft® Edge por primera vez.
   * La imagen de póster se puede ocultar después de la carga de vídeo en Internet Explorer 9 cuando se utiliza la reproducción progresiva.

## Dynamic Media Image Serving 6.3.2 y Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilidad IC - `downsample2x2` ya no se admite el indicador . Este indicador era un downsampler 2x2 de mala calidad que IPS ya no utiliza.
* Encabezado CORS : Actualmente, el encabezado CORS está configurado para `/is/content/` solicitudes.
