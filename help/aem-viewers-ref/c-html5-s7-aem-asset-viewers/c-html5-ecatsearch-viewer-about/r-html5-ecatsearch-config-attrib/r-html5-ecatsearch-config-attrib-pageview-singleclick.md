---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del clic/toque en acciones de zoom. Estableciendo en <span class="codeph"> ninguno </span> desactiva el zoom de un solo clic/toque. Si se establece en <span class="codeph"> zoom </span> al hacer clic en la imagen, se amplía un paso de zoom; CTRL y clic reduce un paso de zoom. Estableciendo en <span class="codeph"> restablecer </span> hace que un solo clic en la imagen restablezca el zoom al nivel inicial. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de zoom actual está en el límite especificado o por encima de él; de lo contrario, se aplica zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-edcfcd6c0bd24ac093442c56450b3c97}

Opcional.

## Predeterminado {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] en equipos de escritorio; [!DNL `none`] en dispositivos táctiles.

## Ejemplo {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
