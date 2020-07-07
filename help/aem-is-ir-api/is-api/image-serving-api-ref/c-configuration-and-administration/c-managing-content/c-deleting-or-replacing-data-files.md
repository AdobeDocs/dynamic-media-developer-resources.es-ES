---
description: Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar estos archivos, se recomienda asignar un nuevo nombre al archivo de reemplazo (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.
seo-description: Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar estos archivos, se recomienda asignar un nuevo nombre al archivo de reemplazo (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.
seo-title: Eliminación o reemplazo de archivos de datos
solution: Experience Manager
title: Eliminación o reemplazo de archivos de datos
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Eliminación o reemplazo de archivos de datos{#deleting-or-replacing-data-files}

Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar estos archivos, se recomienda asignar un nuevo nombre al archivo de reemplazo (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.

>[!NOTE]
>
>Los archivos de datos no deben reemplazarse ni eliminarse durante el uso activo del servicio de imágenes. De lo contrario, pueden producirse errores o incluso un bloqueo del servidor.

En todos los casos, recuerde que la caché de Platform Server y las entradas de caché de cliente deben estar obsoletas antes de que el cliente vea los datos actualizados. Las entradas específicas de la caché se pueden actualizar inmediatamente mediante el `cache=validate` comando.

El administrador de caché no realiza un seguimiento directo de los cambios en los archivos de fuente y los archivos de perfil ICC. Si dicho recurso se modifica sin cambiar su ID, la caché del servidor no conocerá el cambio y no `cache=validate` hará que se actualice la entrada de caché. `cache=update` puede utilizarse para forzar la regeneración de dichas entradas de caché.

Para evitar las complicaciones de reemplazar archivos, se recomienda asignar un nombre nuevo a un archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permitirá reemplazar cualquier archivo de datos mientras el servidor esté activo y hará que las entradas de caché del servidor se vuelvan obsoletas inmediatamente sin ninguna intervención adicional. Este método se puede utilizar para perfiles ICC, fuentes y todas las imágenes administradas por catálogos de imágenes.
