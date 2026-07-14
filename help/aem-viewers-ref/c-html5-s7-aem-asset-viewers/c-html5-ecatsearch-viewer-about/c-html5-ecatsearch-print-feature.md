---
description: El visor permite enviar el contenido del catálogo a una impresora.
solution: Experience Manager
title: Función de impresión
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite enviar el contenido del catálogo a una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar mediante el parámetro de configuración `printquality`. Tenga en cuenta que no se recomienda configurar `printquality` en valores significativamente superiores a los predeterminados. El motivo es que lleva a un consumo de memoria muy alto por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su compañía de Dynamic Media Classic sea mayor que el valor `printquality` configurado.

>[!NOTE]
>
>La función Imprimir sólo está disponible en sistemas de escritorio, excepto Internet Explorer 9.

