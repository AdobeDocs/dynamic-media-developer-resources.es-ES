---
description: El procesamiento de imágenes admite un mecanismo de preprocesamiento de solicitudes simple que se basa en reglas de coincidencia y sustitución de expresiones regulares.
solution: Experience Manager
title: Referencia del conjunto de reglas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Referencia del conjunto de reglas{#rule-set-reference}

El procesamiento de imágenes admite un mecanismo de preprocesamiento de solicitudes simple que se basa en reglas de coincidencia y sustitución de expresiones regulares.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Las colecciones de reglas de preprocesamiento (*conjuntos de reglas*) se pueden adjuntar a los catálogos de materiales o al catálogo predeterminado. Las reglas del catálogo predeterminado se aplican únicamente si la solicitud no adjunta un catálogo de materiales específico.

Las reglas de preprocesamiento de solicitudes pueden modificar las partes de la ruta y la consulta de las solicitudes antes de que las procese el analizador de solicitudes del servidor, lo que incluye la manipulación de la ruta, la adición de comandos, el cambio de los valores de los comandos y la aplicación de plantillas o macros. Las reglas también se pueden utilizar para configurar y anular algunos atributos de catálogo, así como para limitar el servicio a direcciones IP de cliente específicas.

Los conjuntos de reglas se almacenan como archivos de documento XML. La ruta de acceso relativa o absoluta del archivo del conjunto de reglas debe especificarse en `attribute::RuleSetFile`.

## Estructura general {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

Los elementos `<?xml>`, `<!DOCTYPE>` y `<ruleset>` siempre son necesarios en un archivo XML de conjunto de reglas válido, incluso si no se han definido reglas reales.

Se permite un elemento `<ruleset>` que contenga cualquier número de elementos `<rule>`.

El contenido de los archivos de reglas de preprocesamiento distingue entre mayúsculas y minúsculas.

## Preprocesamiento de URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Antes de cualquier otro procesamiento, se analiza parcialmente una solicitud HTTP entrante para determinar qué catálogo de materiales se debe aplicar. Una vez identificado el catálogo, se aplica el conjunto de reglas del catálogo seleccionado (o el catálogo predeterminado, si no se ha identificado ningún catálogo específico).

Los elementos `<rule>` se buscan en el orden especificado para una coincidencia con el contenido del elemento `<expression>` ( *`expression`*).

Si coincide un `<rule>`, se aplica el *`substitution`* opcional y la cadena de solicitud modificada se pasa al analizador de solicitudes del servidor para su procesamiento normal.

Si no se realiza ninguna coincidencia correcta cuando se llega al final de `<ruleset>`, la solicitud se pasa al analizador sin realizar modificaciones.

## El atributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

El comportamiento predeterminado se puede modificar con el atributo `OnMatch` de los elementos `<rule>`. `OnMatch` se puede establecer en `break` (predeterminado), `continue` o `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento y atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Comportamiento cuando se produce una coincidencia </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>El procesamiento de reglas finaliza inmediatamente después de aplicar la sustitución de esta regla. Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La sustitución se aplica y el procesamiento continúa con la siguiente regla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>El procesamiento de reglas finaliza inmediatamente y se devuelve al cliente el estado de respuesta "solicitud rechazada". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anulación de atributos de catálogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` elementos pueden definir opcionalmente atributos que anulan los atributos de catálogo correspondientes cuando la regla coincide correctamente y `OnMatch="break"` está establecido. No se aplica ningún atributo si se establece `OnMatch="continue"`. Consulte la descripción de `<rule>` para obtener una lista de atributos que se pueden controlar con reglas.

## Expresiones regulares {#section-4d326507b52544b0960a9a5f303e3fe6}

La coincidencia de cadenas simple funciona para aplicaciones muy básicas, pero en la mayoría de los casos se requieren expresiones regulares. Aunque las expresiones regulares son estándares del sector, la implementación específica varía según la instancia.

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) describe la implementación de expresión regular específica que usa el servicio de imágenes.

## Subcadenas capturadas {#section-8057cd65d48949ffb6a50e929bd3688b}

Para facilitar las modificaciones complejas de las direcciones URL, se pueden capturar subcadenas en la expresión incluyendo la subcadena entre paréntesis (...). Las subcadenas capturadas se numeran secuencialmente empezando por 1 según la posición del paréntesis de apertura. Las subcadenas capturadas se pueden insertar en la sustitución utilizando *`$n`*, donde *`n`* es el número de secuencia de la subcadena capturada.

## Administración de archivos de conjunto de reglas {#section-e8ce976b56404c009496426fd334d23d}

Se puede adjuntar un archivo de conjunto de reglas a cada catálogo de materiales con el atributo de catálogo `attribute::RuleSetFile`. Aunque puede editar el archivo del conjunto de reglas en cualquier momento, el servidor de imágenes reconoce los cambios únicamente cuando se vuelve a cargar el catálogo de materiales asociado. Esto sucede cuando se inicia o reinicia [!DNL Platform Server] y siempre que el archivo de catálogo principal (que tiene un sufijo de archivo [!DNL .ini]) se modifica o &#39;toca&#39; (para cambiar la fecha del archivo).

## Ejemplos {#section-c4142a41f5cd4ff799a72fbc130c3700}

Se proporcionan ejemplos de conjuntos de reglas en la sección correspondiente de Referencia del catálogo de imágenes en la documentación del servicio de imágenes.

## Véase también {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
