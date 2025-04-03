---
title: Markdown examples
hide:
  - footer
status: new
---

# Markdown

## Setting up markdown files with custom meta

Material provides some things you can add to the top of the markdown pages.
They're called YAML Frontmatter, some of the most useful are:
```md
---
title: your page title will show instead of filename
description: set's the page description, this is used for Social cards if enabled.
icon: material/emoticon-happy // You can set a icon that's shown in the side nav
status: new // as seen in the sidebar on this page it put's a ! sign next to it


hide:
  - footer // hides the prev & next page footer at the bottom.
  - toc // hides the table of contents (better known as right sidebar).
```

For more info on any markdown options, because i havent covered everything (such as buttons, content tabs, math, diagrams etc) follow the guides on [material for Mkdocs](https://squidfunk.github.io/mkdocs-material/reference/).

# H1
## H2
### H3
#### H4
##### H5
###### H6

<hr>

**This is bold text**

__This is bold text__

*This is italic text*

_This is italic text_

~~Strikethrough~~

This is a <sub>subscript</sub> text

This is a <sup>superscript</sup> text

This is an <ins>underlined</ins> text

- H~2~O
- A^T^A

++ctrl+alt+del++

- [x] No installation needed in [Docker image]
- [x] No installation needed in [GitHub Actions] (Ubuntu)
- [ ] Example of an unchecked box

### Highlighted text
Text can be {--deleted--} and replacement text {++added++}. This can also be
combined into {~~one~>a single~~} operation. {==Highlighting==} is also
possible {>>and comments can be added inline<<}.

{==

Formatting can also be applied to blocks by putting the opening and closing
tags on separate lines and adding new lines between the tags and the content.

==}

<!-- Example of a comment -->


#### Ignore formatting
Ignore markdown formatting:
Let's rename \*our-new-project\* to \*our-old-project\*.

## Quote's
Text that is not a quote

> Text that is a quote

> If we pull together and commit ourselves, then we can push through anything.

— Mona the Octocat


## Data tables

### Example
| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |

### Center aligned
| Method      | Description                          |
| :---------: | :----------------------------------: |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |


### More tabs
|File                   |Section            |Key            |Value                  |
|-----------------------|-------------------|---------------|-----------------------|
|`printer.cfg`          |stepper_y          |position_max   |226 (K1) or 306 (K1M)  |
|`cartotouch.cfg`       |scanner            |x_offset       |-16.0                  |
|                       |                   |y_offset       |0.0                    |
|`cartographer-k1.cfg`  |bed_mesh           |mesh_min       |10,10                  |
|                       |                   |mesh_max       |210,215                |
|                       |screws_tilt_adjust |screw1         |42,20                  |
|                       |                   |screw2         |211,20                 |
|                       |                   |screw3         |211,190                |
|                       |                   |screw4         |42,190                 |
|`cartographer-k1m.cfg` |bed_mesh|mesh_min  |10,10          |                       |
|`cartographer-k1m.cfg` |                   |mesh_max       |290,280                |
|                       |screws_tilt_adjust |screw1         |35,23                  |
|                       |                   |screw2         |294,23                 |
|                       |                   |screw3         |264,272                |
|                       |                   |screw4         |64,272                 |


## Footnotes
Footnotes are a great way to add supplemental or additional information to a specific word, phrase or sentence without interrupting the flow of a document. Material for MkDocs provides the ability to define, reference and render footnotes.

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2] (example of these at the bottom)

## Grids
<div class="grid cards" markdown>

-   :material-clock-fast:{ .lg .middle } __Set up in 5 minutes__

    ---

    Install [`mkdocs-material`](#) with [`pip`](#) and get up
    and running in minutes

    [:octicons-arrow-right-24: Getting started](#)

-   :fontawesome-brands-markdown:{ .lg .middle } __It's just Markdown__

    ---

    Focus on your content and generate a responsive and searchable static site

    [:octicons-arrow-right-24: Reference](#)

-   :material-format-font:{ .lg .middle } __Made to measure__

    ---

    Change the colors, fonts, language, icons, logo and more with a few lines

    [:octicons-arrow-right-24: Customization](#)

-   :material-scale-balance:{ .lg .middle } __Open Source, MIT__

    ---

    Material for MkDocs is licensed under MIT and available on [GitHub]

    [:octicons-arrow-right-24: License](#)

</div>

## Lists

### Unordered list
- Nulla et rhoncus turpis. Mauris ultricies elementum leo. Duis efficitur
  accumsan nibh eu mattis. Vivamus tempus velit eros, porttitor placerat nibh
  lacinia sed. Aenean in finibus diam.

    * Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    * Nam vulputate tincidunt fringilla.
    * Nullam dignissim ultrices urna non auctor.

### Ordered list
1.  Vivamus id mi enim. Integer id turpis sapien. Ut condimentum lobortis
    sagittis. Aliquam purus tellus, faucibus eget urna at, iaculis venenatis
    nulla. Vivamus a pharetra leo.

    1.  Vivamus venenatis porttitor tortor sit amet rutrum. Pellentesque aliquet
        quam enim, eu volutpat urna rutrum a. Nam vehicula nunc mauris, a
        ultricies libero efficitur sed.

    2.  Morbi eget dapibus felis. Vivamus venenatis porttitor tortor sit amet
        rutrum. Pellentesque aliquet quam enim, eu volutpat urna rutrum a.

        1.  Mauris dictum mi lacus
        2.  Ut sit amet placerat ante
        3.  Suspendisse ac eros arcu

### Defenition lists
`Lorem ipsum dolor sit amet`

:   Sed sagittis eleifend rutrum. Donec vitae suscipit est. Nullam tempus
    tellus non sem sollicitudin, quis rutrum leo facilisis.

`Cras arcu libero`

:   Aliquam metus eros, pretium sed nulla venenatis, faucibus auctor ex. Proin
    ut eros sed sapien ullamcorper consequat. Nunc ligula ante.

:    Duis mollis est eget nibh volutpat, fermentum aliquet dui mollis.
    Nam vulputate tincidunt fringilla.
    Nullam dignissim ultrices urna non auctor.

### Task lists
- [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
- [ ] Vestibulum convallis sit amet nisi a tincidunt
    * [x] In hac habitasse platea dictumst
    * [x] In scelerisque nibh non dolor mollis congue sed et metus
    * [ ] Praesent sed risus massa
- [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque

### Grouped list
<div class="grid" markdown>

=== "Unordered list"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

``` title="Content tabs"
=== "Unordered list"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci
```
</div>

## Buttons

```md
[Subscribe to our newsletter](#){ .md-button }
```

[Subscribe to our newsletter](#){ .md-button }

### Primary button

```md
[Subscribe to our newsletter](#){ .md-button .md-button--primary }
```

[Subscribe to our newsletter](#){ .md-button .md-button--primary }

### Adding idons to buttons

```md
[Send :fontawesome-solid-paper-plane:](#){ .md-button }
```

[Send :fontawesome-solid-paper-plane:](#){ .md-button }


[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.