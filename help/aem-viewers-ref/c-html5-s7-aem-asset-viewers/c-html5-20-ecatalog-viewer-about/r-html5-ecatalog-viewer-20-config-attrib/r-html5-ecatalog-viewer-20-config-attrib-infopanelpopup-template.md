---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`plantilla`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> plantilla</span></span> </p> </td> 
   <td> <p>Plantilla de contenido en la que se combinan los datos devueltos por el servidor de información. </p> <p>La plantilla de contenido es un XML que sigue esta DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>La sintaxis real de la plantilla de contenido es la siguiente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Es decir, la plantilla debe comenzar con <span class="codeph"> &lt;info&gt;</span> elemento que puede contener opción predeterminada <span class="codeph"> &lt;var&gt;</span> elementos. El contenido de la plantilla, <span class="codeph"> TEMPLATE_CONTENT</span> es texto de HTML. Además, la plantilla de contenido puede contener nombres de variables incluidos en <span class="codeph"> $</span> caracteres que se sustituyen por los valores de variable que devuelve el servidor de información o por los predeterminados. </p> <p>Las variables predeterminadas que se definen en la plantilla pueden ser globales (si no se ha establecido el atributo de rollover) o específicas de una clave de rollover determinada (si está presente el atributo de rollover). </p> <p>Durante el procesamiento de plantillas, las variables específicas para las claves de rollover tienen prioridad sobre las variables globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cuando se configura la ventana emergente del Panel de información, el código de HTML y el código JavaScript que se pasan al Panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código de HTML y código JavaScript sean seguros.

## Propiedades {#section-6dd7785357d740d095fa9f7fd0f67da4}

Opcional.

## Predeterminado {#section-cd5db06d08aa4de49e37d6c938b41570}

Ninguno.

## Ejemplo {#section-16d184665c484964af9a22f79ff3f840}

Suponiendo que la respuesta del servidor de información devuelve el nombre del producto como variable `$1$` y la URL de la imagen del producto se devuelve como variable `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
