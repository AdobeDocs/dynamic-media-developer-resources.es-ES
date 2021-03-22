---
description: Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar Dynamic Media Image Serving.
seo-description: Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar Dynamic Media Image Serving.
seo-title: Restricciones y problemas conocidos
solution: Experience Manager
title: Restricciones y problemas conocidos
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 0%

---


# Restricciones y problemas conocidos{#restrictions-and-known-issues}

Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar Dynamic Media Image Serving.

## Errores de documentación {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* El número de líneas no excederá el máximo de la configuración `\copyfitmaxlines` y el número de líneas explícitas en la entrada de texto.
* Los paréntesis y corchetes de curvas coincidentes son obligatorios en los conjuntos de imágenes. Si no coinciden los paréntesis y los corchetes curvas, deben codificarse con la dirección URL.
* La alerta de tiempo de respuesta global del lado del servidor incluye respuestas de error.
* El comando `id=` actualmente es necesario cuando se utiliza el comando `rect=` con una solicitud de imagen o máscara.

## Diferencias conocidas textPs= frente a text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* El cursiva sintético se representa con menos inclinación que al utilizar `text=`.
* El subrayado es un poco menor y más delgado que cuando se utiliza `text=`.
* `\expnd` y  `\expndtw` se utilizan con valores negativos altos, hacen que los caracteres se coloquen uno delante del otro al utilizar  `text=`.

* `\charscaley` se escala de forma diferente a cuando se utiliza,  `text=` pero no afecta a la altura de línea.

* Si la última línea de texto no cabe, se coloca toda la línea en lugar de aparecer como cortada.
* `\slmult` y  `\sl` se comportan de forma diferente a MS Word y  `text=`, simplemente tienen efecto para los párrafos actual y subsiguientes.

* `\sb` se aplica al primer párrafo tanto para MS Word como para  `text=`, Adobe InDesign y Photoshop no lo hacen.

* `\sa` se aplica al último párrafo tanto para MS Word como para  `text=`, Adobe InDesign y Photoshop no lo hacen.

## Compatibilidad con versiones anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapar del carácter de guión bajo ( `\_`) en una cadena RTF no funciona con todas las fuentes que utilizan `textPs=`

* Compatibilidad con la gestión de macros que no distingue entre mayúsculas y minúsculas.
* La caché del catálogo se ha reducido de 60 segundos a 10 segundos.
* La función de redireccionamiento de errores ahora solo redirige solicitudes que hacen referencia a imágenes, fuentes, perfiles de color e imágenes dañadas publicadas en un catálogo, pero que no se encuentran en el disco.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=` y  `originN=` ahora devuelven un error de análisis si alguno de los valores del modificador es bueno a 2147483648.

* No se admite la codificación de solicitudes anidadas. Realice una transición al nuevo comportamiento y descodifique los valores de solicitud anidados que se encuentren en las solicitudes URL del sitio y en los catálogos de la empresa.
* DefaultImage ahora aplica atributos de miniatura al utilizar `req=tmb`.
* En versiones anteriores que utilizaban `flip=`, la imagen nunca se cambiaba de posición independientemente del punto de ancla.

## Restricciones aplicables a bibliotecas de terceros {#section-79768b96bf634e44ab672c5b893f343d}

La biblioteca Digimarc se niega a aplicar una marca de agua Digimarc a una imagen si ya se ha detectado. Si se realiza suficiente edición en una imagen principal, es posible que la biblioteca Digimarc pueda reconocer que se aplicó la marca de agua. Sin embargo, es posible que no pueda leer esa información. Esto resulta en una nueva imagen donde no se puede obtener la información Digimarc original que se aplicó a la imagen original. Image Serving ahora puede aplicar la marca de agua Digimarc definida en el catálogo de la empresa.

## Restricciones aplicables tanto al servicio de imágenes como al procesamiento de imágenes {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Es posible que Image Serving y Image Rendering no aprovechen al máximo todas las CPUs cuando hay más de 4 CPUs disponibles. Simule el tráfico en estos equipos para ver lo ventajoso que es con más de 4 CPUs.
* Las direcciones URL remotas que devuelven un redireccionamiento (estados HTTP 301, 302 o 303) se rechazan.
* Al configurar `errorRedirect.rootUrl`, la dirección IP definida en esta propiedad debe incluirse en el valor de etiqueta `<addressfilter>` del conjunto de reglas de ese servidor.

   *Ejemplo*:

   El servidor A ha definido `errorRedirect.rootUrl=10.10.10.10` .

   El servidor B, que tiene la dirección IP 10.10.10.10, establece el valor de la etiqueta `<addressfilter>` en el archivo del conjunto de reglas para incluir su dirección IP (10.10.10.10).

* El texto de punto y la ruta de texto con posición pueden mostrar recorte.
* `text=` solo se aplica  `\sa` y  `\sb` a todo el bloque de texto y no a cada párrafo.

* Cuando se utiliza una empresa definida en la dirección URL y otra empresa definida para el modificador `src=` o `mask=`, se debe anteponer una barra diagonal a la empresa definida para `src=` o `mask=` para que funcione esta forma de solicitud.

   *Ejemplo*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   En lugar de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Las solicitudes de tiff o viñeta que no son pirámides producen un mensaje de error similar a

   *&quot;La imagen no  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` tiene un DSF válido y el área de 2,25MPixel supera el máximo de 2MPixel&quot;* .

   La práctica recomendada es utilizar tiffs y viñetas piramidables. Si necesita usar tiffs o viñetas sin pirámides, siga las instrucciones que se indican a continuación para aumentar el límite de tamaño.

   *Solución alternativa*:

   En el caso de las viñetas de renderización de imágenes sin pirámide, aumente el valor de la propiedad IrMaxNonPyrVignetteSize en el archivo de configuración [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Para los TIFF no piramidables de servicio de imágenes, aumente el valor de la propiedad `MaxNonDsfSize` en el archivo de configuración [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Adobe Photoshop CS3 no guarda archivos PSD en capas de forma predeterminada, con una imagen compuesta.

   *Síntomas*:

   El archivo PSD con capas Adobe Photoshop CS3 se muestra en negro con el texto siguiente: &quot;Este archivo Photoshop con capas no se guardó con una imagen compuesta&quot;. para la imagen de respuesta de Image Serving o en IPS.

   *Solución*:

   Guarde el archivo Adobe Photoshop CS3 con la máxima compatibilidad activada.

* Asignar el perfil ICC a una imagen de respuesta CMYK/JPEG hace que los colores se inviertan en algunos navegadores.*Solución alternativa*:

   Cambiar el formato de imagen de respuesta utilizando `fmt=`

* El tamaño de los datos de imagen de respuesta HTTP después de la compresión, incluido el encabezado del archivo, está limitado a 16 MB.
* &quot;..&quot; no está permitido en ningún elemento de ruta en solicitudes HTTP.
* La desinstalación puede eliminar el archivo creado o modificado por el usuario de *[!DNL install_root]* o de cualquier subcarpeta. Copie estos archivos en una ubicación diferente antes de desinstalarlos.

## Restricciones aplicables únicamente a Image Serving {#section-b08ad535e4454265b8157dec244c4faf}

* Los colores de primer plano del comando RTF ( `\cf`) no son compatibles con el texto de PhotoFont.
* La sintetización de negrita, cursiva y negrita/cursiva se rechazará como error para el texto de PhotoFont.
* El flujo de texto vertical no es compatible con el texto PhotoFont.
* Las imágenes PNG de 16 bpc no son compatibles con el texto PhotoFont.
* Las correcciones de color para imágenes PNG con perfiles de color incrustados utilizan opciones codificadas. La interpretación es colorimétrica relativa y la compensación de punto negro está activada para el texto PhotoFont.
* La búsqueda basada en archivos no se admite cuando la traducción de configuración regional está habilitada en el archivo de la empresa [!DNL ini].
* Image Serving no escribe correctamente las rutas de Photoshop no cerradas.
* El servicio de imágenes actualmente no admite el procesamiento de archivos TIFF exportados con Adobe Media Encoder 4.0.1 o anterior. Adobe Media Encoder se incluye con Premiere Pro CS4, After Effects CS4 y Creative Suite 4 Production Premium.
* El uso de `text=` con capas de tamaño automático no admite cadenas RTF que utilicen más de un ajuste para la justificación de líneas.

   *Ejemplo*

   La cadena RTF no puede utilizar justificación de línea izquierda y derecha para una capa de texto de tamaño automático.

* SVG tiene su propia propiedad para la ruta de búsqueda de fuentes de fuentes referenciadas que no están incrustadas en el archivo SVG.

   *Síntomas*

   Las imágenes SVG procesadas que contienen definiciones de fuente utilizan una fuente incorrecta.

   *Solución*

   Establezca la propiedad `svgProvider.fontRoot=` en [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* El recorte está usando actualmente `bgColor=` en lugar de `color=` para rellenar cualquier área recién extendida.

* Puede que la conversión de color no sea correcta cuando `bgColor=` no coincide con el espacio de color base que incluye perfiles de color.
* Los efectos de capa exterior no se representan si la capa no tiene una máscara o datos alfa.

## Restricciones aplicables únicamente a Image Rendering {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Las cubiertas y los materiales murales no son extraíbles.
* El tamaño de las texturas está limitado en relación con el tamaño de la vista de viñeta. En raras ocasiones, el límite predeterminado del 425% del tamaño de la vista puede interferir con una aplicación que utiliza texturas no repetibles muy grandes. Si no es posible cambiar la aplicación o el contenido para que funcionen dentro de las limitaciones predefinidas, el porcentaje se puede aumentar de la siguiente manera. Con un editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], busque `IrMaxTextureSizeFactor` e introduzca un nuevo valor de porcentaje. El cambio entra en vigor inmediatamente sin reiniciar el servidor de imágenes.

* Los motores JavaScript de Netscape y Opera responden a la caché aunque esté establecido el encabezado nocache. Esto interfiere con el correcto funcionamiento de las solicitudes de declaración.

   *Solución*

   Anexe una marca de tiempo u otro identificador único a la cadena de solicitud, como `"&.ts=currentTime`.

## Restricciones aplicables únicamente a las utilidades {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a veces se bloquea con un error de segmentación cuando se detiene con un  `control-c`.
