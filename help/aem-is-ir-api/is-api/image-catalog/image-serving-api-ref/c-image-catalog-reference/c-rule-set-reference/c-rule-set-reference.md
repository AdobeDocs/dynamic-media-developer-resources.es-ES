---
description: El servicio de imágenes admite un mecanismo de preprocesamiento de solicitudes sencillo que se basa en reglas de coincidencia y sustitución de expresiones regulares.
solution: Experience Manager
title: Referencia del conjunto de reglas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Referencia del conjunto de reglas{#rule-set-reference}

El servicio de imágenes admite un mecanismo de preprocesamiento de solicitudes sencillo que se basa en reglas de coincidencia y sustitución de expresiones regulares.

Colecciones de reglas de preprocesamiento (*conjuntos de reglas*) se puede adjuntar a catálogos de imágenes o al catálogo predeterminado. Las reglas del catálogo predeterminado se aplican solo si la solicitud no identifica un catálogo de imágenes principal específico.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que las procese [!DNL Platform Server]El analizador de , incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular ciertas funciones de seguridad que normalmente se controlan únicamente con atributos de catálogo, como confusión de solicitudes, marcado de agua, así como para limitar el servicio a direcciones IP de cliente específicas.

Los conjuntos de reglas se almacenan como archivos de documento XML. La ruta relativa o absoluta del archivo del conjunto de reglas debe especificarse en `attribute::RuleSetFile`.

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

La variable `<?xml>` y `<ruleset>` los elementos siempre son necesarios en un archivo XML de conjunto de reglas válido, aunque no se hayan definido reglas reales.

One `<ruleset>` elemento que contiene cualquier número de `<rule>` están permitidos.

El contenido de los archivos de reglas de preprocesamiento distingue entre mayúsculas y minúsculas.

## Validación del conjunto de reglas {#section-d8d101a0b4d74580835e37d128d05567}

Una copia de [!DNL RuleSet.xsd] se proporciona en la carpeta del catálogo y debe utilizarse para validar un archivo del conjunto de reglas antes de registrarlo en el [!DNL catalog.ini] archivo. Tenga en cuenta que Image Serving utiliza una copia interna de [!DNL RuleSet.xsd] para validación.

## Procesamiento previo de URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Antes de cualquier otro procesamiento, se analiza parcialmente una solicitud HTTP entrante para determinar qué catálogo de imágenes debe aplicarse. Una vez identificado el catálogo, se aplica el conjunto de reglas para el catálogo seleccionado (o el catálogo predeterminado, si no se identificó ningún catálogo específico).

La variable `<rule>` se buscan los elementos en el orden especificado para que coincidan con el contenido del `<expression>` element ( *`expression`*).

Si `<rule>` coincide, la variable *`substitution`* se aplica y la cadena de solicitud modificada se pasa al analizador de solicitudes del servidor para el procesamiento normal.

Si no se realiza una coincidencia correcta al finalizar el `<ruleset>` se alcanza, la solicitud se pasa al analizador sin modificación.

## El atributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

El comportamiento predeterminado se puede modificar con la variable `OnMatch` del `<rule>` elemento. `OnMatch` se puede configurar como `break` (predeterminado), `continue`o `error`.

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
   <td> <p>El procesamiento de reglas se termina inmediatamente después de que se haya aplicado la sustitución de esta regla. Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>La sustitución se aplica y el procesamiento continúa con la siguiente regla. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>El procesamiento de reglas se termina inmediatamente y se devuelve al cliente un estado de respuesta "solicitud rechazada". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anulación de atributos de catálogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

La variable `rule` opcionalmente, puede definir atributos que anulan los atributos de catálogo correspondientes cuando la regla se encuentra correctamente coincidente. Si varias reglas coincidentes establecen el mismo atributo, prevalecerá el último. Consulte [regla](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) para obtener una lista de atributos que se pueden controlar con reglas.

## Expresiones regulares {#section-3f77bb9a265147b38c645f63ab1bad8b}

La coincidencia de cadenas simple funciona para aplicaciones muy básicas, pero en la mayoría de los casos se requieren expresiones regulares. Aunque las expresiones regulares son estándar en el sector, la implementación específica varía de una instancia a otra.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) describe la implementación de expresiones regulares específicas que utiliza Image Serving.

## Subcadenas capturadas {#section-066e659406d5403599cd26ae35e80d68}

Para facilitar modificaciones complejas de la URL, las subcadenas pueden capturarse en la expresión incluyendo la subcadena con paréntesis (...). Las subcadenas capturadas se numeran secuencialmente comenzando por 1 según la posición del paréntesis de apertura. Las subcadenas capturadas se pueden insertar en la sustitución utilizando ` $ *`n`*`, donde *`n`* es el número de secuencia de la subcadena capturada.

## Administración de archivos de conjuntos de reglas {#section-0598a608e4044bb4805fe93ceebe10a9}

Se puede adjuntar un archivo de conjunto de reglas a cada catálogo de imágenes con el atributo de catálogo `attribute::RuleSetFile`. Aunque puede editar el archivo del conjunto de reglas en cualquier momento, el servidor de imágenes reconoce los cambios solo cuando se vuelve a cargar el catálogo de imágenes asociado. Esta recarga se produce cuando se inicia o reinicia el servidor de la plataforma y siempre que el archivo de catálogo principal tenga un [!DNL .ini] para cambiar la fecha del archivo.

## Ejemplos {#section-aa769437d967459299b83a4bf34fe924}

**Ejemplo A.** Defina una regla que aumente la configuración de calidad de la imagen si el nombre de la imagen tiene el sufijo &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

La expresión de regla especifica una coincidencia de &quot; [!DNL _hg]&quot; al final de la cadena URL. El sufijo se sustituye por la cadena de consulta especificada que cambia la configuración de calidad de la imagen. Tenga en cuenta que `?` el carácter de la cadena de sustitución se escapa, ya que se trata de un carácter especial de las expresiones regulares.

>[!NOTE]
>
>La codificación necesaria para el carácter ampersand. Como alternativa, la cadena de sustitución podría incluirse en un bloque CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Ejemplo B.** Una aplicación web concreta no permite cadenas de consulta. Defina una regla que traduzca el elemento de ruta final `small`, `medium`o `large` a una plantilla, usando el resto de la ruta como nombre de la imagen. Por ejemplo, `myCat/myImage/small` traduciría a `myCat/smallTemplate?src=myCat/myImage`.

Se pueden utilizar subcadenas para reestructurar la solicitud:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Véase también {#section-9b748e7c5cff4759a70f96657bd43352}

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
