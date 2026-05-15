---
title: Soporte de tecnología de asistencia
description: Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
TQID: 'https://experienceleague.adobe.com/EyKChB9ZeEsHHy7alcGBi7IrrdElXI8gD88t-AwbwBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 253
ht-degree: 0%

---

# Soporte de tecnología de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten los roles y atributos ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia como lectores de pantalla.

El elemento de visor de nivel superior tiene la función `region` y el atributo `aria-label` establecidos de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con el símbolo de localización `Container.LABEL`.

Los botones tienen el rol `button` y el texto descriptivo establecido con el atributo `aria-label`. El valor del atributo `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando se deshabilita un botón, el atributo `aria-disabled` se establece en consecuencia.

Los componentes del control deslizante tienen la función `slider` con los atributos `aria-valuenow`, `aria-valuemin` y `aria-valuemax` para describir la posición actual del control deslizante.

Las miniaturas tienen el rol `dialog` con el atributo `aria-label` controlado por el símbolo de localización `ThumbnailGridView.LABEL`. Las miniaturas individuales tienen el rol `button`. Si se selecciona una miniatura, se obtiene el atributo `aria-selected` establecido en `true`.

Los componentes que muestran muestras tienen el rol `listbox` con el atributo `aria-label` establecido en el valor del símbolo de localización `LABEL` de ese componente. Las muestras individuales tienen el rol `option` con los atributos `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene el atributo `aria-selected` establecido en `true`.

Las listas desplegables se activan mediante botones con el atributo adicional `aria-haspopup` establecido en `true` y el atributo `aria-controls` que hace referencia al elemento del panel desplegable real. El panel desplegable tiene el rol `menu` con subelementos que tienen el rol `menuitem`. Cada elemento de menú tiene especificado el atributo `aria-label`.

Los cuadros de diálogo modales tienen la función `dialog`. El atributo `aria-labelledby` hace referencia al elemento de encabezado del cuadro de diálogo.
