---
title: Compatibilidad con datos interactivos
description: El visualizador de vídeo interactivo admite la representación de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 0%

---

# Compatibilidad con datos interactivos{#interactive-data-support}

El visualizador de vídeo interactivo admite la representación de muestras interactivas basadas en datos interactivos pasados al visualizador como parámetro de configuración.

La muestra visible actualmente corresponde a la región horaria del vídeo con la que está asociada. Al tocar o hacer clic en la muestra interactiva, se déclencheur la acción asignada en el momento del autor.

La muestra interactiva puede activar una vista rápida en la página web de alojamiento activando una llamada de retorno de JavaScript o puede redirigir al usuario a una página web externa.

## Acerca de Quickview {#section-7990e44f641042d2a38ba20c9413b3f8}

Estos tipos de muestras interactivas deben crearse con el tipo de acción &quot;quickview&quot; en Adobe Experience Manager Assets: bajo demanda. Cuando un usuario activa una muestra de este tipo, el visor ejecuta `quickViewActivate` llamada de retorno de JavaScript y le pasa los datos de la muestra. Se espera que la página web de incrustación escuche esta llamada de retorno y cuando entre en déclencheur, la página abrirá su propia implementación de vista rápida.

## Redirigir a una página web externa {#section-32ebe3c3a7f74892a428c5d48801de4d}

Las muestras creadas para el tipo de acción &quot;vista rápida&quot; en Experience Manager Assets - bajo demanda redirigen al usuario a una URL externa. Según la configuración en el momento de la creación, la URL se puede abrir en una nueva pestaña del explorador, en la misma ventana o en la ventana del explorador con nombre.
