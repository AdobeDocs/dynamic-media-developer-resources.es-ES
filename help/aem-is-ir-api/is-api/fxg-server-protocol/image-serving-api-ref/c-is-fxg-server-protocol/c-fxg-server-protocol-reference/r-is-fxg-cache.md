---
description: Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la memoria caché interna de  [!DNL Platform Server] .
solution: Experience Manager
title: escondrijo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
TQID: 'https://experienceleague.adobe.com/X6q0OKRjjjpgNxl8XDuzkNBzrzTBS4E5BtXQGuJWgmk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 0%

---

# escondrijo{#cache}

Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché interno de [!DNL Platform Server].

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> activado|desactivado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activado|desactivado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activado|desactivado</span> </p></td> 
 </tr> 
</table>

Si solo se especifica un valor *`cacheControl`*, se aplica a las memorias caché del cliente y del servidor.

Atributo de solicitud. Se ignora cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`* se omite cuando el catálogo de imágenes deshabilita el almacenamiento en caché del lado del cliente (si `catalog::Expiration` tiene un valor negativo).

El valor predeterminado es `cache=on,on`.
