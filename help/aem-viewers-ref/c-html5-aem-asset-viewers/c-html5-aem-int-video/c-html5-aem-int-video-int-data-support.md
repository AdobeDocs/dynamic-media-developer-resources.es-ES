---
description: El visualizador de vídeo interactivo es compatible con el procesamiento de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.
seo-description: El visualizador de vídeo interactivo es compatible con el procesamiento de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.
seo-title: Compatibilidad con datos interactivos
solution: Experience Manager
title: Compatibilidad con datos interactivos
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '255'
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
