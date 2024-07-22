---
title: Actualización desde IS 4.7.4 o posterior
description: Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Actualización desde IS 4.7.4 o posterior{#updating-from-is-or-later}

Utilice este procedimiento al actualizar el servicio de imágenes de Dynamic Media.

Si está actualizando desde una versión anterior del servicio de imágenes, póngase en contacto con el servicio de asistencia para obtener el proceso correcto.

>[!NOTE]
>
>La carpeta [!DNL webapps] se puede eliminar en la actualización. Haga una copia de seguridad de la carpeta [!DNL webapps] antes de actualizar.

1. Inicie sesión en el host del servidor con privilegios administrativos.
1. Extraiga el contenido del archivo zip de distribución del servicio de imágenes.
1. Inicie el asistente de instalación ejecutando `setup/setup.exe`.
1. Seleccione **[!UICONTROL Siguiente]** para avanzar al Contrato de licencia para el usuario final (CLUF), lea el contrato de licencia y seleccione **[!UICONTROL Sí]**.

   La página siguiente muestra las opciones de configuración anteriores.
1. Haga clic en **[!UICONTROL Siguiente]** para iniciar la instalación de la actualización.

   >[!NOTE]
   >
   >El instalador realiza una copia de seguridad de los archivos de configuración del servidor antiguos en la carpeta [!DNL BACKUP/].

1. Una vez finalizada la instalación, seleccione **[!UICONTROL Finalizar]** para salir del asistente de instalación.

   A veces, el asistente de instalación puede pedirle que reinicie el sistema.

Durante una actualización, el archivo [!DNL ImageServing/conf/server.xml] se actualiza a la configuración más reciente. Si ha cambiado o agregado valores, debe guardar su [!DNL server.xml] existente y volver a implementar los cambios después de la actualización.

Después de realizar una instalación de actualización, considere la posibilidad de calentar la caché de respuestas HTTP antes de activar el servidor. Consulte la descripción de la utilidad `playlog` para obtener detalles.
