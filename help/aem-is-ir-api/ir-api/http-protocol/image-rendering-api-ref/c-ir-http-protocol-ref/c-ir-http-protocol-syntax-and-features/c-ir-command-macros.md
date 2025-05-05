---
title: Macros de comandos
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** nombre de macro

Las macros se definen en ficheros de definición de macros independientes, que pueden adjuntarse a catálogos de material o al catálogo predeterminado.

*[!DNL name]* no distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras ASCII, números , &#39;-&#39;, &#39;_&#39; y &#39;.&#39; caracteres.

Invocar macros desde cualquier lugar de una solicitud después de &quot;?&quot; o desde cualquier lugar dentro de un campo de `vignette::Modifier`. Las macros solo pueden representar uno o más comandos de procesamiento de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones a macros se sustituyen por sus cadenas de sustitución al principio del análisis. Los comandos dentro de las macros anulan los mismos comandos de la solicitud si se producen antes de la invocación de la macro en la solicitud. Este flujo de trabajo es diferente de `vignette::Modifier`, donde los comandos de la cadena de solicitud anulan los comandos de la cadena `vignette::Modifier`, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero se pueden utilizar variables personalizadas para pasar valores de la solicitud a la macro.

Las macros no pueden estar anidadas.

**Ejemplo**

Las macros pueden resultar útiles si se van a aplicar los mismos comandos o atributos a distintas imágenes procesadas.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Puede definir una macro para los atributos comunes:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro se usaría de la siguiente manera:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Dado que `qlt=` es diferente para la tercera solicitud, el software anula el valor después de invocar la macro (especificando `qlt=` *antes* `$render$`no es eficaz).

**Ver también**

`catalog::MacroFile`, `catalog::Modifier`, referencia de definición de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
