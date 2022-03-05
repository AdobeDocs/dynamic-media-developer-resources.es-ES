---
title: Variables personalizadas
description: La parte de consulta de las solicitudes y las cadenas de Modificador de viñeta pueden incluir variables definidas por el usuario.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Variables personalizadas{#custom-variables}

La parte de consulta de las solicitudes y las cadenas de viñeta::Modifier puede incluir variables definidas por el usuario.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nombre de la variable. Puede consistir en cualquier combinación de caracteres alfa, dígito y caracteres seguros, excepto `$`.

`[!DNL value]` - Valor al que se debe configurar la variable (cadena).

Las variables se definen de forma similar a otros comandos del servidor, utilizando la sintaxis anterior. Para poder hacer referencia a las variables es necesario definirlas. Variables definidas en `vignette::Modifier` se puede hacer referencia a él en la solicitud de URL y, a la inversa.

>[!NOTE]
>
>`[!DNL value]` debe tener codificación de dirección URL de paso único para la transmisión HTTP segura. Se requiere una codificación doble si `[!DNL value]` se retransmite mediante HTTP. Esta situación es así cuando `[!DNL value]` se sustituye en una solicitud externa anidada.

Para hacer referencia a las variables, incruste el nombre de la variable (entre un encabezado y un final) `$`) en cualquier lugar de los valores de comando. Por ejemplo, entre la variable `=`  siguiendo el nombre de comando y las `&` o el final de la solicitud. El servidor sustituye a cada incidencia de `$ [!DNL name]$` con `[!DNL string]`. No se producen sustituciones en ninguna ocurrencia de `$ [!DNL name]$` en nombres de comando (antes del signo igual de un comando) y en la parte de ruta de la solicitud.

Es posible que las variables personalizadas no estén anidadas. Cualquier ocurrencia de `$ [!DNL name]$` en `[!DNL string]` no se sustituyen. Por ejemplo, el fragmento de solicitud `$var2=apple&$var1=my$var2$tree&text=$var1$` resuelve a `text=my$var2$tree`.

`$` no es un carácter reservado; de lo contrario, podría ocurrir en la solicitud. Por ejemplo, `src=my$texture$file.tif` es un comando válido (suponiendo que una entrada de catálogo de material o un archivo de textura denominado `[!DNL my$texture$file.tif]` existe), while `wid=$number$` no, porque `wid=` requiere un argumento numérico.
