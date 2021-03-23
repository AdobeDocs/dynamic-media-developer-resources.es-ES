---
description: Referencia de la API de JavaScript para el visualizador de Video360.
seo-description: Referencia de la API de JavaScript para el visualizador de Video360.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: dd9cf899-8855-463b-a142-698fd1a650fe
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

Referencia de la API de JavaScript para el visualizador de Video360.

` setLocalizedTexts( *`localizationInfo`*)`

Define los valores de SYMBOL de localización para una o más configuraciones regionales. Se debe llamar a este parámetro antes de `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Objeto </span>} JSON con datos de localización. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario </a> para obtener más información. </p> <p>Consulte también la <i>Guía del usuario del SDK de visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

