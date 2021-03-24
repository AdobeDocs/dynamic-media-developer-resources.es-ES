---
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Atributo de configuración para el visualizador de vídeo interactivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`precarga`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, todas las muestras se cargan simultáneamente cuando se inicializa el componente o se cambia el recurso. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, solo se cargan muestras visibles. </p> <p>Establézcalo en <span class="codeph"><span class="varname"> precarga</span></span> para definir cuántas filas/columnas invisibles alrededor del área visible están precargadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

