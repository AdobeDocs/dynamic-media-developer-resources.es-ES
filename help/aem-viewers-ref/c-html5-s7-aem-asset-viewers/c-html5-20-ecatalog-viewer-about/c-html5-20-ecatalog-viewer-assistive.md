---
title: Soporte técnico de asistencia
description: Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Soporte técnico de asistencia{#assistive-technology-support}

Todos los componentes del visor admiten las funciones y atributos de ARIA (Aplicaciones de Internet enriquecidas accesibles) para mejorar la integración con tecnologías de asistencia, como lectores de pantalla.

El elemento del visualizador de nivel superior tiene una función `region` y `aria-label` establecido de forma predeterminada en el nombre del visor. Puede controlar la etiqueta con la variable `Container.LABEL` símbolo de localización.

Los botones tienen la función `button` y el texto descriptivo configurado con la variable `aria-label` atributo. El valor de `aria-label` se rellena a partir del valor del símbolo de localización del botón. Cuando un botón está desactivado, la variable `aria-disabled` se establece en consecuencia.

La vista principal tiene una función `application`. Puede obtener una breve descripción de la vista principal en `aria-roledescription`, con el valor definido por la variable `ROLE_DESCRIPTION` símbolo de localización del componente de vista principal correspondiente. Se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`, el texto de la sugerencia de uso proviene del `USAGE_HINT` símbolo de localización. Si un recurso tiene una etiqueta definida en el campo UserData , la variable `aria-label` se configura con el valor de dicha etiqueta.

Los puntos activos, las regiones y los mapas de imágenes tienen la función `button` y el texto descriptivo configurado con `aria-label` , con el valor de la etiqueta de zona activa o mapa de imagen. Cuando el usuario se centra en puntos interactivos o mapas de imágenes, se proporcionan sugerencias de navegación para los usuarios del teclado mediante `aria-describedby`, con el texto para las sugerencias de uso procedentes de la variable `USAGE_HINT` símbolo de localización.

Las miniaturas tienen la función `dialog` con `aria-label` el atributo controlado por la variable `ThumbnailGridView.LABEL` símbolo de localización. Las miniaturas individuales tienen una función `button`. Si se selecciona una miniatura, obtiene `aria-selected` establecido en `true`.

Los componentes que muestran muestras tienen la función `listbox` con `aria-label` establecido en el valor de la variable `LABEL` símbolo de localización de ese componente. Las muestras individuales tienen la función `option` con `aria-setsize` y `aria-posinset` para describir la posición de la muestra en el conjunto. Si se selecciona una muestra, se obtiene la variable `aria-selected` establecido en `true`.

Las listas desplegables se activan mediante botones con botones adicionales `aria-haspopup` establecido en `true` y `aria-controls` que hace referencia al elemento real del panel desplegable. El propio panel desplegable tiene la función `menu` con subelementos que tengan la función `menuitem`. Cada elemento de menú tiene la variable `aria-label` atributo especificado.

Los cuadros de diálogo modal tienen la función `dialog`. El elemento de encabezado del cuadro de diálogo al que hace referencia el `aria-labelledby` atributo.
