---
description: Referencia de la API de JavaScript para el visor de vídeos.
seo-description: Referencia de la API de JavaScript para el visor de vídeos.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: c87e9f32-59f9-4f7a-a2cb-89813c00524b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setLocalizedTexts{#setlocalizedtexts}

Referencia de la API de JavaScript para el visor de vídeos.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto JSON {<span class="codeph"> Object</span>} con datos de localización. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario</a> para obtener más información. </p> <p>Consulte también la <i>Guía del usuario del SDK del visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Establece los valores de SÍMBOLO de localización para una o varias configuraciones regionales. Se debe llamar a este parámetro antes de `init()`.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

