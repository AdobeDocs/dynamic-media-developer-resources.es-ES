---
title: Visor panorámico
description: Constructor, crea una instancia de visor panorámico HTML5.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---

# Visor panorámico{#panoramicviewer}

`PanoramicViewer([config])`
Constructor, crea una instancia de visor panorámico HTML5.

## Parámetro {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} objeto de configuración JSON opcional, permite pasar todas las configuraciones del visor al constructor y evitar llamar a métodos de establecedor individuales. Contiene las siguientes propiedades:

* containerId - {String} ID del contenedor DOM (normalmente un DIV) en el que se inserta el visor. No es necesario tener el elemento container creado para el momento en que se llama a este método, sin embargo el contenedor debe existir cuando se ejecuta init(). Obligatorio
* parámetros - {Object} Objeto JSON con parámetros de configuración del visor donde el nombre de la propiedad es una opción de configuración específica del visor o un modificador del SDK y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio
* controladores - {Object} Objeto JSON con llamadas de retorno a evento de visor, donde el nombre de propiedad es el nombre del evento de visor admitido y el valor de propiedad es una referencia de función de JavaScript a la llamada de retorno adecuada. Consulte la sección Llamadas de retorno de eventos para obtener más información sobre los eventos de visor. Opcional.


## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
