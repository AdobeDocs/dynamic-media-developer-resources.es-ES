---
title: Función de impresión
description: El visor permite generar el contenido del catálogo en una impresora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite generar el contenido del catálogo en una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar utilizando la variable `printquality` parámetro de configuración. Configuración `printquality` no se recomienda usar valores superiores a los predeterminados. La razón es que conduce a un alto consumo de memoria por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su empresa de Dynamic Media Classic sea mayor que el configurado `printquality` valor.

>[!NOTE]
>
>La función Imprimir solo está disponible en sistemas de escritorio, excepto Internet Explorer 9.
