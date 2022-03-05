---
title: Variación de la opacidad del material
description: La opacidad variable es compatible con el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como con las calcomanías y los materiales de recubrimiento de ventanas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Variación de la opacidad del material{#varying-material-opacity}

La opacidad variable es compatible con el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como con las calcomanías y los materiales de recubrimiento de ventanas.

La información de opacidad se puede proporcionar simplemente utilizando una imagen de RGB con un canal alfa. Además, la opacidad general puede variar con el `opacity=` (tanto para imágenes RGB como RGBA).

Los bordes murales también admiten imágenes RGBA, principalmente para soportar fronteras cortadas.

La variable [!DNL vnw] los archivos que definen las coberturas de ventanas pueden incluir un canal de opacidad. Se combina con el procesador con el canal alfa de la textura repetible y el `opacity=` para proporcionar una gama completa de efectos de opacidad para tratamientos por cristaleras y traslúcidos.
