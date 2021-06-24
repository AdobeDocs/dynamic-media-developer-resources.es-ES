---
description: El visualizador de vídeo interactivo es compatible con el procesamiento de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.
solution: Experience Manager
title: Compatibilidad con datos interactivos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Developer,Business Practitioner
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Compatibilidad con datos interactivos{#interactive-data-support}

El visualizador de vídeo interactivo es compatible con el procesamiento de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.

La muestra visible actualmente corresponde a la zona horaria del vídeo con la que está asociada. Al tocar o hacer clic en la muestra interactiva, se déclencheur la acción que se le asignó en el momento de la creación.

La muestra interactiva puede activar una vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o puede redirigir al usuario a una página web externa.

## Acerca de la vista rápida {#section-7990e44f641042d2a38ba20c9413b3f8}

Estos tipos de muestras interactivas se deben crear utilizando el tipo de acción &quot;vista rápida&quot; en AEM Assets - On-demand. Cuando un usuario activa una muestra de este tipo, el visor ejecuta `quickViewActivate` llamada de retorno de JavaScript y le pasa los datos de muestra. Se espera que la página web incrustante escuche esta llamada de retorno y, cuando déclencheur, la página abre su propia implementación de vista rápida.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

Muestras creadas para el tipo de acción &quot;vista rápida&quot; en AEM Assets: redireccionamiento bajo demanda del usuario a una URL externa. Según la configuración en el momento de la creación, la dirección URL se puede abrir en una nueva pestaña del explorador, en la misma ventana o en la ventana del explorador con nombre.
