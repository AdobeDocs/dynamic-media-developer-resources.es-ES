---
description: Ajustar la saturación. Cambia la saturación de cada píxel visible de la capa o imagen compuesta.
seo-description: Ajustar la saturación. Cambia la saturación de cada píxel visible de la capa o imagen compuesta.
seo-title: op_saturation
solution: Experience Manager
title: op_saturation
uuid: 5e987841-0c3b-4f68-96b1-fad8757f3402
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---


# op_saturation{#op-saturation}

Ajustar la saturación. Cambia la saturación de cada píxel visible de la capa o imagen compuesta.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajuste de saturación (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` desatura completamente la imagen.

## Propiedades {#section-9a3cc9ff060049449554dfa69d92fd53}

Capa. Se aplica a la capa actual o a la imagen compuesta si `layer=comp`. Ignorado por capas de efecto.

## Predeterminado {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, sin ningún cambio en la saturación. Las imágenes o capas CMYK se convierten a RGB antes de aplicar la operación.

## Ejemplo {#section-033b272f1b7e4efeb94e841fd8095357}

Manipule una fotografía en color para conseguir un aspecto &quot;de gran nitidez&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
