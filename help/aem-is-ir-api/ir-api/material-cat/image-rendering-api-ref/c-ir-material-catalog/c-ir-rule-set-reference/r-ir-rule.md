---
description: Solicitar elemento de regla. Uno o más son opcionales en el elemento <ruleset>.
seo-description: Solicitar elemento de regla. Uno o más son opcionales en el elemento <ruleset>.
seo-title: regla
solution: Experience Manager
title: regla
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# regla{#rule}

Solicitar elemento de regla. Uno o más son opcionales en el `<ruleset>` elemento.

## Atributos {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Opcional. El valor predeterminado es &quot;break&quot;.

` Name=" *`text`*"` Opcional. Se utiliza para identificar el `<rule>` elemento en los registros de depuración y los mensajes de error.

Además, `<rule>` los elementos pueden definir cualquiera de los atributos siguientes en cualquier combinación. Si se especifica y la regla se coincide correctamente, se anulan los atributos de catálogo correspondientes para esta solicitud.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo &lt;rule&gt; </p> </th> 
   <th colname="col2" class="entry"> <p>Atributo correspondiente del catálogo de imágenes </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> atributo::DefaultPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Caducidad </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> atributo::Caducidad </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> atributo::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> atributo::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte la descripción del atributo correspondiente del catálogo de imágenes para obtener más información.

El atributo Expiration solo anula el valor de atributo predeterminado; se omite si se aplica un valor específico `catalog::Expiration` a la solicitud.

## Datos {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expresión&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;address sfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Opcional. </p> </td> 
 </tr> 
</table>

## Notas {#section-a27b91f9a03047c0bb7edc0967fb4216}

Si se especifican `<expression>` y `<substitution>` y no se utilizan subcadenas capturadas, la primera subcadena coincidente se sustituye por `<substitution>`.

Si no `<expression>` se especifica, cualquier ruta coincidirá y `<substitution>` se agregará al final de la ruta.

Si no `<substitution>` se especifica, se elimina la subcadena coincidente.

El `<addressfilter>` se aplica solo cuando se produce una coincidencia y antes de que se apliquen las reglas de consulta.
