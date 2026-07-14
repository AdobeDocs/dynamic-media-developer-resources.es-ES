---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2669c8e2-c942-420f-8262-9d76d5c499a2
TQID: 'https://experienceleague.adobe.com/aO-r0pyOX-Qv8OA1B6mqXHDl34kjZXqwPTlV7rU0fAA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 119
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`]

Controla la apariencia del componente cuando un(a) [!DNL `PageView.frametransition`] se establece en [!DNL `turn`] o en [!DNL `auto`] en sistemas de escritorio.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Ancho en píxeles de la sombra divisoria de página que separa las páginas izquierda y derecha del pliego. También controla el ancho de la sombra que se muestra junto a la página de paso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> El color de sombra en formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>Opacidad de la sombra en el intervalo de <span class="codeph"> 0</span> a <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> El marcador (<span class="codeph"> 0</span> o <span class="codeph"> 1</span>) que activa y desactiva el borde alrededor de la página de activación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> El color del borde en formato RRGGBB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Color del relleno sólido del área de componentes utilizado durante la animación de paso de página, en formato RRGGBB. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-54c634116cfe4f17813318e07539264c}

Opcional.

## Predeterminado {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## Ejemplos {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]

