---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
TQID: 'https://experienceleague.adobe.com/Bu8BmcQExGK8nex2r9blfXn3p-gV0r8A4t13ILy2c5Y'
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

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en acciones de zoom. Si se establece en <span class="codeph"> none </span>, se deshabilita el zoom de un solo clic/toque. Si se establece en <span class="codeph">, el zoom </span> al hacer clic en la imagen se amplía un paso de zoom; CTRL y clic reduce un paso de zoom. Si se establece en <span class="codeph"> reset </span>, con un solo clic en la imagen se restablecerá el zoom al nivel inicial de zoom. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de zoom actual está en el límite especificado o por encima de este; de lo contrario, se aplica zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Predeterminado {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` en equipos de escritorio; `none` en dispositivos táctiles.

## Ejemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
