---
title: Variables personalizadas
description: La parte de consulta de las solicitudes y las cadenas de modificador de viñeta pueden incluir variables definidas por el usuario.
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

La parte de consulta de las solicitudes y las cadenas de viñeta::Modifier pueden incluir variables definidas por el usuario.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nombre de variable. Puede consistir en cualquier combinación de caracteres alfa, dígitos y seguros, excepto `$`.

`[!DNL value]` : valor en el que se va a configurar la variable (cadena).

Las variables se definen de forma similar a otros comandos de servidor, utilizando la sintaxis anterior. Se deben definir las variables antes de poder hacer referencia a ellas. Variables definidas en `vignette::Modifier` se puede hacer referencia a en la solicitud de URL y a la inversa.

>[!NOTE]
>
>`[!DNL value]` debe tener codificación URL de un solo paso para la transmisión HTTP segura. Se requiere codificación doble si `[!DNL value]` se retransmite mediante HTTP. Este es el caso cuando `[!DNL value]` se sustituye en una solicitud externa anidada.

Se hace referencia a las variables incrustando el nombre de la variable (entre una inicial y una final) `$`) en cualquier lugar de los valores de comando. Por ejemplo, entre las variables `=`  después del nombre del comando y el siguiente `&` o el final de la solicitud. El servidor sustituye cada incidencia de `$ [!DNL name]$` con `[!DNL string]`. No se producen sustituciones en ninguna incidencia de `$ [!DNL name]$` en nombres de comando (antes del signo igual de un comando) y en la parte de ruta de la solicitud.

Las variables personalizadas no pueden estar anidadas. Cualquier incidencia de `$ [!DNL name]$` dentro `[!DNL string]` no se sustituyen. Por ejemplo, el fragmento de solicitud `$var2=apple&$var1=my$var2$tree&text=$var1$` se resuelve en `text=my$var2$tree`.

`$` no es un carácter reservado; puede ocurrir de otra manera en la solicitud. Por ejemplo, `src=my$texture$file.tif` es un comando válido (suponiendo que una entrada de catálogo de material o un fichero de textura llamado `[!DNL my$texture$file.tif]` existe), mientras que `wid=$number$` no es, porque `wid=` requiere un argumento numérico.
