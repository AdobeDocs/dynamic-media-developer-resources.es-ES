---
description: El visor permite generar el contenido del catálogo en una impresora.
solution: Experience Manager
title: Función de impresión
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Developer,Business Practitioner
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite generar el contenido del catálogo en una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar utilizando el parámetro de configuración `printquality`. Tenga en cuenta que no se recomienda establecer `printquality` en valores significativamente superiores a los predeterminados. La razón es que lleva a un consumo de memoria muy alto por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su empresa de Dynamic Media Classic sea mayor que el valor configurado `printquality`.

>[!NOTE]
>
>La función Imprimir solo está disponible en sistemas de escritorio, excepto Internet Explorer 9.
