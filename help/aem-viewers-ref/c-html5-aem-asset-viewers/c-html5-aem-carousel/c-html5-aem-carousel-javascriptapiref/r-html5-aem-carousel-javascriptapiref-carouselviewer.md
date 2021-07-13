---
description: Referencia de la API de JavaScript para el visor de carrusel.
solution: Experience Manager
title: Visor de carrusel
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# Visor de carrusel{#carouselviewer}

Referencia de la API de JavaScript para el visor de carrusel.

`CarouselViewer([config])`

Constructor, crea una nueva instancia de visor de carrusel HTML 5.

## Parámetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} objeto de configuración JSON  </span> opcional, permite que todos los ajustes del visor pasen al constructor para evitar llamar a métodos de establecimiento individuales. Contiene las siguientes propiedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenedor DOM (normalmente un  <span class="codeph"> DIV  </span>) en el que se inserta el visor. Para cuando se llama a este método, no es necesario tener el elemento contenedor creado. Sin embargo, el contenedor debe existir cuando se ejecuta <span class="codeph"> init() </span>. </p> <p>Obligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object} objeto  </span> JSON con parámetros de configuración del visor en los que el nombre de propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. </p> <p>Obligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> controladores  </span> : objeto  <span class="codeph"> {Object}  </span> JSON con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. </p> <p>Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Llamadas de retorno de eventos </a> para obtener más información sobre los eventos del visor. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts  </span> -  <span class="codeph"> {Object}  </span> </p> <p> objeto JSON con datos de localización. Consulte Localización de elementos de la interfaz de usuario y el ejemplo para obtener más información sobre el contenido del objeto. </p> <p>Opcional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
