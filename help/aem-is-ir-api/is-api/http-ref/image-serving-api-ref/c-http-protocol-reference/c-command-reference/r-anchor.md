---
description: Anclaje de imagen. Define el punto de ancla del rectángulo de la imagen, el color sólido o el cuadro delimitador de texto, antes de aplicar las transformaciones (recortar=, escalar=, rotar=, flip=). También sirve como centro de rotación para rotate=.
seo-description: Anclaje de imagen. Define el punto de ancla del rectángulo de la imagen, el color sólido o el cuadro delimitador de texto, antes de aplicar las transformaciones (recortar=, escalar=, rotar=, flip=). También sirve como centro de rotación para rotate=.
seo-title: delimitador
solution: Experience Manager
title: delimitador
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# delimitador{#anchor}

Anclaje de imagen. Define el punto de ancla del rectángulo de la imagen, el color sólido o el cuadro delimitador de texto, antes de aplicar las transformaciones (recortar=, escalar=, rotar=, flip=). También sirve como centro de rotación para rotate=.

`anchor= *`coord`*`

`anchorN= *`codeN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> code</span></span> </p> </td> 
  <td class="stentry"> <p>desplazamiento de píxeles desde la esquina superior izquierda de la imagen de origen (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> codeN</span></span> </p> </td> 
  <td class="stentry"> <p>desplazamiento normalizado desde el centro de la imagen de origen (real, real) </p></td> 
 </tr> 
</table>

El punto de ancla se transforma con la imagen y se convierte en el punto de origen de la capa (a menos que `origin=` se especifique también, en cuyo caso `anchor=` se utiliza únicamente como centro de rotación para `rotate=`).

`anchorN=0,0` coloca el anclaje de imagen en el centro de la imagen de origen. `anchorN=-0.5,-0.5` o `anchor=0,0` está en la esquina superior izquierda y `anchorN=0.5,0.5` se encuentra en la esquina inferior derecha de la imagen de origen.

## Propiedades {#section-f08942bc6aae46a8b5d341faaff80640}

Atributo de imagen de origen. Se aplica a la capa actual o a la capa 0 si `layer=comp`.

## Predeterminado {#section-35d369fab1254f1a9b91684a6e169ad1}

Si no `anchor=` se especifica, se utiliza catalog::Anchor. Si no `catalog::Anchor` se define, se utiliza el centro del rectángulo de imagen (igual que si se especifica `anchorN=0,0`).

Las capas de texto que involucran `textPs=` y las capas que involucran `clipPath=` pueden tener diferentes anclajes predeterminados.

## Ejemplo {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

Consulte &quot;Ejemplo C&quot; en [Plantillas](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Véase también {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catálogo::Anclaje](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), Capas [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
