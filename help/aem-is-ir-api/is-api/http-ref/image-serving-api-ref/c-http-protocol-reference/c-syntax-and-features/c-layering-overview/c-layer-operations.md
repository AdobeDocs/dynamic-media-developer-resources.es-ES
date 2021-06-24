---
description: Además de cambiar el tamaño (size=) y colocar (pos=) las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden girar (rotar=) y girar (flip=).
solution: Experience Manager
title: Operaciones de capa
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Operaciones de capa{#layer-operations}

Además de cambiar el tamaño (size=) y colocar (pos=) las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden girar (rotar=) y girar (flip=).

Los atributos `origin=` y `anchor=` pueden utilizarse para mantener la alineación deseada entre capas cuando las imágenes o el texto se cambian dinámicamente en las plantillas.

El comando `maskUse=` está disponible para que las capas de imagen accedan al área de fondo de las imágenes que tienen máscaras independientes.

`opac=` puede utilizarse para variar la opacidad de la capa y  `hide=` para mostrar u ocultar la capa.
