---
title: Restricciones
description: Se aplican algunas restricciones para anidar e incrustar.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# Restricciones{#restrictions}

Se aplican algunas restricciones para anidar e incrustar.

Para obtener un buen rendimiento del servidor, la resolución de las imágenes devueltas por las solicitudes anidadas debe coincidir razonablemente con la resolución de textura de los objetos a los que se aplica el material.

Las imágenes externas se almacenan en caché localmente. Cualquier cambio en estas imágenes se detecta solo después de que la entrada de la caché local quede obsoleta (según el encabezado HTTP expires ).

