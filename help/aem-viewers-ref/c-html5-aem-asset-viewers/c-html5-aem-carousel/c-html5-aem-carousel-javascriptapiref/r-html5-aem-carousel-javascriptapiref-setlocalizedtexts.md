---
description: Referencia de la API de JavaScript para el visor de carrusel.
seo-description: Referencia de la API de JavaScript para el visor de carrusel.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setLocalizedTexts{#setlocalizedtexts}

Referencia de la API de JavaScript para el visor de carrusel.

` setLocalizedTexts( *`localizationInfo`*)`

Establece los valores de SÍMBOLO de localización para una o varias configuraciones regionales. Se debe llamar a este parámetro antes de `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto JSON {<span class="codeph"> Object</span>} con datos de localización. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario</a> para obtener más información. </p> <p>Consulte también la <i>Guía del usuario del SDK del visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte también [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

