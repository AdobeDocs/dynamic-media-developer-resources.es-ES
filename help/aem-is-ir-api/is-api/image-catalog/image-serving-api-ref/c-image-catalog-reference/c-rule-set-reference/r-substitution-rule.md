---
description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
solution: Experience Manager
title: sustitución
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 2%

---

# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en `<rule>` elementos.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Ninguno.

## Datos {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Cadena de sustitución.

## Descripción {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define una cadena de reemplazo para la cadena o subcadena coincidente de la ruta de acceso o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas por paréntesis), la primera subcadena coincidente se reemplaza por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

Si `<expression>` está vacío o ausente, la cadena de sustitución se anexa a la ruta de acceso o consulta.

Si `<substitution>` está vacío, se quita la cadena o subcadena coincidente. Si no se especifica `<substitution>`, no se modifica la ruta de acceso o la cadena de consulta.

>[!NOTE]
>
>Todas las coincidencias de la cadena de entrada se sustituyen cuando `replace="all"` se especifica en el elemento `<rule>`, al que pertenece este elemento `<substitution>`. De forma predeterminada, solo la primera coincidencia se reemplaza con la cadena de sustitución.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La cadena de sustitución no debe contener los caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
