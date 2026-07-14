---
title: Actualización desde IS 4.7.4 o posterior
description: Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media en Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
TQID: 'https://experienceleague.adobe.com/RGRlIuemg6bPstlymZg7Ajr9i2ANq-HNjoIULaJydfs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 0%

---

# Actualización desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media en Linux®.

Si está actualizando desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de asistencia para obtener el proceso correcto.

La carpeta [!DNL webapps] se puede eliminar durante la actualización. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de actualizar.

1. Inicie sesión en el host del servidor con privilegios de raíz.
1. Descomprima y desmonte el archivo tar de distribución del servicio de imágenes.
1. En la carpeta [!DNL setup], ejecute [!DNL `./install-is`] para iniciar el asistente de instalación.

   El instalador de la actualización comprueba la integridad y la versión del paquete instalado. Si se ejecuta correctamente, se muestra el Contrato de licencia de usuario final (&quot;EULA&quot;).
1. Lea el contrato de licencia y, a continuación, escriba **[!UICONTROL y]** para continuar con la instalación.

   El instalador realiza una copia de seguridad de los archivos de configuración del servidor antiguos en la carpeta [!DNL BACKUP/].

   Una vez finalizada la instalación, aparece el siguiente mensaje:

   `Image Server was started successfully`

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado valores, guarde los [!DNL server.xml] existentes y vuelva a implementar los cambios después de la actualización.

Después de realizar una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción de la utilidad [!DNL playlog] para obtener detalles.

