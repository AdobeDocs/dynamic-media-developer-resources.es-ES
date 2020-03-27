---
description: El procesamiento de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-description: El procesamiento de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.
seo-title: Referencia de conjunto de reglas
solution: Experience Manager
title: Referencia de conjunto de reglas
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Referencia de conjunto de reglas{#rule-set-reference}

El procesamiento de imágenes admite un mecanismo sencillo de preprocesamiento de solicitudes basado en reglas de coincidencia y sustitución de expresiones regulares.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Las colecciones de reglas de preprocesamiento (conjuntos *de* reglas) se pueden adjuntar a catálogos de material o al catálogo predeterminado. Las reglas del catálogo predeterminado solo se aplican si la solicitud no adjunta un catálogo de material específico.

Las reglas de preprocesamiento de solicitudes pueden modificar la ruta y las partes de consulta de las solicitudes antes de que el analizador de solicitudes del servidor las procese, incluida la manipulación de la ruta, la adición de comandos, el cambio de valores de comandos y la aplicación de plantillas o macros. También se pueden usar reglas para configurar y anular algunos atributos de catálogo, así como para limitar el servicio a direcciones IP de cliente específicas.

Los conjuntos de reglas se almacenan como archivos documento XML. La ruta relativa o absoluta del archivo del conjunto de reglas debe especificarse en `attribute::RuleSetFile`.

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

Los elementos `<?xml>`, `<!DOCTYPE>` y `<ruleset>` siempre son necesarios en un archivo XML de conjunto de reglas válido, aunque no se haya definido ninguna regla real.

Se permite un `<ruleset>` elemento que contenga cualquier número de `<rule>` elementos.

El contenido de los archivos de reglas de preprocesamiento distingue entre mayúsculas y minúsculas.

## Preprocesamiento de URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Antes de cualquier otro procesamiento, una solicitud HTTP entrante se analiza parcialmente para determinar qué catálogo de material debe aplicarse. Una vez identificado el catálogo, se aplica el conjunto de reglas para el catálogo seleccionado (o el catálogo predeterminado, si no se ha identificado ningún catálogo específico).

Se busca en los `<rule>` elementos en el orden especificado para que coincidan con el contenido del `<expression>` elemento ( *`expression`*).

Si `<rule>` se coincide con un elemento, se aplica la opción *`substitution`* y la cadena de solicitud modificada se pasa al analizador de solicitudes del servidor para un procesamiento normal.

Si no se realiza una coincidencia correcta cuando se llega al final del `<ruleset>` evento, la solicitud se pasa al analizador sin ninguna modificación.

## El atributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

El comportamiento predeterminado se puede modificar con el `OnMatch` atributo de los `<rule>` elementos. `OnMatch` puede establecerse en `break` (predeterminado), `continue`o `error.`

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
   <td colname="col2"> <p>El procesamiento de reglas finaliza inmediatamente después de que se haya aplicado la sustitución de esta regla. Predeterminado. </p> </td> 
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

`<rule>` de forma opcional, los elementos pueden definir atributos que anulan los atributos de catálogo correspondientes cuando la regla se coincide y `OnMatch="break"` se establece correctamente. No se aplican atributos si `OnMatch="continue"` está establecido. Consulte la descripción de `<rule>` para obtener una lista de atributos que se pueden controlar con reglas.

## expresiones regulares {#section-4d326507b52544b0960a9a5f303e3fe6}

La coincidencia simple de cadenas funciona para aplicaciones muy básicas, pero en la mayoría de los casos se requieren expresiones regulares. Aunque las expresiones regulares son estándar del sector, la implementación específica varía de una instancia a otra.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) describe la implementación de expresión regular específica utilizada por el servicio de imágenes.

## Subcadenas capturadas {#section-8057cd65d48949ffb6a50e929bd3688b}

Para facilitar las modificaciones de direcciones URL complejas, las subcadenas se pueden capturar en la expresión rodeando la subcadena con paréntesis (...). Las subcadenas capturadas se numeran secuencialmente comenzando por 1 según la posición del paréntesis inicial. Las subcadenas capturadas se pueden insertar en la sustitución utilizando *`$n`*, donde *`n`* es el número de secuencia de la subcadena capturada.

## Administración de archivos de conjunto de reglas {#section-e8ce976b56404c009496426fd334d23d}

Se puede adjuntar un archivo de conjunto de reglas a cada catálogo de materiales con el atributo de catálogo `attribute::RuleSetFile`. Aunque puede editar el archivo del conjunto de reglas en cualquier momento, el servidor de imágenes solo reconoce los cambios cuando se vuelve a cargar el catálogo de materiales asociado. Esto sucede cuando se inicia o reinicia el servidor de plataformas y cuando se modifica o se &quot;toca&quot; el archivo de catálogo principal (que tiene un sufijo de [!DNL .ini] archivo) (para cambiar la fecha del archivo).

## Ejemplos {#section-c4142a41f5cd4ff799a72fbc130c3700}

Los ejemplos de conjuntos de reglas se proporcionan en la sección correspondiente de Referencia del catálogo de imágenes de la documentación del servicio de imágenes.

## Véase también {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[paquete java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
