---
title: Instalación de varios visores de Dynamic Media en el mismo servidor
description: Instrucciones para instalar la API de visualizadores de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
TQID: 'https://experienceleague.adobe.com/Zz0BTc333AIELPKRWFeIxhNvTyOJZH1RHLYNvZpt-ZY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Instalación de varios visores en el mismo servidor{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instrucciones para instalar la API de visores de Dynamic Media.

Instale y pruebe el servicio de imágenes antes de instalar los visores del servicio de imágenes.

Copie los archivos de visores de IIS en el disco duro y, a continuación, implemente el archivo `s7viewers.war` en el directorio `../ImageServing/webapps`. Consulte la documentación del servicio de imágenes para obtener instrucciones sobre cómo implementar, iniciar, detener y administrar el servidor de imágenes.

>[!NOTE]
>
>No hay ninguna instalación de actualización para los visores del servicio de imágenes. Adobe recomienda realizar una copia de seguridad de cualquier directorio de visores de Dynamic Media (s7viewers) existente antes de continuar con la instalación.

**Para instalar varios visores en el mismo servidor:**

1. Cambie el nombre del archivo .war del visor al contexto deseado e implemente el archivo en la ubicación que desee.
1. Establecer el parámetro `this.isViewerRoot` en `config.js`.
1. Abra `config.js` en la raíz de la carpeta de visor recién creada.
1. Establezca el parámetro `this.isViewerRoot = "/s7viewers"` en el contexto del archivo `s7viewers.war`. Por ejemplo, `"/s7viewers-4.0"`.
1. Guarde el archivo y cierre.
