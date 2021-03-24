---
description: Referencia de la API de JavaScript para el visualizador de giros.
solution: Experience Manager
title: setLocalizedTexts
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---


# setLocalizedTexts{#setlocalizedtexts}

Referencia de la API de JavaScript para el visualizador de giros.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto JSON {<span class="codeph"></span>} con datos de localización. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localización de los elementos de la interfaz de usuario</a> para obtener más información. </p> <p>Consulte también la <i>Guía del usuario del SDK de visor</i> y el ejemplo para obtener más información sobre el contenido del objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define los valores de SYMBOL de localización para una o más configuraciones regionales. Se debe llamar a este parámetro antes de `init()`.

Consulte también [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

