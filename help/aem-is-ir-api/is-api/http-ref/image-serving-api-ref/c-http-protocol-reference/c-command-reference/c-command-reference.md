---
description: Esta sección describe los comandos del protocolo HTTP.
seo-description: Esta sección describe los comandos del protocolo HTTP.
seo-title: Referencia de comandos
solution: Experience Manager
title: Referencia de comandos
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f

---


# Referencia de comandos{#command-reference}

Esta sección describe los comandos del protocolo HTTP.

**Solo** para Dynamic Media en AEM: Más allá de los ajustes de imagen básicos disponibles en la interfaz de usuario, [!DNL Dynamic Media] en AEM ( [!DNL Adobe Experience Manager]) admite numerosas modificaciones de imagen avanzadas que se pueden especificar en el campo Modificadores **de** imagen. Estos parámetros se definen a continuación. Sin embargo, tenga en cuenta que las siguientes funciones no son compatibles con Dynamic Media en AEM.

* Comandos de corrección de color: `icc=` y `iccEmbed=`.
* Comandos básicos de creación de plantillas y procesamiento de texto: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` y `textPs=`.
* Comandos de Localización: `locale=` y `req=xlate`.
* `req=set` no está disponible para uso general.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Servicios de Dynamic Media no principales: SVG, procesamiento de imágenes e impresión virtual.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulte también Opciones [de ajustes preestablecidos de](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) imagen de Dynamic Media en la documentación de AEM 6.5.

* [align](r-align.md)
* [delimitador](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [caché](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [recorte](r-crop.md)
* [cutPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [efecto](r-effect.md)
* [effectMask](r-effectmask.md)
* [extender](r-extend.md)
* [Ajuste](r-fit.md)
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
* [locale](r-locale.md)
* [mapa](r-map.md)
* [máscara](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_bright](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_compare](r-op-contrast.md)
* [op_Growth](r-op-grow.md)
* [op_GrowthMask](r-op-growmask.md)
* [op_GrowthMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_sound](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origen](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectiva](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [cuantificar](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
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
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
