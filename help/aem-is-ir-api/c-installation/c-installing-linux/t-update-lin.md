---
title: Actualización de IS 4.7.4 o posterior
description: Utilice este procedimiento al actualizar Dynamic Media Image Serving en Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Actualización de IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar Dynamic Media Image Serving en Linux®.

Si está actualizando desde una versión anterior de Image Serving, póngase en contacto con el servicio de asistencia técnica para el proceso correcto.

La variable [!DNL webapps] se puede eliminar al actualizar. Haga una copia de seguridad del [!DNL webapps] antes de la actualización.

1. Inicie sesión en el host del servidor con privilegios de root.
1. Descomprima y descomprima el archivo tar de distribución de Image Serving.
1. En el [!DNL setup] carpeta, ejecutar [!DNL `./install-is`] para iniciar el asistente de instalación.

   El instalador de actualización comprueba la integridad y la versión del paquete instalado. Si se realiza correctamente, se muestra el Acuerdo de licencia del usuario final (&quot;EULA&quot;).
1. Lea el contrato de licencia y, a continuación, introduzca **[!UICONTROL y]** para continuar con la instalación.

   El instalador realiza una copia de seguridad de los archivos de configuración del servidor antiguos en la [!DNL BACKUP/] carpeta.

   Cuando se completa la instalación, se muestra el siguiente mensaje:

   `Image Server was started successfully`

Durante una actualización, la variable [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado valores, guarde los [!DNL server.xml] y vuelva a implementar los cambios después de la actualización.

Después de una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción del [!DNL playlog] para obtener más información.
