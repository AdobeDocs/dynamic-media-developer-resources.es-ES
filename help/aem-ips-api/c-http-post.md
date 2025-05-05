---
title: Carga de recursos mediante POST HTTP en el servlet UploadFile
description: La carga de recursos en  [!DNL Dynamic Media] Classic implica una o más solicitudes de POST HTTP que configuran un trabajo para coordinar toda la actividad de registro asociada con los archivos cargados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Carga de recursos mediante POST HTTP en el servlet UploadFile{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

La carga de recursos en Dynamic Media Classic implica una o más solicitudes de POST HTTP que configuran un trabajo para coordinar toda la actividad de registro asociada con los archivos cargados.

Utilice la siguiente URL para acceder al servlet UploadFile:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Todas las solicitudes de POST para un trabajo de carga deben proceder de la misma dirección IP.

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
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Oriente Medio, Asia </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japón/Asia-Pacífico </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Flujo de trabajo del trabajo de carga {#section-873625b9512f477c992f5cdd77267094}

El trabajo de carga consiste en uno o más POST HTTP que utilizan un `jobHandle` común para correlacionar el procesamiento en el mismo trabajo. Cada solicitud está codificada `multipart/form-data` y consta de las siguientes partes de formulario:

>[!NOTE]
>
>Todas las solicitudes de POST para un trabajo de carga deben proceder de la misma dirección IP.

|  Parte del formulario del POST HTTP  |  Descripción  |
|---|---|
| `auth`  |   Requerido. Documento XML authHeader que especifica la información de autenticación y de cliente. SOAP Ver **Solicitud de autenticación** en [&#128279;](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Opcional. Puede incluir uno o más archivos para cargar con cada solicitud de POST. Cada parte del archivo puede incluir un parámetro filename en el encabezado Content-Disposition que se utiliza como nombre de archivo de destino en IPS si no se especifica ningún parámetro `uploadPostParams/fileName`. |

|  Parte del formulario del POST HTTP   |  Nombre del elemento uploadPostParams   |  Tipo   |  Descripción   |
|---|---|---|---|
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga)   |   `companyHandle`  |  `xsd:string`  | Requerido. Identificador de la empresa a la que se carga el archivo.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `jobName`  |  `xsd:string`  | Se requiere `jobName` o `jobHandle`. Nombre del trabajo de carga.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `jobHandle`  |  `xsd:string`  | Se requiere `jobName` o `jobHandle`. Administrar a un trabajo de carga iniciado en una solicitud anterior.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `locale`  |  `xsd:string`  | Opcional. Código de idioma y país para la localización.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `description`  |  `xsd:string`  | Opcional. Descripción del trabajo.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `destFolder`  |  `xsd:string`  | Opcional. Ruta de la carpeta de destino como prefijo de una propiedad de nombre de archivo, especialmente para exploradores y otros clientes que pueden no admitir rutas de acceso completas en un nombre de archivo.  |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `fileName`  |  `xsd:string`  | Opcional. Nombre del archivo de destino. Anula la propiedad filename. |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `endJob`  |  `xsd:boolean`  | Opcional. El valor predeterminado es false. |
| `uploadParams` (obligatorio). Un documento XML `uploadParams` que especifica los parámetros de carga) | `uploadParams`  |  `types:UploadPostJob`  | Opcional si se trata de una solicitud posterior para un trabajo activo existente. Si hay un trabajo existente, `uploadParams` se omite y se usan los parámetros de carga del trabajo existentes. Ver [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Dentro del bloque `<uploadPostParams>` está el bloque `<uploadParams>` que designa el procesamiento de los archivos incluidos.

Consulte [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Aunque puede suponer que el parámetro `uploadParams` puede cambiar para archivos individuales como parte del mismo trabajo, no es el caso. Usar los mismos `uploadParams` parámetros para todo el trabajo.

La solicitud inicial del POST para un nuevo trabajo de carga debe especificar el parámetro `jobName`, preferiblemente con un nombre de trabajo único para simplificar las consultas subsiguientes de sondeo de estado de trabajo y registro de trabajo. Las solicitudes de POST adicionales para el mismo trabajo de carga deben especificar el parámetro `jobHandle` en lugar de `jobName`, utilizando el valor `jobHandle` devuelto desde la solicitud inicial.

La solicitud final del POST para un trabajo de carga debe establecer el parámetro `endJob` en true para que no se publiquen archivos futuros para este trabajo. A su vez, esto permite que el trabajo se complete inmediatamente después de ingerir todos los archivos POSTed. De lo contrario, se agota el tiempo de espera del trabajo si no se reciben solicitudes de POST adicionales en un plazo de 30 minutos.

## Respuesta de UploadPOST {#section-421df5cc04d44e23a464059aad86d64e}

Para una solicitud de POST correcta, el cuerpo de respuesta es un documento XML `uploadPostReturn`, como especifica el XSD en lo siguiente:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

El `jobHandle` devuelto se pasa en el parámetro `uploadPostParams`/ `jobHandle` para cualquier solicitud de POST posterior para el mismo trabajo. También puede utilizarlo para sondear el estado del trabajo con la operación `getActiveJobs` o para consultar los registros del trabajo con la operación `getJobLogDetails`.

Si hay un error al procesar la solicitud del POST, el cuerpo de respuesta consta de uno de los tipos de errores de API como se describe en [Errores](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Ejemplo de solicitud de POST {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Ejemplo de respuesta del POST: correcta {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Ejemplo de respuesta del POST: error {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
