---
title: Macros de comandos
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

Las macros se definen en archivos de definición de macros independientes, que se pueden adjuntar a los catálogos de imágenes o al catálogo predeterminado.

Las macros pueden invocarse en cualquier lugar de una solicitud después de &quot;?&quot; y en cualquier lugar dentro de un `catalog::Modifier` field. Las macros solo pueden representar uno o más comandos completos de servicio de imágenes; por lo tanto, debe ir entre separadores &quot;&amp;&quot; (excepto cuando se encuentra al principio o al final de la cadena del modificador).

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anulan los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Este flujo es diferente al siguiente `catalog::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de `catalog::Modifier` cadena, independientemente de la posición en la solicitud.

Las macros se pueden anidar. Sin embargo, una macro sólo se puede invocar si ya está definida en el momento de analizar la definición de la macro. Este flujo se lleva a cabo apareciendo anteriormente en el mismo archivo de definición de macro o colocando la definición de dicha macro incrustada en el archivo de definición de macro predeterminado.

Las macros pueden resultar útiles si se van a aplicar los mismos atributos a imágenes diferentes.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Puede definir una macro para los atributos comunes:

`view wid=240&fmt=pdf&imageRes=300`

La macro se usaría de la siguiente manera:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Porque `wid=` es diferente para la tercera solicitud, solo tiene que anular el valor *después* se invoca la macro (especificando `wid=` *antes* `$view$` no tiene ningún efecto).

+ [nombre](r-name.md)
