---
description: Reenvía la lista proporcionada de direcciones URL al proveedor de CDN de Scene7 (Red de distribución de contenido) para invalidar la caché existente de las respuestas HTTP.
seo-description: Reenvía la lista proporcionada de direcciones URL al proveedor de CDN de Scene7 (Red de distribución de contenido) para invalidar la caché existente de las respuestas HTTP.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Reenvía la lista proporcionada de direcciones URL al proveedor de CDN de Scene7 (Red de distribución de contenido) para invalidar la caché existente de las respuestas HTTP.

## cdnCacheInvalidation: Acerca de {#section-4f70d2bc79d64288b961836ab17e9690}

La invalidación de caché de CDN fuerza a todas las solicitudes HTTP para que estas direcciones URL se revaliden con los datos publicados actualmente en la red de Scene7 una vez que esta solicitud de invalidación se procesa a través de la red de CDN. Las direcciones URL que no estén conectadas a la estructura URL del servicio de Scene7 y que coincidan directamente con el ID de raíz de la compañía de Scene7 asignado al crear la compañía generarán un error de API para toda la solicitud. Cualquier dirección URL no válida que la CDN no admita y que considere no válida también generará un error de API para toda la solicitud.

**Frecuencia de uso: Reglas**

Las reglas que rigen la frecuencia de uso de esta función las controlan los socios de CDN de Scene7. La CDN conserva la discreción de degradar la capacidad de respuesta de estas invalidaciones para mantener un rendimiento óptimo de su servicio a sus usuarios. Si se notifica a Scene7 del uso excesivo de esta función, tendremos que deshabilitar la función por compañía o por completo en todo el servicio.

**Correos electrónicos de confirmación**

Los mensajes de correo electrónico de confirmación del socio de CDN de Scene7 se pueden enviar al creador de la lista o a un máximo de cinco direcciones de correo electrónico más. La API envía la confirmación cuando se ha notificado a toda la red CDN que se han borrado las direcciones URL a las que se hace referencia en el correo electrónico. Una sola llamada para `cdnCacheInvalidation` enviar varios correos electrónicos si el número de direcciones URL suministradas supera el número que Scene7 puede enviar al socio de CDN en una sola notificación. Actualmente, esto sería si la solicitud supera las 100 direcciones URL, pero está sujeta a cambios según la solicitud del socio de CDN.

**Admitido desde**

6.0

## Tipos de usuarios autorizados {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parámetros {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Entrada** ( `cdnCacheInvalidationParam`)

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
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Sí </p> </td> 
   <td> <p> Identificador de la compañía conectada con las direcciones URL para invalidar. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span></span> </p> </td> 
   <td> <p> <span class="codeph"> tipos:UrlArray</span> </p> </td> 
   <td> <p> Sí </p> </td> 
   <td> <p> Lista de hasta 1000 direcciones URL para invalidar desde la caché de CDN. Todas las direcciones URL deben contener el ID raíz de compañía de Scene7 para invalidarlo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>Un identificador que hace referencia a la solicitud de depuración. </p> <p>La API <span class="codeph"> cdnCacheInvalidation</span> ahora invalida la caché casi inmediatamente (~5 segundos). Como tal, ya no es necesario sondear para obtener la invalidación. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> calculatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Segundos estimados hasta la finalización de la solicitud de purga. Los clientes deben esperar este tiempo antes del estado de la encuesta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ejemplo {#section-f414361a58e84dfcbbac30a358d02125}

Este ejemplo solicita que se invaliden cuatro direcciones URL en la caché de CDN. La respuesta contiene recuentos resumidos del éxito de las operaciones y una lista de detalles de errores suministrados directamente desde la CDN para ayudar al cliente en el uso de esta función.

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

