---
description: Reenvía la lista suministrada de direcciones URL al proveedor de CDN de Dynamic Media (Red de distribución de contenido) para invalidar la caché existente de respuestas HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 4%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Reenvía la lista suministrada de direcciones URL al proveedor de CDN de Dynamic Media (Red de distribución de contenido) para invalidar la caché existente de respuestas HTTP.

## cdnCacheInvalidation: Acerca de {#section-4f70d2bc79d64288b961836ab17e9690}

La invalidación de caché de CDN obliga a todas las solicitudes HTTP para que estas URL se revaliden con los datos publicados actualmente en la red de Dynamic Media después de que esta solicitud de invalidación se procese a través de la red de CDN. Cualquier URL que no esté conectada a la estructura de la URL del servicio de Dynamic Media y que coincida directamente con el ID raíz de la empresa de Dynamic Media asignado cuando se crea la empresa dará como resultado un error de API para toda la solicitud. Cualquier URL no válida que la CDN no admita y que considere no válida también generará un error de API para toda la solicitud.

**Frecuencia de uso: Reglas**

Las reglas que rigen la frecuencia de uso de esta función están controladas por los socios de CDN de Dynamic Media. La CDN conserva la discreción de degradar la capacidad de respuesta de estas invalidaciones para mantener un rendimiento óptimo de su servicio a sus usuarios. Si se notifica a Dynamic Media del uso excesivo de esta función, tendremos que recurrir a la desactivación de la función, ya sea por empresa o por completo a través del servicio.

**Correos electrónicos de confirmación**

Los correos electrónicos de confirmación del socio de CDN de Dynamic Media se pueden enviar al creador de la lista o hasta 5 direcciones de correo electrónico más. La API envía la confirmación cuando se ha notificado a toda la red de CDN que se han borrado las direcciones URL a las que se hace referencia en el correo electrónico. Una sola llamada a `cdnCacheInvalidation` puede enviar varios correos electrónicos si el número de URL suministradas supera el número que Dynamic Media puede enviar al socio de CDN en una sola notificación. Actualmente, eso sería si la solicitud supera las 100 direcciones URL, pero está sujeta a cambios según la solicitud del socio de CDN.

**Admitido desde**

6,0

## Tipos de usuarios autorizados {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parámetros {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nombre</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obligatorio</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Sí </p> </td> 
   <td> <p> El identificador de la empresa conectada con las URL para invalidar. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> tipos:UrlArray</span> </p> </td> 
   <td> <p> Sí </p> </td> 
   <td> <p> Lista de hasta 1000 direcciones URL que se van a invalidar desde la caché de CDN. Todas las direcciones URL deben contener el ID raíz de la empresa de Dynamic Media para invalidarse. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nombre</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obligatorio</b> </th> 
   <th class="entry"> <b> Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Un controlador que hace referencia a la solicitud de depuración. </p> <p>La API <span class="codeph"> cdnCacheInvalidation</span> ahora invalida la caché casi inmediatamente (~5 segundos). Por lo tanto, ya no suele ser necesario sondear el estado de invalidación. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Segundos estimados hasta la finalización de la solicitud de depuración. Los clientes deben esperar este tiempo antes del estado de sondeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-f414361a58e84dfcbbac30a358d02125}

Este ejemplo solicita que se invaliden cuatro direcciones URL en la caché de CDN. La respuesta contiene recuentos resumidos del éxito de las operaciones y una lista de detalles de error suministrados directamente desde la CDN para ayudar al cliente en el uso de esta función.

`getCdnCacheInvalidationStatus` operación.

**Solicitar**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Respuesta**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

