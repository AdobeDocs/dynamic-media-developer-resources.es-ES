---
description: Control de caché. Permite desactivar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la [!DNL Platform Server] caché.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# cache{#cache}

Control de caché. Permite desactivar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la [!DNL Platform Server] caché.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Si solo uno *`cacheControl`* se especifica, se aplica tanto a las cachés de cliente como de servidor.

Atributo de solicitud. Se omite cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`* se ignora cuando el catálogo de imágenes deshabilita el almacenamiento en caché del lado del cliente (si `catalog::Expiration` tiene un valor negativo).

Defaults to `cache=on,on`.
