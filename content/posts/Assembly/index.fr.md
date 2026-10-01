+++
date = '2026-08-26T17:09:09+02:00'
draft = true
title = "Assembly : un workflow pour une automatisation totale de la box-anim Harmony"
tags = ['Toon Boom', 'Harmony', 'box']
categories = ["Pipeline", '2D', 'scripting']
keywords = ['Pipeline', 'scripting', 'toon boom', 'harmony', 'build']
description = 'pour SEO'
summary = 'La BoxAnim dans Harmony bien que nécessaire pour établir et livrer une base techniquement solide aux animateurs, n’est pas l’étape la plus glamour dans l’animation. Beaucoup d’opérations redondantes deviennent fastidieuses… alors place aux scripts _🚀'
featured = 'featured-gen.png'
showHero = true
heroStyle = 'background'
layoutBackgroundBlur = true
showTableOfContents = true
upcoming = true
+++

## Contexte

La **box-anim** dans Toon Boom Harmony (build de la scène avec import de tous les assets) bien que nécessaire pour établir et livrer une base techniquement solide aux animateurs, n’est pas l’étape la plus glamour dans l’animation. Beaucoup d’opérations redondantes deviennent fastidieuses… alors place à un workflow pensé et aux scripts 🚀 

{{< lead >}}
Schéma du workflow
{{< /lead >}}


{{< mermaid >}}
flowchart TB
    A["`**HighLight**`"] L_A_B_0@== CopyLinkFunc ==> B("`**Radius / R / G / B**`")
    n1["`**PEG**`"] L_n1_n3_0@== "position.Y" ==> n3["`**Expression Offset Y**`"]
    n1 L_n1_n4_0@== "position.X" ==> n4["`**Expression Offset X**`"]
    n5["`**Master PEG**`"] L_n5_n3_0@== "scale.Y" ==> n3 & n4
    n8["`**Master Controller**`"] ==> n1
    B L_B_n9_0@== LinkFunc ==> n9["`**HighLight**`"]
    n3 L_n3_n10_0@== Linkexpression ==> n10["`**Auto Offset PEG**`"]
    n4 L_n4_n10_0@== Link Expression ==> n10
    n11["`***RIMLIGHT NODE***`"]
    n2["`***RIMLIGHT CTRL***`"]
    n6["`***ASSET***`"]

    n1@{ shape: rect}
    n3@{ shape: rounded}
    n4@{ shape: rounded}
    n5@{ shape: rect}
    n8@{ shape: rounded}
    n9@{ shape: rect}
    n10@{ shape: rect}
    n11@{ shape: text}
    n2@{ shape: text}
    n6@{ shape: text}
    style A fill:#32C2FF,stroke:#35719D,stroke-width:4px,stroke-dasharray: 0
    style B fill:#e6e6e6
    style n1 fill:#99FF4D,stroke-width:4px,stroke-dasharray: 0,stroke:#72BF3A
    style n3 fill:#e6e6e6
    style n4 fill:#e6e6e6
    style n5 fill:#99FF4D,stroke-width:4px,stroke-dasharray: 0,stroke:#72BF3A
    style n8 stroke-width:4px,stroke-dasharray: 0,fill:#FFCDD2,stroke:#ff5dff
    style n9 fill:#32C2FF,stroke:#35719D,stroke-width:4px,stroke-dasharray: 0
    style n10 fill:#99FF4D,stroke-width:4px,stroke-dasharray: 0,stroke:#72BF3A
    style n11 fill:#e6e6e6
    style n2 fill:#e6e6e6
    style n6 fill:#e6e6e6
    linkStyle 0 stroke:#35719D,fill:none
    linkStyle 1 stroke:#72BF3A,fill:none
    linkStyle 2 stroke:#72BF3A,fill:none
    linkStyle 3 stroke:#72BF3A,fill:none
    linkStyle 4 stroke:#72BF3A,fill:none
    linkStyle 5 stroke:#ff5dff,fill:none
    linkStyle 6 stroke:#35719D,fill:none
    linkStyle 7 stroke:#72BF3A,fill:none
    linkStyle 8 stroke:#72BF3A,fill:none

    L_A_B_0@{ animation: slow } 
    L_n1_n3_0@{ animation: slow } 
    L_n1_n4_0@{ animation: slow } 
    L_n5_n3_0@{ animation: slow } 
    L_n5_n4_0@{ animation: slow } 
    L_B_n9_0@{ animation: slow } 
    L_n3_n10_0@{ animation: slow } 
    L_n4_n10_0@{ animation: slow }
{{< /mermaid >}}


> [!TIP] TIP
> Il y a un préambule technique pour que la cohérence des rimlights fonctionne : **la normalisation des caméras**. Elle est indispensable que pour une même valeur de plan (ensemble/gros/moyen/serré…) le *scale x/y* d'un asset soit indentique.

## TitreH2

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.

## TitreH2

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.

## TitreH2

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.

## TitreH2

{{< lead >}}
Ceci est une mise en avant.
{{< /lead >}}

### TitreH3
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.


### TitreH3
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.

### TitreH3
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.

### TitreH3
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since 1966, when designers at Letraset and James Mosley, the librarian at St Bride Printing Library in London, took a 1914 Cicero translation and scrambled it to make dummy text for Letraset's Body Type sheets. It has survived not only many decades, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised thanks to these sheets and more recently with desktop publishing software like Aldus PageMaker and Microsoft Word including versions of Lorem Ipsum.
