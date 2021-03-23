---
description: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
uuid: 791164a1-93fa-411f-9fb8-f78efb96f16b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de giros
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> La cadena de comando del Servidor de imágenes que se aplica a la imagen de giro. Si se especifica en la dirección URL, todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben codificarse con HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota:  No se admiten los comandos de manipulación del tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

Ninguno.

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Cuando se especifique en la dirección URL del visor:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
