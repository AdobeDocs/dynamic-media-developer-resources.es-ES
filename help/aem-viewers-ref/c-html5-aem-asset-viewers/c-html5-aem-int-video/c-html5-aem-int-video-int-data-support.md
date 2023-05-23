---
title: Compatibilidad con datos interactivos
description: El visualizador de vídeo interactivo admite la representación de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Compatibilidad con datos interactivos{#interactive-data-support}

El visualizador de vídeo interactivo admite la representación de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.

La muestra visible actualmente corresponde a la región horaria del vídeo con la que está asociada. Al tocar o hacer clic en la muestra interactiva, se déclencheur la acción asignada en el momento del autor.

La muestra interactiva puede activar una vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o puede redirigir al usuario a una página web externa.

## Acerca de Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Estos tipos de muestras interactivas deben crearse con el tipo de acción &quot;vista rápida&quot; en Adobe Experience Manager Assets: bajo demanda. Cuando un usuario activa una muestra de este tipo, se ejecuta el visor `quickViewActivate` Llamada de retorno de JavaScript y le pasa los datos de muestra. Se espera que la página web de incrustación escuche esta llamada de retorno y cuando entre en déclencheur, la página abrirá su propia implementación de vista rápida.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

Las muestras creadas para el tipo de acción &quot;vista rápida&quot; en Experience Manager Assets - bajo demanda redirigen al usuario a una URL externa. Según la configuración en el momento de la creación, la URL se puede abrir en una nueva pestaña del explorador, en la misma ventana o en la ventana del explorador con nombre.
