---
description: El visor permite imprimir el contenido del catálogo en una impresora.
seo-description: El visor permite imprimir el contenido del catálogo en una impresora.
seo-title: Función de impresión
solution: Experience Manager
title: Función de impresión
topic: Dynamic media
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Función de impresión{#print-feature}

El visor permite imprimir el contenido del catálogo en una impresora.

La función de impresión se activa mediante un botón dedicado en la barra de herramientas. Al hacer clic en el botón, el usuario puede elegir un intervalo de impresión y el número de páginas por hoja.

La calidad de la impresión se puede ajustar utilizando el parámetro de configuración `printquality` . Tenga en cuenta que no se recomienda establecer `printquality` en valores significativamente superiores a los predeterminados. La razón es que lleva a un consumo de memoria muy alto por parte del navegador web en el sistema del cliente. Además, asegúrese de que el tamaño máximo de respuesta de la imagen establecido para la compañía de SPS es mayor que el valor `printquality` configurado.

>[!NOTE]
>
>La función Imprimir solo está disponible en sistemas de escritorio, excepto en Internet Explorer 9.

