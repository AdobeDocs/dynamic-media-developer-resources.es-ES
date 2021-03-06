---
title: Macros de comandos
description: Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Macros de comandos{#command-macros}

Las macros de comandos proporcionan accesos directos con nombre para conjuntos de comandos.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nombre de macro

Las macros se definen en archivos de definición de macro separados, que pueden adjuntarse a catálogos de material o al catálogo predeterminado.

*[!DNL name]* no distingue entre mayúsculas y minúsculas y puede constar de cualquier combinación de letras ASCII, números , &#39;-&#39;, &#39;_&#39; y &#39;.&#39; caracteres.

Invoque macros en cualquier lugar de una solicitud después de &#39;?&#39; o en cualquier lugar dentro de un `vignette::Modifier` campo . Las macros solo pueden representar uno o más comandos de renderización de imágenes y deben separarse de otros comandos con separadores &quot;&amp;&quot;.

Las invocaciones de macro se sustituyen por sus cadenas de sustitución antes de analizar. Los comandos dentro de las macros anulan los mismos comandos en la solicitud si se producen antes de la invocación de macro en la solicitud. Este flujo de trabajo es diferente de `vignette::Modifier`, donde los comandos de la cadena de solicitud anulan los comandos de la función `vignette::Modifier` , independientemente de la posición en la solicitud.

Las macros de comandos no pueden tener valores de argumento, pero pueden utilizarse variables personalizadas para pasar valores de la solicitud a la macro.

Es posible que las macros no estén anidadas.

**Ejemplo**

Las macros pueden resultar útiles si se van a aplicar los mismos comandos o atributos a diferentes imágenes procesadas.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Puede definir una macro para los atributos comunes:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

La macro se utilizaría de la siguiente manera:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Porque `qlt=` es diferente para la tercera solicitud, el software anula el valor después de invocar la macro (especificación `qlt=` *before* `$render$`es ineficaz).

**Véase también**

`catalog::MacroFile`, `catalog::Modifier`, Referencia de definición de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
