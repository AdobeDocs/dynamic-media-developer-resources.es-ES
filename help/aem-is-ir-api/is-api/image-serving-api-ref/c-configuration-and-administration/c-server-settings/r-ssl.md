---
description: Utilice esta configuración de servidor para SSL.
seo-description: Utilice esta configuración de servidor para SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---


# SSL{#ssl}

Utilice esta configuración de servidor para SSL.

## TC::SslPort - Puerto de escucha {#section-c80eb582bf684b3fa7313a77cc606769}

Especifica el puerto de escucha para las conexiones SSL de Platform Server. El valor predeterminado es 8443.

## TC::keystoreFile - Ruta del archivo del almacén de claves {#section-0cdf9b3cfcf249818b22221d01bafebe}

Especifique la ruta/nombre del archivo SSL keystore. Puede ser una ruta absoluta o una ruta relativa a [!DNL *[!DNL install_folder]*/conf]. El valor predeterminado es *install_folder*/conf/scene7keystore.

## TC::keystorePass - Contraseña de keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

La contraseña del archivo de almacén de claves. El valor predeterminado es `scene7`.

## TC::keystoreType - Tipo de almacén de claves {#section-8f263e1ba67740728cd39181960d7c7d}

Seleccione el tipo de almacén de claves. Se admiten &#39; `Java'` (predeterminado) y &#39; `PKCS12`&#39;.
