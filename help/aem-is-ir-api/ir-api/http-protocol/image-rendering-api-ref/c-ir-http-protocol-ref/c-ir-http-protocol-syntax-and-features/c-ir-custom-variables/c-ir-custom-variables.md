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

`[!DNL name]` - Nombre de variable. Puede consistir en cualquier combinación de caracteres alfanuméricos, dígitos y caracteres seguros, excluyendo `$`.

`[!DNL value]` - Valor en el que se va a establecer la variable (cadena).

Las variables se definen de forma similar a otros comandos de servidor, utilizando la sintaxis anterior. Se deben definir las variables antes de poder hacer referencia a ellas. Se puede hacer referencia a las variables definidas en `vignette::Modifier` en la solicitud de URL y a la inversa.

>[!NOTE]
>
>`[!DNL value]` debe tener codificación URL de un solo paso para la transmisión HTTP segura. Se requiere una codificación doble si `[!DNL value]` se retransmite mediante HTTP. Este es el caso cuando `[!DNL value]` se sustituye en una solicitud externa anidada.

Se hace referencia a las variables incrustando el nombre de la variable (entre un `$` inicial y un  final) en cualquier lugar de los valores del comando. Por ejemplo, entre el `=` que sigue al nombre del comando y el `&` posterior o el final de la solicitud. El servidor sustituye cada ocurrencia de este tipo de `$ [!DNL name]$` por `[!DNL string]`. No hay sustituciones en ninguna ocurrencia de `$ [!DNL name]$` en los nombres de comando (antes del signo igual de un comando) ni en la parte de ruta de acceso de la solicitud.

Las variables personalizadas no pueden estar anidadas. No se sustituye ninguna aparición de `$ [!DNL name]$` en `[!DNL string]`. Por ejemplo, el fragmento de solicitud `$var2=apple&$var1=my$var2$tree&text=$var1$` se resuelve en `text=my$var2$tree`.

`$` no es un carácter reservado; de lo contrario, puede ocurrir en la solicitud. Por ejemplo, `src=my$texture$file.tif` es un comando válido (suponiendo que existe un archivo de textura o entrada de catálogo de materiales denominado `[!DNL my$texture$file.tif]`), mientras que `wid=$number$` no lo es, porque `wid=` requiere un argumento numérico.
