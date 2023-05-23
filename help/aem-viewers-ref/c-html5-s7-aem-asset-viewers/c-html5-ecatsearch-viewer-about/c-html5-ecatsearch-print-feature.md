---
description: El visor permite enviar el contenido del catálogo a una impresora.
solution: Experience Manager
title: Función de impresión
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite enviar el contenido del catálogo a una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar utilizando el `printquality` parámetro de configuración. Tenga en cuenta que `printquality` no se recomienda usar en valores significativamente superiores a los predeterminados. El motivo es que lleva a un consumo de memoria muy alto por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su empresa de Dynamic Media Classic sea mayor que el configurado `printquality` valor.

>[!NOTE]
>
>La función Imprimir sólo está disponible en sistemas de escritorio, excepto Internet Explorer 9.
