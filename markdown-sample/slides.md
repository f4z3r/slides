---
title: Test
theme: ipt
author: me
institute: ipt
date: 2025-05-17
subtitle: other test
title-slide-attributes:
   data-background-image: ../../assets/img/cover-blue-01.png
   data-background-size: cover
revealjs-url: "../assets/revealjs/base"
progress: true
controls: false
hash: true
highlightjs: true
css:
- style.css
animate: true
history: false
overview: true
controls: false
hash: true
fragmentInURL: true
showSlideNumber: speaker
autoPlayMedia: true
transitionSpeed: fast
viewDistance: 5
width: 2550
height: 1440
margin: 0.1
center: false
disableLayout: false
---

# Slide 1 {data-background="../assets/img/cover-pink-01.png"}

<!-- can also use a URL for source -->

## Incremental lists

::: incremental
- Point 1
- Point 2
- Point 3
:::

## Pauses

This and ...

<!-- below is a pause -->
. . .

[link](https://google.com)!

## Quotes

> A quote!

## Tables

| header1 | header2 |
| ---     | ----    |
| data    | data    |
| data2   | other   |

## Inline Code

some `inline` code

## Columns

:::::::::::::: {.columns}
::: {.column .boxed width="40%"}
### Test
contents...
:::
::: {.column width="60%"}
more contents...
:::
::::::::::::::

# Examples

## Include Code

```{.python include="./assets/app.py" dedent=4 start-line=14 end-line=15 .numberLines data-line-numbers="1|2"}
```

<!-- include for code is relative to base directory -->

## Sub-Slide Code {data-transition="zoom"}

```{.python data-line-numbers="1-3|2"}
def sample_function(name: str, arg: int):
    if arg > 0:
        # comment
        return 42
    return f"this is a {name}"
```

# Annimations {.center .uppercase}

## {data-auto-animate=true}

<pre data-id="code-animation"><code data-trim data-line-numbers>
  let planets = [
    { name: 'mars', diameter: 6779 },
  ]
</code></pre>

## {data-auto-animate=true}
<pre data-id="code-animation"><code data-trim data-line-numbers>
  let planets = [
    { name: 'mars', diameter: 6779 },
    { name: 'earth', diameter: 12742 },
    { name: 'jupiter', diameter: 139820 }
  ]
</code></pre>

## {data-auto-animate=true}
<pre data-id="code-animation"><code data-trim data-line-numbers>
  let circumferenceReducer = ( c, planet ) => {
    return c + planet.diameter * Math.PI;
  }

  let planets = [
    { name: 'mars', diameter: 6779 },
    { name: 'earth', diameter: 12742 },
    { name: 'jupiter', diameter: 139820 }
  ]

  let c = planets.reduce( circumferenceReducer, 0 )
</code></pre>

# Definition Lists

This is a term
: This is a definition

This is another term
: This is another definition

# Warnings and Infos

:::{.warning}
> This is a warning that is evry long and will wrap across many lines and this and that will do yes.
:::

:::{.info}
> This is an info
:::
