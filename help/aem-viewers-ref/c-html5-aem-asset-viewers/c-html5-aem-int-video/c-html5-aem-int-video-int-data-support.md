---
description: El visor de vídeo interactivo admite el procesamiento de muestras interactivas basadas en datos interactivos pasados al visor como parámetro de configuración.
seo-description: El visor de vídeo interactivo admite el procesamiento de muestras interactivas basadas en datos interactivos pasados al visor como parámetro de configuración.
seo-title: Compatibilidad con datos interactivos
solution: Experience Manager
title: Compatibilidad con datos interactivos
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Compatibilidad con datos interactivos{#interactive-data-support}

El visor de vídeo interactivo admite el procesamiento de muestras interactivas basadas en datos interactivos pasados al visor como parámetro de configuración.

La muestra visible actualmente corresponde a la región de tiempo de vídeo con la que está asociada. Al tocar o hacer clic en la muestra interactiva, se activa la acción que se le asigna en el momento de la creación.

La muestra interactiva puede activar una Vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o puede redirigir al usuario a una página web externa.

## Acerca de la Vista rápida {#section-7990e44f641042d2a38ba20c9413b3f8}

Estos tipos de muestras interactivas se deben crear con el tipo de acción &quot;vista rápida&quot; en Recursos AEM - On-demand. Cuando un usuario activa una muestra de este tipo, el visor ejecuta la llamada de retorno de `quickViewActivate` JavaScript y le pasa los datos de la muestra. Se espera que la página web de incrustación escuche esta llamada de retorno y cuando se activa, la página abre su propia implementación de Vista rápida.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

Muestras creadas para el tipo de acción &quot;vista rápida&quot; en Recursos AEM: redireccionamiento a petición del usuario a una URL externa. Según la configuración en el momento de la creación, la dirección URL se puede abrir en una nueva ficha de explorador, en la misma ventana o en la ventana de explorador con nombre.
