---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ninguno|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la asignación del doble clic/toque para acciones de zoom. Si se establece en <span class="codeph"> none </span>, se deshabilita el zoom de doble clic/toque. Si se establece en <span class="codeph">, el zoom </span> al hacer clic en la imagen se amplía un paso de zoom; CTRL y clic reduce un paso de zoom. Si se establece en <span class="codeph"> reset </span>, con un solo clic en la imagen se restablecerá el zoom al nivel inicial de zoom. Para <span class="codeph"> zoomReset </span>, se aplica reset si el factor de zoom actual está en el límite especificado o por encima de este; de lo contrario, se aplica zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Opcional.

## Predeterminado {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] en equipos de escritorio; [!DNL `zoomReset`] en dispositivos táctiles.

## Ejemplo {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
