---
description: Máscara de imagen. Solicita los datos de la máscara (canal alfa).
solution: Experience Manager
title: enmascarar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# enmascarar{#mask}

Máscara de imagen. Solicita los datos de la máscara (canal alfa).

`req=mask`

Admite los mismos comandos que `req=img`. El servidor la procesa del mismo modo, pero en lugar de devolver los datos de RGB o RGBA, descarta la información de color y devuelve únicamente los datos de la máscara (canal alfa). El formato de datos de respuesta y el tipo MIME de respuesta están determinados por `fmt=`.

La respuesta HTTP se puede almacenar en caché con el TTL basado en `catalog::Expiration`.
