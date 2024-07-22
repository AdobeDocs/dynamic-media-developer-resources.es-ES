---
description: Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de reemplazar simplemente estos archivos, se recomienda dar un nuevo nombre al archivo de reemplazo (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez que el nuevo archivo se ha publicado, se puede eliminar la versión antigua.
solution: Experience Manager
title: Eliminar o reemplazar archivos de datos
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Eliminar o reemplazar archivos de datos{#deleting-or-replacing-data-files}

Aunque la adición de nuevos archivos de datos es sencilla y directa, se debe tener especial cuidado al reemplazar los archivos de datos existentes que el servidor utiliza activamente. En lugar de reemplazar simplemente estos archivos, se recomienda dar un nuevo nombre al archivo de reemplazo (por ejemplo, anexar un sufijo de versión al nombre del archivo). Una vez que el nuevo archivo se ha publicado, se puede eliminar la versión antigua.

>[!NOTE]
>
>Los archivos de datos nunca deben reemplazarse ni eliminarse mientras el servicio de imágenes los esté utilizando activamente. De lo contrario, pueden producirse errores o incluso un bloqueo del servidor.

En todos los casos, recuerde que la caché de [!DNL Platform Server] y las entradas de la caché del cliente deben quedar obsoletas antes de que el cliente vea los datos actualizados. Las entradas de caché específicas se pueden actualizar inmediatamente con el comando `cache=validate`.

El administrador de caché no realiza un seguimiento directo de los cambios en los archivos de fuente y los archivos de perfil ICC. Si se modifica un recurso de este tipo sin cambiar su identificador, la caché del servidor no conoce el cambio y `cache=validate` no hace que se actualice la entrada de caché. `cache=update` se puede usar para forzar la regeneración de dichas entradas de caché.

Para evitar las complicaciones derivadas de reemplazar archivos, se recomienda dar un nuevo nombre al archivo de reemplazo y actualizar las entradas de catálogo correspondientes. Esto permite reemplazar cualquier archivo de datos mientras el servidor esté activo y hace que las entradas de la caché del servidor queden obsoletas inmediatamente sin ninguna intervención adicional. Este método se puede utilizar para perfiles ICC, fuentes y todas las imágenes gestionadas por catálogos de imágenes.
