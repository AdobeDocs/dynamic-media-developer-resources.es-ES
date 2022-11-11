---
description: El procesamiento de imágenes admite un mecanismo de preprocesamiento de solicitud simple que se basa en reglas de sustitución y coincidencia de expresiones regulares.
solution: Experience Manager
title: Referencia del conjunto de reglas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Referencia del conjunto de reglas{#rule-set-reference}

El procesamiento de imágenes admite un mecanismo de preprocesamiento de solicitud simple que se basa en reglas de sustitución y coincidencia de expresiones regulares.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Colecciones de reglas de preprocesamiento (*conjuntos de reglas*) se puede adjuntar a catálogos de material o al catálogo predeterminado. Las reglas del catálogo predeterminado se aplican solo si la solicitud no adjunta un catálogo de materiales específico.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que las procese el analizador de solicitudes del servidor, incluida la manipulación de la ruta, la adición de comandos, la modificación de los valores de los comandos y la aplicación de plantillas o macros. También se pueden utilizar reglas para configurar y anular algunos atributos de catálogo, así como para limitar el servicio a direcciones IP de cliente específicas.

Los conjuntos de reglas se almacenan como archivos de documento XML. La ruta relativa o absoluta del archivo del conjunto de reglas debe especificarse en `attribute::RuleSetFile`.

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

La variable `<?xml>`, `<!DOCTYPE>` y `<ruleset>` los elementos siempre son necesarios en un archivo XML de conjunto de reglas válido, aunque no se hayan definido reglas reales.

One `<ruleset>` elemento que contiene cualquier número de `<rule>` están permitidos.

El contenido de los archivos de reglas de preprocesamiento distingue entre mayúsculas y minúsculas.

## Procesamiento previo de URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Antes de cualquier otro procesamiento, se analiza parcialmente una solicitud HTTP entrante para determinar qué catálogo de materiales debe aplicarse. Una vez identificado el catálogo, se aplica el conjunto de reglas para el catálogo seleccionado (o el catálogo predeterminado, si no se identificó ningún catálogo específico).

La variable `<rule>` se buscan los elementos en el orden especificado para que coincidan con el contenido del `<expression>` element ( *`expression`*).

Si `<rule>` coincide, la variable *`substitution`* se aplica y la cadena de solicitud modificada se pasa al analizador de solicitudes del servidor para el procesamiento normal.

Si no se realiza una coincidencia correcta al finalizar el `<ruleset>` se alcanza, la solicitud se pasa al analizador sin modificación.

## El atributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

El comportamiento predeterminado se puede modificar con la variable `OnMatch` del `<rule>` elementos. `OnMatch` se puede configurar como `break` (predeterminado), `continue`o `error.`

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
   <td colname="col2"> <p>El procesamiento de reglas se termina inmediatamente después de que se haya aplicado la sustitución de esta regla. Predeterminado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>La sustitución se aplica y el procesamiento continúa con la siguiente regla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>El procesamiento de reglas se termina inmediatamente y se devuelve al cliente un estado de respuesta "solicitud rechazada". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anulación de atributos de catálogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` Los elementos pueden definir, opcionalmente, atributos que anulan los atributos de catálogo correspondientes cuando la regla se encuentra correctamente coincidente y `OnMatch="break"` está configurado. No se aplican atributos si `OnMatch="continue"` está configurado. Consulte la descripción de `<rule>` para obtener una lista de atributos que se pueden controlar con reglas.

## Expresiones regulares {#section-4d326507b52544b0960a9a5f303e3fe6}

La coincidencia de cadenas simple funciona para aplicaciones muy básicas, pero en la mayoría de los casos se requieren expresiones regulares. Aunque las expresiones regulares son estándar en el sector, la implementación específica varía de una instancia a otra.

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) describe la implementación de expresiones regulares específicas que utiliza Image Serving.

## Subcadenas capturadas {#section-8057cd65d48949ffb6a50e929bd3688b}

Para facilitar modificaciones complejas de la URL, las subcadenas pueden capturarse en la expresión incluyendo la subcadena con paréntesis (...). Las subcadenas capturadas se numeran secuencialmente comenzando por 1 según la posición del paréntesis de apertura. Las subcadenas capturadas se pueden insertar en la sustitución utilizando *`$n`*, donde *`n`* es el número de secuencia de la subcadena capturada.

## Administración de archivos de conjuntos de reglas {#section-e8ce976b56404c009496426fd334d23d}

Se puede adjuntar un archivo de conjunto de reglas a cada catálogo de materiales con el atributo de catálogo `attribute::RuleSetFile`. Aunque puede editar el archivo del conjunto de reglas en cualquier momento, el servidor de imágenes reconoce los cambios solo cuando se vuelve a cargar el catálogo de materiales asociado. Esto sucede cuando la variable [!DNL Platform Server] se inicia o reinicia, y siempre que el archivo de catálogo principal (que tiene un [!DNL .ini] sufijo de archivo) se modifica o se modifica (para cambiar la fecha del archivo).

## Ejemplos {#section-c4142a41f5cd4ff799a72fbc130c3700}

Se proporcionan ejemplos de conjuntos de reglas en la sección correspondiente de la Referencia del catálogo de imágenes en la documentación del servicio de imágenes.

## Véase también {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
