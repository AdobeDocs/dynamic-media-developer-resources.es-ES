---
description: Actualiza el estado del contexto de publicación de un recurso.
seo-description: Actualiza el estado del contexto de publicación de un recurso.
seo-title: ContextStateUpdate
solution: Experience Manager
title: ContextStateUpdate
topic: Scene7 Image Production System API
uuid: ef579d3c-1899-4088-903e-e6ed5a414ca8
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# ContextStateUpdate{#contextstateupdate}

Actualiza el estado del contexto de publicación de un recurso.

Sintaxis

## Parámetros {#section-9f747df071854c6896fdbb95684ad947}

Establezca el estado del contexto de publicación de un recurso con `setAssetsContextState`.

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nombre </th>
   <th colname="col2" class="entry"> Tipo </th>
   <th colname="col3" class="entry"> Descripción </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> Gestionar en el contexto de publicación. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">Estado de publicación actualizado del recurso para el contexto de publicación especificado. Incluye: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Estado de publicación](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

