---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
TQID: 'https://experienceleague.adobe.com/RzYRPsMpjXnUZtayjQNF52QgGU8Mz0nHm4ZDDT37d1Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del doble clic/toque para las acciones de giro. Si se establece en <span class="codeph"> none </span>, se deshabilita el giro de doble clic/toque. Si se establece en <span class="codeph"> zoom </span>, al hacer clic en la imagen, se gira en un paso de giro; CTRL y clic gira un paso de giro. Si se establece en <span class="codeph">, restablecer </span>, con un solo clic en la imagen se restablecerá el giro al nivel inicial de giro. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de giro actual está en el límite especificado o por encima de este; de lo contrario, se aplica el giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Predeterminado {#section-7a2128fd488941948aff18421f533ccf}

`reset` en equipos de escritorio; `zoomReset` en dispositivos táctiles.

## Ejemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
