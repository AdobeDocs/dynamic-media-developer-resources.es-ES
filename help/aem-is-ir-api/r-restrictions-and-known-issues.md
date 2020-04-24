---
description: Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar el servicio de imágenes de Scene7.
seo-description: Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar el servicio de imágenes de Scene7.
seo-title: Restricciones y problemas conocidos
solution: Experience Manager
title: Restricciones y problemas conocidos
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Restricciones y problemas conocidos{#restrictions-and-known-issues}

Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar el servicio de imágenes de Scene7.

## Errores de documentación {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* El número de líneas no excederá el máximo de la configuración y el número de líneas explícitas en la entrada de texto. `\copyfitmaxlines`
* Los paréntesis y corchetes redondos coincidentes son obligatorios en los conjuntos de imágenes. Si no coinciden los paréntesis y los corchetes redondos, deben tener codificación de dirección URL.
* La alerta de tiempo de respuesta global del lado del servidor incluye respuestas de error.
* Actualmente, el `id=` comando es necesario cuando se utiliza el `rect=` comando con una solicitud de imagen o máscara.

## Diferencias conocidas textPs= frente a text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* El cursiva sintético se procesa con menos inclinación que cuando se utiliza `text=`.
* El subrayado es un poco más bajo y delgado que cuando se utiliza `text=`.
* `\expnd` y `\expndtw` se utilizan con valores negativos altos, hacen que los caracteres se coloquen uno frente al otro al usar `text=`.

* `\charscaley` cambia de escala de forma diferente que cuando se utiliza `text=` pero no afecta a la altura de la línea.

* Si la última línea de texto no cabe, la línea completa se coloca en lugar de aparecer como cortada.
* `\slmult` y `\sl` se comportan de forma diferente a MS Word y `text=`, simplemente surten efecto para los párrafos actuales y posteriores.

* `\sb` se aplica al primer párrafo para MS Word y `text=`, Adobe InDesign y Photoshop no lo hacen.

* `\sa` se aplica al último párrafo para MS Word y `text=`, Adobe InDesign y Photoshop no lo hacen.

## Compatibilidad con versiones anteriores {#section-a76842f751944f4fb664af296d064122}

* Escapar el carácter de subrayado ( `\_`) en una cadena RTF no funciona con todas las fuentes que utilizan `textPs=`

* Compatibilidad con la gestión de macros que no distingue entre mayúsculas y minúsculas.
* La caché del catálogo se ha reducido de 60 segundos a 10 segundos.
* La función de redirección de errores ahora solo redirige solicitudes que hacen referencia a imágenes, fuentes, perfiles de color e imágenes dañadas que se han publicado en un catálogo pero que no se encuentran en el disco.
* `posN=`, `anchor=`, `anchorN=`, `origin=`y `originN=` ahora devuelven un error de análisis si alguno de los valores del modificador es bueno a 2147483648.

* No se admite la codificación de solicitudes anidadas. Transición al nuevo comportamiento y descodificar cualquier valor de solicitud anidado que se encuentre en las solicitudes URL del sitio y en los catálogos de compañías.
* DefaultImage ahora aplica atributos de miniatura al usar `req=tmb`.
* En versiones anteriores que utilizaban `flip=`, la imagen nunca se cambiaba de posición independientemente del punto de ancla.

## Restricciones aplicables a bibliotecas de terceros {#section-79768b96bf634e44ab672c5b893f343d}

La biblioteca Digimarc se niega a aplicar una marca de agua Digimarc a una imagen si ya se ha detectado una. Si se realiza una edición suficiente en una imagen principal, es posible que la biblioteca Digimarc pueda reconocer que se ha aplicado la marca de agua. Sin embargo, es posible que no pueda leer esa información. Esto resulta en una nueva imagen en la que no se puede obtener la información de Digimarc original que se aplicó a la imagen original. El servicio de imágenes ahora puede aplicar la marca de agua Digimarc definida en el catálogo de compañías.

## Restricciones aplicables al servicio de imágenes y al procesamiento de imágenes {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Es posible que el servicio de imágenes y el procesamiento de imágenes no aprovechen al máximo todas las CPU cuando hay más de 4 CPU disponibles. Simule el tráfico en estos equipos para ver cuán ventajoso resulta con más de 4 CPU.
* Se rechazan las direcciones URL remotas que devuelven una redirección (estados HTTP 301, 302 o 303).
* Al configurar `errorRedirect.rootUrl` la dirección IP definida en esta propiedad, debe incluirse en el valor de la `<addressfilter>` etiqueta del conjunto de reglas de ese servidor.

   *Ejemplo*:

   El servidor A ha definido `errorRedirect.rootUrl=10.10.10.10` .

   El servidor B, que tiene la dirección IP 10.10.10.10, establece el valor de la `<addressfilter>` etiqueta en el archivo de conjunto de reglas para incluir su dirección IP (10.10.10.10).

* El texto del punto y el trazado de texto con posición pueden mostrar recorte.
* `text=` solo se aplica `\sa` y `\sb` a todo el bloque de texto y no a cada párrafo.

* Al utilizar una compañía definida en la URL y otra compañía definida para el modificador `src=` o `mask=` , debe anteponer una barra diagonal a la compañía definida para `src=` o `mask=` para que funcione esta forma de solicitud.

   *Ejemplo*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   En lugar de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Las solicitudes Tiff o Vignette no pirámidas producen un mensaje de error similar a

   *&quot;La imagen`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`no tiene un DSF válido y el área de 2,25MPixel supera el máximo de 2MPixel&quot;* .

   Lo mejor es usar tiñas pirámidas y viñetas. Si necesita usar tifones o viñetas no piramidables, siga las instrucciones siguientes para aumentar el límite de tamaño.

   *Solución*:

   En el caso de las viñetas de procesamiento de imágenes que no son piramidables, aumente el valor de propiedad de IrMaxNonPyrVignetteSize en el archivo de configuración [!DNL *[!DNL install_root]*/ImageServing/bin/ ImageServerRegistry.xml].

   Para los TIFF que no son piramidables del servicio de imágenes, aumente el valor de la propiedad `MaxNonDsfSize` en el archivo de configuración [!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml].

* Adobe Photoshop CS3 no guarda archivos PSD con capas de forma predeterminada en una imagen compuesta.

   *Síntomas*:

   El archivo PSD con capas de Adobe Photoshop CS3 se muestra en negro con texto que indica: &quot;Este archivo de Photoshop con capas no se guardó con una imagen compuesta&quot;. para la imagen de respuesta del servicio de imágenes o en IPS.

   *Solución*:

   Guarde el archivo de Adobe Photoshop CS3 con la máxima compatibilidad activada.

* La asignación de Perfil ICC a una imagen de respuesta CMYK/JPEG hace que los colores se inviertan en algunos exploradores.*Solución*:

   Cambiar el formato de imagen de respuesta mediante `fmt=`

* El tamaño de los datos de imagen de respuesta HTTP después de la compresión, incluido el encabezado de archivo, está limitado a 16 MB.
* &quot; ..&quot; no está permitido en ningún elemento de ruta en solicitudes HTTP.
* La desinstalación puede eliminar del archivo creado o modificado por el usuario *[!DNL install_root]* o de cualquier subcarpeta. Copie estos archivos en una ubicación diferente antes de desinstalar.

## Restricciones aplicables solo al servicio de imágenes {#section-b08ad535e4454265b8157dec244c4faf}

* Los colores de primer plano del comando RTF ( `\cf`) no son compatibles con el texto PhotoFont.
* La sintetización de negrita, cursiva y negrita/cursiva se rechazará como un error en el texto de PhotoFont.
* El flujo de texto vertical no es compatible con el texto PhotoFont.
* El texto PhotoFont no admite imágenes PNG de 16 bpc.
* Las correcciones de color para imágenes PNG con perfiles de color incrustados utilizan opciones codificadas. La calidad de representación es colorimétrica relativa y la compensación de punto negro está activada para el texto PhotoFont.
* La búsqueda basada en archivos no se admite cuando la traducción de configuraciones regionales está habilitada en el [!DNL ini] archivo de compañía.
* El servicio de imágenes no escribe correctamente las rutas de Photoshop no cerradas.
* El servicio de imágenes no admite actualmente el procesamiento de archivos TIFF exportados con Adobe Media Encoder 4.0.1 o anterior. Adobe Media Encoder se incluye con Premiere Pro CS4, After Effects CS4 y Creative Suite 4 Production Premium.
* El uso `text=` con capas de tamaño propio no admite cadenas RTF que utilicen más de un ajuste para la justificación de línea.

   *Ejemplo*

   La cadena RTF no puede utilizar justificación de línea izquierda y derecha para una capa de texto con tamaño propio.

* SVG tiene su propia propiedad para la ruta de búsqueda de fuentes de las fuentes a las que se hace referencia que no están incrustadas en el archivo SVG.

   *Síntomas*

   Las imágenes SVG representadas que contienen definiciones de fuente utilizan una fuente incorrecta.

   *Solución*

   Establezca la propiedad `svgProvider.fontRoot=` en [!DNL *[!DNL install_root]* /ImageServing/conf/PlatformServer.conf].

* Actualmente, el recorte se utiliza `bgColor=` en lugar de `color=` para rellenar cualquier área recientemente extendida.

* Es posible que la conversión de color no sea correcta cuando `bgColor=` no coincide con el espacio de color base que implica perfiles de color.
* Los efectos de capa externa no se procesan si la capa no tiene datos de máscara o alfa.

## Restricciones aplicables solo al procesamiento de imágenes {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Las cubiertas y los materiales murales no son extraíbles.
* El tamaño de las texturas está limitado en relación con el tamaño de la vista de la viñeta. En circunstancias excepcionales, el límite predeterminado del 425 % del tamaño de vista puede interferir con una aplicación que utilice texturas no repetibles muy grandes. Si no es posible cambiar la aplicación o el contenido para que funcionen con las limitaciones predefinidas, el porcentaje se puede aumentar de la siguiente manera. Con un editor de texto, abra [!DNL *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml], busque `IrMaxTextureSizeFactor` e introduzca un nuevo valor de porcentaje. El cambio surte efecto inmediatamente sin reiniciar el servidor de imágenes.

* Los motores JavaScript de Netscape y Opera procesan los datos de respuesta de caché aunque se haya establecido el encabezado nocache. Esto interfiere con el correcto funcionamiento de las solicitudes de estado.

   *Solución*

   Anexe una marca de hora u otro identificador único a la cadena de solicitud, como `"&.ts=currentTime`.

## Restricciones aplicables solamente a utilidades {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a veces se bloquea con un error de segmentación cuando se detiene con un `control-c`.
