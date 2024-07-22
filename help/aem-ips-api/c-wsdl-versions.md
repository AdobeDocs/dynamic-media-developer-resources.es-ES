---
description: El servicio web IPS es compatible con un conjunto de documentos WSDL (Lenguaje de descripción de servicios web) a los que se accede desde cualquier instalación de IPS en la que esté instalado el componente Servicio web IPS. Cada versión de la API de IPS incluye un nuevo archivo WSDL que hace referencia a un espacio de nombres XML de destino con versiones. Las versiones de área de nombres de WSDL anteriores también son compatibles para permitir la compatibilidad con versiones anteriores de las aplicaciones existentes.
solution: Experience Manager
title: Versiones WSDL del servicio web IPS
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# Versiones WSDL del servicio web IPS{#ips-web-service-wsdl-versions}

El servicio web IPS es compatible con un conjunto de documentos WSDL (Lenguaje de descripción de servicios web) a los que se accede desde cualquier instalación de IPS en la que esté instalado el componente Servicio web IPS. Cada versión de la API de IPS incluye un nuevo archivo WSDL que hace referencia a un espacio de nombres XML de destino con versiones. Las versiones de área de nombres de WSDL anteriores también son compatibles para permitir la compatibilidad con versiones anteriores de las aplicaciones existentes.

## Acceso a WSDL {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Acceda a los WSDL de Scene7 como se muestra a continuación.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

El valor predeterminado de `<IPS_webapp>` es `scene7`.

**Ubicación del servicio**

La dirección URL del servicio se especifica en la sección de servicio del documento WSDL del servicio web IPS. La URL del servicio suele tener el siguiente formato:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**URL de acceso para regiones de Dynamic Media**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Ubicación geográfica </p> </th> 
   <th colname="col2" class="entry"> <p>URL de producción </p> </th> 
   <th colname="col3" class="entry"> <p>URL de ensayo (se utiliza para el desarrollo y la prueba previos a la producción) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>América del Norte </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Oriente Medio, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japón/Asia-Pacífico </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## WSDL admitidos {#section-ebbba69880f94e9c823f1147974eb404}

Recuerde que es posible que tenga que modificar el código si desea utilizar características de en la última versión de la API de IPS. La API de IPS admite WSDL para las siguientes versiones:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Versión de versión de API </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API namespace </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anterior a 4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Las aplicaciones existentes que necesiten modificarse para utilizar nuevas funciones deben actualizarse a la última versión de la API y es posible que tengan que realizar cambios en el código existente. Consulte el registro de cambios para obtener más información.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Enlaces**

SOAP El servicio web de la API de IPS solo admite un enlace de.

**Transportes compatibles**

SOAP El enlace de la API de IPS solo admite transporte HTTP. SOAP Realice todas las peticiones de la utilizando el método del POST HTTPS.

SOAP **Encabezado de acción de**

Para procesar una solicitud, establezca el encabezado HTTP SOAPAction en el nombre de la operación solicitada. El atributo de nombre de operación de la sección de enlace de WSDL especifica el nombre.

**Formato del mensaje**

El estilo documento/literal se utiliza para todos los mensajes de entrada y salida con tipos basados en el lenguaje de definición de esquema XML ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) y especificados en el archivo WSDL. Todos los tipos requieren nombres completos utilizando el valor de área de nombres de destino especificado en el archivo WSDL.

**Solicitar autenticación**

El método preferido para pasar credenciales de autenticación en solicitudes de API es utilizar el elemento `authHeader` tal como se define en el WSDL de la API de IPS.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Campos**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> usuario </span> </p> </td> 
   <td colname="col2"> <p> Correo electrónico de usuario de IPS válido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contraseña </span> </p> </td> 
   <td colname="col2"> <p>Contraseña de la cuenta de usuario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> configuración regional </span> </p> </td> 
   <td colname="col2"> <p> Configuración regional opcional para la solicitud. Consulte <b>Configuración regional</b> para obtener más información. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Llamando al nombre de aplicación. Este parámetro es opcional, pero se recomienda incluirlo en todas las solicitudes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Llamando a la versión de aplicación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Indicador opcional para habilitar o deshabilitar la compresión gzip del XML de respuesta. De forma predeterminada, las respuestas se comprimen con gzip si el encabezado HTTP Accept-Encoding indica compatibilidad con gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> failureHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Parámetro opcional para anular el código de estado HTTP para las respuestas de errores. De forma predeterminada, las respuestas de errores devuelven el código de estado HTTP 500 (error interno del servidor). Algunas plataformas cliente, incluido el Flash de Adobe, no pueden leer el cuerpo de la respuesta a menos que se devuelva un código de estado 200 (OK). </p> </td> 
  </tr> 
 </tbody> 
</table>

El elemento `authHeader` siempre se define en el espacio de nombres `http://www.scene7.com/IpsApi/xsd`, independientemente de la versión de la API.

SOAP A continuación se muestra un ejemplo del uso del elemento `authHeader` en un encabezado de solicitud de la:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Otros métodos de autenticación de solicitudes**

SOAP Si, por algún motivo, la aplicación cliente no puede pasar el encabezado de `authHeader`, las solicitudes de API también pueden especificar credenciales mediante la autenticación HTTP Basic (como se especifica en RFC 2617).

SOAP Para la autenticación HTTP Basic, la sección de encabezado HTTP de cada solicitud de POST de la debe incluir un encabezado con el siguiente formato:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Donde `base64()` aplica la codificación Base64 estándar, `<IPS_user_email>` es la dirección de correo electrónico de un usuario IPS válido y `<password>` es la contraseña del usuario.

Envíe el encabezado Autorización de forma preventiva con la solicitud inicial. Si no se incluyen credenciales de autenticación en la solicitud, `IpsApiService` no responde con un código de estado de `401 (Unauthorized)`. SOAP En su lugar, se devuelve un código de estado de `500 (Internal Server Error)` con un cuerpo de error de que indica que no se pudo autenticar la solicitud.

SOAP Antes de IPS 3.8, la autenticación mediante el encabezado de la se implementaba utilizando los elementos `AuthUser` y `AuthPassword` en el espacio de nombres `http://www.scene7.com/IpsApi`. Por ejemplo:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Este estilo sigue siendo compatible con la compatibilidad con versiones anteriores, pero ha quedado obsoleto en favor del elemento `authHeader`.

**Solicitar autorización**

Una vez autenticadas las credenciales del llamador, se comprueba la solicitud para asegurarse de que el llamador está autorizado para realizar la operación solicitada. La autorización se basa en la función de usuario del autor de la llamada y también puede requerir la comprobación de la compañía, el usuario y otros parámetros de operación de destino. Además, los usuarios del portal de imágenes deben pertenecer a un grupo con los permisos necesarios para realizar determinadas operaciones de carpetas y recursos. La sección de referencia Operaciones detalla los requisitos de autorización para cada operación.

SOAP **Solicitud y respuesta de ejemplo de la lista de distribución**

El ejemplo siguiente muestra una operación `addCompany` completa, incluidos los encabezados HTTP:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

Y la respuesta correspondiente:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

SOAP **fallas de la**

SOAP SOAP Cuando una operación encuentra una condición de excepción, se devuelve un error de como el cuerpo del mensaje de error en lugar de la respuesta normal. Por ejemplo, si un usuario no administrador intenta enviar la solicitud `addCompany` anterior, se devuelve la siguiente respuesta:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
