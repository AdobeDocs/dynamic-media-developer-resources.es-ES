---
description: Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar esos archivos, se recomienda dar al archivo de reemplazo un nuevo nombre (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.
seo-description: Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar esos archivos, se recomienda dar al archivo de reemplazo un nuevo nombre (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.
seo-title: Eliminación o reemplazo de archivos de datos
solution: Experience Manager
title: Eliminación o reemplazo de archivos de datos
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Eliminación o reemplazo de archivos de datos{#deleting-or-replacing-data-files}

Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de simplemente reemplazar esos archivos, se recomienda dar al archivo de reemplazo un nuevo nombre (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez activado el nuevo archivo, se puede eliminar la versión antigua.

>[!NOTE]
>
>Los archivos de datos no deben reemplazarse ni eliminarse nunca mientras el servicio de imágenes los utiliza activamente. De lo contrario, podrían producirse errores o incluso un bloqueo del servidor.

En todos los casos, recuerde que la caché de Platform Server y las entradas de la caché del cliente deben quedar obsoletas antes de que el cliente vea los datos actualizados. Las entradas específicas de la caché se pueden actualizar inmediatamente mediante el comando `cache=validate`.

El administrador de caché no realiza un seguimiento directo de los cambios en los archivos de fuente y los archivos de perfil ICC. Si se modifica un recurso de este tipo sin cambiar su id, la caché del servidor no conocerá el cambio y `cache=validate` no hará que la entrada de caché se actualice. `cache=update` se puede utilizar para forzar la regeneración de estas entradas de caché.

Para evitar las complicaciones de reemplazar archivos, se recomienda dar un nombre nuevo a un archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permitirá reemplazar cualquier archivo de datos mientras el servidor está activo, y hará que las entradas de caché del servidor se queden obsoletas inmediatamente sin intervención adicional. Este método se puede utilizar para perfiles ICC, fuentes y todas las imágenes administradas por catálogos de imágenes.
