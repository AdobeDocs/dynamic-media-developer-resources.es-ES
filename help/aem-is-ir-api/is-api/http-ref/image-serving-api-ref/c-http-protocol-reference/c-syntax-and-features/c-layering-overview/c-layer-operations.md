---
description: Además de cambiar el tamaño (size=) y la posición (pos=) de las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden rotar (rotate=) y voltear (flip=).
solution: Experience Manager
title: Operaciones de capa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Operaciones de capa{#layer-operations}

Además de cambiar el tamaño (size=) y la posición (pos=) de las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden rotar (rotate=) y voltear (flip=).

Los atributos `origin=` y `anchor=` se pueden usar para mantener la alineación deseada entre las capas cuando las imágenes o el texto se cambian dinámicamente en las plantillas.

El comando `maskUse=` está disponible para que las capas de imagen accedan al área de fondo de las imágenes que tienen máscaras independientes.

`opac=` se puede usar para variar la opacidad de la capa, y `hide=` para mostrar u ocultar la capa.
