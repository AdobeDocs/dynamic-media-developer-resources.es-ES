---
description: Se admite la opacidad variable en el caso de colores sólidos y texturas repetibles aplicadas a objetos superpuestos, así como en el caso de las calcomanías y los materiales de revestimiento de ventanas.
seo-description: Se admite la opacidad variable en el caso de colores sólidos y texturas repetibles aplicadas a objetos superpuestos, así como en el caso de las calcomanías y los materiales de revestimiento de ventanas.
seo-title: Variación de la opacidad del material
solution: Experience Manager
title: Variación de la opacidad del material
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Variación de la opacidad del material{#varying-material-opacity}

Se admite la opacidad variable en el caso de colores sólidos y texturas repetibles aplicadas a objetos superpuestos, así como en el caso de las calcomanías y los materiales de revestimiento de ventanas.

La información sobre la opacidad se puede proporcionar simplemente utilizando una imagen RGB con un canal alfa. Además, la opacidad global puede variar con el `opacity=` comando (tanto para imágenes RGB como RGBA).

Los bordes de las paredes también admiten imágenes de RGBA, principalmente para admitir bordes cortados.

Los [!DNL vnw] archivos que definen las coberturas de ventana pueden incluir un canal de opacidad, que combina el procesador con el canal alfa de la textura repetible y el `opacity=` valor para proporcionar una gama completa de efectos de opacidad para los tratamientos de ventana pura y translúcida.
