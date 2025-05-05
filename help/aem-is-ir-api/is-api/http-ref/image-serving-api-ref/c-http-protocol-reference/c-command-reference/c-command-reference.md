---
title: Referencia de comando
description: En esta sección se describen los comandos del protocolo HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# Referencia de comando{#command-reference}

En esta sección se describen los comandos del protocolo HTTP.

>[!TIP]
>
>Pruebe y descubra las ventajas de los modificadores de imagen de Dynamic Media y de las imágenes inteligentes con Dynamic Media [_Snapshot_](https://snapshot.scene7.com/).
>
> Snapshot es una herramienta de demostración visual diseñada para ilustrar la potencia de Dynamic Media para la entrega de imágenes optimizadas y dinámicas. Experimente con imágenes de prueba o direcciones URL de Dynamic Media para observar visualmente la salida de varios modificadores de imagen de Dynamic Media y optimizaciones de imágenes inteligentes para lo siguiente:
>* Tamaño de archivo (con envío WebP y AVIF)
>* Ancho de banda de red
>* DPR (proporción de píxeles del dispositivo)
>
>Para aprender lo fácil que es usar Snapshot, reproduzca el [vídeo de entrenamiento Snapshot](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=es) (3 minutos y 17 segundos).


**Solo para Dynamic Media en Adobe Experience Manager AEM**: más allá de la configuración de imagen básica disponible en la interfaz de usuario, [!DNL Dynamic Media] en ( [!DNL Adobe Experience Manager]) admite numerosas modificaciones de imagen avanzadas que se pueden especificar en el campo **Modificadores de imagen**. Estos parámetros se definen a continuación. Sin embargo, tenga en cuenta que la siguiente funcionalidad no es compatible con Dynamic Media AEM en el caso de los usuarios de.

* Comandos de corrección de color: `icc=` y `iccEmbed=`.
* Plantillas básicas y comandos de procesamiento de texto: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` y `textPs=`.
* Comandos de localización: `locale=` y `req=xlate`.
* `req=set` no está disponible para uso general.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Servicios no principales de Dynamic Media: SVG, procesamiento de imágenes y web para impresión.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulte también las [Opciones de ajustes preestablecidos de imagen](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=es#dynamic) de Dynamic Media AEM en la documentación de la versión 6.5 de la documentación de la.

* [alinear](r-align.md)
* [delimitador](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [mixedMode](r-blendmode.md)
* [escondrijo](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [recorte](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [efecto](r-effect.md)
* [effectMask](r-effectmask.md)
* [extender](r-extend.md)
* [ajuste](r-fit.md)
* [voltear](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [ocultar](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [capa](r-layer.md)
* [configuración regional](r-locale.md)
* [mapa](r-map.md)
* [enmascarar](r-mask.md)
* [maskUse](r-maskuse.md)
* [red](r-network.md)
* [op_blur](r-op-blur.md)
* [op_bright](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grew](r-op-grow.md)
* [op_grewMask](r-op-growmask.md)
* [op_grewMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_sound](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opaco](r-opac.md)
* [origen](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectiva](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [cuantificar](r-is-http-quantize.md)
* [recto](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotar](r-rotate.md)
* [desconchar](r-is-http-scale.md)
* [scl](r-scl.md)
* [tamaño](r-size-reference.md)
* [src](r-src.md)
* [plantilla](r-template.md)
* [texto](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [tipo](r-type.md)
* [enredar](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
