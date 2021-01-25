---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-title: Macros de comandos
solution: Experience Manager
title: Macros de comandos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

Las macros se definen en archivos de definición de macro independientes, que pueden adjuntarse a catálogos de imágenes o al catálogo predeterminado.

Las macros se pueden invocar en cualquier parte de una solicitud después de &#39;?&#39;, así como en cualquier parte dentro de un campo `catalog::Modifier`. Las macros solo pueden representar uno o más comandos completos de servicio de imágenes, por lo que deben estar encerrados entre separadores &#39;&amp;&#39; (excepto cuando se encuentra al principio o al final de la cadena del modificador).

Las invocaciones de macro se sustituyen por sus cadenas de sustitución en un principio durante el análisis. Los comandos dentro de las macros anularán los mismos comandos en la solicitud si se producen antes de la invocación de macro en la solicitud. Esto es diferente a `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre sobrescribirán los comandos de la cadena `catalog::Modifier`, independientemente de la posición en la solicitud.

Las macros se pueden anidar con la siguiente restricción: una macro solo se puede invocar si ya está definida en el momento en que se analiza la definición de la macro, ya sea mostrándola antes en el mismo archivo de definición de macro o colocando la definición de dicha macro incrustada en el archivo de definición de macro predeterminada.

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a distintas imágenes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Se puede definir una macro para los atributos comunes:

`view wid=240&fmt=pdf&imageRes=300`

La macro se utilizaría de la siguiente manera:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Dado que `wid=` es diferente para la tercera solicitud, simplemente anulamos el valor *después de que se invoque* la macro (especificar `wid=`*antes* `$view$` no tendría ningún efecto).

+ [name](r-name.md)
