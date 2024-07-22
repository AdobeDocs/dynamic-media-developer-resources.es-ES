---
description: Utilice esta configuración de servidor para SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# SSL{#ssl}

Utilice esta configuración de servidor para SSL.

## TC::SslPort: Puerto de escucha {#section-c80eb582bf684b3fa7313a77cc606769}

Especifica el puerto de escucha para [!DNL Platform Server] para conexiones SSL. El valor predeterminado es 8443.

## TC::keystoreFile: ruta de archivo del almacén de claves {#section-0cdf9b3cfcf249818b22221d01bafebe}

Especifique la ruta/nombre del archivo del almacén de claves SSL. Puede ser una ruta absoluta o una ruta relativa a [!DNL *[!DNL install_folder]*/conf]. El valor predeterminado es *install_folder*/conf/scene7keystore.

## TC::keystorePass: contraseña de Keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Contraseña del archivo de almacén de claves. El valor predeterminado es `scene7`.

## TC::keystoreType - Tipo de almacén de claves {#section-8f263e1ba67740728cd39181960d7c7d}

Seleccione el tipo de almacén de claves. Se admiten &#39; `Java'` (predeterminado) y &#39; `PKCS12`&#39;.
