---
title: regla
description: Solicitar elemento de regla. Una o más reglas son opcionales en la variable <ruleset> Elemento.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 7%

---

# regla{#rule}

Solicitar elemento de regla. Una o más reglas son opcionales en la variable `<ruleset>` Elemento.

## Atributos {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: Opcional. El valor predeterminado es &quot;break&quot;.

`Replace = "first" | "all"`: Opcional. El valor predeterminado es &quot;primero&quot;.

`RequestType` = *&quot;`types`&quot;*: Opcional. Especifica el contexto de entrada al que se aplica la regla. *`types`* es una lista separada por comas, que puede incluir uno o más de los tokens enumerados en la siguiente tabla. If `RequestType` no se ha especificado, la regla se aplica a las solicitudes recibidas en todos los contextos admitidos.

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
   <td> <p>Aplicado a solicitudes del servicio de imágenes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Aplicado a solicitudes de procesamiento de imágenes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> estático</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Aplicado a solicitudes de contenido estático </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: Opcional. Se utiliza para identificar el `<rule>` en los registros de depuración y los mensajes de error.

`  *`Atributo`* ="value"`: Opcional. `<rule>` Los elementos pueden definir cualquiera de los atributos siguientes en cualquier combinación. Si se especifica y la regla se ajusta correctamente, anulan los atributos de catálogo correspondientes para esta solicitud. El valor predeterminado es `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Atributo </span> </b> </th> 
   <th class="entry"> <p>Atributo de catálogo de imágenes correspondiente </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> attribute::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Caducidad</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> attribute::Caducidad</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestObfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribute::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> attribute::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> WaterMark</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribute::MarcaAgua</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte la descripción del atributo del catálogo de imágenes correspondiente para obtener más información.

Los atributos de caducidad solo anulan los valores de atributo predeterminados. La anulación se ignora si una `catalog::Expiration` El valor se aplica a la solicitud.

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

Si ambos `<expression>` y `<substitution>` se especifican y no se utilizan subcadenas capturadas, la primera subcadena coincidente se reemplaza por `<substitution>`.

If `<expression>` no se ha especificado, cualquier ruta coincide con y `<substitution>` se anexa al final de la ruta.

If `<substitution>` no se ha especificado, no se produce ninguna transformación de ruta o consulta, pero se anulan todos los atributos de catálogo especificados. If `<substitution>` está vacío, se elimina la subcadena coincidente.

El `<addressfilter>` solo se aplica cuando se produce una coincidencia y antes de que se apliquen las reglas de consulta.
