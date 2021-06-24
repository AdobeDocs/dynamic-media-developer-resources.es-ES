---
description: Determina si un recurso está listo para publicarse.
solution: Experience Manager
title: setAssetPublishState
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: 0dc195ee-9229-40a3-ad8b-8f00c2c9ff97
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 18%

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
   <td colname="col4"> El identificador de la empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sí </td> 
   <td colname="col4"> Identificador de recurso. </td> 
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
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**Salida**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-c31ead6d0e594317a12c120509527792}

Este ejemplo de código establece el estado de publicación de un recurso mediante `NotMarkedForPublish`.

**Solicitar**

```java
<setAssetPublishStateParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <publishState>NotMarkedForPublish</publishState>
</setAssetPublishStateParam>
```

**Respuesta**

Ninguno.
