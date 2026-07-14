---
title: Enfoque destacado
description: Resalte de enfoque de entrada mostrado alrededor del elemento de interfaz de usuario del visor enfocado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
TQID: 'https://experienceleague.adobe.com/E7n09sJ0qY9Aivp5OUFr5Jc6bwS5Ah3N-HdS9-H2Pgw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# Enfoque destacado{#focus-highlight}

Resalte de enfoque de entrada mostrado alrededor del elemento de interfaz de usuario del visor enfocado.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

El aspecto del resaltado de enfoque se controla con el siguiente selector de clase CSS:

```
.s7ecatalogviewer *:focus
```

**Propiedades CSS del resaltado de enfoque**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> descripción </span> </p> </td> 
   <td colname="col2"> <p> Estilo de resalte de enfoque. </p> </td> 
  </tr> 
 </tbody> 
</table>

Por ejemplo, para deshabilitar el resaltado de enfoque del explorador predeterminado para todos los elementos de la interfaz de usuario del visor, agregue el siguiente selector CSS a la hoja de estilo del visor:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

