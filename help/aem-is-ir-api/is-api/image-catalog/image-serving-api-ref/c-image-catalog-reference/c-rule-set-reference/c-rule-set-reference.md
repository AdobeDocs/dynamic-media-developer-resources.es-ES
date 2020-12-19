---
description: El servicio de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-description: El servicio de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-title: Referencia de conjunto de reglas
solution: Experience Manager
title: Referencia de conjunto de reglas
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 0%

---


# Referencia del conjunto de reglas{#rule-set-reference}

El servicio de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.

Las colecciones de reglas de preprocesamiento (*conjuntos de reglas*) se pueden adjuntar a catálogos de imágenes o al catálogo predeterminado. Las reglas del catálogo predeterminado solo se aplican si la solicitud no identifica un catálogo de imágenes principal específico.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que el analizador de Platform Server las procese, incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente se controlan únicamente con atributos de catálogo, como confusión de solicitudes, marcado de agua, así como limitar el servicio a direcciones IP de clientes específicas.

Los conjuntos de reglas se almacenan como archivos documento XML. La ruta relativa o absoluta del archivo del conjunto de reglas debe especificarse en `attribute::RuleSetFile`.

## Estructura general {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Los elementos `<?xml>` y `<ruleset>` siempre son obligatorios en un archivo XML de conjunto de reglas válido, aunque no se hayan definido reglas reales.

Se permite un elemento `<ruleset>` que contenga cualquier número de elementos `<rule>`.

El contenido de los archivos de reglas de preprocesamiento distingue entre mayúsculas y minúsculas.

## Validación de conjunto de reglas {#section-d8d101a0b4d74580835e37d128d05567}

Se proporciona una copia de [!DNL RuleSet.xsd] en la carpeta del catálogo y debe utilizarse para validar un archivo de conjunto de reglas antes de registrarlo en el archivo [!DNL catalog.ini]. Tenga en cuenta que el servicio de imágenes utiliza una copia interna de [!DNL RuleSet.xsd] para la validación.

## Preprocesamiento de URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Antes de cualquier otro procesamiento, una solicitud HTTP entrante se analiza parcialmente para determinar qué catálogo de imágenes debe aplicarse. Una vez identificado el catálogo, se aplica el conjunto de reglas para el catálogo seleccionado (o el catálogo predeterminado, si no se ha identificado ningún catálogo específico).

Los elementos `<rule>` se buscan en el orden especificado para una coincidencia con el contenido del elemento `<expression>` ( *`expression`*).

Si coincide con un `<rule>`, se aplica el *`substitution`* opcional y la cadena de solicitud modificada se pasa al analizador de solicitudes del servidor para un procesamiento normal.

Si no se realiza una coincidencia correcta cuando se llega al final del `<ruleset>`, la solicitud se pasa al analizador sin ninguna modificación.

## El atributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

El comportamiento predeterminado se puede modificar con el atributo `OnMatch` del elemento `<rule>`. `OnMatch` se puede establecer en  `break` (predeterminado),  `continue`o  `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elemento y atributo</b> </th> 
   <th class="entry"> <b>Comportamiento cuando se produce una coincidencia</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>El procesamiento de reglas finaliza inmediatamente después de que se haya aplicado la sustitución de esta regla. Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La sustitución se aplica y el procesamiento continúa con la siguiente regla. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>El procesamiento de reglas finaliza inmediatamente y se devuelve al cliente el estado de respuesta "solicitud rechazada". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anulando atributos de catálogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` opcionalmente, los elementos pueden definir atributos que anulan los atributos de catálogo correspondientes cuando la regla se coincide correctamente. Si varias reglas coincidentes establecen el mismo atributo, prevalecerá el último. Consulte la descripción del elemento ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` para obtener una lista de atributos que se pueden controlar con reglas.

## Expresiones regulares {#section-3f77bb9a265147b38c645f63ab1bad8b}

La coincidencia simple de cadenas funciona para aplicaciones muy básicas, pero en la mayoría de los casos se requieren expresiones regulares. Aunque las expresiones regulares son estándar del sector, la implementación específica varía de una instancia a otra.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) describe la implementación de expresión regular específica utilizada por el servicio de imágenes.

## Subcadenas capturadas {#section-066e659406d5403599cd26ae35e80d68}

Para facilitar las modificaciones de direcciones URL complejas, las subcadenas se pueden capturar en la expresión rodeando la subcadena con paréntesis (...). Las subcadenas capturadas se numeran secuencialmente comenzando por 1 según la posición del paréntesis inicial. Las subcadenas capturadas se pueden insertar en la sustitución mediante ` $ *`n`*`, donde *`n`* es el número de secuencia de la subcadena capturada.

## Administración de archivos de conjunto de reglas {#section-0598a608e4044bb4805fe93ceebe10a9}

Se puede adjuntar un archivo de conjunto de reglas a cada catálogo de imágenes con el atributo de catálogo `attribute::RuleSetFile`. Aunque puede editar el archivo del conjunto de reglas en cualquier momento, el servidor de imágenes solo reconoce los cambios cuando se vuelve a cargar el catálogo de imágenes asociado. Esta recarga se produce cuando se inicia o reinicia el servidor de la plataforma y cuando se modifica o &quot;toca&quot; el archivo de catálogo principal, que tiene un sufijo de archivo [!DNL .ini], para cambiar la fecha del archivo.

## Ejemplos {#section-aa769437d967459299b83a4bf34fe924}

**Ejemplo A.** Defina una regla que aumente la configuración de calidad de imagen si el nombre de la imagen tiene el sufijo &quot;  [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

La expresión de regla especifica una coincidencia sin distinción de mayúsculas y minúsculas de &quot; [!DNL _hg]&quot; al final de la cadena URL. El sufijo se sustituye por la cadena de consulta especificada que cambia la configuración de calidad de imagen. Tenga en cuenta que el carácter `?` de la cadena de sustitución se escapa, ya que es un carácter especial en expresiones regulares.

>[!NOTE]
>
>Codificación necesaria para el carácter de símbolo de unión. De forma alternativa, la cadena de sustitución se podría incluir en un bloque CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Ejemplo B.** Una aplicación web en particular no permite cadenas de consulta. Defina una regla que traduzca el elemento de ruta final `small`, `medium` o `large` a una plantilla, utilizando el resto de la ruta como nombre de la imagen. Por ejemplo, `myCat/myImage/small` se traduciría a `myCat/smallTemplate?src=myCat/myImage`.

Se pueden usar subcadenas para reestructurar la solicitud:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Véase también {#section-9b748e7c5cff4759a70f96657bd43352}

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
