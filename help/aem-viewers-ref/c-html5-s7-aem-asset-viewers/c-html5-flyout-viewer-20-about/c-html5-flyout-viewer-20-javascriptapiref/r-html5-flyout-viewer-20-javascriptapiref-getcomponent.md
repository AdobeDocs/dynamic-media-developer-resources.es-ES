---
description: Referencia de la API de JavaScript para el visor flotante
seo-description: Referencia de la API de JavaScript para el visor flotante
seo-title: getComponent
solution: Experience Manager
title: getComponent
uuid: 039d5df8-e912-4868-8ae6-855617693797
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flotante
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---


# getComponent{#getcomponent}

Referencia de la API de JavaScript para el visor flotante

`getComponent(componentId)`

Devuelve una referencia al componente SDK de visor que utiliza el visor. La página web puede utilizar este método para ampliar o personalizar el comportamiento del visor integrado. Llame a este método solo después de que se haya ejecutado la llamada de retorno del visualizador `initComplete`; de lo contrario, es posible que la lógica del visor no cree aún el componente.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` :  `{String}` ID del componente SDK de visor utilizado por el visor. Este visor admite los siguientes ID de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre de clase del componente del SDK del visor </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenedor </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flotante  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> muestras  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Cuando se trabaja con API de SDK, es importante utilizar un espacio de nombres de SDK correcto y completo, tal como se describe en [Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-namespace.md#concept-453501a601634dd1bca7b96878c22605).

Consulte la documentación de la API del SDK de visor para obtener más información sobre un componente en particular.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` una referencia al componente SDK del visor. El método devuelve `null` si `componentId` no es un componente de visor compatible o si la lógica del visor aún no ha creado el componente.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```

