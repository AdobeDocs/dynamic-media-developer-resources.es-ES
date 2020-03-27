---
description: Instrucciones para instalar la API de visores de Scene7.
seo-description: Instrucciones para instalar la API de visores de Scene7.
seo-title: Instalación de varios visores en el mismo servidor
solution: Experience Manager
title: Instalación de varios visores en el mismo servidor
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Instalación de varios visores en el mismo servidor{#installing-multiple-viewers-on-the-same-server}

Instrucciones para instalar la API de visores de Scene7.

Instale y pruebe el servicio de imágenes antes de instalar los visores del servicio de imágenes.

Copie los archivos de visores de IS en el disco duro y, a continuación, implemente el `s7viewers.war` archivo en el `../ImageServing/webapps` directorio. Consulte la documentación del servicio de imágenes para obtener instrucciones sobre cómo implementar, inicio, detener y administrar el servidor de imágenes.

>[!NOTE]
>
>No hay ninguna instalación de actualización para los visores de servicio de imágenes. Adobe recomienda realizar una copia de seguridad de cualquier directorio de visores de Scene7 existente antes de continuar con la instalación.

**Para instalar los visores en el mismo servidor**

1. Cambie el nombre del archivo .war del visor al contexto deseado e implemente el archivo en la ubicación que desee.
1. Defina `this.isViewerRoot` el parámetro en `config.js`.
1. Se abre `config.js` en la raíz de la carpeta del visor recién creada.
1. Establezca el parámetro `this.isViewerRoot = "/s7viewers"` en el contexto del `s7viewers.war` archivo. Por ejemplo, `"/s7viewers-4.0"`. Guarde y cierre el archivo.
1. Guarde el archivo y cierre.
