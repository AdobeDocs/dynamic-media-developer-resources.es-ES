---
description: Utilice esta configuración del servidor para registrar el acceso.
solution: Experience Manager
title: Registro de acceso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 3%

---

# Registro de acceso{#access-logging}

Utilice esta configuración del servidor para registrar el acceso.

Sintaxis

## TC::directory: carpeta de archivos de registro {#section-5d9e2168d4504bbe9868b7d6051c9d67}

La carpeta a la que [!DNL Platform Server] escribe archivos de registro. Puede ser una ruta absoluta o una ruta relativa a *`install_folder`*. El valor predeterminado es [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>La nueva carpeta debe crearse antes de cambiar esta configuración. Asegúrese de que la carpeta tenga los privilegios de acceso de lectura y escritura correctos si el servicio de imágenes está instalado para ejecutarse en una cuenta de usuario que no sea raíz.

## TC::maxDays: número de días para conservar los archivos de registro {#section-45cbecffc5694c87b7d5c176a44a4885}

Se debe conservar el número de días que los archivos de registro. Todos los días a medianoche se crean nuevos archivos de registro. En este momento, el servidor eliminará todos los archivos de la carpeta de archivos de registro que tengan una antigüedad mayor que el número de días especificado, incluidos los escritos por el servidor de imágenes o el servidor de procesamiento. El valor predeterminado es 10.

## TC::prefix - Nombre del archivo de registro de acceso {#section-1003856323b844049632710a5a056aa7}

Prefijo de nombre del archivo en el que se escriben los datos del registro de acceso. La fecha y el sufijo de archivo ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) se anexan a la cadena especificada. El nombre del archivo de registro de acceso debe ser diferente del del archivo de registro de seguimiento. El valor predeterminado es &quot; `access-`&quot;.

## TC::pattern: patrón de registro de acceso {#section-22775ea85cee444d8a7d7336a3b1feef}

Especifica el patrón de datos para [!DNL Platform Server] acceder a registros de registro. La cadena pattern especifica variables que se sustituyen por sus valores correspondientes. Todos los demás caracteres de la cadena de patrón se transfieren literalmente al registro de registro.

Para utilizar la utilidad de calentamiento de caché, los espacios deben utilizarse como separadores de campo. El [!DNL Platform Server] reemplaza todos los espacios y caracteres &quot;%&quot; en los valores de campo por `%20` y `%25`, respectivamente.

Se admiten las siguientes variables de patrón:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Patrón</b> </th> 
   <th class="entry"> <b>Descripción</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Dirección IP remota. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Dirección IP local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Recuento de bytes de respuesta excluyendo encabezados HTTP o ' ' si es cero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Recuento de bytes de respuesta excluyendo encabezados HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Tiempo de procesamiento de la solicitud en milisegundos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>id de subproceso (para las entradas del registro de depuración/error de referencia cruzada). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>fecha y hora, con el formato <span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS </span> offset </span> </p> <p> ( <span class="varname"> SSS </span> son ms, <span class="varname"> offset </span> es la diferencia horaria GMT); el valor de hora se captura cuando la respuesta se envía al cliente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Método de solicitud ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>, etc.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Superposición de solicitudes (número de solicitudes procesadas simultáneamente). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Puerto local en el que se recibió esta solicitud. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Cadena de consulta (precedida de "?") si existe). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Primera línea de solicitud (método de solicitud, URI, versión HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Igual que <span class="codeph"> %r </span>, pero aplica una codificación HTTP limitada al URI para evitar problemas de análisis de registros. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Código de estado de respuesta HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ID de sesión de usuario. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Fecha y hora, en formato de registro común. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Usuario remoto autenticado (si lo hay); de lo contrario, ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>Ruta de URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Nombre del servidor local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> % </span> </p> </td> 
   <td> <p>Tiempo de procesamiento de la solicitud en segundos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] clave de caché (carpeta/nombre del archivo de caché). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] palabra clave de administración de caché: <span class="codeph"> { REUTILIZADO | CREADO | ACTUALIZADO | REMOTO | REMOTE_CREATED | REMOTE_UPDATED | CACHÉ_REMOTA | VALIDADO | IGNORADO | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>El tipo MIME de respuesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>El contexto de destino si se produce un reenvío de contexto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>El <span class="codeph"> etag </span> valor del encabezado de respuesta (firma MD5 de los datos de respuesta). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Mensaje de error. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Tiempo necesario para recuperar la entrada de caché o los datos del servidor de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Tiempo empleado para el análisis de la solicitud y la búsqueda en el catálogo de imágenes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Indica si esta solicitud intentó o no algún acceso basado en rutas fuera del sistema de catálogos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>Dirección IP del servidor del mismo nivel en el clúster de caché que entregó la entrada de caché o "-" si <span class="codeph"> CacheUse </span> es ninguna <span class="codeph"> REMOTE_CREATED </span> ni <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Categoría de error: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=sin error. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=imágenes no encontradas en el servidor. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=error de uso de protocolo IS o un error de contenido distinto de 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=error de otro servidor. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=solicitud rechazada debido a sobrecarga temporal del servidor. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>El valor en mayúsculas de <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>El ID raíz del catálogo principal de la solicitud. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>El tiempo que tarda [!DNL Platform Server] para enviar una respuesta después de escribir datos en el flujo de salida. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Like <span class="codeph"> %B </span>, pero incluye valores para respuestas 304 (no modificadas). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformationUrl}r </span> </p> </td> 
   <td> <p>La dirección URL final después de todas las transformaciones del conjunto de reglas. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>El valor del encabezado de solicitud HTTP especificado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>El valor del encabezado de respuesta HTTP especificado. </p> </td> 
  </tr> 
 </tbody> 
</table>

El valor predeterminado es `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
