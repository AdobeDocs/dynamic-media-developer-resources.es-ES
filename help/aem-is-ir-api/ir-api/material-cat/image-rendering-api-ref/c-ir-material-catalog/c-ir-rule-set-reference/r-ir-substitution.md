---
title: sustitución
description: Elemento de cadena de sustitución. Opcional en elementos <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 3%

---

# sustitución{#substitution}

Elemento de cadena de sustitución. Opcional en `<rule>` elementos.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Ninguno.

## Datos {#section-a2688866ed6d41279a8478886e511ae3}

Cadena de sustitución.

## Descripción {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define una cadena de reemplazo para la cadena o subcadena coincidente de la ruta de acceso o consulta.

Si la expresión de patrón incluye subexpresiones (delimitadas por paréntesis), la primera subcadena coincidente se reemplaza por la cadena de sustitución. Si la expresión de patrón no incluye subexpresiones, se sustituye toda la cadena coincidente.

Si `<expression>` está vacío o ausente, la cadena de sustitución se anexa a la ruta de acceso o consulta.

Si `<substitution>` está vacío, se quita la cadena o subcadena coincidente. Si no se especifica `<substitution>`, no se modifica la ruta de acceso o la cadena de consulta.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La cadena de sustitución no debe contener los caracteres literales &lt; y &amp;. Estos caracteres reservados se pueden codificar con `&` y `<`, respectivamente, o toda la cadena se puede incluir en una sección XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`

