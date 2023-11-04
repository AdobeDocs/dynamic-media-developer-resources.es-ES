---
description: Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar el servicio de imágenes de Dynamic Media.
solution: Experience Manager
title: Restricciones y problemas conocidos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Restricciones y problemas conocidos{#restrictions-and-known-issues}

Existen algunas restricciones y problemas conocidos que deben tenerse en cuenta al utilizar el servicio de imágenes de Dynamic Media.

## erratas de documentación {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* El número de líneas no supera el máximo del `\copyfitmaxlines` configuración y el número de líneas explícitas en la entrada de texto.
* En los conjuntos de imágenes se requieren llaves y paréntesis coincidentes. Si no coinciden los paréntesis angulares y los paréntesis, deben codificarse con la dirección URL.
* La alerta de tiempo de respuesta global del lado del servidor incluye respuestas de error.
* El `id=` se requiere actualmente al utilizar el comando `rect=` con una solicitud de imagen o máscara.

## Diferencias conocidas textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* La cursiva sintética se representa menos inclinada que al utilizar `text=`.
* El subrayado es un poco más bajo y delgado que al utilizar `text=`.
* `\expnd` y `\expndtw` cuando se utiliza con valores negativos altos, los caracteres se colocan uno delante del otro cuando se utiliza `text=`.

* `\charscaley` se adapta de forma diferente que al usar `text=` pero no afecta al alto de línea.

* Si la última línea de texto no cabe, se suelta toda la línea en lugar de aparecer como punto de corte.
* `\slmult` y `\sl` comportarse de forma diferente a MS Word y `text=`, simplemente surten efecto para el párrafo actual y los párrafos siguientes.

* `\sb` se aplica al primer párrafo de MS Word y `text=`, ADOBE INDESIGN y [!DNL Photoshop] no haga esto.

* `\sa` se aplica al último párrafo de MS Word y `text=`, ADOBE INDESIGN y [!DNL Photoshop] no haga esto.

## Compatibilidad con versiones anteriores {#section-a76842f751944f4fb664af296d064122}

* Omisión del carácter de subrayado ( `\_`) en una cadena RTF no funciona con todas las fuentes que utilizan `textPs=`

* Compatibilidad con la gestión de macros sin distinción de mayúsculas y minúsculas.
* La caché del catálogo se ha reducido de 60 a 10 segundos.
* La función de redirección de errores ahora solo redirige solicitudes que hacen referencia a imágenes, fuentes, perfiles de color e imágenes dañadas publicadas en un catálogo, pero que no se encuentran en el disco.
* `posN=`, `anchor=`, `anchorN=`, `origin=`, y `originN=` ahora devuelve un error de análisis si alguno de los valores de modificador es mayor que 2147483648.

* No se admite la codificación de solicitudes anidadas. Realice la transición al nuevo comportamiento y descodifique los valores de solicitud anidados que se encuentren en las solicitudes de URL del sitio y en los catálogos de la empresa.
* DefaultImage ahora aplica atributos de miniatura al utilizar `req=tmb`.
* En versiones anteriores utilizando `flip=`Sin embargo, la imagen nunca se reposicionó independientemente del punto de ancla.

## Restricciones aplicables a las bibliotecas de terceros {#section-79768b96bf634e44ab672c5b893f343d}

La biblioteca Digimarc rechaza aplicar una marca de agua Digimarc a una imagen si ya se ha detectado una. Si se realiza suficiente edición en una imagen principal, la biblioteca Digimarc puede reconocer que se aplicó la marca de agua. Sin embargo, es posible que no pueda leer esa información. Esto da como resultado una nueva imagen en la que no se puede obtener la información original de Digimarc que se aplicó a la imagen original. El servicio de imágenes ahora puede aplicar la marca de agua Digimarc definida en el catálogo de la empresa.

## Restricciones aplicables al servicio y al procesamiento de imágenes {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Es posible que el servicio de imágenes y el procesamiento de imágenes no saquen el máximo partido de todas las CPU cuando hay más de 4 CPU disponibles. Simule su tráfico en estas máquinas para ver lo ventajoso que es con más de 4 CPU.
* Las direcciones URL remotas que devuelven un redireccionamiento (estados HTTP 301, 302 o 303) se rechazan.
* Al configurar `errorRedirect.rootUrl` la dirección IP definida en esta propiedad debe incluirse en el conjunto de reglas `<addressfilter>` valor de etiqueta en ese servidor.

  *Ejemplo*:

  El servidor A ha definido `errorRedirect.rootUrl=10.10.10.10` .

  El servidor B que tiene la dirección IP 10.10.10.10, establece el `<addressfilter>` en el archivo del conjunto de reglas para incluir su dirección IP (10.10.10.10).

* El texto de punto y el trazado de texto con posición pueden mostrar recorte.
* `text=` solo se aplica `\sa` y `\sb` a todo el bloque de texto y no por párrafo.

* Al utilizar una compañía definida en la URL y otra compañía definida para la `src=` o `mask=` modificador, se debe anteponer una barra diagonal a la compañía definida para `src=` o `mask=` para que este formulario de solicitud funcione.

  *Ejemplo*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  En lugar de: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Las solicitudes de tiff o viñeta no piramidadas generan un mensaje de error similar al siguiente

  *&quot;Imagen `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` no tiene DSF válido, y el área de 2.25MPixel supera el máximo de 2MPixel&quot;* .

  La práctica recomendada es utilizar tiffs y viñetas piramidales. Si necesita utilizar tiffs o viñetas no piramidales, siga las instrucciones a continuación para aumentar el límite de tamaño.

  *Solución alternativa*:

  Para viñetas no piramidadas de procesamiento de imágenes, aumente el valor de la propiedad para IrMaxNonPyrVignetteSize en [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] archivo de configuración.

  Para TIFF no piramidales del servicio de imágenes, aumente el valor de la propiedad para `MaxNonDsfSize` en el [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] archivo de configuración.

* Adobe [!DNL Photoshop] CS3 no guarda archivos de PSD con capas de forma predeterminada como imagen compuesta.

  *Síntomas*:

  El Adobe [!DNL Photoshop] El archivo de PSD en capas CS3 se muestra en negro con un texto que indica: &quot;Esta capa [!DNL Photoshop] el archivo no se ha guardado con una imagen compuesta.&quot; para la imagen de respuesta del servicio de imágenes o en IPS.

  *Solución*:

  Guardar el Adobe [!DNL Photoshop] Archivo CS3 con la máxima compatibilidad activada.

* Al asignar un perfil ICC a una imagen de respuesta CMYK/JPEG, los colores se invierten en algunos exploradores.*Solución alternativa*:

  Cambiar el formato de imagen de respuesta mediante `fmt=`

* El tamaño de los datos de imagen de respuesta HTTP tras la compresión, incluido el encabezado de archivo, está limitado a 16 MB.
* &quot;...&quot; no está permitido en ningún elemento de ruta en solicitudes HTTP.
* La desinstalación puede eliminar el archivo creado por el usuario o modificado de *[!DNL install_root]* o cualquier subcarpeta. Copie estos archivos en una ubicación diferente antes de desinstalarlos.

## Restricciones aplicables solo al servicio de imágenes {#section-b08ad535e4454265b8157dec244c4faf}

* Colores de primer plano en formato RTF ( `\cf`) no son compatibles con el texto de PhotoFont.
* La síntesis de negrita, cursiva y negrita/cursiva se rechaza como error para el texto de PhotoFont.
* El flujo de texto vertical no es compatible con el texto de PhotoFont.
* Las imágenes PNG de 16 bpc no son compatibles con el texto de PhotoFont.
* Las correcciones de color para imágenes PNG con perfiles de color incrustados utilizan opciones codificadas. La interpretación es colorimétrica relativa y la compensación de punto negro está activada para el texto de PhotoFont.
* La búsqueda basada en archivos no es compatible cuando la traducción de configuración regional está habilitada en la empresa [!DNL ini] archivo.
* El servicio de imágenes no escribe sin cerrar [!DNL Photoshop] rutas correctamente.
* Actualmente, el servicio de imágenes no admite el procesamiento de archivos de TIFF exportados con Adobe Media Encoder 4.0.1 o versiones anteriores. Adobe Media Encoder se incluye con Premiere Pro CS4, After Effects CS4 y Creative Suite 4 Production Premium.
* Uso de `text=` con capas de tamaño propio no admite cadenas RTF que utilicen más de una configuración para la justificación de líneas.

  *Ejemplo*

  La cadena RTF no puede utilizar justificación de línea izquierda y derecha para una capa de texto de tamaño personalizado.

* SVG tiene su propia propiedad para la ruta de búsqueda de fuentes de referencia que no están incrustadas en el archivo del SVG.

  *Síntomas*

  Las imágenes de SVG procesadas que contienen definiciones de fuentes utilizan la fuente incorrecta.

  *Solución*

  Establezca la propiedad `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* El recorte está utilizando actualmente `bgColor=` en lugar de `color=` para rellenar cualquier área recién extendida.

* La conversión de color puede no ser correcta cuando `bgColor=` no coincide con el espacio de color base que implica perfiles de color.
* Los efectos de capa externa no se representan si la capa no tiene una máscara o datos alfa.

## Restricciones aplicables solo a Image Rendering {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Las calcomanías y los materiales de pared no son extraíbles.
* El tamaño de las texturas está limitado en relación con el tamaño de la vista de la viñeta. En circunstancias excepcionales, el límite predeterminado del 425% del tamaño de la vista puede interferir con una aplicación que utiliza texturas no repetibles muy grandes. Si no es posible cambiar la aplicación o el contenido para que funcione dentro de las limitaciones predefinidas, el porcentaje se puede aumentar de la siguiente manera. Con un editor de texto, abra [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localice `IrMaxTextureSizeFactor` e introduzca un nuevo valor porcentual. El cambio surtirá efecto inmediatamente sin reiniciar el servidor de imágenes.

* Los motores JavaScript de Netscape y Opera almacenan los datos de respuesta en caché incluso si se ha definido el encabezado nocache. Esto interfiere con el funcionamiento adecuado de las solicitudes con estado.

  *Solución*

  Anexe una marca de tiempo u otro identificador único a la cadena de solicitud, como `"&.ts=currentTime`.

## Restricciones aplicables solo a las utilidades {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a veces se bloquea con un error de segmentación cuando se detiene con un `control-c`.
