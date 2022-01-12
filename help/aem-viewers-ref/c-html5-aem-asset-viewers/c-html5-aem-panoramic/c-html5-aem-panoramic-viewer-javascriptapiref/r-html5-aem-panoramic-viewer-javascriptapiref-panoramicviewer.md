---
title: Visor panorámico
description: Constructor, crea una nueva instancia de Visor de carrusel de HTML5.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---

# Visor panorámico{#panoramicviewer}

`PanoramicViewer([config])`
Constructor, crea una nueva instancia de Visor panorámico de HTML5.

## Parámetro {#section-fa807db629ce43bab286b1e1dc96c492}

config {Object} objeto de configuración JSON opcional, permite pasar todos los ajustes del visor al constructor y evitar llamar a métodos de establecedor individuales. Contiene las siguientes propiedades:
* containerId - {String} ID del contenedor DOM (normalmente un DIV) en el que se inserta el visor. No es necesario tener el elemento contenedor creado para cuando se llama a este método, pero el contenedor debe existir cuando se ejecuta init() . Obligatorio
* params : objeto JSON {Object} con parámetros de configuración del visor en el que el nombre de la propiedad es una opción de configuración específica del visor o un modificador SDK, y el valor de esa propiedad es un valor de configuración correspondiente. Obligatorio
* controladores: objeto JSON {Object} con llamadas de retorno de eventos del visor, donde el nombre de la propiedad es el nombre del evento del visor admitido y el valor de la propiedad es una referencia de función JavaScript a una llamada de retorno adecuada. Consulte la sección Llamadas de retorno de eventos para obtener más información sobre los eventos del visor. Opcional


## Devuelve {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Ninguno.

## Ejemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
