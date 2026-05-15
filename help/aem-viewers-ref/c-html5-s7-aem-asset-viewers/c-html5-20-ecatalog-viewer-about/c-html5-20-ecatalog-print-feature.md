---
title: Función de impresión
description: El visor permite enviar el contenido del catálogo a una impresora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
TQID: 'https://experienceleague.adobe.com/5eIB7D6O7-d8prjO0MJ9PzUU9TPQe7SZcZAEtznPsv4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Función de impresión{#print-feature}

El visor permite enviar el contenido del catálogo a una impresora.

La función de impresión se activa mediante un botón específico en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar mediante el parámetro de configuración `printquality`. No se recomienda establecer `printquality` en valores superiores al valor predeterminado. La razón es que lleva a un alto consumo de memoria por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de imagen establecido para su compañía de Dynamic Media Classic sea mayor que el valor `printquality` configurado.

>[!NOTE]
>
>La función Imprimir sólo está disponible en sistemas de escritorio, excepto Internet Explorer 9.
