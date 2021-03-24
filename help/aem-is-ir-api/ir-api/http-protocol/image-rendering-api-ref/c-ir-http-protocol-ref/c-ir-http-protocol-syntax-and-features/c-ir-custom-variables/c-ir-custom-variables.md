---
description: La parte de consulta de las solicitudes y las cadenas de Modificador de viñeta pueden incluir variables definidas por el usuario.
solution: Experience Manager
title: Variables personalizadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Variables personalizadas{#custom-variables}

La parte de consulta de las solicitudes y las cadenas de viñeta::Modifier puede incluir variables definidas por el usuario.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nombre de variable. Puede consistir en cualquier combinación de caracteres alfa, dígito y caracteres seguros, excepto &#39;$&#39;.

** *[!DNL value]* ** Valor al que se debe configurar la variable (cadena).

Las variables se definen de forma similar a otros comandos del servidor, utilizando la sintaxis anterior. Para poder hacer referencia a las variables es necesario definirlas. Se puede hacer referencia a las variables definidas en `vignette::Modifier` en la solicitud de URL y viceversa.

>[!NOTE]
>
>*[!DNL value]* debe tener codificación de dirección URL de paso único para la transmisión HTTP segura. Se requiere una doble codificación si *[!DNL value]* se retransmite mediante HTTP. Este es el caso cuando *[!DNL value]* se sustituye en una solicitud externa anidada.

Para hacer referencia a las variables, incruste el nombre de la variable (delimitado por un $ inicial y un $ final) en cualquier parte de los valores de comando. Por ejemplo, entre el &#39;=&#39; que sigue al nombre del comando y el &#39;&amp;&#39; posterior o el final de la solicitud. El servidor sustituye cada incidencia de $ *[!DNL name]*$ por *[!DNL string]*. No se producirán sustituciones en ninguna ocurrencia de $ *[!DNL name]*$ en nombres de comando (antes del signo igual de un comando) y en la parte de ruta de la solicitud.

Es posible que las variables personalizadas no estén anidadas. No se sustituye ninguna ocurrencia de $ *[!DNL name]*$ dentro de *[!DNL string]*. Por ejemplo, el fragmento de solicitud `$var2=apple&$var1=my$var2$tree&text=$var1$` se resuelve en `text=my$var2$tree`.

$ no es un carácter reservado; de lo contrario, podría ocurrir en la solicitud. Por ejemplo, `src=my$texture$file.tif` es un comando válido (suponiendo que existe una entrada de catálogo de material o un archivo de textura llamado [!DNL my$texture$file.tif]), mientras que `wid=$number$` no lo es, porque `wid=` requiere un argumento numérico.
