---
title: Procesamiento de variables en solicitudes anidadas
description: Las referencias $var$ pueden producirse en cualquier lugar dentro de las llaves de una solicitud de servicio o procesamiento de imágenes anidada, incluso a la izquierda de "?" que separa la ruta de la consulta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Procesamiento de variables en solicitudes anidadas{#variable-processing-in-nested-requests}

Las referencias $var$ pueden producirse en cualquier lugar dentro de las llaves de una solicitud de servicio o procesamiento de imágenes anidada, incluso a la izquierda de &quot;?&quot; que separa la ruta de la consulta.

El servidor sustituye estas referencias por valores (desde la dirección URL o desde `catalog::Modifier` del catálogo de imágenes principal) antes de analizar y procesar más la solicitud anidada.

Además, todas las definiciones de `$ *[!DNL var]*=` de la dirección URL y `catalog::Modifier` se reenvían a todas las solicitudes anidadas de servicio y procesamiento de imágenes. Al hacerlo, se asegura de que todas las definiciones de variables estén disponibles para todas las plantillas, independientemente del nivel de anidación.

Independientemente del nivel de anidamiento, solo se debe aplicar la codificación HTTP de un solo paso a los valores de variable que se van a sustituir en cualquier lugar de las solicitudes anidadas de Image Rendering o Image Serving.

