---
description: nulo
seo-description: nulo
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación de clics/toques de doble para girar acciones. Si se establece en <span class="codeph"> ninguno </span> se deshabilita la opción de tocar o hacer clic en el doble. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen, se gira un paso de giro; CTRL+clic desplaza un paso de giro. Si se establece en <span class="codeph"> reset </span>, se hace un solo clic en la imagen para restablecer el giro al nivel de giro inicial. Para <span class="codeph"> zoomReset </span>, el restablecimiento se aplica si el factor de giro actual está en el límite especificado o por encima de él; de lo contrario, se aplica el giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`reset` en equipos de escritorio;  `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
