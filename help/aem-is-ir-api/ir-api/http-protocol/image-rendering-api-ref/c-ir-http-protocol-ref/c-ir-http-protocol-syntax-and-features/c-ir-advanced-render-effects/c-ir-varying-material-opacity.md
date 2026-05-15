---
title: Opacidad de material variable
description: La opacidad variable se admite para el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como para calcomanías y materiales que cubren las ventanas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Opacidad de material variable{#varying-material-opacity}

La opacidad variable se admite para el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como para calcomanías y materiales que cubren las ventanas.

La información de opacidad se puede proporcionar simplemente utilizando una imagen de RGB con un canal alfa. Además, la opacidad general puede variar con el comando `opacity=` (tanto para imágenes RGB como RGBA).

Los bordes de pared también admiten imágenes RGBA, principalmente para apoyar bordes troquelados.

Los [!DNL vnw] archivos que definen las cubiertas de ventana pueden incluir un canal de opacidad. Lo combina el procesador con el canal alfa de la textura repetible y el valor `opacity=` para proporcionar una gama completa de efectos de opacidad para tratamientos de ventana transparente y translúcida.
