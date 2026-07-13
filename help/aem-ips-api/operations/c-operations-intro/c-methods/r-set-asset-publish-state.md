---
description: Determina si un recurso está listo para publicarse.
solution: Experience Manager
title: setAssetPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 0dc195ee-9229-40a3-ad8b-8f00c2c9ff97
TQID: 'https://experienceleague.adobe.com/iOheZ-j-0cYoAfC4JRHkluQM7VriuVy8PAjDna2odb4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 11%

---

# setAssetPublishState{#setassetpublishstate}

Determina si un recurso está listo para publicarse.

Sintaxis

## Tipos de usuarios autorizados {#section-11bec77e50b24461bb8c8aacf016eec8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-09d2ba001a2a455a9102550272f3eecb}

**Entrada (setAssetPublishStateParam)**

<table id="table_23CB72BFB8984CDF82D7207E7D82FC43"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obligatorio </th> 
   <th colname="col4" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> El identificador de la compañía. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Controlador de recurso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4">Estados disponibles: 
    <ul id="ul_A2614608DF1E4DB6BF8141D33E59D180"> 
     <li id="li_8C90BFEEE2B14A0184F342018C45EE67"><span class="codeph"> MarkedForPublish</span> </li> 
     <li id="li_C4BC12B304DA4763956C3049AF597D06"><span class="codeph"> NotMarkedForPublish</span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**Salida**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-c31ead6d0e594317a12c120509527792}

Este ejemplo de código establece el estado de publicación de un recurso mediante `NotMarkedForPublish`.

**Solicitud**

```java
<setAssetPublishStateParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <publishState>NotMarkedForPublish</publishState>
</setAssetPublishStateParam>
```

**Respuesta**

Ninguno.

