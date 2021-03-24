---
description: La opacidad variable es compatible con el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como con las calcomanías y los materiales de recubrimiento de ventanas.
solution: Experience Manager
title: Variación de la opacidad del material
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Variación de la opacidad del material{#varying-material-opacity}

La opacidad variable es compatible con el color sólido y las texturas repetibles aplicadas a objetos superpuestos, así como con las calcomanías y los materiales de recubrimiento de ventanas.

La información de opacidad se puede proporcionar simplemente utilizando una imagen RGB con un canal alfa. Además, la opacidad general puede variar con el comando `opacity=` (tanto para imágenes RGB como RGBA).

Los bordes murales también admiten imágenes RGBA, principalmente para soportar fronteras cortadas.

Los archivos [!DNL vnw] que definen las coberturas de las ventanas pueden incluir un canal de opacidad, que es combinado por el procesador con el canal alfa de la textura repetible y el valor `opacity=` para proporcionar una gama completa de efectos de opacidad para los tratamientos de las ventanas delgadas y translúcidas.
