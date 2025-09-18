---
bookHidden: true
---

# Hidden Shortcode Palette

## Badges

{{< badge title="Title" value="Value" >}}
{{< badge style="info" title="Hugo" value="0.147.6" >}}
{{< badge style="success" title="Build" value="Passing" >}}
{{< badge style="warning" title="Coverage" value="25%" >}}
{{< badge style="danger" title="Issues" value="120" >}}

| Shortcode | Output |
| --        | --     |
| `{{</* badge style="info" title="hugo" value="0.147.6" */>}}`     | {{< badge style="info" title="Hugo" value="0.147.6" >}}     |
| `{{</* badge style="success" title="Build" value="Passing" */>}}` | {{< badge style="success" title="Build" value="Passing" >}} |
| `{{</* badge style="warning" title="Coverage" value="25%" */>}}`  | {{< badge style="warning" title="Coverage" value="25%" >}}  |
| `{{</* badge style="danger" title="Issues" value="120" */>}}`     | {{< badge style="danger" title="Issues" value="120" >}}     |
| | |
| `{{</* badge style="info" title="Title" */>}}`                    | {{< badge style="info" title="Title" >}}                    |
| `{{</* badge style="info" value="Value" */>}}`                    | {{< badge style="info" value="Value" >}}                    |
| `{{</* badge title="Default" */>}}`                               | {{< badge value="Default" >}}                               |

A badge can be wrapped in markdown link producing following result: [{{< badge title="Hugo" value="0.147.6" >}}](https://github.com/gohugoio/hugo/releases/tag/v0.147.6)
```tpl
[{{</* badge title="Hugo" value="0.147.6" */>}}](https://github.com/gohugoio/hugo/releases/tag/v0.147.6)
```

## Buttons

```tpl
{{</* button relref="/" [class="..."] */>}}Get Home{{</* /button */>}}
{{</* button href="https://github.com/alex-shpak/hugo-book" */>}}Contribute{{</* /button */>}}
```

{{<button href="/">}}Get Home{{</button>}}
{{<button href="https://github.com/alex-shpak/hugo-book">}}Contribute{{</button>}} 

## Cards

{{% columns %}}
- {{< card image="placeholder.svg" >}}
  ### Line 1
  Line 2
  {{< /card >}}

- {{< card image="placeholder.svg" >}}
  This is tab MacOS content.
  {{< /card >}}
{{% /columns %}}

{{% columns %}}
- {{< card href="/docs/shortcodes/cards" >}}
  **Markdown**  
  Suspendisse sed congue orci, eu congue metus. Nullam feugiat urna massa.
  {{< /card >}}

- {{< card >}}
  Suspendisse sed congue orci, eu congue metus. Nullam feugiat urna massa, et fringilla metus consectetur molestie.
  {{< /card >}}

- {{< card title="Card" >}}
  ### Heading
  This is tab MacOS content.
  {{< /card >}}
{{% /columns %}}

Hugo's built-in figure shortcode is also styled as a card

{{% columns %}}
- ```go-html-template
  {{</* figure
    src="placeholder.svg"
    alt="A placeholder image"
    link="#"
    caption="A placeholder image caption"
    loading="lazy"
    target="_blank"
    title="Figure Title"
    caption="A caption for the figure"
    attr="An attribution"
    attrlink="#"
  */>}}
  ```

- {{< figure
    src="placeholder.svg"
    alt="A placeholder image"
    link="#"
    caption="A placeholder image caption"
    loading="lazy"
    target="_blank"
    title="Figure Title"
    caption="A caption for the figure"
    attr="An attribution"
    attrlink="#"
  >}}
{{% /columns %}}

## Columns

```tpl
{{%/* columns [ratio="1:1"] [class="..."] */%}}
- ### Left Content
  Lorem markdownum insigne...

- ### Mid Content
  Lorem markdownum insigne...

- ### Right Content
  Lorem markdownum insigne...
{{%/* /columns */%}}
```

{{% columns %}}
- ### Left Content
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
  protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
  Miseratus fonte Ditis conubia.

- ### Mid Content
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter!

- ### Right Content
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
  protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
  Miseratus fonte Ditis conubia.
{{% /columns %}}

Settings size ratio for columns

```tpl
{{%/* columns ratio="1:2" */%}}
- ## x1 Column
  Lorem markdownum insigne...

- ## x2 Column
  Lorem markdownum insigne...
{{%/* /columns */%}}
```

{{% columns ratio="1:2" %}}
- ### x1 Column
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
  protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
  Miseratus fonte Ditis conubia.

- ### x2 Column
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter!
  
  Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
  stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
  protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
  Miseratus fonte Ditis conubia.
{{% /columns %}}

## Details

```tpl
{{%/* details "Title" [open] */%}}
Markdown content
Lorem markdownum insigne...
{{%/* /details */%}}
```
```tpl
{{%/* details title="Title" open=true */%}}
Markdown content
Lorem markdownum insigne...
{{%/* /details */%}}
```

{{% details "Title" open %}}
Markdown content
Lorem markdownum insigne...
{{% /details %}}

## Hints

```tpl
{{%/* hint [info|success|warning|danger] */%}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{%/* /hint */%}}

> [!NOTE|TIP|IMPORTANT|WARNING|CAUTION]
> **Markdown content**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
```

## Example

{{% hint %}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{% /hint %}}

{{% hint info %}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{% /hint %}}

{{% hint success %}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{% /hint %}}

{{% hint warning %}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{% /hint %}}

{{% hint danger %}}
**Markdown content**  
Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
{{% /hint %}}

Support for markdown alerts

> [!NOTE]
> **Note**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa

> [!TIP]
> **Tip**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa

> [!IMPORTANT]
> **Important**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa

> [!WARNING]
> **Warning**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa

> [!CAUTION]
> **Caution**  
> Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
> stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa

## images

```go-html-template
{{</* image src="placeholder.svg" alt="A placeholder" title="A placeholder" loading="lazy" */>}}
```
{{< image src="placeholder.svg" alt="A placeholder" title="A placeholder" loading="lazy" >}}

Parameters

`src` {{< badge style="warning" title="Required" >}}
: The link to the image

`class` {{< badge style="info" title="Optional" >}}  
: An optional CSS class name that will be applied to the `img` element

`alt` {{< badge style="info" title="Optional" >}}  
: An optional alternate text for the image

`title` {{< badge style="info" title="Optional" >}}  
: An optional title for the image

`loading` {{< badge style="info" title="Optional" >}}  
: Sets `loading` control for the image: `lazy`, `eager` or `auto`

## KaTeX

KaTeX shortcode let you render math typesetting in markdown document. See [KaTeX](https://katex.org/)

{{% hint info %}}
**Override KaTeX initialization config**  
To override the [initialization config](https://katex.org/docs/options.html) for KaTeX,
create a `katex.json` file in your `assets` folder!
{{% /hint %}}

{{< katex />}}


Activation
KaTeX is activated on the page by first use of the shortcode or render block. you can force activation with empty `{{</* katex /*/>}}` and use delimiters defined in configuration in `assets/katex.json`.

Rendering as block

{{% columns %}}

```latex
{{</* katex display=true >}}
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
{{< /katex */>}}
```

````latex
```katex
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
```
````

````latex
$$
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$
````

<--->

{{< katex display=true >}}
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
{{< /katex >}}

---

```katex
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
```

---

$$
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
$$

{{% /columns %}}

Rendering inline 

When KaTeX is active on the page it is possible to write inline expressions.  

| Code | Output |
| --   | --     |
| `{{</* katex >}}\pi(x){{< /katex */>}}` | {{< katex >}}\pi(x){{< /katex >}} |
| `\\( \pi(x) \\)` | \\( \pi(x) \\) |

Configuration

KaTeX configuration could be adjusted by editing `assets/katex.json` file. For example to enabled inline delimiters `$..$` put content below into the file.

```json
{
  "delimiters": [
    {"left": "$$", "right": "$$", "display": true},
    {"left": "$", "right": "$", "display": false},
    {"left": "\\(", "right": "\\)", "display": false},
    {"left": "\\[", "right": "\\]", "display": true}
  ]
}
```

## Mermaid

[MermaidJS](https://mermaid-js.github.io/) is library for generating svg charts and diagrams from text.

{{% hint info %}}
**Override Mermaid initialization config**  
To override the [initialization config](https://mermaid-js.github.io/mermaid/#/Setup) for Mermaid,
create a `mermaid.json` file in your `assets` folder!
{{% /hint %}}

Example

{{% columns %}}

````tpl
```mermaid
stateDiagram-v2
    State1: The state with a note
    note right of State1
        Important information! You can write
        notes.
    end note
    State1 --> State2
    note left of State2 : This is the note to the left.
```
````

<--->

```mermaid
stateDiagram-v2
    State1: The state with a note
    note right of State1
        Important information! You can write
        notes.
    end note
    State1 --> State2
    note left of State2 : This is the note to the left.
```

{{% /columns %}}

{{% columns %}}

```tpl
{{</* mermaid [class="..."] >}}
stateDiagram-v2
    State1: The state with a note
    note right of State1
        Important information! You can write
        notes.
    end note
    State1 --> State2
    note left of State2 : This is the note to the left.
{{< /mermaid */>}}
```

<--->

{{< mermaid >}}
stateDiagram-v2
    State1: The state with a note
    note right of State1
        Important information! You can write
        notes.
    end note
    State1 --> State2
    note left of State2 : This is the note to the left.
{{< /mermaid >}}

{{% /columns %}}

Diagrams

Explore more diagrams and syntax on Mermaid [documentation page](https://mermaid.js.org/syntax/flowchart.html).

{{% columns %}}

```mermaid
stateDiagram-v2
    State1: The state with a note
    note right of State1
        Important information! You can write
        notes.
    end note
    State1 --> State2
    note left of State2 : This is the note to the left.
```

```mermaid
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
    Alice-)John: See you later!
```

```mermaid
---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

```mermaid
---
title: Simple sample
---
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

<--->

```mermaid
---
title: Example Git diagram
---
gitGraph
   commit
   commit
   branch develop
   checkout develop
   commit
   commit
   checkout main
   merge develop
   commit
   commit
```

```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :after a1, 20d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :24d
```

```mermaid
pie title Pets adopted by volunteers
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
```

```mermaid
quadrantChart
    title Reach and engagement of campaigns
    x-axis Low Reach --> High Reach
    y-axis Low Engagement --> High Engagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A: [0.3, 0.6]
    Campaign B: [0.45, 0.23]
    Campaign C: [0.57, 0.69]
    Campaign D: [0.78, 0.34]
    Campaign E: [0.40, 0.34]
    Campaign F: [0.35, 0.78]
```

{{% /columns %}}

## Steps

```tpl
{{%/* steps */%}}
1. ## Suspendisse sed congue orci.
   ...

2. ## Maecenas scelerisque sem.
   ...

3. ## Etiam risus purus.
   ...

4. ## Curabitur sed lacinia velit.
   ...
{{%/* /steps */%}}
```

{{% steps %}}
1. ## Suspendisse sed congue orci.
   Suspendisse sed congue orci, eu congue metus. Nullam feugiat urna massa, et fringilla metus consectetur molestie. Curabitur pellentesque sodales ipsum, sed efficitur libero euismod ac. Donec sit amet erat nunc. Suspendisse porta nisl velit, quis auctor massa commodo nec. Donec sollicitudin tellus sit amet massa condimentum luctus. Etiam molestie at ante et convallis.

2. ## Maecenas scelerisque sem.
   Maecenas scelerisque sem a tellus dignissim, in sodales neque varius. Integer quis ex quis sem posuere consequat. Morbi interdum ex et mollis maximus. Proin sed quam nisl. Donec tempus non risus vel auctor. Ut ultricies vitae urna in laoreet. Phasellus cursus nunc sit amet sodales euismod. Suspendisse potenti.

3. ## Etiam risus purus.
   Etiam risus purus, suscipit a orci quis, mollis mollis ante. Vestibulum congue nisl malesuada tortor egestas, a lobortis tellus dictum. Nam nec ultrices justo. Donec malesuada dignissim posuere. 

4. ## Curabitur sed lacinia velit.
   Curabitur sed lacinia velit. Nullam sed ante non quam lobortis hendrerit. Phasellus elementum, erat sit amet imperdiet pulvinar, odio massa lobortis ipsum, in tincidunt metus dolor vel ligula.

{{% /steps %}}

## Tabs

```tpl
{{</* tabs "id" */>}}
{{%/* tab "MacOS" */%}} # MacOS Content {{%/* /tab */%}}
{{%/* tab "Linux" */%}} # Linux Content {{%/* /tab */%}}
{{%/* tab "Windows" */%}} # Windows Content {{%/* /tab */%}}
{{</* /tabs */>}}
```

{{< tabs >}}

{{% tab "MacOS" %}}
# MacOS

This is tab **MacOS** content.

Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
Miseratus fonte Ditis conubia.
{{% /tab %}}

{{% tab "Linux" %}}
# Linux

This is tab **Linux** content.

Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
Miseratus fonte Ditis conubia.
{{% /tab %}}

{{% tab "Windows" %}}
# Windows

This is tab **Windows** content.

Lorem markdownum insigne. Olympo signis Delphis! Retexi Nereius nova develat
stringit, frustra Saturnius uteroque inter! Oculis non ritibus Telethusa
protulit, sed sed aere valvis inhaesuro Pallas animam: qui _quid_, ignes.
Miseratus fonte Ditis conubia.
{{% /tab %}}

{{< /tabs >}}


