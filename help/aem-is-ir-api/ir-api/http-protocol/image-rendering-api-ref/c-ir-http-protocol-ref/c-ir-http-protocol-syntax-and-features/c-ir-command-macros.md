---
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
seo-title: Macros de comandos *
solution: Experience Manager
title: Macros de comandos *
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---


# Macros de comandos *{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nombre de macro

Las macros se definen en archivos de definición de macro separados, que pueden adjuntarse a catálogos de material o al catálogo predeterminado.

*[!DNL name]* no distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras ASCII, números , &#39;-&#39;, &#39;_&#39; y &#39;.&#39; caracteres.

Invoque macros en cualquier lugar de una solicitud después de &#39;?&#39; o en cualquier lugar dentro de un campo `vignette::Modifier`. Las macros solo pueden representar uno o más comandos completos de renderización de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones de macro se sustituyen por sus cadenas de sustitución antes de analizar. Los comandos dentro de las macros anulan los mismos comandos en la solicitud si se producen antes de la invocación de macro en la solicitud. Esto es diferente a `vignette::Modifier`, donde los comandos de la cadena de solicitud siempre anulan los comandos de la cadena `vignette::Modifier`, independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero pueden utilizarse variables personalizadas para pasar valores de la solicitud a la macro.

Es posible que las macros no estén anidadas.

**Ejemplo**

Las macros pueden resultar útiles si se van a aplicar los mismos comandos o atributos a diferentes imágenes procesadas.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Puede definir una macro para los atributos comunes:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro se utilizaría de la siguiente manera:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Dado que `qlt=` es diferente para la tercera solicitud, simplemente anulamos el valor después de invocar la macro (especificar `qlt=`*antes* `$render$`no tendría ningún efecto).

**Véase también**

`catalog::MacroFile`,  `catalog::Modifier`, Referencia de definición de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

