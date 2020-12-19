---
description: nulo
seo-description: nulo
seo-title: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: c7063907-78e8-47f8-9424-78ab9d123ad1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`plantilla`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> plantilla</span></span> </p> </td> 
   <td> <p>Plantilla de contenido en la que se combinan los datos devueltos por el servidor de información. </p> <p>La plantilla de contenido es un XML que sigue a este DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>La sintaxis real de la plantilla de contenido es la siguiente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Es decir, la plantilla debe estar en inicio con el elemento <span class="codeph"> &lt;info&gt;</span> que puede contener elementos <span class="codeph"> &lt;var&gt;</span> predeterminados opcionales. El contenido de la plantilla en sí, <span class="codeph"> TEMPLATE_CONTENT</span> es texto HTML. Además, la plantilla de contenido puede contener nombres de variables entre <span class="codeph"> $</span> caracteres que se reemplazan por los valores de variable que devuelve el servidor de información o por los predeterminados. </p> <p>Las variables predeterminadas que se definen en la plantilla pueden ser globales (si no se ha establecido el atributo rollover) o específicas de una determinada clave de rollover (si el atributo rollover está presente). </p> <p>Durante el procesamiento de plantillas, las variables específicas para pasar sobre las claves tienen prioridad sobre las variables globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tenga en cuenta que, al configurar la ventana emergente del panel de información, el código HTML y el código JavaScript que se pasan al panel de información se ejecutan en el equipo del cliente. Por lo tanto, asegúrese de que dicho código HTML y código JavaScript sean seguros.

## Propiedades {#section-6dd7785357d740d095fa9f7fd0f67da4}

Opcional.

## Predeterminado {#section-cd5db06d08aa4de49e37d6c938b41570}

Ninguno.

## Ejemplo {#section-16d184665c484964af9a22f79ff3f840}

Suponiendo que la respuesta del servidor de información devuelve el nombre del producto como variable `$1$` y que la dirección URL de la imagen del producto se devuelve como variable `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
