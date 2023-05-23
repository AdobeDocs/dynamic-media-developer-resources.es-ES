---
title: Actualización desde IS 4.7.4 o posterior
description: Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media en Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Actualización desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media en Linux®.

Si está actualizando desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de asistencia para obtener el proceso correcto.

El [!DNL webapps] La carpeta se puede eliminar durante la actualización. Haga una copia de seguridad del [!DNL webapps] antes de la actualización.

1. Inicie sesión en el host del servidor con privilegios de raíz.
1. Descomprima y desmonte el archivo tar de distribución del servicio de imágenes.
1. En el [!DNL setup] carpeta, ejecutar [!DNL `./install-is`] para iniciar el asistente de instalación.

   El instalador de la actualización comprueba la integridad y la versión del paquete instalado. Si se ejecuta correctamente, se muestra el Contrato de licencia de usuario final (&quot;EULA&quot;).
1. Lea el contrato de licencia y escriba **[!UICONTROL y]** para continuar con la instalación.

   El instalador realiza una copia de seguridad de los archivos de configuración del servidor antiguos en [!DNL BACKUP/] carpeta.

   Una vez finalizada la instalación, aparece el siguiente mensaje:

   `Image Server was started successfully`

Durante una actualización, la variable [!DNL ImageServing/conf/server.xml] El archivo de se ha actualizado a la configuración más reciente. Si ha cambiado o agregado valores, guarde los existentes [!DNL server.xml] y vuelva a implementar los cambios después de la actualización.

Después de realizar una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción de [!DNL playlog] para obtener más información.
