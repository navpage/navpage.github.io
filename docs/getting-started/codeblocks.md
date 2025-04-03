## Codeblocks


### Adding annotations
``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

### codeblock languages
In order to have codeblocks show syntax highlights note the language
like:
```md
    ``` yaml
    theme:
    features:
        - content.code.annotate # (1)
    ```
```
Some of the popular ones are:
- html
- py
- md
- css
- js

``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.

### Highlighting inline code blocks
small inline codeblocks can be used with laguage syntax too like:
```md
The `#!python range()` function is used to generate a sequence of numbers.
```
The `#!python range()` function is used to generate a sequence of numbers.

### Adding a title
``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### Adding annotations

Code annotations can be placed anywhere in a code block where a comment for the
language of the block can be placed, e.g. for JavaScript in `#!js // ...` and
`#!js /* ... */`, for YAML in `#!yaml # ...`, etc.[^1]:

  [^1]:
    Code annotations require syntax highlighting with [Pygments] – they're
    currently not compatible with JavaScript syntax highlighters, or languages
    that do not have comments in their grammar. However, we're actively working
    on supporting alternate ways of defining code annotations, allowing to
    always place code annotations at the end of lines.

```` markdown title="Code block with annotation"
``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.
````

<div class="result" markdown>

``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.

</div>

### Adding line numbers
``` py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### Highlight specefic lines
``` py hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```
### Adding titles
In order to provide additional context, a custom title can be added to a code block by using the title="<custom title>" option directly after the shortcode, e.g. to display the name of a file:

``` { py title="namefile.py" linenums="1" .select }
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

### Filename as title
In order to show a filename as title you set up the following:
 ```md

    === ":octicons-file-code-16: `cartographer.conf`"

        ``` linenums="1" hl_lines="4 5"
        [update_manager Cartographer]
        type: git_repo
        path: usrdatacartographer-klipper
        channel: stable
        primary_branch: master
        origin: https://github.com/Cartographer3D/cartographer-klipper.git
        install_script: install.sh
        is_system_service: False
        managed_services: klipper
        info_tags:
            desc=Cartographer Probe
        ```

```
<div class="result" markdown>`:octicons-file-code-16:` is the icon shown.</div>


=== ":octicons-file-code-16: `cartographer.conf`"

    ``` linenums="1" hl_lines="4 5"
    [update_manager Cartographer]
    type: git_repo
    path: usrdatacartographer-klipper
    channel: stable
    primary_branch: master
    origin: https://github.com/Cartographer3D/cartographer-klipper.git
    install_script: install.sh
    is_system_service: False
    managed_services: klipper
    info_tags:
        desc=Cartographer Probe
    ```

### Content tabs
=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```