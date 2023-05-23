---
title: Opacidad de material variable
description: La opacidad variable se admite para el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como para calcomanías y materiales que cubren las ventanas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacidad de material variable{#varying-material-opacity}

La opacidad variable se admite para el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como para calcomanías y materiales que cubren las ventanas.

La información de opacidad se puede proporcionar simplemente utilizando una imagen de RGB con un canal alfa. Además, la opacidad global puede variar con el `opacity=` (para imágenes de RGB y RGBA).

Los bordes de pared también admiten imágenes RGBA, principalmente para apoyar bordes troquelados.

El [!DNL vnw] los ficheros que definen las cubiertas de ventana pueden incluir un canal de opacidad. Lo combina el procesador con el canal alfa de la textura repetible y la `opacity=` valor para proporcionar una gama completa de efectos de opacidad para tratamientos de ventanas transparentes y translúcidas.
