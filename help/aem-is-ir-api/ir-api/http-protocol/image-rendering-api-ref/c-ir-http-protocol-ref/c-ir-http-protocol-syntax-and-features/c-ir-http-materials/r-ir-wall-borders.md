---
title: Bordes de pared
description: Un material se considera un borde de pared cuando se especifica en un MSS borde de pared (introducido con sub=3.5).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e11c38d0-8255-4363-ae60-f47be37a1495
TQID: 'https://experienceleague.adobe.com/aq9RzIcQC6pmvWsqY0huvARpA-zEUCR-og9crmiUPfg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 4%

---

# Bordes de pared{#wall-borders}

Un material se considera un borde de pared cuando se especifica en un MSS borde de pared (introducido con sub=3.5).

Las imágenes de textura de borde de pared pueden incluir un canal alfa para definir la forma del borde. Los bordes de pared sólo se pueden aplicar a objetos de pared.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descripción </p> </th> 
   <th colname="col3" class="entry"> <p>Predeterminado </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Imagen de textura repetible; obligatorio </p> </td> 
   <td colname="col3"> <p>Ninguna </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolución de textura </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> atributo::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anclaje= </span> </a> </p> </td> 
   <td colname="col2"> <p>Alineación de textura horizontal (se omite el valor y) </p> </td> 
   <td colname="col3"> <p>0 (borde de la imagen izquierda) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Enfoque </p> </td> 
   <td colname="col3"> <p>0 (sin enfoque) </p> </td> 
  </tr> 
 </tbody> 
</table>

