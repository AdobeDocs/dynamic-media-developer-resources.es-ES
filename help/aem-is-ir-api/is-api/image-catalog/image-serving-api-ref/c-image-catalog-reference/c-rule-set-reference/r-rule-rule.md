---
description: Solicitar elemento de regla. Una o más reglas son opcionales en el elemento <ruleset>.
seo-description: Solicitar elemento de regla. Una o más reglas son opcionales en el elemento <ruleset>.
seo-title: regla
solution: Experience Manager
title: regla
topic: Scene7 Image Serving - Image Rendering API
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 7%

---


# regla{#rule}

Solicitar elemento de regla. Una o más reglas son opcionales en el elemento `<ruleset>`.

## Atributos {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Opcional. El valor predeterminado es &quot;break&quot;.

`Replace = "first" | "all"`: Opcional. El valor predeterminado es &quot;first&quot;.

`RequestType` =  *&quot;`types`&quot;*: Opcional. Especifica el contexto de entrada al que se aplica la regla. *`types`* es una lista separada por comas, que puede incluir uno o varios de los tokens enumerados en la tabla siguiente. Si no se especifica `RequestType`, la regla se aplica a las solicitudes recibidas en todos los contextos admitidos.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>testigo</b> </p> </th> 
   <th class="entry"> <p><b>Contexto</b> </p> </th> 
   <th class="entry"> <p><b>Descripción</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> es</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Se aplica a solicitudes de servicio de imágenes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/procesar/</span> </p> </td> 
   <td> <p>Aplicado a solicitudes de procesamiento de imágenes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> estático</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Se aplica a solicitudes de contenido estático </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Opcional. Se utiliza para identificar el elemento `<rule>` en los registros de depuración y los mensajes de error.

`  *`Atributo`* ="value"`: Opcional. `<rule>` pueden definir cualquiera de los atributos siguientes en cualquier combinación. Si se especifica y la regla se coincide correctamente, se anularán los atributos de catálogo correspondientes para esta solicitud. El valor predeterminado es `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Atributo  </span> </b> </th> 
   <th class="entry"> <p>Atributo de catálogo de imágenes correspondiente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> atributo::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Caducidad</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> atributo::Caducidad</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> atributo::MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> atributo::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> atributo::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> atributo::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> atributo::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Marca de agua</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> atributo::WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte la descripción del atributo correspondiente del catálogo de imágenes para obtener más información.

Los atributos Caducidad solo anulan los valores de atributo predeterminados. La anulación se omite si se aplica un valor `catalog::Expiration` específico a la solicitud.

## Datos {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;encabezado&gt;</span> </p></td> 
  <td class="stentry"> <p>Opcional </p></td> 
 </tr> 
</table>

## Notas {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Si se especifican `<expression>` y `<substitution>` y no se utilizan subcadenas capturadas, la primera subcadena coincidente se reemplaza por `<substitution>`.

Si no se especifica `<expression>`, cualquier ruta coincide y `<substitution>` se anexa al final de la ruta.

Si no se especifica `<substitution>`, no se produce ninguna transformación de ruta o consulta, pero se sobrescriben los atributos de catálogo especificados. Si `<substitution>` está vacío, se elimina la subcadena coincidente.

El `<addressfilter>` se aplica solamente cuando se produce una coincidencia y antes de que se apliquen las reglas de consulta.
