---
title: Instalación por primera vez
description: Este procedimiento muestra cómo instalar Image Serving por primera vez en Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Instalación por primera vez{#installing-for-the-first-time}

Este procedimiento muestra cómo instalar Image Serving por primera vez en Linux®.

1. Inicie sesión en el host del servidor con permisos de raíz.
1. Cree la carpeta [!DNL /usr/local/scene7/licenses].

   Si el archivo de clave de licencia del servicio de imágenes o del procesamiento de imágenes (con [!DNL .sc8] archivo (sufijo) está disponible, cópielo en esta carpeta. De lo contrario, continúe con la instalación e instale la clave de licencia más adelante.
1. Descomprima y desmonte el archivo tar de distribución del servicio de imágenes.
1. En el [!DNL Setup] carpeta, inicie el asistente de instalación ejecutando [!DNL ./install-is].

   Si no se encuentra ninguna clave de licencia, se muestran instrucciones que describen cómo obtener un archivo de licencia. Hágalo en este momento o continúe con la instalación del servicio de imágenes e instale la clave de licencia más adelante.
1. Cuando aparezca el Acuerdo de licencia del usuario final (CLUF), lea el acuerdo de licencia y, a continuación, escriba `y` para continuar.

   El instalador muestra los indicadores que aparecen en la tabla siguiente.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha principal [8080]:</span> </p> </td>
   <td colname="col2"> <p>Puerto de escucha HTTP principal para el servicio y el procesamiento de imágenes. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Puerto de escucha de administrador [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Puerto de escucha del administrador. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Tamaño máximo de caché HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Tamaño inicial de la caché de respuestas principal. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Carpeta raíz de caché [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Carpeta de caché de PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID de propietario del servidor de imágenes [root]:</span> </p> </td>
   <td colname="col2"> <p>La cuenta de usuario en la que se instalará el servidor de Image Serving. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Id. de grupo de Image Server [root]:</span> </p> </td>
   <td colname="col2"> <p>La cuenta de grupo en la que se instalará el servidor de servicio de imágenes. </p> </td>
  </tr>
 </tbody>
</table>

1. Prensa **[!UICONTROL Entrar]** para aceptar el valor predeterminado o especificar un valor diferente.

   Asegúrese de que todos los números de puerto especificados sean únicos y no se utilicen en caso contrario en este host.

   >[!IMPORTANT]
   >
   >Si se especifica una cuenta que no sea raíz, debe asegurarse de que los permisos de acceso para todos los archivos y carpetas que el servidor de imágenes necesita leer y escribir estén correctamente configurados cuando estas carpetas se reconfiguren en los archivos de configuración.
   >
   >El servicio de imágenes ahora está instalado en [!DNL /usr/local/Scene7/ImageServing]. Algunos contenidos de Image Rendering están instalados en [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Hacia el final de la instalación, el asistente de instalación intenta iniciar Image Server. Si no se encuentra ninguna clave de licencia válida, el servidor de imágenes no se podrá iniciar. Si hay una licencia válida y el servidor de imágenes sigue sin iniciarse, consulte los archivos de registro.

>[!NOTE]
>
>Si la licencia se instala después de instalar el servicio de imágenes, el servidor de imágenes debe iniciarse manualmente antes de su uso.
