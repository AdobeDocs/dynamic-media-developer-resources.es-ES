---
description: Ejecuta un trabajo específico.
seo-description: Ejecuta un trabajo específico.
seo-title: executeJob
solution: Experience Manager
title: executeJob
topic: Dynamic Media Image Production System API
uuid: e73223c1-9032-4745-92b6-a5840949a824
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 19%

---


# executeJob{#executejob}

Ejecuta un trabajo específico.

Sintaxis

## Tipos de usuarios autorizados {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador de la compañía a la que pertenece el trabajo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sí </p> </td> 
   <td colname="col4"> <p>Identificador del trabajo que se va a ejecutar. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (executeJobReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-96f71aa58a954293b9a98ff96d86f232}

Este ejemplo de código ejecuta un trabajo que está programado para ejecutarse en IPS.

**Solicitar**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Respuesta**

Ninguno.
