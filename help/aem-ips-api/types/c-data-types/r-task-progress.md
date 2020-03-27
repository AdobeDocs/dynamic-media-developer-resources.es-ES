---
description: Información sobre el progreso de la Tarea.
seo-description: Información sobre el progreso de la Tarea.
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TaskProgress{#taskprogress}

Información sobre el progreso de la Tarea.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nombre </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descripción </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Descripción del tipo de Tarea. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de elementos de tarea ya procesados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de elementos de tarea en curso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numpending</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de elementos de tarea pendientes (aún no procesados). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progreso</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:doble</span> </td> 
   <td colname="col3"> % de progreso (intervalo 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Mensaje de progreso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Hora en que se actualizó la última información de progreso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Matriz de elementos de tarea. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Los valores incluyen: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Desconocido</span>: Cuando la tarea monitorea transiciones entre estados. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nuevo</span>: Se ha creado el monitor de Tarea, pero aún no ha aceptado tareas. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Procesamiento</span>: El monitor de Tarea está procesando activamente tareas. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Deteniendo</span>: El monitor de Tarea está deteniendo un trabajo debido a una solicitud de trabajo de detención. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Listo</span>: Se han completado los trabajos asignados a los trabajos del monitor de tarea. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Error</span>: Indica un error fatal. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

