---
description: Utilice los siguientes comandos para aplicar formato básico a los caracteres.
seo-description: Utilice los siguientes comandos para aplicar formato básico a los caracteres.
seo-title: Formato básico de caracteres
solution: Experience Manager
title: Formato básico de caracteres
topic: Scene7 Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Formato básico de caracteres{#basic-character-formatting}

Utilice los siguientes comandos para aplicar formato básico a los caracteres.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descripción </th> 
   <th class="entry"> Notas </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \sin formato </span> </td> 
   <td> <p>Restablezca el formato de caracteres al formato predeterminado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span></span> </td> 
   <td> <p>Cara de fuente. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span></span> </td> 
   <td> <p>Tamaño de fuente. </p> </td> 
   <td> <p>Puntos medios; el valor predeterminado es 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span></span> </td> 
   <td> <p>Color de la fuente. </p> </td> 
   <td> <p>Índice basado en 0 en la tabla de colores. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>Estilo negrita. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>Estilo cursiva. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>Subíndice. </p> </td> 
   <td> <p>Reduce el tamaño de fuente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>Superíndice. </p> </td> 
   <td> <p>Reduce el tamaño de fuente. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>Subrayar. </p> </td> 
   <td> <p>El servicio de imágenes también reconoce los siguientes comandos de subrayado RTF: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>Estos se implementan en este momento como un subrayado estándar <span class="codeph"> \ul </span> . Todos los demás comandos de subrayado RTF se omiten. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone </span> </td> 
   <td> <p>desactivar subrayado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>desactivar subrayado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Mayúsculas </span> </td> 
   <td> <p>mayúsculas </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps </span> </td> 
   <td> <p>minúsculas ("versalitas") </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> solamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

