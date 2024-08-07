---
title: Función de impresión
description: El visor permite enviar el contenido del catálogo a una impresora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite enviar el contenido del catálogo a una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar mediante el parámetro de configuración `printquality`. No se recomienda establecer `printquality` en valores superiores al valor predeterminado. La razón es que lleva a un alto consumo de memoria por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su compañía de Dynamic Media Classic sea mayor que el valor `printquality` configurado.

>[!NOTE]
>
>La función Imprimir sólo está disponible en sistemas de escritorio, excepto Internet Explorer 9.
