---
description: Referencia de la API de JavaScript para el visor de giros
seo-description: Referencia de la API de JavaScript para el visor de giros
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic Media
uuid: c7585cd5-6a95-43b1-8f68-c1eba868164c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# getComponent{#getcomponent}

Referencia de la API de JavaScript para el visor de giros

`getComponent(componentId)`

Devuelve una referencia al componente SDK de visor que utiliza el visor. La página web puede utilizar este método para ampliar o personalizar el comportamiento del visor incorporado. Llame a este método solo después de que se haya ejecutado la llamada de retorno del visor `initComplete`; de lo contrario, es posible que el componente no se haya creado aún mediante la lógica del visor.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` :  `{String}` ID del componente SDK de visor que utiliza el visor. Este visor admite los siguientes ID de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID del componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre de clase de componente del SDK de visor </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenedor </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Contenedor  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SpinView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinLeftButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spinRightButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Al trabajar con API de SDK, es importante utilizar una Área de nombres de SDK correcta y completa, tal como se describe en [SDK de visor](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-namespace.md#concept-fa293878c9ff4758ae888415c70fbeef).

Consulte la documentación de la API de Viewer SDK para obtener más información sobre un componente concreto.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` una referencia al componente SDK de visor. El método devuelve `null` si `componentId` no es un componente de visor admitido o si la lógica del visor aún no ha creado el componente.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var spinView = <instance>.getComponent("spinView"); 
} 
})
```

