---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
TQID: 'https://experienceleague.adobe.com/VRC82qSYkgsI0ceaXdKtfGq-aYlw-Y0M-nRtq1pjg7A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 2%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`plantilla`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> plantilla</span></span> </p> </td> 
   <td> <p>Plantilla de contenido en la que se combinan los datos devueltos por el servidor de información. </p> <p>La plantilla de contenido es un XML que sigue esta DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>La sintaxis real de la plantilla de contenido es la siguiente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Es decir, la plantilla debe comenzar con el elemento <span class="codeph"> &lt;info&gt;</span> que puede contener elementos opcionales predeterminados <span class="codeph"> &lt;var&gt;</span>. El contenido de la plantilla en sí, <span class="codeph"> TEMPLATE_CONTENT</span> es texto de HTML. Además, la plantilla de contenido puede contener nombres de variables entre <span class="codeph"> $</span> caracteres. Estos caracteres se sustituyen por los valores de variable que devuelve el servidor de información o por los predeterminados. </p> <p>Las variables predeterminadas que se definen en la plantilla pueden ser globales (si no se ha establecido el atributo de rollover) o específicas de una clave de rollover determinada (si está presente el atributo de rollover). </p> <p>Durante el procesamiento de plantillas, las variables específicas para las claves de rollover tienen prioridad sobre las variables globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del Panel de información, el código HTML y el código JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código de JavaScript sean seguros.

## Propiedades {#section-6dd7785357d740d095fa9f7fd0f67da4}

Opcional.

## Predeterminado {#section-cd5db06d08aa4de49e37d6c938b41570}

Ninguno.

## Ejemplo {#section-16d184665c484964af9a22f79ff3f840}

Suponiendo que la respuesta del servidor de información devuelve el nombre del producto como variable `$1$` y que la dirección URL de la imagen del producto se devuelve como variable `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
