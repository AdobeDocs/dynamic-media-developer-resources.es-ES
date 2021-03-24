---
description: El visor permite generar el contenido del catálogo en una impresora.
solution: Experience Manager
title: Función de impresión
feature: Dynamic Media Classic,Visualizadores,SDK/API,Búsqueda de catálogos electrónicos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Función de impresión{#print-feature}

El visor permite generar el contenido del catálogo en una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar utilizando el parámetro de configuración `printquality`. Tenga en cuenta que no se recomienda establecer `printquality` en valores significativamente superiores a los predeterminados. La razón es que lleva a un consumo de memoria muy alto por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su empresa de Dynamic Media Classic sea mayor que el valor configurado `printquality`.

>[!NOTE]
>
>La función Imprimir solo está disponible en sistemas de escritorio, excepto Internet Explorer 9.

