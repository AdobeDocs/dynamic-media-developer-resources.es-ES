---
description: Referencia de la API de JavaScript para el visualizador de Video360.
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: b0434886-defa-47d4-9853-bfd73c64d036
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '80'
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
