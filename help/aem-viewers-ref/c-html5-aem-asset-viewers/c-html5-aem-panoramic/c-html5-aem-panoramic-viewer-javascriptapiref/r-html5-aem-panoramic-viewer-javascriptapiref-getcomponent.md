---
title: getComponent
description: Referencia de la API de JavaScript para el visor panorámico.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
autotag-review: '2026-05-13T22:09:12.361Z'
TQID: 'https://experienceleague.adobe.com/6tWQNhwyzc-PV8TLegYBXSzAYEMkVKyvGCu5BDv2uIo'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# getComponent{#getcomponent}

Referencia de la API de JavaScript para el visor panorámico

`getComponent(componentId)`


Devuelve una referencia al componente de SDK del visor que utiliza el visor. La página web puede utilizar este método para ampliar o personalizar el comportamiento del visualizador integrado. Llame a este método únicamente después de que se haya ejecutado la devolución de llamada del visor `initComplete`; de lo contrario, es posible que la lógica del visor aún no haya creado el componente.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` es un ID del componente de SDK de visor que usa el visor. Este visor es compatible con los siguientes ID de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID de componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nombre de clase de componente de visor SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenedor </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vista panorámica </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Al trabajar con las API de SDK, es importante usar el espacio de nombres de SDK correcto y completo, tal como se describe en [Espacio de nombres de SDK de visor](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Consulte la documentación de la API de Viewer SDK para obtener más información sobre un componente en particular.

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` una referencia al componente SDK de visor. El método devuelve `null` si `componentId` no es un componente de visor compatible o si la lógica del visor aún no ha creado el componente.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
