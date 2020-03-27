---
description: Obtiene recursos asociados a un recurso especificado y detalles sobre su relación.
seo-description: Obtiene recursos asociados a un recurso especificado y detalles sobre su relación.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

Obtiene recursos asociados a un recurso especificado y detalles sobre su relación.

Sintaxis

## Tipos de usuarios autorizados {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Entrada (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Gestionar en la compañía que posee el recurso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador de recurso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de campos de respuesta que desee. Consulte response- FieldArray/excludeFieldArray en Introducción. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de campos de respuesta excluidos. Consulte response- FieldArray/excludeFieldArray en Introducción. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Salida (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nombre </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descripción </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de conjuntos y elementos de plantilla que contienen el recurso que se va a recopilar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> miembroArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de recursos incluidos en el conjunto o recurso de plantilla especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de recursos a los que se hace referencia en una URL de capa o plantilla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de recursos que son propietarios del recurso especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivadaArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Matriz de recursos que se utilizaron para generar el recurso especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>GeneratorArray <span class="codeph"></span> lista la forma en que se creó este recurso. Por ejemplo, si <span class="codeph"> assetHandler</span> fuera una página de imágenes de un PDF, contendría la herramienta de procesador PDF y haría referencia al recurso PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>El <span class="codeph"> conjunto generado</span> invierte la forma en que se creó este recurso. Por ejemplo, el <span class="codeph"> conjunto</span> generado podría contener la lista de imágenes generadas desde este <span class="codeph"> controlador</span> de recursos si se trata de un recurso PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:recurso</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>La información del recurso de miniatura asociada al recurso de solicitud. Si no se asigna ningún recurso de miniatura, el campo se omite en la respuesta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puede utilizar los parámetros `responseFieldArray` o `excludeFieldArray` limitar el tamaño de respuesta. En particular, los `GenerationInfo` elementos devueltos en `generatorArray` `generatedArray` o de forma predeterminada para incluir tanto el iniciador como los registros de recursos generados. Para un tipo de recurso PDF, este comportamiento da como resultado varias copias no deseadas del registro de recursos PDF &quot;originador&quot; en la respuesta. Puede eliminar este problema agregando `generatedArray/items/originator` a `excludeFieldArray`. O bien, puede especificar una lista explícita de los campos de respuesta que desee incluir en `responseFieldArray`.

## Ejemplos {#section-8946ea4b9cb94912a8408249c897f192}

El siguiente ejemplo básico es una solicitud del identificador del generador para una imagen extraída de un PDF. Incluye una longitud `containerArray` de uno con un elemento que incluye el `assetHandle` del PDF.

**Solicitar**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Respuesta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

Lo contrario del ejemplo anterior es lo siguiente:

**Solicitar**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Respuesta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

En el siguiente ejemplo, se agrega un grupo a una compañía con `groupHandleArray`. En este ejemplo solo se utiliza un grupo.

**Solicitar**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Respuesta**

Ninguno.
