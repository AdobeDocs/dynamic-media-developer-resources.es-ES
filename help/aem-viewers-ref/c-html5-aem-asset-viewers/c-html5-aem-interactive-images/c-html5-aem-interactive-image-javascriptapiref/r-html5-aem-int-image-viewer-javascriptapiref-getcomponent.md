---
description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-description: Referencia de la API de JavaScript para el visor de imágenes de vídeo.
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 6dd112f1-7b34-4d04-969e-b0cef46b4ad4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# getComponent{#getcomponent}

Referencia de la API de JavaScript para el visor de imágenes de vídeo.

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
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Cuando se trabaja con API de SDK, es importante utilizar la Área de nombres de SDK completa y correcta, tal como se describe en [Área de nombres de SDK de visor](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265).

Consulte la documentación de la API de Viewer SDK para obtener más información sobre un componente concreto.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` una referencia al componente SDK de visor. El método devuelve `null` si `componentId` no es un componente de visor admitido o si la lógica del visor aún no ha creado el componente.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

